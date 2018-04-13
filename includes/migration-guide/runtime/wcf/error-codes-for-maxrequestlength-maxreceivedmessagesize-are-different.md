### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a><span data-ttu-id="c19d2-101">Codes d’erreur pour maxRequestLength ou maxReceivedMessageSize sont différents</span><span class="sxs-lookup"><span data-stu-id="c19d2-101">Error codes for maxRequestLength or maxReceivedMessageSize are different</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c19d2-102">Détails</span><span class="sxs-lookup"><span data-stu-id="c19d2-102">Details</span></span>|<span data-ttu-id="c19d2-103">Messages dans WCF services web hébergés dans Internet Information Services (IIS) ou le serveur de développement ASP.NET qui dépassent maxRequestLength (dans ASP.NET) ou maxReceivedMessageSize (dans WCF) ont une erreur autre code d’état HTTP de code hiérarchiqueLes est passé de 400 (demande incorrecte ) à 413 (entité de demande trop grande) et les messages qui dépassent le paramètre maxReceivedMessageSize ou l’attribut maxRequestLength lever un <xref:System.ServiceModel.ProtocolException?displayProperty=name> exception.</span><span class="sxs-lookup"><span data-stu-id="c19d2-103">Messages in WCF web services hosted in Internet Information Services (IIS) or ASP.NET Development Server that exceed maxRequestLength (in ASP.NET) or maxReceivedMessageSize (in WCF) have different error codeThe HTTP status code has changed from 400 (Bad Request) to 413 (Request Entity Too Large), and messages that exceed either the maxRequestLength or the maxReceivedMessageSize setting throw a <xref:System.ServiceModel.ProtocolException?displayProperty=name> exception.</span></span> <span data-ttu-id="c19d2-104">Cela inclut les cas dans lequel le mode de transfert est transmis en continu.</span><span class="sxs-lookup"><span data-stu-id="c19d2-104">This includes cases in which the transfer mode is Streamed.</span></span>|
|<span data-ttu-id="c19d2-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="c19d2-105">Suggestion</span></span>|<span data-ttu-id="c19d2-106">Cette modification facilite le débogage dans les cas où la longueur du message dépasse les limites autorisées par ASP.NET ou WCF. Vous devez modifier tout code qui effectue le traitement basé sur un code d’état HTTP 400.</span><span class="sxs-lookup"><span data-stu-id="c19d2-106">This change facilitates debugging in cases where the message length exceeds the limits allowed by ASP.NET or WCF.You must modify any code that performs processing based on an HTTP 400 status code.</span></span>|
|<span data-ttu-id="c19d2-107">Portée</span><span class="sxs-lookup"><span data-stu-id="c19d2-107">Scope</span></span>|<span data-ttu-id="c19d2-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c19d2-108">Edge</span></span>|
|<span data-ttu-id="c19d2-109">Version</span><span class="sxs-lookup"><span data-stu-id="c19d2-109">Version</span></span>|<span data-ttu-id="c19d2-110">4.5</span><span class="sxs-lookup"><span data-stu-id="c19d2-110">4.5</span></span>|
|<span data-ttu-id="c19d2-111">Type</span><span class="sxs-lookup"><span data-stu-id="c19d2-111">Type</span></span>|<span data-ttu-id="c19d2-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="c19d2-112">Runtime</span></span>|
