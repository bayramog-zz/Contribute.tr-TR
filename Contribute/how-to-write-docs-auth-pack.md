---
title: VS Code için Docs Yazma Paketi
description: docs.microsoft.com’da Markdown yazmayı kolaylaştırmak için VS Code uzantı paketi.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.article: contributor-guide
ms.prod: n.a
ms.service: n.a
ms.technology: n.a
ms.openlocfilehash: 5c857deb07e28e1f6744c895a291bf78a6acf1df
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2018
---
# <a name="docs-authoring-pack-for-vs-code"></a>VS Code için Docs Yazma Paketi

Docs Yazma Paketi, docs.microsoft.com içim Markdown yazmaya yardımcı VS Code uzantılarının bir koleksiyonudur. Paketi [VS Code Marketi’nde mevcuttur](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) ve şu uzantıları barındırır:

- **DocFx:** docs.microsoft.com’a özel Markdown önizlemesi sağlar. Daha fazla bilgi için bkz. [DocFx](https://marketplace.visualstudio.com/items?itemName=ms-docfx.DocFX).
- **markdownlint:** David Anson tarafından oluşturulan popüler bir Markdown lint aracı, Markdown’ınızın en iyi uygulamaları izlemesini sağlar. Daha fazla bilgi için bkz. [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint).
- **Docs Markdown:** docs.microsoft.com’a içerik yazmak için Açık Yayımlama Sistemi’nde (OPS) temel Markdown desteği ve özel Markdown söz dizimi desteği dahil olmak üzere Markdown yazma yardımı sağlar. Bu konunun geri kalan kısmında Docs Markdown uzantısı açıklanır.

## <a name="prerequisites-and-assumptions"></a>Önkoşullar ve varsayımlar

Markdown uzantısını kullanarak ilgili bağlantılar, görüntüler ve diğer eklenen içeriği eklemek için VS Code iş alanınızın kapsamı, kopyalanmış OPS deponuzun kökü olmalıdır.

Uzantı tarafından desteklenen uyarılar ve kod parçacıkları gibi bazı söz dizimleri, OPS için özel Markdown’dır ve OPS yoluyla yayımlanmadığı sürece doğru işlenmez.

## <a name="how-to-use-the-docs-markdown-extension"></a>Docs Markdown uzantısını kullanma

Docs Markdown menüsüne ulaşmak için `ALT+M` tuşlarına basın. İstediğiniz işlevi seçmek için yukarı/aşağı okları kullanabilir veya tıklayabilirsiniz ya da yazarak filtrelemeye başlayabilir ve istediğiniz işlev menüde vurgulandığında `ENTER` tuşuna basabilirsiniz. Şunlar kullanılabilir:

|İşlev     |Komut             |Açıklama           |
|-------------|--------------------|----------------------|
|Kalın         |`formatBold`        |Metni **kalın** olarak biçimlendirir.|
|İtalik       |`formatItalic`      |Metni *italik* olarak biçimlendirir.|
|Kod         |`formatCode`        |Bir satır veya daha azı seçilmişse, metni `inline code` olarak biçimlendirir.<br><br>Birden fazla satır seçilmişse bunları etrafı çevrili kod blokları olarak biçimlendirir ve isteğe bağlı olarak OPS tarafından desteklenen bir bilgisayar dili seçmenize olanak tanır.|
|Uyarı        |`insertAlert`       |Bir Not, Önemli, Uyarı veya İpucu ekler.<br><br>Menüden Uyarı’yı ve ardından uyarı türünü seçin. Önceden metin seçtiyseniz bu, seçili uyarı söz dizimiyle çevrelenir. Metin seçilmemişse yeni uyarı, yer tutucu metinle birlikte eklenir.|
|Numaralı liste|`insertNumberedList` |Yeni bir numaralı liste ekler.<br><br> Birden fazla satır seçilmişse bunların her biri liste öğesi olur. Markdown’da gösterilen numaralı listelerin tamamı 1 olarak gözükse de bunların docs.microsoft.com’da ardışık sayılar veya iç içe listeler söz konusu olduğunda harf olarak görüneceğini unutmayın. Yeni bir iç içe geçmiş numaralı liste oluşturmak için üst listede tab tuşunu kullanın.|
|Madde işaretli liste|`insertBulletedList` |Yeni bir madde işaretli liste ekler.|
|Tablo        |`insertTable`        |Bir Markdown tablo yapısı ekler.<br><br>Tablo komutunu seçtikten sonra sütun:satır biçiminde sütun ve satır sayısını belirtin, örneğin 3:4. Bu uzantıyla belirtebileceğiniz en fazla sütun sayısının 5 olduğunu unutmayın. Bu sayı, okunabilirlik için önerilen en yüksek değerdir.|
|Bağlantı         |`selectLinkType`      |Bir bağlantı ekler. Bu komutu seçtiğinizde aşağıdaki alt menü görünür.<br><br>`External`: URI ile bir web sayfasına bağlantı sağlar. “http” veya “https” içermelidir.<br>`Internal`: Aynı depodaki bir başka dosyaya göreli bağlantı ekler. Bu seçeneği seçtikten sonra dosyaları filtrelemek için komut penceresinde dosya adını yazmaya başlayın ve istediğiniz dosyayı seçin. <br>`Bookmark in this file`: Doğru biçimlendirilmiş bir yer işareti eklemek için geçerli dosyadaki başlıklar listesinden bir seçim yapın.<br>`Bookmark in another file`: Önce dosya adına göre filtreme yapın ve bağlantı verilecek dosyayı seçin, daha sonra seçili dosyada uygun başlığı seçin.|
|Görüntü        |`insertImage`     |Alternatif metni yazın (erişilebilirlik içi gereklidir) ve seçin, daha sonra depodaki desteklenen görüntü dosyaları listesini filtrelemek için bu komuta çağrı yapın ve istediğiniz görüntü dosyasını seçin. Bu komuta çağrı yaptığınızda alternatif metni seçmemişseniz, bir görüntü dosyası seçmeden önce metni seçmek için istem alırsınız.|
|Ekle      |`insertInclude`   |Geçerli dosyaya eklemek üzere bir dosya bulur.|
|Kod Parçacığı      |`insertSnippet`   |Geçerli dosyaya eklemek üzere depoda bir kod parçacığı bulur.|
|Video        |`insertVideo`     |Ekli bir video ekler.|
|Önizleme      |`previewTopic`    |DocFX uzantısı kullanarak yan yana pencerede geçerli konunun önizlemesini gösterir.  DocFX uzantısı yüklü değilse veya yüklü ancak devre dışıysa, konu işlenmez.


## <a name="how-to-assign-keyboard-shortcuts"></a>Klavye kısayolları atama

1. `CTRL+K` ve ardından `CTRL+S` tuşlarına basarak Klavye Kısayolları listesini açın.
1. Özel tuş bağlaması oluşturmak istediğiniz komutu aratın, örneğin `formatBold`.
1. Fare imlecinizle satırın üzerine geldiğinizde komutun yanında beliren artı işaretine tıklayın.
1. Giriş kutusu göründüğünde, bu komuta bağlamak istediğiniz klavye kısayolunu girin. Örneğin kalın biçimi için yaygın kullanılan bir kısayolu girmek isterseniz `ctrl+b` tuşlarına basın.
1. Tuş bağlamanıza `when` yan tümcesini eklemek iyi bir fikir olabilir, böylece bu kısayol Markdown dışındaki dosyalarda geçerli olmayacaktır. Bunu yapmak için *keybindings.json* dosyasını açın ve komut adı altındaki şu satırı girin (satırlar arasına virgül koyduğunuzdan emin olun):
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Tamamlanmış özel tuş bağlamanız, keybindings.json dosyasına şu şekilde görünmelidir:

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. keybindings.json dosyasını kaydedin.

Daha fazla bilgi için VS Code belgelerindeki [Tuş Bağlamaları](https://code.visualstudio.com/docs/getstarted/keybindings) bölümüne bakın.

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>Eski “Gauntlet” araç çubuğunu gösterme

Eskiden “Gauntlet” adlı uzantıyı kullanmakta olan kullanıcılar, Docs Markdown Uzantısı yüklendiğinde VS Code penceresinin altında artık yazma araç çubuğunun olmadığını fark edeceklerdir. Bu araç çubuğu, VS Code durum çubuğunda çok fazla yer kapladığı ve uzantı UX’i için en iyi deneyimleri izlemediği için yeni uzantıda devre dışı bırakılmıştır. Ancak dilerseniz settings.json dosyasında VS Code ayarlarınızı aşağıdaki gibi güncelleştirerek bu araç çubuğunu tekrar gösterebilirsiniz:

1. VS Code’da Dosya -> Tercihler -> Ayarlar’a gidin (`CTRL+Comma`).
1. Ayarları tüm VS Code iş alanları için değiştirmek istiyorsanız Kullanıcı Ayarları’nı, yalnızca geçerli iş alanı için değiştirmek istiyorsanız İş Alanı Ayarları’nı seçin.
1. Varsayılan Ayarlar bölmesinde Docs Yazma Uzantısı Yapılandırması’nı bulun ve istediğiniz ayarın yanındaki kalem simgesini seçin. Daha sonra sizden `true` veya `false` seçmeniz istenecek. Seçiminizi yaptıktan sonra VS Code bu değeri settings.json dosyasına otomatik olarak ekleyecek ve değişikliklerin uygulanması için sizden pencereyi yeniden yüklemeniz istenecek.

## <a name="known-issues"></a>Bilinen sorunlar

- [DocFX Önizleme] MacOS ve Linux: DocFX Önizleme, önizlemeyi doğru başlatmıyor (bu platformlarda varsayılan olarak VS Code Markdown önizlemesi gösteriliyor).
- [DocFX Önizleme] Tüm platformlar: xref (çapraz başvuru) gibi bazı söz dizimleri API’lere bağlantı veriyor, önizlemede doğru işlenmiyor ve bazı durumlarda içeriği boş bırakabiliyor.
- [Dış yer işaretleri] Linux: Dosya listesi görüntüleniyor ancak seçilecek başlık görünmüyor.
- [Eklemeler] Linux: Dosya listesi görüntüleniyor ancak seçim yapıldıktan sonra hiçbir bağlantı eklenmiyor.