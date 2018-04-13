### <a name="xml-schema-validation-is-stricter"></a><span data-ttu-id="77e51-101">Validation de schéma XML est plus stricte</span><span class="sxs-lookup"><span data-stu-id="77e51-101">XML schema validation is stricter</span></span>

|   |   |
|---|---|
|<span data-ttu-id="77e51-102">Détails</span><span class="sxs-lookup"><span data-stu-id="77e51-102">Details</span></span>|<span data-ttu-id="77e51-103">Dans le .NET Framework 4.5, la validation de schéma XML est plus stricte.</span><span class="sxs-lookup"><span data-stu-id="77e51-103">In the .NET Framework 4.5, XML schema validation is more strict.</span></span> <span data-ttu-id="77e51-104">Si vous utilisez xsd:anyURI pour valider un URI tel qu'un protocole mailto, la validation échoue si l'URI contient des espaces.</span><span class="sxs-lookup"><span data-stu-id="77e51-104">If you use xsd:anyURI to validate a URI such as a mailto protocol, validation fails if there are spaces in the URI.</span></span> <span data-ttu-id="77e51-105">Dans les versions antérieures du .NET Framework, la validation réussissait.</span><span class="sxs-lookup"><span data-stu-id="77e51-105">In previous versions of the .NET Framework, validation succeeded.</span></span> <span data-ttu-id="77e51-106">La modification affecte uniquement les applications qui ciblent le .NET Framework 4.5.</span><span class="sxs-lookup"><span data-stu-id="77e51-106">The change affects only applications that target the .NET Framework 4.5.</span></span>|
|<span data-ttu-id="77e51-107">Suggestion</span><span class="sxs-lookup"><span data-stu-id="77e51-107">Suggestion</span></span>|<span data-ttu-id="77e51-108">Si un contrôle de .NET Framework 4.0 est nécessaire, l’application de validation peut cibler la version 4.0 de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="77e51-108">If looser .NET Framework 4.0 validation is needed, the validating application can target version 4.0 of the .NET Framework.</span></span> <span data-ttu-id="77e51-109">Lorsque le reciblage vers .NET 4.5, toutefois, révision du code doit être effectuée pour vous assurer que les URI non valide (avec espaces) ne doivent pas en tant que valeurs d’attribut avec le type de données anyURI.</span><span class="sxs-lookup"><span data-stu-id="77e51-109">When retargeting to .NET 4.5, however, code review should be done to be sure that invalid URIs (with spaces) are not expected as attribute values with the anyURI data type.</span></span>|
|<span data-ttu-id="77e51-110">Portée</span><span class="sxs-lookup"><span data-stu-id="77e51-110">Scope</span></span>|<span data-ttu-id="77e51-111">Mineur</span><span class="sxs-lookup"><span data-stu-id="77e51-111">Minor</span></span>|
|<span data-ttu-id="77e51-112">Version</span><span class="sxs-lookup"><span data-stu-id="77e51-112">Version</span></span>|<span data-ttu-id="77e51-113">4.5</span><span class="sxs-lookup"><span data-stu-id="77e51-113">4.5</span></span>|
|<span data-ttu-id="77e51-114">Type</span><span class="sxs-lookup"><span data-stu-id="77e51-114">Type</span></span>|<span data-ttu-id="77e51-115">Reciblage</span><span class="sxs-lookup"><span data-stu-id="77e51-115">Retargeting</span></span>|
