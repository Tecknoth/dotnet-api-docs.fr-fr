### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a><span data-ttu-id="c790e-101">HttpRuntime.AppDomainAppPath lève une exception NullReferenceException</span><span class="sxs-lookup"><span data-stu-id="c790e-101">HttpRuntime.AppDomainAppPath Throws a NullReferenceException</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c790e-102">Détails</span><span class="sxs-lookup"><span data-stu-id="c790e-102">Details</span></span>|<span data-ttu-id="c790e-103">Dans le .NET Framework 4.6.2, le runtime lève une <code>T:System.NullReferenceException</code> lorsque vous récupérez un <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> valeur qui inclut des caractères null. Dans le .NET Framework 4.6.1 et versions antérieures, le runtime lève une <code>T:System.ArgumentNullException</code>.</span><span class="sxs-lookup"><span data-stu-id="c790e-103">In the .NET Framework 4.6.2, the runtime throws a <code>T:System.NullReferenceException</code> when retrieving a <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> value that includes null characters.In the .NET Framework 4.6.1 and earlier versions, the runtime throws an <code>T:System.ArgumentNullException</code>.</span></span>|
|<span data-ttu-id="c790e-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="c790e-104">Suggestion</span></span>|<span data-ttu-id="c790e-105">Vous pouvez procéder de la suite pour répondre à cette modification :</span><span class="sxs-lookup"><span data-stu-id="c790e-105">You can do either of the follow to respond to this change:</span></span><ul><li><span data-ttu-id="c790e-106">Gérer le <code>T:System.NullReferenceException</code> si votre application est en cours d’exécution sur le .NET Framework 4.6.2.</span><span class="sxs-lookup"><span data-stu-id="c790e-106">Handle the <code>T:System.NullReferenceException</code> if you application is running on the .NET Framework 4.6.2.</span></span></li><li><span data-ttu-id="c790e-107">Mise à niveau vers la 4.7 .NET Framework, qui rétablit le comportement précédent et lève un <code>T:System.ArgumentNullException</code>.</span><span class="sxs-lookup"><span data-stu-id="c790e-107">Upgrade to the .NET Framework 4.7, which restores the previous behavior and throws an <code>T:System.ArgumentNullException</code>.</span></span></li></ul>|
|<span data-ttu-id="c790e-108">Portée</span><span class="sxs-lookup"><span data-stu-id="c790e-108">Scope</span></span>|<span data-ttu-id="c790e-109">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c790e-109">Edge</span></span>|
|<span data-ttu-id="c790e-110">Version</span><span class="sxs-lookup"><span data-stu-id="c790e-110">Version</span></span>|<span data-ttu-id="c790e-111">4.6.2</span><span class="sxs-lookup"><span data-stu-id="c790e-111">4.6.2</span></span>|
|<span data-ttu-id="c790e-112">Type</span><span class="sxs-lookup"><span data-stu-id="c790e-112">Type</span></span>|<span data-ttu-id="c790e-113">Reciblage</span><span class="sxs-lookup"><span data-stu-id="c790e-113">Retargeting</span></span>|
|<span data-ttu-id="c790e-114">API affectées</span><span class="sxs-lookup"><span data-stu-id="c790e-114">Affected APIs</span></span>|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|
