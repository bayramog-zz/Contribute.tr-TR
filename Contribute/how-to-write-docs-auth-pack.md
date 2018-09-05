---
title: VS Code için Docs Yazma Paketi
description: Bu makale, docs.microsoft.com’da Markdown yazmayı kolaylaştıran VS Code uzantı paketini açıklar.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.openlocfilehash: b9fedce0a73c5c4212ffd0893c745fab56677c8c
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308928"
---
# <a name="docs-authoring-pack-for-vs-code"></a>VS Code için Docs Yazma Paketi

Docs Yazma Paketi, docs.microsoft.com içim Markdown yazmaya yardımcı VS Code uzantılarının bir koleksiyonudur. Paketi [VS Code Marketi’nde mevcuttur](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) ve şu uzantıları barındırır:

- [markdownlint:](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) David Anson tarafından oluşturulan popüler bir Markdown lint aracı, Markdown’ınızın en iyi yöntemleri izlemesini sağlar.
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): Street Side Software tarafından oluşturulan tamamen çevrimdışı bir yazım denetimi aracı.
- [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): Özel Markdown dahil olmak üzere daha kesin bir Markdown önizlemesi için docs.microsoft.com CSS dosyasını kullanır.
- [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): docs.microsoft.com’a içerik yazmak için Açık Yayımlama Sistemi’nde (OPS) temel Markdown desteği ve özel Markdown söz dizimi desteği dahil olmak üzere Markdown yazma yardımı sağlar. Bu konunun geri kalan kısmında Docs Markdown uzantısı açıklanır.
- [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): Kullanıcıların yeni dosyalara Markdown çatısı içeriğini uygulamasını sağlar.

## <a name="prerequisites-and-assumptions"></a>Önkoşullar ve varsayımlar

Markdown uzantısını kullanarak ilgili bağlantılar, görüntüler ve diğer eklenen içeriği eklemek için VS Code iş alanınızın kapsamı, kopyalanmış Açık Yayımlama Sistemi (OPS) deponuzun kökü olmalıdır.

Uzantı tarafından desteklenen uyarılar ve kod parçacıkları gibi bazı söz dizimleri, OPS için özel Markdown’dır ve OPS yoluyla yayımlanmadığı sürece doğru işlenmez.

## <a name="how-to-use-the-docs-markdown-extension"></a>Docs Markdown uzantısını kullanma

Docs Markdown menüsüne ulaşmak için `ALT+M` tuşlarına basın. İstediğiniz işlevi seçmek için yukarı/aşağı okları kullanabilir veya tıklayabilirsiniz ya da yazarak filtrelemeye başlayabilir ve istediğiniz işlev menüde vurgulandığında `ENTER` tuşuna basabilirsiniz. Şunlar kullanılabilir:

