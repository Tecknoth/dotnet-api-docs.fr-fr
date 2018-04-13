### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a><span data-ttu-id="92f12-101">Items.Refresh appel sur un contrôle ListBox de WPF, ListView ou DataGrid avec les éléments sélectionnés peuvent entraîner des éléments en double dans l’élément</span><span class="sxs-lookup"><span data-stu-id="92f12-101">Calling Items.Refresh on a WPF ListBox, ListView, or DataGrid with items selected can cause duplicate items to appear in the element</span></span>

|   |   |
|---|---|
|<span data-ttu-id="92f12-102">Détails</span><span class="sxs-lookup"><span data-stu-id="92f12-102">Details</span></span>|<span data-ttu-id="92f12-103">Dans le .NET Framework 4.5, appeler ListBox.Items.Refresh à partir du code, tandis que les éléments sont sélectionnés dans un <xref:System.Windows.Controls.ListBox?displayProperty=name> peut entraîner les éléments sélectionnés à être dupliqué dans la liste.</span><span class="sxs-lookup"><span data-stu-id="92f12-103">In the .NET Framework 4.5, calling ListBox.Items.Refresh from code while items are selected in a <xref:System.Windows.Controls.ListBox?displayProperty=name> can cause the selected items to be duplicated in the list.</span></span> <span data-ttu-id="92f12-104">Un problème similaire se produit avec <xref:System.Windows.Controls.ListView?displayProperty=name> et <xref:System.Windows.Controls.DataGrid?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="92f12-104">A similar issue occurs with <xref:System.Windows.Controls.ListView?displayProperty=name> and <xref:System.Windows.Controls.DataGrid?displayProperty=name>.</span></span> <span data-ttu-id="92f12-105">Ce problème a été résolu dans le .NET Framework 4.6.</span><span class="sxs-lookup"><span data-stu-id="92f12-105">This is fixed in the .NET Framework 4.6.</span></span>|
|<span data-ttu-id="92f12-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="92f12-106">Suggestion</span></span>|<span data-ttu-id="92f12-107">Ce problème peut être contourné en désactivant par programmation des éléments avant <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> est appelée, puis ré-en les sélectionnant après la fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="92f12-107">This issue may be worked around by programatically unselecting items before <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> is called and then re-selecting them after the call is completed.</span></span> <span data-ttu-id="92f12-108">Étant donné que ce problème a été résolu dans le .NET Framework 4.6, vous pouvez également mettre à niveau votre version du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="92f12-108">Alternatively, this issue has been fixed in the .NET Framework 4.6 and may be addressed by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="92f12-109">Portée</span><span class="sxs-lookup"><span data-stu-id="92f12-109">Scope</span></span>|<span data-ttu-id="92f12-110">Mineur</span><span class="sxs-lookup"><span data-stu-id="92f12-110">Minor</span></span>|
|<span data-ttu-id="92f12-111">Version</span><span class="sxs-lookup"><span data-stu-id="92f12-111">Version</span></span>|<span data-ttu-id="92f12-112">4.5</span><span class="sxs-lookup"><span data-stu-id="92f12-112">4.5</span></span>|
|<span data-ttu-id="92f12-113">Type</span><span class="sxs-lookup"><span data-stu-id="92f12-113">Type</span></span>|<span data-ttu-id="92f12-114">Runtime</span><span class="sxs-lookup"><span data-stu-id="92f12-114">Runtime</span></span>|
|<span data-ttu-id="92f12-115">API affectées</span><span class="sxs-lookup"><span data-stu-id="92f12-115">Affected APIs</span></span>|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|
