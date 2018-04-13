### <a name="wpf-grid-allocation-of-space-to-star-columns"></a><span data-ttu-id="1d56c-101">Allocation d’espace aux colonnes de l’étoile grille de WPF</span><span class="sxs-lookup"><span data-stu-id="1d56c-101">WPF Grid allocation of space to star-columns</span></span>

|   |   |
|---|---|
|<span data-ttu-id="1d56c-102">Détails</span><span class="sxs-lookup"><span data-stu-id="1d56c-102">Details</span></span>|<span data-ttu-id="1d56c-103">À partir de la 4.7 Framework .NET, WPF remplace l’algorithme qui <xref:System.Windows.Controls.Grid> utilise pour allouer de l’espace à \*-colonnes.</span><span class="sxs-lookup"><span data-stu-id="1d56c-103">Starting with the .NET Framework 4.7, WPF replaces the algorithm that <xref:System.Windows.Controls.Grid> uses to allocate space to \*-columns.</span></span> <span data-ttu-id="1d56c-104">Cela modifie la largeur réelle assignée à \*-colonnes dans un nombre de cas :</span><span class="sxs-lookup"><span data-stu-id="1d56c-104">This will change the actual width assigned to \*-columns in a number of cases:</span></span><ul><li><span data-ttu-id="1d56c-105">Lorsqu’un ou plusieurs \*-colonnes ont également une largeur minimale ou maximale qui remplace l’allocation proportionnelle pour cette colonne.</span><span class="sxs-lookup"><span data-stu-id="1d56c-105">When one or more \*-columns also have a minimum or maximum width that overrides the proportional allocation for that colum.</span></span> <span data-ttu-id="1d56c-106">(La largeur minimale peut dériver à partir d’une déclaration MinWidth explicite ou un minimum obtenu à partir du contenu de la colonne.</span><span class="sxs-lookup"><span data-stu-id="1d56c-106">(The minimum width can derive from an explicit MinWidth declaration, or from an implicit minimum obtained from the column's content.</span></span> <span data-ttu-id="1d56c-107">La largeur maximale ne peut être définie explicitement, à partir d’une déclaration MaxWidth.)</span><span class="sxs-lookup"><span data-stu-id="1d56c-107">The maximum width can only be defined explicitly, from a MaxWidth declaration.)</span></span></li><li><span data-ttu-id="1d56c-108">Lorsqu’un ou plusieurs *-colonnes déclarent un pourcentage extrêmement élevé *-poids supérieur à 10 ^ 298.</span><span class="sxs-lookup"><span data-stu-id="1d56c-108">When one or more *-columns declare an extremely large *-weight, greater than 10^298.</span></span></li><li><span data-ttu-id="1d56c-109">Lorsque le \*-poids sont suffisamment différents de rencontrer une instabilité à virgule flottante (dépassement de capacité, dépassement de capacité négatif, une perte de précision).</span><span class="sxs-lookup"><span data-stu-id="1d56c-109">When the \*-weights are sufficiently different to encounter floating-point instability (overflow, underflow, loss of precision).</span></span></li><li><span data-ttu-id="1d56c-110">Lorsque l’arrondi de disposition est activé, et que la résolution d’affichage efficace en PPP est suffisamment élevée.</span><span class="sxs-lookup"><span data-stu-id="1d56c-110">When layout rounding is enabled, and the effective display DPI is sufficiently high.</span></span></li></ul><span data-ttu-id="1d56c-111">Dans les deux premiers cas, la largeur des produits par le nouvel algorithme peuvent être considérablement différentes de ceux générés par l’ancien algorithme ; dans le dernier cas, la différence sera au plus un ou deux pixels. Le nouvel algorithme résout plusieurs bogues présents dans l’ancien algorithme :</span><span class="sxs-lookup"><span data-stu-id="1d56c-111">In the first two cases, the widths produced by the new algorithm can be significantly different from those produced by the old algorithm; in the last case, the difference will be at most one or two pixels.The new algorithm fixes several bugs present in the old algorithm:</span></span><ol><li><span data-ttu-id="1d56c-112">L’allocation totale à des colonnes peut dépasser la largeur de la grille.</span><span class="sxs-lookup"><span data-stu-id="1d56c-112">Total allocation to columns can exceed the Grid's width.</span></span> <span data-ttu-id="1d56c-113">Cela peut se produire lors de l’allocation d’espace pour une colonne dont la part proportionnelle est inférieure à sa taille minimale.</span><span class="sxs-lookup"><span data-stu-id="1d56c-113">This can occur when allocating space to a column whose proportional share is less than its minimum size.</span></span> <span data-ttu-id="1d56c-114">L’algorithme alloue la taille minimale, ce qui réduit l’espace disponible pour les autres colonnes.</span><span class="sxs-lookup"><span data-stu-id="1d56c-114">The algorithm allocates the minimum size, which decreases the space available to other columns.</span></span> <span data-ttu-id="1d56c-115">S’il n’y aucun \*-pour allouer des colonnes, l’allocation totale sera trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="1d56c-115">If there are no \*-columns left to allocate, the total allocation will be too large.</span></span></li><li><span data-ttu-id="1d56c-116">L’allocation totale peut être inférieure à la largeur de la grille.</span><span class="sxs-lookup"><span data-stu-id="1d56c-116">Total allocation can fall short of the Grid's width.</span></span> <span data-ttu-id="1d56c-117">Il s’agit de la double problème à #1, lors de l’allocation à une colonne dont la part proportionnelle est supérieure à sa taille maximale, sans aucune \*-colonnes pour occuper la marge.</span><span class="sxs-lookup"><span data-stu-id="1d56c-117">This is the dual problem to #1, arising when allocating to a column whose proportional share is greater than its maximum size, with no \*-columns left to take up the slack.</span></span></li><li><span data-ttu-id="1d56c-118">Deux *-colonnes peuvent recevoir des allocations non proportionnelles à leur *-poids.</span><span class="sxs-lookup"><span data-stu-id="1d56c-118">Two *-columns can receive allocations not proportional to their *-weights.</span></span> <span data-ttu-id="1d56c-119">Il s’agit d’une version atténuée de #1/2, survenant lors de l’allocation aux colonnes \* A, B et C (dans cet ordre), où la part proportionnelle de B ne respecte pas la contrainte min (ou max).</span><span class="sxs-lookup"><span data-stu-id="1d56c-119">This is a milder version of #1/#2, arising when allocating to \*-columns A, B, and C (in that order), where B's proportional share violates its min (or max) constraint.</span></span> <span data-ttu-id="1d56c-120">Comme ci-dessus, cela modifie l’espace disponible pour la colonne C, qui obtient une allocation proportionnelle inférieure (ou supérieure) à A,</span><span class="sxs-lookup"><span data-stu-id="1d56c-120">As above, this changes the space available to column C, who gets less (or more) proportional allocation than A did,</span></span></li><li><span data-ttu-id="1d56c-121">Colonnes avec des poids de très grande taille (&gt; 10 ^ 298) sont traitées comme si elles avaient poids 10 ^ 298.</span><span class="sxs-lookup"><span data-stu-id="1d56c-121">Columns with extremely large weights (&gt; 10^298) are all treated as if they had weight 10^298.</span></span> <span data-ttu-id="1d56c-122">Les différences proportionnelles entre elles (et entre les colonnes avec des poids légèrement inférieurs) ne sont pas respectées.</span><span class="sxs-lookup"><span data-stu-id="1d56c-122">Proportional differences between them (and between columns with slightly smaller weights) are not honored.</span></span></li><li><span data-ttu-id="1d56c-123">Colonnes avec des poids d’inifinte ne sont pas traitées correctement.</span><span class="sxs-lookup"><span data-stu-id="1d56c-123">Columns with inifinte weights are not handled correctly.</span></span> <span data-ttu-id="1d56c-124">[Il est en fait impossible de définir un poids infini, mais il s’agit d’une restriction artificielle.</span><span class="sxs-lookup"><span data-stu-id="1d56c-124">[Actually you can't set a weight to Infinity, but this is an artificial restriction.</span></span> <span data-ttu-id="1d56c-125">Le code d’allocation essayait de le gérer, sans succès.]</span><span class="sxs-lookup"><span data-stu-id="1d56c-125">The allocation code was trying to handle it, but doing a bad job.]</span></span></li><li><span data-ttu-id="1d56c-126">Plusieurs problèmes mineurs en évitant le dépassement de capacité positif ou négatif, la perte de précision et autres problèmes liées aux nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="1d56c-126">Several minor problems while avoiding overflow, underflow, loss of precision and similar floating-point issues.</span></span></li><li><span data-ttu-id="1d56c-127">Les ajustements d’arrondi de disposition sont incorrects à un niveau de PPP suffisamment élevé.</span><span class="sxs-lookup"><span data-stu-id="1d56c-127">Adjustments for layout rounding are incorrect at sufficiently high DPI.</span></span></li></ol><span data-ttu-id="1d56c-128">Le nouvel algorithme produit des résultats qui répondent aux critères suivant : A.</span><span class="sxs-lookup"><span data-stu-id="1d56c-128">The new algorithm produces results that meet the following criteria:A.</span></span> <span data-ttu-id="1d56c-129">La largeur réelle assignée à un \*-colonne n’est jamais inférieure à sa largeur minimale ni supérieure à sa largeur maximale. B.</span><span class="sxs-lookup"><span data-stu-id="1d56c-129">The actual width assigned to a \*-column is never less than its minimum width nor greater than its maximum width.B.</span></span> <span data-ttu-id="1d56c-130">Chaque <em>-affecté à la colonne qui n’est pas sa valeur minimale ou la largeur maximale est affectée à une largeur proportionnelle à son <em>-poids. Pour être précis, si deux colonnes sont déclarées avec largeur x</em> et y</em> respectivement, et si aucune colonne reçoit sa largeur minimal ou maximal, les largeurs réel v w assignés aux colonnes dans la même proportion : v / w == x / y.C.</span><span class="sxs-lookup"><span data-stu-id="1d56c-130">Each <em>-column that is not assigned its minimum or maximum width is assigned a width proportional to its <em>-weight. To be precise, if two columns are declared with width x</em> and y</em> respectively, and if neither column receives its minimum or maximum width, the actual widths v and w assigned to the columns are in the same proportion: v / w == x / y.C.</span></span> <span data-ttu-id="1d56c-131">La largeur totale allouée à &quot;proportionnel&quot; *-colonnes est égal à l’espace disponible après avoir alloué pour les colonnes de contraintes (fixe, auto, et *-les colonnes qui sont affectés à leur largeur min ou max).</span><span class="sxs-lookup"><span data-stu-id="1d56c-131">The total width allocated to &quot;proportional&quot; *-columns is equal to the space available after allocating to the constrained columns (fixed, auto, and *-columns that are allocated their min or max width).</span></span> <span data-ttu-id="1d56c-132">Cela peut être égal à zéro, par exemple si la somme des largeurs minimales dépasse la largeur d’availbable de la grille. D.</span><span class="sxs-lookup"><span data-stu-id="1d56c-132">This might be zero, for instance if the sum of the minimum widths exceeds the Grid's availbable width.D.</span></span> <span data-ttu-id="1d56c-133">Toutes ces instructions doivent être interprétés par rapport à la &quot;idéale&quot; mise en page.</span><span class="sxs-lookup"><span data-stu-id="1d56c-133">All these statements are to be interpreted with respect to the &quot;ideal&quot; layout.</span></span> <span data-ttu-id="1d56c-134">Lors de l’arrondi de disposition, la largeur réelle peut différer de la largeur idéale autant qu’un pixel. L’ancien algorithme honorées (A), mais n’a pas pu honorer les autres critères dans les cas présentées ci-dessus. Tout ce dont les informations sur les colonnes et les largeurs dans cet article s’applique également aux lignes et de hauteur.</span><span class="sxs-lookup"><span data-stu-id="1d56c-134">When layout rounding is in effect, the actual widths can differ from the ideal widths by as much as one pixel.The old algorithm honored (A) but failed to honor the other criteria in the cases outlined above.Everything said about columns and widths in this article applies as well to rows and heights.</span></span>|
|<span data-ttu-id="1d56c-135">Suggestion</span><span class="sxs-lookup"><span data-stu-id="1d56c-135">Suggestion</span></span>|<span data-ttu-id="1d56c-136">Par défaut, les applications que ciblent des versions du .NET Framework en commençant par le 4.7 Framework .NET seront afficher le nouvel algorithme, pendant que la cible du .NET Framework 4.6.2 ou des versions antérieures seront afficher l’ancien algorithme des applications. Pour remplacer la valeur par défaut, utilisez le paramètre de configuration suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d56c-136">By default, apps that target versions of the .NET Framework starting with the .NET Framework 4.7 will see the new algorithm, while apps that target the .NET Framework 4.6.2 or earlier versions will see the old algorithm.To override the default, use the following configuration setting:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre><span data-ttu-id="1d56c-137">La valeur 'true' Sélectionne l’algorithme ancien, 'false' Sélectionne le nouvel algorithme.</span><span class="sxs-lookup"><span data-stu-id="1d56c-137">The value 'true' selects the old algorithm, 'false' selects the new algorithm.</span></span>|
|<span data-ttu-id="1d56c-138">Portée</span><span class="sxs-lookup"><span data-stu-id="1d56c-138">Scope</span></span>|<span data-ttu-id="1d56c-139">Mineur</span><span class="sxs-lookup"><span data-stu-id="1d56c-139">Minor</span></span>|
|<span data-ttu-id="1d56c-140">Version</span><span class="sxs-lookup"><span data-stu-id="1d56c-140">Version</span></span>|<span data-ttu-id="1d56c-141">4.7</span><span class="sxs-lookup"><span data-stu-id="1d56c-141">4.7</span></span>|
|<span data-ttu-id="1d56c-142">Type</span><span class="sxs-lookup"><span data-stu-id="1d56c-142">Type</span></span>|<span data-ttu-id="1d56c-143">Reciblage</span><span class="sxs-lookup"><span data-stu-id="1d56c-143">Retargeting</span></span>|
