### <a name="wpf-spell-checking-fails-in-unexpected-ways"></a><span data-ttu-id="48bf9-101">La correction orthographique dans WPF échoue de façon inattendue</span><span class="sxs-lookup"><span data-stu-id="48bf9-101">WPF Spell Checking fails in unexpected ways</span></span>

|   |   |
|---|---|
|<span data-ttu-id="48bf9-102">Détails</span><span class="sxs-lookup"><span data-stu-id="48bf9-102">Details</span></span>|<span data-ttu-id="48bf9-103">Cela inclut un nombre de problèmes de vérificateur d’orthographe WPF :</span><span class="sxs-lookup"><span data-stu-id="48bf9-103">This includes a number of WPF Spell Checker issues:</span></span><ul><li><span data-ttu-id="48bf9-104">Vérificateur d’orthographe WPF lève parfois <xref:System.Runtime.InteropServices.COMException?displayProperty=name></span><span class="sxs-lookup"><span data-stu-id="48bf9-104">WPF Spell Checker sometimes throws <xref:System.Runtime.InteropServices.COMException?displayProperty=name></span></span></li><li><span data-ttu-id="48bf9-105">Vérificateur d’orthographe WPF échoue avec <xref:System.UnauthorizedAccessException> lorsque les applications sont lancées à l’aide de « exécuter en tant qu’utilisateur différent »</span><span class="sxs-lookup"><span data-stu-id="48bf9-105">WPF Spell Checker fails with <xref:System.UnauthorizedAccessException> when applications are launched using 'run as different user'</span></span></li><li><span data-ttu-id="48bf9-106">Vérificateur d’orthographe WPF identifie incorrectement les fautes d’orthographe dans les mots composés comme 'Hausnummer' en allemand.</span><span class="sxs-lookup"><span data-stu-id="48bf9-106">WPF Spell Checker incorrectly identifies spelling errors in compound words like 'Hausnummer' in German.</span></span></li></ul>|
|<span data-ttu-id="48bf9-107">Suggestion</span><span class="sxs-lookup"><span data-stu-id="48bf9-107">Suggestion</span></span>|<span data-ttu-id="48bf9-108">Problème #1 : ce problème a été corrigé dans .NET Framework 4.6.2 problème n° 2 - vérificateur orthographique de WPF n’est plus pris en charge lorsque les applications sont lancées à l’aide de « exécuter en tant qu’utilisateur différent ».</span><span class="sxs-lookup"><span data-stu-id="48bf9-108">Issue #1 - This has been fixed in .NET Framework 4.6.2 Issue #2 - WPF Spell Checker is no longer supported when applications are launched using 'run as different user'.</span></span> <span data-ttu-id="48bf9-109">À partir de .NET Framework 4.6.2, applications lancées de cette manière ne seront bloquent plus inattendu : à la place le vérificateur d’orthographe va être désactivé en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="48bf9-109">Starting .NET Framework 4.6.2, applications launched in this manner will no longer crash unexpectedly - instead the Spell Checker will be silently disabled.</span></span> <span data-ttu-id="48bf9-110">Problème #3 - ce problème a été corrigé dans .NET Framework 4.6.2.</span><span class="sxs-lookup"><span data-stu-id="48bf9-110">Issue #3 - This has been fixed in .NET Framework 4.6.2.</span></span>|
|<span data-ttu-id="48bf9-111">Portée</span><span class="sxs-lookup"><span data-stu-id="48bf9-111">Scope</span></span>|<span data-ttu-id="48bf9-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="48bf9-112">Edge</span></span>|
|<span data-ttu-id="48bf9-113">Version</span><span class="sxs-lookup"><span data-stu-id="48bf9-113">Version</span></span>|<span data-ttu-id="48bf9-114">4.6.1</span><span class="sxs-lookup"><span data-stu-id="48bf9-114">4.6.1</span></span>|
|<span data-ttu-id="48bf9-115">Type</span><span class="sxs-lookup"><span data-stu-id="48bf9-115">Type</span></span>|<span data-ttu-id="48bf9-116">Runtime</span><span class="sxs-lookup"><span data-stu-id="48bf9-116">Runtime</span></span>|
