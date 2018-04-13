### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a><span data-ttu-id="25a96-101">L’accès aux éléments sélectionnés d’un DataGrid WPF à partir d’un gestionnaire d’événement de UnloadingRow du DataGrid peut provoquer une exception NullReferenceException</span><span class="sxs-lookup"><span data-stu-id="25a96-101">Accessing a WPF DataGrid's selected items from a handler of the DataGrid's UnloadingRow event can cause a NullReferenceException</span></span>

|   |   |
|---|---|
|<span data-ttu-id="25a96-102">Détails</span><span class="sxs-lookup"><span data-stu-id="25a96-102">Details</span></span>|<span data-ttu-id="25a96-103">En raison d’un bogue dans le .NET Framework 4.5, les gestionnaires d’événements pour <xref:System.Windows.Controls.DataGrid> événements liés à la suppression d’une ligne peuvent entraîner un <xref:System.NullReferenceException?displayProperty=name> levée si elles accèdent à la <xref:System.Windows.Controls.DataGrid>de <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> ou <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> propriétés.</span><span class="sxs-lookup"><span data-stu-id="25a96-103">Due to a bug in the .NET Framework 4.5, event handlers for <xref:System.Windows.Controls.DataGrid> events involving the removal of a row can cause a <xref:System.NullReferenceException?displayProperty=name> to be thrown if they access the <xref:System.Windows.Controls.DataGrid>'s <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> or <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> properties.</span></span>|
|<span data-ttu-id="25a96-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="25a96-104">Suggestion</span></span>|<span data-ttu-id="25a96-105">Ce problème a été résolu dans le .NET Framework 4.6 et peut être adressé par la mise à niveau vers cette version du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="25a96-105">This issue has been fixed in the .NET Framework 4.6 and may be addressed by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="25a96-106">Portée</span><span class="sxs-lookup"><span data-stu-id="25a96-106">Scope</span></span>|<span data-ttu-id="25a96-107">Mineur</span><span class="sxs-lookup"><span data-stu-id="25a96-107">Minor</span></span>|
|<span data-ttu-id="25a96-108">Version</span><span class="sxs-lookup"><span data-stu-id="25a96-108">Version</span></span>|<span data-ttu-id="25a96-109">4.5</span><span class="sxs-lookup"><span data-stu-id="25a96-109">4.5</span></span>|
|<span data-ttu-id="25a96-110">Type</span><span class="sxs-lookup"><span data-stu-id="25a96-110">Type</span></span>|<span data-ttu-id="25a96-111">Runtime</span><span class="sxs-lookup"><span data-stu-id="25a96-111">Runtime</span></span>|
|<span data-ttu-id="25a96-112">API affectées</span><span class="sxs-lookup"><span data-stu-id="25a96-112">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|
