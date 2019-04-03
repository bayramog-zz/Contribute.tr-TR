---
title: ms-date-too-late
description: Belgeler derleme sorunu ms-date-too-late için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637403"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

## <a name="warning"></a>Uyarı

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

`ms.date` özniteliği "yeniliği", diğer bir deyişle, makalenin ilgi, doğruluk, doğru ekran görüntüleri ve çalışan bağlantılarının son kez ne zaman gözden geçirildiğini belirtmek için kullanılır. Bu yüzden gelecekteki bir tarih olamaz! İçeriğin önemli bir olaya hazırlanırken kalite denetimi için kilitlenmesi gibi durumlarda serbest bırakma süresi için beş gün izin verilir.

## <a name="resolution"></a>Çözüm

Bugünden başlayarak AA/GG/YYYY biçiminde en fazla beş günlük `ms.date` belirtin:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
