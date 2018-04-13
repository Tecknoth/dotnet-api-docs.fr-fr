### <a name="deserialization-of-objects-across-appdomains-can-fail"></a><span data-ttu-id="d2f7c-101">La désérialisation des objets sur des appdomains peut échouer.</span><span class="sxs-lookup"><span data-stu-id="d2f7c-101">Deserialization of objects across appdomains can fail</span></span>

|   |   |
|---|---|
|<span data-ttu-id="d2f7c-102">Détails</span><span class="sxs-lookup"><span data-stu-id="d2f7c-102">Details</span></span>|<span data-ttu-id="d2f7c-103">Dans certains cas, quand une application utilise deux domaines d'application ou plus avec des bases d'application différentes, une tentative de désérialisation des objets dans le contexte d'appel logique entre les domaines d'application lève une exception.</span><span class="sxs-lookup"><span data-stu-id="d2f7c-103">In some cases, when an app uses two or more app domains with different application bases, trying to deserialize objects in the logical call context across app domains throws an exception.</span></span>|
|<span data-ttu-id="d2f7c-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="d2f7c-104">Suggestion</span></span>|<span data-ttu-id="d2f7c-105">Consultez [atténuation : désérialisation des objets à travers les domaines d’application](~/docs/framework/migration-guide/mitigation-deserialization-of-objects-across-app-domains.md)</span><span class="sxs-lookup"><span data-stu-id="d2f7c-105">See [Mitigation: Deserialization of Objects Across App Domains](~/docs/framework/migration-guide/mitigation-deserialization-of-objects-across-app-domains.md)</span></span>|
|<span data-ttu-id="d2f7c-106">Portée</span><span class="sxs-lookup"><span data-stu-id="d2f7c-106">Scope</span></span>|<span data-ttu-id="d2f7c-107">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d2f7c-107">Edge</span></span>|
|<span data-ttu-id="d2f7c-108">Version</span><span class="sxs-lookup"><span data-stu-id="d2f7c-108">Version</span></span>|<span data-ttu-id="d2f7c-109">4.5.1</span><span class="sxs-lookup"><span data-stu-id="d2f7c-109">4.5.1</span></span>|
|<span data-ttu-id="d2f7c-110">Type</span><span class="sxs-lookup"><span data-stu-id="d2f7c-110">Type</span></span>|<span data-ttu-id="d2f7c-111">Runtime</span><span class="sxs-lookup"><span data-stu-id="d2f7c-111">Runtime</span></span>|
