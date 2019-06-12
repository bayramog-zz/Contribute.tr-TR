---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: Yerel ayara özgü bağlantılar
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841242"
---
# <a name="locale-specific-links"></a><span data-ttu-id="54488-102">Yerel ayara özgü bağlantılar</span><span class="sxs-lookup"><span data-stu-id="54488-102">Locale-specific links</span></span>

<span data-ttu-id="54488-103">`en-us` gibi yerel ayar kodları belirli Microsoft sitelerine giden bağlantılara dahil edilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="54488-103">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="54488-104">İngilizce içerikli bir bağlantıya bir yerel ayar kodu dahil ederseniz, kod yerelleştirilmiş bağlantılara da dahil edilir ve bu kötü bir yerelleştirilmiş deneyimle sonuçlanır.</span><span class="sxs-lookup"><span data-stu-id="54488-104">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="54488-105">Örneğin Almanca yerelleştirilmiş içerikte `en-us` bulunursa, Alman müşteriler, makalenin Almancası olduğu halde kendilerini makalenin İngilizcesine bağlanırken bulurlar.</span><span class="sxs-lookup"><span data-stu-id="54488-105">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="54488-106">Microsoft sitelerine giden bağlantılardan yerel ayar kodlarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="54488-106">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="54488-107">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="54488-107">The following is an example.</span></span>

<span data-ttu-id="54488-108">Önce:</span><span class="sxs-lookup"><span data-stu-id="54488-108">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="54488-109">Sonra:</span><span class="sxs-lookup"><span data-stu-id="54488-109">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="54488-110">Aşağıdaki siteleri bunu doğrulamak için kapsam içindedir:</span><span class="sxs-lookup"><span data-stu-id="54488-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="54488-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="54488-111">azure.microsoft.com</span></span>
- <span data-ttu-id="54488-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="54488-112">docs.microsoft.com</span></span>
- <span data-ttu-id="54488-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="54488-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="54488-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="54488-114">technet.microsoft.com</span></span>