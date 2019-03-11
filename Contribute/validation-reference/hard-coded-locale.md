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
# <a name="hard-coded-locale"></a>hard-coded-locale

## <a name="warning"></a>Uyarı

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

`en-us` gibi yerel ayar kodları belirli Microsoft sitelerine giden bağlantılara dahil edilmemelidir. İngilizce içerikli bir bağlantıya bir yerel ayar kodu dahil ederseniz, kod yerelleştirilmiş bağlantılara da dahil edilir ve bu kötü bir yerelleştirilmiş deneyimle sonuçlanır. Örneğin Almanca yerelleştirilmiş içerikte `en-us` bulunursa, Alman müşteriler, makalenin Almancası olduğu halde kendilerini makalenin İngilizcesine bağlanırken bulurlar.

Aşağıdaki siteleri bunu doğrulamak için kapsam içindedir:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com

## <a name="resolution"></a>Çözüm

Microsoft sitelerine giden bağlantılardan yerel ayar kodlarını kaldırın. Aşağıda bir örnek verilmiştir.

Önce:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Sonra:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]