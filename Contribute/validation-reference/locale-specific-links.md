# <a name="locale-specific-links"></a><span data-ttu-id="0b5bd-101">Yerel ayara özgü bağlantılar</span><span class="sxs-lookup"><span data-stu-id="0b5bd-101">Locale-specific links</span></span>

<span data-ttu-id="0b5bd-102">`en-us` gibi yerel ayar kodları belirli Microsoft sitelerine giden bağlantılara dahil edilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="0b5bd-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="0b5bd-103">İngilizce içerikli bir bağlantıya bir yerel ayar kodu dahil ederseniz, kod yerelleştirilmiş bağlantılara da dahil edilir ve bu kötü bir yerelleştirilmiş deneyimle sonuçlanır.</span><span class="sxs-lookup"><span data-stu-id="0b5bd-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="0b5bd-104">Örneğin Almanca yerelleştirilmiş içerikte `en-us` bulunursa, Alman müşteriler, makalenin Almancası olduğu halde kendilerini makalenin İngilizcesine bağlanırken bulurlar.</span><span class="sxs-lookup"><span data-stu-id="0b5bd-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="0b5bd-105">Microsoft sitelerine giden bağlantılardan yerel ayar kodlarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="0b5bd-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="0b5bd-106">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="0b5bd-106">The following is an example.</span></span>

<span data-ttu-id="0b5bd-107">Önce:</span><span class="sxs-lookup"><span data-stu-id="0b5bd-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="0b5bd-108">Sonra:</span><span class="sxs-lookup"><span data-stu-id="0b5bd-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="0b5bd-109">Aşağıdaki siteleri bunu doğrulamak için kapsam içindedir:</span><span class="sxs-lookup"><span data-stu-id="0b5bd-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="0b5bd-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0b5bd-110">azure.microsoft.com</span></span>
- <span data-ttu-id="0b5bd-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0b5bd-111">docs.microsoft.com</span></span>
- <span data-ttu-id="0b5bd-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0b5bd-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="0b5bd-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="0b5bd-113">technet.microsoft.com</span></span>