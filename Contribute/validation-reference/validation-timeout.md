---
title: validation-timeout
description: Docs derleme sorunu validation-timeout için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024222"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Uyarı

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

Doğrulama hizmetinde bulunan hatalı durumdaki bir sunucu gibi geçici sorunlar Docs Derlemesinin hizmeti başarılı bir şekilde çağırmasını engelliyor. Üç denemenin ardından çağrı zaman aşımına uğrar ve derleme gecikmelerini ve derleme işlem hattının tıka basa dolmasını engellemek için doğrulama işlemi iptal edilir.

## <a name="resolution"></a>Çözüm

PR’ınızı kapatıp yeniden açmayı deneyin veya bir derlemeyi el ile yeniden çalıştırmayı deneyin (yalnızca depo yöneticileri). Sık karşılaşılan hizmet sorunları ilk yeniden denemenin ardından kendilerini temizler. [https://SiteHelp](https://SiteHelp) üzerinden bir ileti almaya veya sorun bildirmeye devam ederseniz, Microsoft çalışanıysanız veya yardım için PR’ınızdaki bir makalenin yazarından @ bahsederseniz veya bir dış katkıda bulunansanız.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
