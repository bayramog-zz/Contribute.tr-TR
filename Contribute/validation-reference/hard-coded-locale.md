---
title: hard-coded-locale
description: Docs derleme sorunu hard-coded-locale için açıklama ve çözüm.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57428167"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="51bb6-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="51bb6-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="51bb6-104">Uyarı</span><span class="sxs-lookup"><span data-stu-id="51bb6-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="51bb6-105">`en-us` gibi yerel ayar kodları belirli Microsoft sitelerine giden bağlantılara dahil edilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="51bb6-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="51bb6-106">İngilizce içerikli bir bağlantıya bir yerel ayar kodu dahil ederseniz, kod yerelleştirilmiş bağlantılara da dahil edilir ve bu kötü bir yerelleştirilmiş deneyimle sonuçlanır.</span><span class="sxs-lookup"><span data-stu-id="51bb6-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="51bb6-107">Örneğin Almanca yerelleştirilmiş içerikte `en-us` bulunursa, Alman müşteriler, makalenin Almancası olduğu halde kendilerini makalenin İngilizcesine bağlanırken bulurlar.</span><span class="sxs-lookup"><span data-stu-id="51bb6-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="51bb6-108">Aşağıdaki siteleri bunu doğrulamak için kapsam içindedir:</span><span class="sxs-lookup"><span data-stu-id="51bb6-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="51bb6-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="51bb6-109">azure.microsoft.com</span></span>
- <span data-ttu-id="51bb6-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="51bb6-110">docs.microsoft.com</span></span>
- <span data-ttu-id="51bb6-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="51bb6-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="51bb6-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="51bb6-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="51bb6-113">Çözüm</span><span class="sxs-lookup"><span data-stu-id="51bb6-113">Resolution</span></span>

<span data-ttu-id="51bb6-114">Microsoft sitelerine giden bağlantılardan yerel ayar kodlarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="51bb6-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="51bb6-115">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="51bb6-115">The following is an example.</span></span>

<span data-ttu-id="51bb6-116">Önce:</span><span class="sxs-lookup"><span data-stu-id="51bb6-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="51bb6-117">Sonra:</span><span class="sxs-lookup"><span data-stu-id="51bb6-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]