---
title: ms-prod-or-service-missing
description: Belgeler derleme sorunu ms-prod-or-service-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6eeb4a95e4d4aeba527b1078bc646fcbc56898a2
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987572"
---
# <a name="ms-prod-or-service-missing"></a>ms-prod-or-service-missing

**Çok yakında!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>Çözüm

`ms.prod` veya `ms.service` gereklidir ve her ikisi de mevcut olamaz: `ms.prod` şirket içi ürünler için kullanılır, `ms.service` ise bulut hizmetleri için kullanılır. Makaleniz için hangisinin uygun olduğunu belirleyin, değerin doğru olduğunu onaylayın ve diğer alanı kaldırın.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]