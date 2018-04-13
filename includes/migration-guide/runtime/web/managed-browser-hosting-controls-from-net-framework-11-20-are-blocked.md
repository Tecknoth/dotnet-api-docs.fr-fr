### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a><span data-ttu-id="83431-101">Hébergement des contrôles managés de navigateur à partir de .NET Framework 1.1 et 2.0 sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="83431-101">Managed browser hosting controls from the .NET Framework 1.1 and 2.0 are blocked</span></span>

|   |   |
|---|---|
|<span data-ttu-id="83431-102">Détails</span><span class="sxs-lookup"><span data-stu-id="83431-102">Details</span></span>|<span data-ttu-id="83431-103">L'hébergement de ces contrôles est bloqué dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="83431-103">Hosting these controls is blocked in Internet Explorer.</span></span>|
|<span data-ttu-id="83431-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="83431-104">Suggestion</span></span>|<span data-ttu-id="83431-105">Internet Explorer ne démarrera pas les applications qui utilisent des contrôles d'hébergement de navigateur géré.</span><span class="sxs-lookup"><span data-stu-id="83431-105">Internet Explorer will fail to launch an application that uses managed browser hosting controls.</span></span> <span data-ttu-id="83431-106">Le comportement précédent peut être restauré en définissant la valeur EnableIEHosting de la sous-clé de Registre <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> à <code>1</code> pour x86 systèmes et pour les processus 32 bits sur x64 systèmes et en définissant le <code>EnableIEHosting</code> valeur de la sous-clé de Registre <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>à <code>1</code> pour les processus 64 bits sur x64 systèmes.</span><span class="sxs-lookup"><span data-stu-id="83431-106">The previous behavior can be restored by setting the EnableIEHosting value of the registry subkey <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> to <code>1</code> for x86 systems and for 32-bit processes on x64 systems, and by setting the <code>EnableIEHosting</code> value of the registry subkey <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code> to <code>1</code> for 64-bit processes on x64 systems.</span></span>|
|<span data-ttu-id="83431-107">Portée</span><span class="sxs-lookup"><span data-stu-id="83431-107">Scope</span></span>|<span data-ttu-id="83431-108">Mineur</span><span class="sxs-lookup"><span data-stu-id="83431-108">Minor</span></span>|
|<span data-ttu-id="83431-109">Version</span><span class="sxs-lookup"><span data-stu-id="83431-109">Version</span></span>|<span data-ttu-id="83431-110">4.5</span><span class="sxs-lookup"><span data-stu-id="83431-110">4.5</span></span>|
|<span data-ttu-id="83431-111">Type</span><span class="sxs-lookup"><span data-stu-id="83431-111">Type</span></span>|<span data-ttu-id="83431-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="83431-112">Runtime</span></span>|
