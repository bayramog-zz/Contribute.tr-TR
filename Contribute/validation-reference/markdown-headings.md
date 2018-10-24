---
title: Markdown Başlıkları
description: Markdown başlıklarının gereksinimlerini açıklar.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084567"
---
# <a name="markdown-headings"></a>Markdown başlıkları

Aşağıdaki doğrulama gereksinimleri, OPS Markdown dosyalarındaki başlıklar için geçerlidir.

## <a name="h1"></a>H1

`H1` bir Markdown dosyasındaki ilk başlığı gösterir. H1, docs.microsoft.com sitesinde yayımlandığında sayfanın en üstünde büyük bir yazıtipi ile gösterilir.

H1, bir satıra tek bir çatal altı işareti (`#`), ardından bir boşluk, daha sonra ise başlık metni girilerek oluşturulur. Örneğin bu makalenin H1 başlığı şöyledir:

```md
# Markdown headings
```

H1 başlıkları için aşağıdaki kurallar geçerlidir:

- Bir dosyada bir H1 bulunmalıdır.
- Yalnızca bir tane H1 bulunabilir.
- H1'in içeriği olmalıdır.

  ```markdown
  # 
  This is not allowed.
  ```
- `#` ile H1 içeriği arasında bir boşluk olmalıdır. Boşluğu olmayan bir H1 yayımlanan bir sayfada bir başlık olarak ekrana çizilmez.

  ```markdown
  #This looks bad on the site.
  ```
- H1, dosyada YML meta veri başlığından sonraki ilk içerik olmalıdır. YML başlığı ile H1 arasına metin veya görüntü gibi hiçbir içerik konamaz.

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- İlk düzey başlıkların HTML öğesi olan `<h1>` kullanılmamalıdır. Markdown sözdizimini (`# `) kullanın.
- H1 en çok 100 karakter uzunlukta olabilir. Bu bir stil yönergesidir.

## <a name="h2---h6"></a>H2 - H6

H2 (`## `) ile H6 (`###### `) arasındaki başlıklar OPS'de kullanılabilir. Başlık oluşturmak için HTML (`<h2>` - `<h6>`) değil Markdown başlıklarını kullanın.
