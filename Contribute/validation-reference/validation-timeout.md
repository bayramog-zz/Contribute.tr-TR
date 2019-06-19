---
title: validation-timeout
description: Docs derleme sorunu validation-timeout için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 00461768491c25b9bafaff6b117a356d9e291e22
ms.sourcegitcommit: 412ce4ab23e758d41947043f1463e96595ba3bfe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033305"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Uyarı

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or  If you continue to see this message, file an issue via https://SiteHelp.`

Doğrulama hizmetinde bulunan hatalı durumdaki bir sunucu gibi geçici sorunlar Docs Derlemesinin hizmeti başarılı bir şekilde çağırmasını engelliyor. Birkaç denemenin ardından çağrı zaman aşımına uğrar ve derleme gecikmeleri ile derleme işlem hattının tıka basa dolmasını engellemek için doğrulama işlemi iptal edilir.

## <a name="resolution"></a>Çözüm

PR’ınızı kapatıp yeniden açmayı deneyin veya Docs Portal’dan bir derlemeyi el ile yeniden çalıştırmayı deneyin (yalnızca depo yöneticileri). Sık karşılaşılan hizmet sorunları ilk yeniden denemenin ardından kendilerini temizler. Bir yöneticinin yardımına ihtiyaç duyarsanız, [https://SiteHelp](https://SiteHelp) üzerinden bir ileti almaya veya sorun bildirmeye devam ederseniz, Microsoft çalışanıysanız veya yardım için PR’ınızdaki bir makalenin yazarından @ bahsederseniz veya bir dış katkıda bulunansanız.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
