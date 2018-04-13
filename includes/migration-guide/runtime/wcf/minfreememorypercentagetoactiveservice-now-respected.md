### <a name="minfreememorypercentagetoactiveservice-is-now-respected"></a><span data-ttu-id="394c8-101">MinFreeMemoryPercentageToActiveService est respectée maintenant</span><span class="sxs-lookup"><span data-stu-id="394c8-101">MinFreeMemoryPercentageToActiveService is now respected</span></span>

|   |   |
|---|---|
|<span data-ttu-id="394c8-102">Détails</span><span class="sxs-lookup"><span data-stu-id="394c8-102">Details</span></span>|<span data-ttu-id="394c8-103">Ce paramètre détermine la mémoire minimale devant être disponible sur le serveur avant l’activation d’un service WCF.</span><span class="sxs-lookup"><span data-stu-id="394c8-103">This setting establishes the minimum memory that must be available on the server before a WCF service can be activated.</span></span> <span data-ttu-id="394c8-104">Il a pour but de prévenir les exceptions <xref:System.OutOfMemoryException?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="394c8-104">It is designed to prevent <xref:System.OutOfMemoryException?displayProperty=name> exceptions.</span></span> <span data-ttu-id="394c8-105">Dans le .NET Framework 4.5, ce paramètre était sans effet.</span><span class="sxs-lookup"><span data-stu-id="394c8-105">In the .NET Framework 4.5, this setting had no effect.</span></span> <span data-ttu-id="394c8-106">Dans le .NET Framework 4.5.1, ce paramètre est pris en compte.</span><span class="sxs-lookup"><span data-stu-id="394c8-106">In the .NET Framework 4.5.1, the setting is observed.</span></span>|
|<span data-ttu-id="394c8-107">Suggestion</span><span class="sxs-lookup"><span data-stu-id="394c8-107">Suggestion</span></span>|<span data-ttu-id="394c8-108">Une exception se produit si la mémoire disponible sur le serveur web est inférieure au pourcentage défini par le paramètre de configuration.</span><span class="sxs-lookup"><span data-stu-id="394c8-108">An exception occurs if the free memory available on the web server is less than the percentage defined by the configuration setting.</span></span> <span data-ttu-id="394c8-109">Certains services WCF qui ont réussi à démarrer et à s'exécuter dans un environnement où la mémoire est limitée risquent à présent d'échouer.</span><span class="sxs-lookup"><span data-stu-id="394c8-109">Some WCF services that successfully started and ran in a constrained memory environment may now fail.</span></span>|
|<span data-ttu-id="394c8-110">Portée</span><span class="sxs-lookup"><span data-stu-id="394c8-110">Scope</span></span>|<span data-ttu-id="394c8-111">Mineur</span><span class="sxs-lookup"><span data-stu-id="394c8-111">Minor</span></span>|
|<span data-ttu-id="394c8-112">Version</span><span class="sxs-lookup"><span data-stu-id="394c8-112">Version</span></span>|<span data-ttu-id="394c8-113">4.5.1</span><span class="sxs-lookup"><span data-stu-id="394c8-113">4.5.1</span></span>|
|<span data-ttu-id="394c8-114">Type</span><span class="sxs-lookup"><span data-stu-id="394c8-114">Type</span></span>|<span data-ttu-id="394c8-115">Runtime</span><span class="sxs-lookup"><span data-stu-id="394c8-115">Runtime</span></span>|
