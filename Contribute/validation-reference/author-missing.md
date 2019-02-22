---
title: author-missing
description: Belgeler derleme sorunu author-missing için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 89725dcfbd4ec266071c45a003748021b480bbc2
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431542"
---
# <a name="author-missing"></a>author-missing

**Çok yakında!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Missing attribute: author. Add a valid GitHub ID.`

`author` özniteliği GitHub kimliğine göre makalenin yazarını tanımlar. 

## <a name="resolution"></a>Çözüm

Yazarın GitHub kimliğini YML üst bilgisine ekleyin:

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]