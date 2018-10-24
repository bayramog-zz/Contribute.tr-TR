---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084629"
---
# <a name="docs-pr-validation-service"></a><span data-ttu-id="505b2-101">Docs çekme isteği doğrulama hizmeti</span><span class="sxs-lookup"><span data-stu-id="505b2-101">Docs PR validation service</span></span>

<span data-ttu-id="505b2-102">Docs çekme isteği doğrulama hizmeti, bir çekme isteği dosyaları üzerinde doğrulama kuralları çalıştıran bir GitHub uygulamasıdır.</span><span class="sxs-lookup"><span data-stu-id="505b2-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="505b2-103">Doğrulama hizmeti bir havuzda etkinleştirildiğinde aşağıdaki davranışları görürsünüz:</span><span class="sxs-lookup"><span data-stu-id="505b2-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="505b2-104">Bir çekme isteği gönderirsiniz.</span><span class="sxs-lookup"><span data-stu-id="505b2-104">You submit a PR.</span></span>
1. <span data-ttu-id="505b2-105">Çekme isteğinizin durumunu gösteren GitHub açıklamasında havuzda "denetimler" durumunun etkin olduğunu görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="505b2-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="505b2-106">Bu örnekte iki denetimin; "İşleme Doğrulaması" ve "OpenPublishing.Build"'ın etkinleştirildiğine dikkat edin:</span><span class="sxs-lookup"><span data-stu-id="505b2-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![bazı denetimler başarısız oldu](media/validation-failed.png)

   <span data-ttu-id="505b2-108">İşleme doğrulaması başarısız olsa bile derleme geçebilir.</span><span class="sxs-lookup"><span data-stu-id="505b2-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="505b2-109">Daha fazla bilgi için **Ayrıntılar**'ı görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="505b2-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="505b2-110">Ayrıntılar sayfasında, doğrulama denetimlerinin başarısız olduğunu ve beraberinde verilen sorunu çözme bilgilerini görürsünüz:</span><span class="sxs-lookup"><span data-stu-id="505b2-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![doğrulama mesajı](media/validation-details.png)

<span data-ttu-id="505b2-112">Şu anda hizmette olan doğrulamaların listesi için bu makalenin sol tarafındaki İçindekiler Tablosu'na bakın.</span><span class="sxs-lookup"><span data-stu-id="505b2-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>