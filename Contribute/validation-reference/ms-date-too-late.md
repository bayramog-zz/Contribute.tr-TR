---
title: ms-date-too-late
description: Belgeler derleme sorunu ms-date-too-late için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713120"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

**Çok yakında!**

## <a name="warning"></a>Uyarı

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

`ms.date` özniteliği "yeniliği", diğer bir deyişle, makalenin ilgi, doğruluk, doğru ekran görüntüleri ve çalışan bağlantılarının son kez ne zaman gözden geçirildiğini belirtmek için kullanılır. Bu yüzden gelecekteki bir tarih olamaz! İçeriğin önemli bir olaya hazırlanırken kalite denetimi için kilitlenmesi gibi durumlarda serbest bırakma süresi için beş gün izin verilir.

## <a name="resolution"></a>Çözüm

Bugünden başlayarak AA/GG/YYYY biçiminde en fazla beş günlük `ms.date` belirtin.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
