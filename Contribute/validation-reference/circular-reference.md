---
title: circular-reference
description: Docs derleme sorunu circular-reference için açıklama ve çözüm
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459223"
---
# <a name="circular-reference"></a>circular-reference

## <a name="error"></a>Hata

`Files '{file name 1}' and '{file name 2}' reference each other.`

Örneğin, bu geçerli dosyaya bağlanan bir ekli dosya veya geçerli dosyaya yönlendirilmiş bir dosyanın bağlantısı olabilir.

## <a name="resolution"></a>Çözüm

Dosyalardaki bağlantıları gözden geçirin ve hiçbir dosyanın kendisine bağlanmamasını veya kendisini içermemesini sağlayacak gerekli düzenlemeleri yapın.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
