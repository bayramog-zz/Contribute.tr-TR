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
# <a name="docs-pr-validation-service"></a>Docs çekme isteği doğrulama hizmeti

Docs çekme isteği doğrulama hizmeti, bir çekme isteği dosyaları üzerinde doğrulama kuralları çalıştıran bir GitHub uygulamasıdır.

Doğrulama hizmeti bir havuzda etkinleştirildiğinde aşağıdaki davranışları görürsünüz:

1. Bir çekme isteği gönderirsiniz.
1. Çekme isteğinizin durumunu gösteren GitHub açıklamasında havuzda "denetimler" durumunun etkin olduğunu görürsünüz. Bu örnekte iki denetimin; "İşleme Doğrulaması" ve "OpenPublishing.Build"'ın etkinleştirildiğine dikkat edin:

   ![bazı denetimler başarısız oldu](media/validation-failed.png)

   İşleme doğrulaması başarısız olsa bile derleme geçebilir.

1. Daha fazla bilgi için **Ayrıntılar**'ı görüntüleyin.
1. Ayrıntılar sayfasında, doğrulama denetimlerinin başarısız olduğunu ve beraberinde verilen sorunu çözme bilgilerini görürsünüz:

   ![doğrulama mesajı](media/validation-details.png)

Şu anda hizmette olan doğrulamaların listesi için bu makalenin sol tarafındaki İçindekiler Tablosu'na bakın.