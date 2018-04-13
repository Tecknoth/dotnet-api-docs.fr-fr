### <a name="changes-in-path-normalization"></a><span data-ttu-id="0ce9c-101">Modifications apportées à la normalisation du chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="0ce9c-101">Changes in path normalization</span></span>

|   |   |
|---|---|
|<span data-ttu-id="0ce9c-102">Détails</span><span class="sxs-lookup"><span data-stu-id="0ce9c-102">Details</span></span>|<span data-ttu-id="0ce9c-103">Compter des applications qui ciblent le .NET Framework 4.6.2, la normalise les chemins d’accès dans lequel le runtime a été modifiée. Normalisation d’un chemin d’accès implique la modification de la chaîne qui identifie un fichier ou un chemin d’accès afin qu’il soit conforme à un chemin d’accès valide sur le système d’exploitation cible.</span><span class="sxs-lookup"><span data-stu-id="0ce9c-103">Starting with apps that target the .NET Framework 4.6.2, the way in which the runtime normalizes paths has changed.Normalizing a path involves modifying the string that identifies a path or file so that it conforms to a valid path on the target operating system.</span></span> <span data-ttu-id="0ce9c-104">La normalisation implique généralement :</span><span class="sxs-lookup"><span data-stu-id="0ce9c-104">Normalization typically involves:</span></span><ul><li><span data-ttu-id="0ce9c-105">La mise en forme canonique des composants et séparateurs de répertoires.</span><span class="sxs-lookup"><span data-stu-id="0ce9c-105">Canonicalizing component and directory separators.</span></span></li><li><span data-ttu-id="0ce9c-106">L’application du répertoire actuel à un chemin d’accès relatif.</span><span class="sxs-lookup"><span data-stu-id="0ce9c-106">Applying the current directory to a relative path.</span></span></li><li><span data-ttu-id="0ce9c-107">L’évaluation du répertoire relatif (.) ou le répertoire parent (.) dans un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="0ce9c-107">Evaluating the relative directory (.) or the parent directory (..) in a path.</span></span></li><li><span data-ttu-id="0ce9c-108">La suppression des caractères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0ce9c-108">Trimming specified characters.</span></span></li></ul><span data-ttu-id="0ce9c-109">Compter des applications qui ciblent le .NET Framework 4.6.2, les modifications suivantes dans la normalisation du chemin d’accès sont activées par défaut :</span><span class="sxs-lookup"><span data-stu-id="0ce9c-109">Starting with apps that target the .NET Framework 4.6.2, the following changes in path normalization are enabled by default:</span></span><ul><li><span data-ttu-id="0ce9c-110">Le runtime défère à la fonction [GetFullPathName](https://msdn.microsoft.com/library/windows/desktop/aa364963(v=vs.85).aspx) du système d’exploitation pour normaliser les chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="0ce9c-110">The runtime defers to the operating system's [GetFullPathName](https://msdn.microsoft.com/library/windows/desktop/aa364963(v=vs.85).aspx) function to normalize paths.</span></span></li><li><span data-ttu-id="0ce9c-111">La normalisation n’implique plus la suppression de la fin des segments de répertoire (comme un espace à la fin d’un nom de répertoire).</span><span class="sxs-lookup"><span data-stu-id="0ce9c-111">Normalization no longer involves trimming the end of directory segments (such as a space at the end of a directory name).</span></span></li><li><span data-ttu-id="0ce9c-112">Prise en charge pour la syntaxe de chemin d’accès de périphérique en mode confiance totale, y compris <code>\\.\</code> and, for file I/O APIs in mscorlib.dll, '\?'.</span><span class="sxs-lookup"><span data-stu-id="0ce9c-112">Support for device path syntax in full trust, including <code>\\.\</code> and, for file I/O APIs in mscorlib.dll, '\?'.</span></span></li><li>The runtime does not validate device syntax paths.</li><li>The use of device syntax to access alternate data streams is supported.</li></ul>These changes improve performance while allowing methods to access previously inaccessible paths. Apps that target the .NET Framework 4.6.1 and earlier versions but are running under the .NET Framework 4.6.2 or later are unaffected by this change.|
|<span data-ttu-id="0ce9c-113">Suggestion</span><span class="sxs-lookup"><span data-stu-id="0ce9c-113">Suggestion</span></span>|<span data-ttu-id="0ce9c-114">Les applications qui ciblent le .NET Framework 4.6.2 ou version ultérieure peuvent la refuser cette modifier et utiliser la normalisation héritée en ajoutant le code suivant à la <code>&lt;runtime&gt;</code> section du fichier de configuration d’application :</span><span class="sxs-lookup"><span data-stu-id="0ce9c-114">Apps that target the .NET Framework 4.6.2 or later can opt out of this change and use legacy normalization by adding the following to the <code>&lt;runtime&gt;</code> section of the application configuration file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.UseLegacyPathHandling=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre><span data-ttu-id="0ce9c-115">Les applications qui ciblent le .NET Framework 4.6.1 ou antérieures mais sont en cours d’exécution sur le .NET Framework 4.6.2 ou versions ultérieures permettent les modifications apportées à la normalisation du chemin d’accès en ajoutant la ligne suivante à la <code>&lt;runtime&gt;</code> section du fichier .configuration application :</span><span class="sxs-lookup"><span data-stu-id="0ce9c-115">Apps that target the .NET Framework 4.6.1 or earlier but are running on the .NET Framework 4.6.2 or later can enable the changes to path normalization by adding the following line to the <code>&lt;runtime&gt;</code> section of the application .configuration file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.UseLegacyPathHandling=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="0ce9c-116">Portée</span><span class="sxs-lookup"><span data-stu-id="0ce9c-116">Scope</span></span>|<span data-ttu-id="0ce9c-117">Mineur</span><span class="sxs-lookup"><span data-stu-id="0ce9c-117">Minor</span></span>|
|<span data-ttu-id="0ce9c-118">Version</span><span class="sxs-lookup"><span data-stu-id="0ce9c-118">Version</span></span>|<span data-ttu-id="0ce9c-119">4.6.2</span><span class="sxs-lookup"><span data-stu-id="0ce9c-119">4.6.2</span></span>|
|<span data-ttu-id="0ce9c-120">Type</span><span class="sxs-lookup"><span data-stu-id="0ce9c-120">Type</span></span>|<span data-ttu-id="0ce9c-121">Reciblage</span><span class="sxs-lookup"><span data-stu-id="0ce9c-121">Retargeting</span></span>|
