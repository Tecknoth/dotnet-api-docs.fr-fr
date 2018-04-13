### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a><span data-ttu-id="496ab-101">ObsoleteAttribute exporte comme ObsoleteAttribute et DeprecatedAttribute dans les scénarios de WinMD</span><span class="sxs-lookup"><span data-stu-id="496ab-101">ObsoleteAttribute exports as both ObsoleteAttribute and DeprecatedAttribute in WinMD scenarios</span></span>

|   |   |
|---|---|
|<span data-ttu-id="496ab-102">Détails</span><span class="sxs-lookup"><span data-stu-id="496ab-102">Details</span></span>|<span data-ttu-id="496ab-103">Lorsque vous créez une bibliothèque de métadonnées Windows (fichier .winmd), le <xref:System.ObsoleteAttribute?displayProperty=name> attribut est exporté en tant que les deux <xref:System.ObsoleteAttribute?displayProperty=name> et [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute).</span><span class="sxs-lookup"><span data-stu-id="496ab-103">When you create a Windows Metadata library (.winmd file), the <xref:System.ObsoleteAttribute?displayProperty=name> attribute is exported as both <xref:System.ObsoleteAttribute?displayProperty=name> and [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute).</span></span>|
|<span data-ttu-id="496ab-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="496ab-104">Suggestion</span></span>|<span data-ttu-id="496ab-105">La recompilation de code source existant qui utilise le <xref:System.ObsoleteAttribute?displayProperty=name> attribut peut générer des avertissements lors de l’utilisation de ce code à partir de C + c++ / CX ou JavaScript.We déconseillons d’appliquer à la fois <xref:System.ObsoleteAttribute?displayProperty=name> et [ Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) au code dans les assemblys managés ; il peut générer des avertissements de build.</span><span class="sxs-lookup"><span data-stu-id="496ab-105">Recompilation of existing source code that uses the <xref:System.ObsoleteAttribute?displayProperty=name> attribute may generate warnings when consuming that code from C++/CX or JavaScript.We do not recommend applying both <xref:System.ObsoleteAttribute?displayProperty=name> and [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) to code in managed assemblies; it may result in build warnings.</span></span>|
|<span data-ttu-id="496ab-106">Portée</span><span class="sxs-lookup"><span data-stu-id="496ab-106">Scope</span></span>|<span data-ttu-id="496ab-107">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="496ab-107">Edge</span></span>|
|<span data-ttu-id="496ab-108">Version</span><span class="sxs-lookup"><span data-stu-id="496ab-108">Version</span></span>|<span data-ttu-id="496ab-109">4.5.1</span><span class="sxs-lookup"><span data-stu-id="496ab-109">4.5.1</span></span>|
|<span data-ttu-id="496ab-110">Type</span><span class="sxs-lookup"><span data-stu-id="496ab-110">Type</span></span>|<span data-ttu-id="496ab-111">Reciblage</span><span class="sxs-lookup"><span data-stu-id="496ab-111">Retargeting</span></span>|
