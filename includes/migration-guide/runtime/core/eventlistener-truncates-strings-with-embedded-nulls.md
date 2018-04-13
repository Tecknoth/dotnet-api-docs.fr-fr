### <a name="eventlistener-truncates-strings-with-embedded-nulls"></a><span data-ttu-id="08cca-101">EventListener tronque les chaînes comportant des valeurs null incorporées</span><span class="sxs-lookup"><span data-stu-id="08cca-101">EventListener truncates strings with embedded nulls</span></span>

|   |   |
|---|---|
|<span data-ttu-id="08cca-102">Détails</span><span class="sxs-lookup"><span data-stu-id="08cca-102">Details</span></span>|<span data-ttu-id="08cca-103"><xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> tronque les chaînes comportant des valeurs null incorporées.</span><span class="sxs-lookup"><span data-stu-id="08cca-103"><xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> truncates strings with embedded nulls.</span></span> <span data-ttu-id="08cca-104">Les caractères Null ne sont pas pris en charge par la classe <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="08cca-104">Null characters are not supported by the <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> class.</span></span> <span data-ttu-id="08cca-105">La modification affecte uniquement les applications qui utilisent <xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> pour lire des données <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> dans le processus et qui utilisent des caractères Null comme délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="08cca-105">The change only affects apps that use <xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> to read <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> data in process and that use null characters as delimiters.</span></span>|
|<span data-ttu-id="08cca-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="08cca-106">Suggestion</span></span>|<span data-ttu-id="08cca-107"><xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> données doivent être mises à jour, si possible, pour ne pas utiliser de caractères null incorporés.</span><span class="sxs-lookup"><span data-stu-id="08cca-107"><xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> data should be updated, if possible, to not use embedded null characters.</span></span>|
|<span data-ttu-id="08cca-108">Portée</span><span class="sxs-lookup"><span data-stu-id="08cca-108">Scope</span></span>|<span data-ttu-id="08cca-109">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="08cca-109">Edge</span></span>|
|<span data-ttu-id="08cca-110">Version</span><span class="sxs-lookup"><span data-stu-id="08cca-110">Version</span></span>|<span data-ttu-id="08cca-111">4.5.1</span><span class="sxs-lookup"><span data-stu-id="08cca-111">4.5.1</span></span>|
|<span data-ttu-id="08cca-112">Type</span><span class="sxs-lookup"><span data-stu-id="08cca-112">Type</span></span>|<span data-ttu-id="08cca-113">Runtime</span><span class="sxs-lookup"><span data-stu-id="08cca-113">Runtime</span></span>|
|<span data-ttu-id="08cca-114">API affectées</span><span class="sxs-lookup"><span data-stu-id="08cca-114">Affected APIs</span></span>|<ul><li><xref:System.Diagnostics.Tracing.EventListener.%23ctor?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel,System.Diagnostics.Tracing.EventKeywords)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel,System.Diagnostics.Tracing.EventKeywords,System.Collections.Generic.IDictionary{System.String,System.String})?displayProperty=nameWithType></li></ul>|
