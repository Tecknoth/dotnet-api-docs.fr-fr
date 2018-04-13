### <a name="systemuri-escaping-now-supports-rfc-3986"></a><span data-ttu-id="c9bec-101">Séquence d’échappement System.Uri prend désormais en charge la norme RFC 3986</span><span class="sxs-lookup"><span data-stu-id="c9bec-101">System.Uri escaping now supports RFC 3986</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c9bec-102">Détails</span><span class="sxs-lookup"><span data-stu-id="c9bec-102">Details</span></span>|<span data-ttu-id="c9bec-103">L’échappement d’URI a été modifié dans le .NET 4.5 de manière à prendre en charge la norme [RFC 3986](http://tools.ietf.org/html/rfc3986).</span><span class="sxs-lookup"><span data-stu-id="c9bec-103">URI escaping has changed in .NET 4.5 to support [RFC 3986](http://tools.ietf.org/html/rfc3986).</span></span> <span data-ttu-id="c9bec-104">Ces modifications sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9bec-104">Specific changes include:</span></span><ul><li><span data-ttu-id="c9bec-105"><xref:System.Uri.EscapeDataString(System.String)?displayProperty=name> représente une séquence d'échappement pour les caractères réservés basés sur la norme RFC 3986.</span><span class="sxs-lookup"><span data-stu-id="c9bec-105"><xref:System.Uri.EscapeDataString(System.String)?displayProperty=name> escapes reserved characters based on RFC 3986.</span></span></li><li><span data-ttu-id="c9bec-106"><xref:System.Uri.EscapeUriString(System.String)?displayProperty=name> ne représente pas une séquence d'échappement pour les caractères réservés.</span><span class="sxs-lookup"><span data-stu-id="c9bec-106"><xref:System.Uri.EscapeUriString(System.String)?displayProperty=name> does not escape reserved characters.</span></span></li><li><span data-ttu-id="c9bec-107"><xref:System.Uri.UnescapeDataString(System.String)?displayProperty=name> ne lève pas d'exception s'il rencontre une séquence d'échappement non valide.</span><span class="sxs-lookup"><span data-stu-id="c9bec-107"><xref:System.Uri.UnescapeDataString(System.String)?displayProperty=name> does not throw an exception if it encounters an invalid escape sequence.</span></span></li><li><span data-ttu-id="c9bec-108">Les caractères d'échappement non réservés sont sans séquence d'échappement.</span><span class="sxs-lookup"><span data-stu-id="c9bec-108">Unreserved escaped characters are un-escaped.</span></span></li></ul>|
|<span data-ttu-id="c9bec-109">Suggestion</span><span class="sxs-lookup"><span data-stu-id="c9bec-109">Suggestion</span></span>|<ul><li><span data-ttu-id="c9bec-110">Mettre à jour les applications ne peuvent ne pas compter sur <xref:System.Uri.UnescapeDataString(System.String)?displayProperty=name> levée dans le cas d’une séquence d’échappement non valide.</span><span class="sxs-lookup"><span data-stu-id="c9bec-110">Update applications to not rely on <xref:System.Uri.UnescapeDataString(System.String)?displayProperty=name> to throw in the case of an invalid escape sequence.</span></span> <span data-ttu-id="c9bec-111">Ces séquences sont à présent directement détectées.</span><span class="sxs-lookup"><span data-stu-id="c9bec-111">Such sequences must be detected directly now.</span></span></li><li><span data-ttu-id="c9bec-112">Il est également possible que les URI avec et sans séquence d’échappement, ainsi que les chaînes de données, varient entre les versions 4.0 et 4.5 du .NET. En outre, ils ne doivent pas être comparés directement entre différentes versions du .NET.</span><span class="sxs-lookup"><span data-stu-id="c9bec-112">Similarly, expect that Escaped and Unescaped URI and Data strings may vary from .NET 4.0 and .NET 4.5 and should not be compared across .NET versions directly.</span></span> <span data-ttu-id="c9bec-113">Ils doivent être analysés et normalisés dans une seule version du .NET avant de faire l’objet d’une comparaison.</span><span class="sxs-lookup"><span data-stu-id="c9bec-113">Instead, they should be parsed and normalized in a single .NET version before any comparisons are made.</span></span></li></ul>|
|<span data-ttu-id="c9bec-114">Portée</span><span class="sxs-lookup"><span data-stu-id="c9bec-114">Scope</span></span>|<span data-ttu-id="c9bec-115">Mineur</span><span class="sxs-lookup"><span data-stu-id="c9bec-115">Minor</span></span>|
|<span data-ttu-id="c9bec-116">Version</span><span class="sxs-lookup"><span data-stu-id="c9bec-116">Version</span></span>|<span data-ttu-id="c9bec-117">4.5</span><span class="sxs-lookup"><span data-stu-id="c9bec-117">4.5</span></span>|
|<span data-ttu-id="c9bec-118">Type</span><span class="sxs-lookup"><span data-stu-id="c9bec-118">Type</span></span>|<span data-ttu-id="c9bec-119">Runtime</span><span class="sxs-lookup"><span data-stu-id="c9bec-119">Runtime</span></span>|
|<span data-ttu-id="c9bec-120">API affectées</span><span class="sxs-lookup"><span data-stu-id="c9bec-120">Affected APIs</span></span>|<ul><li><xref:System.Uri.EscapeDataString(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.EscapeUriString(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.UnescapeDataString(System.String)?displayProperty=nameWithType></li></ul>|
