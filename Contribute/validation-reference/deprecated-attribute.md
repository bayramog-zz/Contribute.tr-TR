---
title: deprecated-attribute
description: Docs derleme sorunu deprecated-attribute için açıklama ve çözünürlük
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 564bd35c418fb9def6bf20240fca64265a477f46
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987802"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

**Çok yakında!**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Öneri

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Bulut hizmetlerini belirtmek için `ms.service` kullanın. `ms.service` hakkında daha ayrıntılı bilgi belirtmek için isteğe bağlı olarak `ms.subservice` belirtebilirsiniz. `ms.component` kullanmayın; bu içerik için kullanım dışıdır.

## <a name="resolution"></a>Çözüm

Makaleniz için `ms.service` değerinizin doğru olduğunu onaylayın. Sonra geçerli bir `ms.subservice` değeri seçin.

Geçerli değerler [bu Microsoft iç sitesinde](https://docsmetadatatool.azurewebsites.net/allowlists) bulunabilir.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
