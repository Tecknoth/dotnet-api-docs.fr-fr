### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a><span data-ttu-id="1a78b-101">Faites défiler vers le dernier élément dans ItemsControls (par exemple, la zone de liste et DataGrid) par intermittence impossible lors de l’utilisation de DataTemplates personnalisé</span><span class="sxs-lookup"><span data-stu-id="1a78b-101">Intermittently unable to scroll to bottom item in ItemsControls (like ListBox and DataGrid) when using custom DataTemplates</span></span>

|   |   |
|---|---|
|<span data-ttu-id="1a78b-102">Détails</span><span class="sxs-lookup"><span data-stu-id="1a78b-102">Details</span></span>|<span data-ttu-id="1a78b-103">Dans certains cas, un bogue dans le .NET Framework 4.5 est à l’origine ItemsControls (comme <xref:System.Windows.Controls.ListBox?displayProperty=name>, <xref:System.Windows.Controls.ComboBox?displayProperty=name>, <xref:System.Windows.Controls.DataGrid?displayProperty=name>, etc.) pour faire défiler ne pas à leur élément bas lors de l’utilisation de DataTemplates personnalisé.</span><span class="sxs-lookup"><span data-stu-id="1a78b-103">In some instances, a bug in the .NET Framework 4.5 is causing ItemsControls (like <xref:System.Windows.Controls.ListBox?displayProperty=name>, <xref:System.Windows.Controls.ComboBox?displayProperty=name>, <xref:System.Windows.Controls.DataGrid?displayProperty=name>, etc.) to not scroll to their bottom item when using custom DataTemplates.</span></span> <span data-ttu-id="1a78b-104">Si le défilement est tenté une deuxième fois (après avoir fait défiler jusqu’en haut), il fonctionnera.</span><span class="sxs-lookup"><span data-stu-id="1a78b-104">If the scrolling is attempted a second time (after scrolling back up), it will work then.</span></span>|
|<span data-ttu-id="1a78b-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="1a78b-105">Suggestion</span></span>|<span data-ttu-id="1a78b-106">Étant donné que ce problème a été résolu dans le .NET Framework 4.5.2, vous pouvez également mettre à niveau votre version du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="1a78b-106">This issue has been fixed in the .NET Framework 4.5.2 and may be addressed by upgrading to that version (or a later version) of the .NET Framework.</span></span> <span data-ttu-id="1a78b-107">Vous pouvez également faire glisser les barres de défilement jusqu’au dernier élément de la collection, mais aurez peut-être à recommencer l’opération une deuxième fois pour y arriver.</span><span class="sxs-lookup"><span data-stu-id="1a78b-107">Alternatively, users can still drag scroll bars to the final items in these collections, but may need to try twice to do so successfully.</span></span>|
|<span data-ttu-id="1a78b-108">Portée</span><span class="sxs-lookup"><span data-stu-id="1a78b-108">Scope</span></span>|<span data-ttu-id="1a78b-109">Mineur</span><span class="sxs-lookup"><span data-stu-id="1a78b-109">Minor</span></span>|
|<span data-ttu-id="1a78b-110">Version</span><span class="sxs-lookup"><span data-stu-id="1a78b-110">Version</span></span>|<span data-ttu-id="1a78b-111">4.5</span><span class="sxs-lookup"><span data-stu-id="1a78b-111">4.5</span></span>|
|<span data-ttu-id="1a78b-112">Type</span><span class="sxs-lookup"><span data-stu-id="1a78b-112">Type</span></span>|<span data-ttu-id="1a78b-113">Runtime</span><span class="sxs-lookup"><span data-stu-id="1a78b-113">Runtime</span></span>|
