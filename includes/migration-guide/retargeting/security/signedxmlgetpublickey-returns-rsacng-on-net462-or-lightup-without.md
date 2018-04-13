### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a><span data-ttu-id="81314-101">SignedXml.GetPublicKey retourne RSACng sur net462 (ou lightup) sans modification de reciblage</span><span class="sxs-lookup"><span data-stu-id="81314-101">SignedXml.GetPublicKey returns RSACng on net462 (or lightup) without retargeting change</span></span>

|   |   |
|---|---|
|<span data-ttu-id="81314-102">Détails</span><span class="sxs-lookup"><span data-stu-id="81314-102">Details</span></span>|<span data-ttu-id="81314-103">En commençant par le .NET Framework 4.6.2, le type concret de l’objet retourné par la <xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType> méthode modifiée (sans une particularité) à partir d’une implémentation CryptoServiceProvider vers une implémentation Cng.</span><span class="sxs-lookup"><span data-stu-id="81314-103">Starting with the .NET Framework 4.6.2, the concrete type of the object returned by the <xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType> method changed (without a quirk) from a CryptoServiceProvider implementation to a Cng implementation.</span></span> <span data-ttu-id="81314-104">Il s’agit, car il est modifié par l’implémentation de l’utilisation <code>certificate.PublicKey.Key</code> à l’utilisation interne <code>certificate.GetAnyPublicKey</code> qui transfère à <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="81314-104">This is because the implementation changed from using <code>certificate.PublicKey.Key</code> to using the internal <code>certificate.GetAnyPublicKey</code> which forwards to <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>.</span></span>|
|<span data-ttu-id="81314-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="81314-105">Suggestion</span></span>|<span data-ttu-id="81314-106">Compter des applications en cours d’exécution sur le .NET Framework 4.7.1, vous pouvez utiliser l’implémentation CryptoServiceProvider utilisée par défaut dans le .NET Framework 4.6.1 et versions antérieures en ajoutant la configuration suivante basculer vers le [runtime](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)section de votre fichier de configuration d’application :</span><span class="sxs-lookup"><span data-stu-id="81314-106">Starting with apps running on the .NET Framework 4.7.1, you can use the CryptoServiceProvider implementation used by default in the .NET Framework 4.6.1 and earlier versions by adding the following configuration switch to the [runtime](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) section of your app config file:</span></span><pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="81314-107">Portée</span><span class="sxs-lookup"><span data-stu-id="81314-107">Scope</span></span>|<span data-ttu-id="81314-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="81314-108">Edge</span></span>|
|<span data-ttu-id="81314-109">Version</span><span class="sxs-lookup"><span data-stu-id="81314-109">Version</span></span>|<span data-ttu-id="81314-110">4.6.2</span><span class="sxs-lookup"><span data-stu-id="81314-110">4.6.2</span></span>|
|<span data-ttu-id="81314-111">Type</span><span class="sxs-lookup"><span data-stu-id="81314-111">Type</span></span>|<span data-ttu-id="81314-112">Reciblage</span><span class="sxs-lookup"><span data-stu-id="81314-112">Retargeting</span></span>|
|<span data-ttu-id="81314-113">API affectées</span><span class="sxs-lookup"><span data-stu-id="81314-113">Affected APIs</span></span>|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|
