---
title: ms-date-missing
description: Belgeler derleme sorunu ms-date-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: d7697c8449e451879c137d9d6cdf42327e597be6
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431473"
---
# <a name="ms-date-missing"></a>ms-date-missing

**Çok yakında!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

Bu tarih "yeniliği", diğer bir deyişle, makalenin ilgi, doğruluk, doğru ekran görüntüleri ve çalışan bağlantılarının son kez ne zaman gözden geçirildiğini belirtmek için kullanılır. Bu tarih makalenin *yayımlandığı* son tarih ile aynı değildir. Son yayımlama tarihi `ms.date` açıkça belirtilmezse sayfada gösterilir.

## <a name="resolution"></a>Çözüm

Makalenin bozuk bir içerik olmaksızın güncel olduğunu onaylayın, ardından AA/GG/YYYY biçiminde geçerli bir tarih ekleyin:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