|İşlev     |Açıklama           |
|-------------|----------------------|
|Önizleme      |Docs Preview uzantısını kullanarak yan yana pencerede geçerli konunun önizlemesini gösterir. Bu seçenek yalnızca Docs Preview uzantısı yüklüyse kullanılabilir.|
|Kalın         |Metni **kalın** olarak biçimlendirir.|
|İtalik       |Metni *italik* olarak biçimlendirir.|
|Kod         |Bir satır veya daha azı seçilmişse, metni `inline code` olarak biçimlendirir.<br><br>Birden fazla satır seçilmişse bunları etrafı çevrili kod blokları olarak biçimlendirir ve isteğe bağlı olarak OPS tarafından desteklenen bir bilgisayar dili seçmenize olanak tanır.|
|Uyarı        |Bir Not, Önemli, Uyarı veya İpucu ekler.<br><br>Menüden Uyarı’yı ve ardından uyarı türünü seçin. Önceden metin seçtiyseniz bu, seçili uyarı söz dizimiyle çevrelenir. Metin seçilmemişse yeni uyarı, yer tutucu metinle birlikte eklenir.|
|Numaralı liste|Yeni bir numaralı liste ekler.<br><br> Birden fazla satır seçilmişse bunların her biri liste öğesi olur. Markdown’da gösterilen numaralı listelerin tamamı 1 olarak gözükse de bunların docs.microsoft.com’da ardışık sayılar veya iç içe listeler söz konusu olduğunda harf olarak görüneceğini unutmayın. Yeni bir iç içe geçmiş numaralı liste oluşturmak için üst listede tab tuşunu kullanın.|
|Madde işaretli liste|Yeni bir madde işaretli liste ekler.|
|Tablo        |Bir Markdown tablo yapısı ekler.<br><br>Tablo komutunu seçtikten sonra sütun:satır biçiminde sütun ve satır sayısını belirtin, örneğin 3:4. Bu uzantıyla belirtebileceğiniz en fazla sütun sayısının 5 olduğunu unutmayın. Bu sayı, okunabilirlik için önerilen en yüksek değerdir.|
|Depodaki dosyaya bağlantı|Geçerli depodaki bir başka dosyaya göreli bağlantı ekler. Bu seçeneği seçtikten sonra dosyaları filtrelemek için komut penceresinde dosya adını yazmaya başlayın ve istediğiniz dosyayı seçin. Önceden bir metin seçtiyseniz bağlantı metni olarak kullanılır. Seçmediyseniz hedef dosyanın H1 değeri bağlantı metni olarak kullanılır.|
|Web sayfası bağlantısı    |Bir web sayfası bağlantısı ekler. Bu seçeneği belirledikten sonra URI'yi komut penceresine yapıştırın veya yazın. `https://` gereklidir. Önceden bir metin seçtiyseniz bağlantı metni olarak kullanılır. Seçmediyseniz URI bağlantı metni olarak kullanılır.|
|Başlık bağlantısı     |Geçerli dosyada veya depodaki başka bir dosyada bulunan bir yer işaretine bağlantı ekler.<br>`Bookmark in this file`: Doğru biçimlendirilmiş bir yer işareti eklemek için geçerli dosyadaki başlıklar listesinden bir seçim yapın.<br>`Bookmark in another file`: Önce dosya adına göre filtreme yapın ve bağlantı verilecek dosyayı seçin, daha sonra seçili dosyada uygun başlığı seçin.|
|Görüntü        |Alternatif metni yazın (erişilebilirlik içi gereklidir) ve seçin, daha sonra depodaki desteklenen görüntü dosyaları listesini filtrelemek için bu komuta çağrı yapın ve istediğiniz görüntü dosyasını seçin. Bu komuta çağrı yaptığınızda alternatif metni seçmemişseniz, bir görüntü dosyası seçmeden önce metni seçmek için istem alırsınız.|
|Ekle      |Geçerli dosyaya eklemek üzere bir dosya bulur.|
|Kod Parçacığı      |Geçerli dosyaya eklemek üzere depoda bir kod parçacığı bulur.|
|Video        |Ekli bir video ekler.|
|Şablon     |Yeni bir dosya oluşturur ve bir Markdown şablonu uygular. Daha fazla bilgi için aşağıdaki [Şablonlar](#how-to-use-docs-templates) bölümüne bakın.|

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

## <a name="how-to-show-the-legacy-toolbar"></a>Eski araç çubuğunu gösterme

Uzantının yayın öncesi sürümünü kullanmakta olan kullanıcılar, Docs Markdown Uzantısı yüklendiğinde VS Code penceresinin altında artık yazma araç çubuğunun olmadığını fark edeceklerdir. Bu araç çubuğu, VS Code durum çubuğunda çok fazla yer kapladığı ve uzantı UX’i için en iyi deneyimleri izlemediği için yeni uzantıda devre dışı bırakılmıştır. Ancak dilerseniz settings.json dosyasında VS Code ayarlarınızı aşağıdaki gibi güncelleştirerek bu araç çubuğunu tekrar gösterebilirsiniz:

1. VS Code’da Dosya -> Tercihler -> Ayarlar’a gidin (`CTRL+Comma`).
1. Ayarları tüm VS Code iş alanları için değiştirmek istiyorsanız Kullanıcı Ayarları’nı, yalnızca geçerli iş alanı için değiştirmek istiyorsanız İş Alanı Ayarları’nı seçin.
1. Varsayılan Ayarlar bölmesinde Docs Yazma Uzantısı Yapılandırması’nı bulun ve istediğiniz ayarın yanındaki kalem simgesini seçin. Daha sonra sizden `true` veya `false` seçmeniz istenecek. Seçiminizi yaptıktan sonra VS Code bu değeri settings.json dosyasına otomatik olarak ekleyecek ve değişikliklerin uygulanması için sizden pencereyi yeniden yüklemeniz istenecek.

## <a name="how-to-use-docs-templates"></a>Docs şablonlarını kullanma

Docs Article Templates uzantısı yazıcıların VS Code içindeki merkezi bir depodan bir Markdown şablonu çekip bir dosyaya uygulamasını sağlar. Şablonlar makalelere gerekli meta verilerin eklenmesi ve içerik standartlarına uygun hareket edilmesi gibi konulardan emin olmanıza yardımcı olabilir. Şablonlar, genel bir GitHub deposunda Markdown dosyaları olarak yönetilir.

### <a name="to-apply-a-template-in-vs-code"></a>VS Code'da şablon uygulama

1. Docs Markdown uzantısı yüklü değilse F1 tuşuna basarak komut paletini açın, filtreleme için "template" yazın ve `Docs: Template` öğesine tıklayın. Docs Markdown uzantısı yüklüyse komut paletini kullanarak veya `Alt+M` öğesine tıklayarak Docs Markdown QuickPick menüsünü açabilir ve listeden `Template` öğesini seçebilirsiniz.
1. Açılan listeden istenen şablonu seçin.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>GitHub kimliğinizi ve/veya Microsoft diğer adınızı VS Code ayarlarınıza ekleme

Templates uzantısı, üç dinamik meta veri alanını destekler: author, ms.author ve ms.date. Bu da şablon oluşturan bir kullanıcının bu alanları bir Markdown şablonunun meta veri başlığında kullanması durumunda bu değerlerin şablonu uyguladığınızda aşağıdaki şekilde dosyanıza otomatik olarak ekleneceği anlamına gelir:

|Meta veriler  |Değer|
|----------|---------------|
|author    |VS Code ayar dosyasında belirtilen GitHub kimliğiniz.|
|ms.author |VS Code ayar dosyasında belirtilen Microsoft diğer adınız. Microsoft çalışanı değilseniz bu alanı boş bırakın.|
|ms.date   |Docs tarafından desteklenen biçimde geçerli tarih: AA/GG/YYYY. Dosyayı daha sonra güncelleştirdiğinizde tarihin otomatik olarak güncelleştirilmeyeceğini unutmayın. Makalenin güncelleştirme tarihini belirtmek için bu değeri el ile ayarlamanız gerekir.|

### <a name="to-set-author-github-id-andor-msauthor-microsoft-alias"></a>author (GitHub kimliği) ve/veya ms.author (Microsoft diğer adı) değerlerini ayarlama

1. VS Code’da Dosya -> Tercihler -> Ayarlar’a gidin (`CTRL+Comma`).
1. Ayarları tüm VS Code iş alanları için değiştirmek istiyorsanız Kullanıcı Ayarları’nı, yalnızca geçerli iş alanı için değiştirmek istiyorsanız İş Alanı Ayarları’nı seçin.
1. Sol taraftaki Varsayılan Ayarlar bölmesinde Docs Article Templates Uzantısı Yapılandırması'nı bulun, değiştirmek istediğiniz ayarın yanındaki kalem simgesine ve ardından Ayarlar bölümünde Değiştir'e tıklayın.
1. Kullanıcı Ayarları bölmesi yan tarafta açılır ve en altta yeni bir giriş gösterilir.
1. GitHub kimliğinizi veya Microsoft e-posta diğer adınızı ekleyin ve dosyayı kaydedin.
1. Değişikliklerin geçerli olması için VS Code uygulamasını kapatıp yeniden başlatmanız gerekebilir.
1. Artık dinamik alanları kullanan bir şablon uyguladığınızda GitHub kimliğiniz ve/veya Microsoft takma adınız meta veri başlığına otomatik olarak eklenecek.
