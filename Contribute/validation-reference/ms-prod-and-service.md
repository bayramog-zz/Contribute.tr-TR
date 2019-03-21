---
title: ms-prod-and-service
description: Belgeler derleme sorunu ms-prod-and-service için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b685144e92485df2dddb9bdda09fea47d75f588f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987687"
---
# <a name="ms-prod-and-service"></a>ms-prod-and-service

**Çok yakında!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>Çözüm

`ms.prod` veya `ms.service` gereklidir ve her ikisi de mevcut olamaz: `ms.prod` şirket içi ürünler için kullanılır, `ms.service` ise bulut hizmetleri için kullanılır. Makaleniz için hangisinin uygun olduğunu belirleyin, değerin doğru olduğunu onaylayın ve diğer alanı kaldırın.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
