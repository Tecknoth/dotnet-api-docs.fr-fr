### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a><span data-ttu-id="c3d94-101">Application.FilterMessage ne lève plus pour les implémentations réentrantes de IMessageFilter.PreFilterMessage</span><span class="sxs-lookup"><span data-stu-id="c3d94-101">Application.FilterMessage no longer throws for re-entrant implementations of IMessageFilter.PreFilterMessage</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c3d94-102">Détails</span><span class="sxs-lookup"><span data-stu-id="c3d94-102">Details</span></span>|<span data-ttu-id="c3d94-103">Avant le .NET Framework 4.6.1, en appelant <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> avec un <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> qui appelée <xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> ou <xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> (tout en appelant <xref:System.Windows.Forms.Application.DoEvents>) provoquerait une <xref:System.IndexOutOfRangeException?displayProperty=name>. À partir des applications qui ciblent le .NET Framework 4.6.1, cette exception ne soit plus levée et rentrant comme décrit ci-dessus peut utiliser des filtres.</span><span class="sxs-lookup"><span data-stu-id="c3d94-103">Prior to the .NET Framework 4.6.1, calling <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> with an <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> which called <xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> or <xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> (while also calling <xref:System.Windows.Forms.Application.DoEvents>) would cause an <xref:System.IndexOutOfRangeException?displayProperty=name>.Beginning with applications targeting the .NET Framework 4.6.1, this exception is no longer thrown, and re-entrant filters as described above may be used.</span></span>|
|<span data-ttu-id="c3d94-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="c3d94-104">Suggestion</span></span>|<span data-ttu-id="c3d94-105">N’oubliez pas que <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> n’est plus lève pour le réentrante <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> comportement décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c3d94-105">Be aware that <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> will no longer throw for the re-entrant <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> behavior described above.</span></span> <span data-ttu-id="c3d94-106">Cela affecte uniquement les applications qui ciblent le .NET Framework 4.6.1.Apps ciblant le .NET Framework 4.6.1 peut refuser cette modification (ou les applications ciblant des infrastructures plus anciens peuvent s’abonner) à l’aide de la [DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation) commutateur de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="c3d94-106">This only affects applications targeting the .NET Framework 4.6.1.Apps targeting the .NET Framework 4.6.1 can opt out of this change (or apps targeting older Frameworks may opt in) by using the [DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation) compatibility switch.</span></span>|
|<span data-ttu-id="c3d94-107">Portée</span><span class="sxs-lookup"><span data-stu-id="c3d94-107">Scope</span></span>|<span data-ttu-id="c3d94-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c3d94-108">Edge</span></span>|
|<span data-ttu-id="c3d94-109">Version</span><span class="sxs-lookup"><span data-stu-id="c3d94-109">Version</span></span>|<span data-ttu-id="c3d94-110">4.6.1</span><span class="sxs-lookup"><span data-stu-id="c3d94-110">4.6.1</span></span>|
|<span data-ttu-id="c3d94-111">Type</span><span class="sxs-lookup"><span data-stu-id="c3d94-111">Type</span></span>|<span data-ttu-id="c3d94-112">Reciblage</span><span class="sxs-lookup"><span data-stu-id="c3d94-112">Retargeting</span></span>|
|<span data-ttu-id="c3d94-113">API affectées</span><span class="sxs-lookup"><span data-stu-id="c3d94-113">Affected APIs</span></span>|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|
