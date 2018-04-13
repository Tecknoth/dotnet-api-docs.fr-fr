### <a name="incorrect-implementation-of-memberdescriptorequals"></a><span data-ttu-id="cf0e0-101">Implémentation incorrecte de MemberDescriptor.Equals</span><span class="sxs-lookup"><span data-stu-id="cf0e0-101">Incorrect implementation of MemberDescriptor.Equals</span></span>

|   |   |
|---|---|
|<span data-ttu-id="cf0e0-102">Détails</span><span class="sxs-lookup"><span data-stu-id="cf0e0-102">Details</span></span>|<span data-ttu-id="cf0e0-103">Implémentation d’origine de &quot;est égal à&quot; méthode a été comparant deux propriétés de chaîne différents à partir des objets sous comparaison : nom de catégorie pour la chaîne de description.</span><span class="sxs-lookup"><span data-stu-id="cf0e0-103">Original implementation of &quot;Equals&quot; method was comparing two different string properties from the objects under comparison: category name to description string.</span></span> <span data-ttu-id="cf0e0-104">La solution consiste à comparer &quot;catégorie&quot; du premier objet à &quot;catégorie&quot; de la seconde et &quot;description&quot; à &quot;description&quot;.</span><span class="sxs-lookup"><span data-stu-id="cf0e0-104">The fix is to compare &quot;category&quot; of first object to &quot;category&quot; of the second one and &quot;description&quot; to &quot;description&quot;.</span></span> <span data-ttu-id="cf0e0-105">Valeur de configuration de MemberDescriptorEqualsReturnsFalseIfEquivalent peut être définie sur true pour désactiver le nouveau comportement si 4.6.2 ou false pour activer ce correctif lorsque cibler la version de framework est inférieur à 4.6.2.</span><span class="sxs-lookup"><span data-stu-id="cf0e0-105">MemberDescriptorEqualsReturnsFalseIfEquivalent configuration value can be set to true to opt out of the new behavior if targeting 4.6.2 or to false to enable this fix when targeting framework version is below 4.6.2.</span></span>|
|<span data-ttu-id="cf0e0-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="cf0e0-106">Suggestion</span></span>|<span data-ttu-id="cf0e0-107">Si votre application dépend de MemberDescriptor.Equals parfois retournant la valeur false lorsque les descripteurs sont équivalents, et que vous prévoyez 4.6.2 version du .NET Framework, vous disposez de plusieurs options :</span><span class="sxs-lookup"><span data-stu-id="cf0e0-107">If your application depends on MemberDescriptor.Equals sometimes returning false when descriptors are equivalent, and you are targeting 4.6.2 version of the .NET Framework, you have several options:</span></span><ol><li><span data-ttu-id="cf0e0-108">Apporter des modifications de code à comparer &quot;catégorie&quot; et &quot;description&quot; champs manuellement en plus de la méthode Equals en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cf0e0-108">Make code changes to compare &quot;category&quot; and &quot;description&quot; fields manually in addition to running Equals method.</span></span></li><li><span data-ttu-id="cf0e0-109">Choisir à partir de cette modification en ajoutant la valeur suivante au fichier app.config :</span><span class="sxs-lookup"><span data-stu-id="cf0e0-109">Opt out from this change by adding the following value to the app.config file:</span></span></li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre><span data-ttu-id="cf0e0-110">Si votre application cible 4.6.1 ou une version antérieure de .NET Framework et que vous souhaitez que cette modification activée, vous pouvez définir le commutateur de compatibilité à false en ajoutant la valeur suivante au fichier app.config :</span><span class="sxs-lookup"><span data-stu-id="cf0e0-110">If your application targets 4.6.1 or lower version of the .NET Framework, and you want this change enabled, you can set the compatibility switch to false by adding the following value to the app.config file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="cf0e0-111">Portée</span><span class="sxs-lookup"><span data-stu-id="cf0e0-111">Scope</span></span>|<span data-ttu-id="cf0e0-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cf0e0-112">Edge</span></span>|
|<span data-ttu-id="cf0e0-113">Version</span><span class="sxs-lookup"><span data-stu-id="cf0e0-113">Version</span></span>|<span data-ttu-id="cf0e0-114">4.6.2</span><span class="sxs-lookup"><span data-stu-id="cf0e0-114">4.6.2</span></span>|
|<span data-ttu-id="cf0e0-115">Type</span><span class="sxs-lookup"><span data-stu-id="cf0e0-115">Type</span></span>|<span data-ttu-id="cf0e0-116">Reciblage</span><span class="sxs-lookup"><span data-stu-id="cf0e0-116">Retargeting</span></span>|
|<span data-ttu-id="cf0e0-117">API affectées</span><span class="sxs-lookup"><span data-stu-id="cf0e0-117">Affected APIs</span></span>|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|
