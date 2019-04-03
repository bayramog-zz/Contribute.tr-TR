---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653563"
---
# <a name="locale-specific-links"></a>Yerel ayara özgü bağlantılar

`en-us` gibi yerel ayar kodları belirli Microsoft sitelerine giden bağlantılara dahil edilmemelidir. İngilizce içerikli bir bağlantıya bir yerel ayar kodu dahil ederseniz, kod yerelleştirilmiş bağlantılara da dahil edilir ve bu kötü bir yerelleştirilmiş deneyimle sonuçlanır. Örneğin Almanca yerelleştirilmiş içerikte `en-us` bulunursa, Alman müşteriler, makalenin Almancası olduğu halde kendilerini makalenin İngilizcesine bağlanırken bulurlar.

Microsoft sitelerine giden bağlantılardan yerel ayar kodlarını kaldırın. Aşağıda bir örnek verilmiştir.

Önce:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Sonra:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

Aşağıdaki siteleri bunu doğrulamak için kapsam içindedir:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com