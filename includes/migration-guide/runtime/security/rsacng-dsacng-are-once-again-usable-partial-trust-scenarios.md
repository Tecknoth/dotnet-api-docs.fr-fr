### <a name="rsacng-and-dsacng-are-once-again-usable-in-partial-trust-scenarios"></a><span data-ttu-id="eb84f-101">RSACng et DSACng sont à nouveau utilisables dans les scénarios de confiance partielle</span><span class="sxs-lookup"><span data-stu-id="eb84f-101">RSACng and DSACng are once again usable in Partial Trust scenarios</span></span>

|   |   |
|---|---|
|<span data-ttu-id="eb84f-102">Détails</span><span class="sxs-lookup"><span data-stu-id="eb84f-102">Details</span></span>|<span data-ttu-id="eb84f-103">CngLightup (utilisé dans le chiffrement de niveau supérieur plusieurs API, telles que <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType>) et <xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType> dans certains cas, s’appuient sur la confiance totale.</span><span class="sxs-lookup"><span data-stu-id="eb84f-103">CngLightup (used in several higher-level crypto apis, such as <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType>) and <xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType> in some cases rely on full trust.</span></span> <span data-ttu-id="eb84f-104">Notamment les P/Invoke sans déclarer <xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType> autorisations et les chemins de code où <xref:System.Security.Cryptography.CngKey?displayProperty=nameWithType> a des demandes d’autorisation pour <xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="eb84f-104">These include P/Invokes without asserting <xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType> permissions, and code paths where <xref:System.Security.Cryptography.CngKey?displayProperty=nameWithType> has permission demands for <xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType>.</span></span> <span data-ttu-id="eb84f-105">À compter de .NET Framework 4.6.2, CngLightup a été utilisée pour basculer vers <xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType> autant que possible.</span><span class="sxs-lookup"><span data-stu-id="eb84f-105">Starting with the .NET Framework 4.6.2, CngLightup was used to switch to <xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType> wherever possible.</span></span> <span data-ttu-id="eb84f-106">Par conséquent, les applications de confiance partielle qui a été utilisé <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType> a commencé à échouer et lever <xref:System.Security.SecurityException> exceptions. Cette modification ajoute que les assertions nécessaires afin que toutes les fonctions à l’aide de CngLightup dispose des autorisations requises.</span><span class="sxs-lookup"><span data-stu-id="eb84f-106">As a result, partial trust apps that successfully used <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType> began to fail and throw <xref:System.Security.SecurityException> exceptions.This change adds the required asserts so that all functions using CngLightup have the required permissions.</span></span>|
|<span data-ttu-id="eb84f-107">Suggestion</span><span class="sxs-lookup"><span data-stu-id="eb84f-107">Suggestion</span></span>|<span data-ttu-id="eb84f-108">Si cette modification dans le .NET Framework 4.6.2 a affectés négativement à vos applications de confiance partielle, mettez à niveau vers le Kit de développement .NET Framework 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="eb84f-108">If this change in the .NET Framework 4.6.2 has negatively impacted your partial trust apps, upgrade to the .NET Framework 4.7.1.</span></span>|
|<span data-ttu-id="eb84f-109">Portée</span><span class="sxs-lookup"><span data-stu-id="eb84f-109">Scope</span></span>|<span data-ttu-id="eb84f-110">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="eb84f-110">Edge</span></span>|
|<span data-ttu-id="eb84f-111">Version</span><span class="sxs-lookup"><span data-stu-id="eb84f-111">Version</span></span>|<span data-ttu-id="eb84f-112">4.6.2</span><span class="sxs-lookup"><span data-stu-id="eb84f-112">4.6.2</span></span>|
|<span data-ttu-id="eb84f-113">Type</span><span class="sxs-lookup"><span data-stu-id="eb84f-113">Type</span></span>|<span data-ttu-id="eb84f-114">Runtime</span><span class="sxs-lookup"><span data-stu-id="eb84f-114">Runtime</span></span>|
|<span data-ttu-id="eb84f-115">API affectées</span><span class="sxs-lookup"><span data-stu-id="eb84f-115">Affected APIs</span></span>|<ul><li><xref:System.Security.Cryptography.DSACng.%23ctor(System.Security.Cryptography.CngKey)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.Key?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.LegalKeySizes?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.CreateSignature(System.Byte[])?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.VerifySignature(System.Byte[],System.Byte[])?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.%23ctor(System.Security.Cryptography.CngKey)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.Key?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.Decrypt(System.Byte[],System.Security.Cryptography.RSAEncryptionPadding)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.SignHash(System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|
