---
title: ms-author-invalid
description: Belgeler derleme sorunu ms-author-invalid için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6d6c77b9b378865913e2055abf2b64ccba8ca482
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636736"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Çözüm

`ms.author` değerinin geçerli bir Microsoft diğer adı olduğunu doğrulayın. Diğer ad bir dağıtım listesiyse aynı zamanda izin verilenler listesine de alınmış olmalıdır.

DL’ler için geçerli değerleri [buradaki Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulabilirsiniz.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
