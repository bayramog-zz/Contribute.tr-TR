---
title: docs.microsoft.com için Markdown başvurusu
description: Markdown özelliklerini ve Microsoft Docs platformunda kullanılan söz dizimini öğrenin.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.openlocfilehash: 17bc6d3bf2de5077f490bea2f03cddf23d925b78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55712959"
---
# <a name="markdown-reference"></a>Markdown Başvurusu

Markdown, düz metin biçimli söz dizimine sahip hafif bir biçimlendirme dilidir. Docs platformu, Markdown için CommonMark standardını ve docs.microsoft.com’da daha zengin içerik sağlamak üzere tasarlanmış bazı Markdown uzantılarını destekler. Bu makale, docs.microsoft.com’da Markdown kullanmaya yönelik alfabetik başvuru sağlar.

Markdown yazmak için herhangi bir metin düzenleyiciyi kullanabilirsiniz. Hem standart Markdown söz dizimini hem de özel Docs uzantılarını eklemeyi kolaylaştıran bir düzenleyici olarak [Docs Yazma Paketi](https://aka.ms/DocsAuthoringPack) yükleyip [VS Code](https://code.visualstudio.com/) kullanmanızı öneririz.

Docs, Markdig Markdown altyapısını kullanır. [https://babelmark.github.io/](https://babelmark.github.io/) adresine giderek Markdig’e kıyasla diğer altyapılarda Markdown’ın nasıl işlendiğini test edebilirsiniz.

## <a name="alerts-note-tip-important-caution-warning"></a>Uyarılar (Not, İpucu, Önemli, Dikkat, Uyarı)

Uyarılar, docs.microsoft.com’da içeriğin önemini belirtmek adına renkler ve simgelerle işlenen blok alıntı oluşturma amaçlı bir Docs Markdown uzantısıdır. Aşağıdaki uyarı türleri desteklenir:

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

Bu uyarılar docs.microsoft.com’da şu şekilde görünür:

> [!NOTE]
> Kullanıcıların hızlıca göz gezdirirken bile fark etmesi gereken bilgiler.

> [!TIP]
> Kullanıcıların daha başarılı olmasına yardımcı ek bilgiler.

> [!IMPORTANT]
> Kullanıcı başarısı için gerekli bilgiler.

> [!CAUTION]
> Bir eylemin olası olumsuz sonuçları.

> [!WARNING]
> Bir eylemin kesin tehlikeli sonuçları.

## <a name="code-snippets"></a>Kod parçacıkları

Markdown dosyalarınıza kod parçacıkları ekleyebilirsiniz:

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>Bölüm başlıkları

Docs, altı Markdown bölüm başlığı düzeyini destekler:

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Son `#` ile bölüm başlığı metni arasında bir boşluk olmalıdır.
- Tüm Markdown dosyalarında yalnızca ve yalnızca bir H1 olmalıdır.
- H1, dosyada YML meta veriler bloğundan sonraki ilk içerik olmalıdır.
- H2’ler, yayımlanan dosyanın sağ tarafındaki gezinti menüsünde otomatik olarak görüntülenir. Daha düşük düzeydeki bölüm başlıkları burada görüntülenmez; kullanıcıların içeriğinizde gezinmesine yardımcı olmak için H2’leri stratejik olarak kullanın.
- `<h1>` gibi HTML bölüm başlıkları önerilmez ve bazı durumlarda derleme uyarılarına sebep olur.
- [Yer işaretleri](#bookmark-links) yoluyla bir dosyadaki bağımsız bölüm başlıklarına bağlantı verebilirsiniz.

## <a name="html"></a>HTML

Markdown satır içi HTML’yi desteklese de Docs yoluyla belge yayımlarken HTML önerilmez ve bazı değerler dışında derleme hatalarına ve uyarılarına sebep olur. <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a>Görüntüler

Bir görüntüyü ekleme söz dizimi şu şekildedir:

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

`alt text`, görüntünün kısa bir açıklamasını ve `<folder path>`, görüntünün göreli yolunu ifade eder. Alternatif metin, görme engellilere yönelik ekran okuyucular için gereklidir. Ayrıca görüntünün işlenememesine yol açan bir site hatası durumunda işe yarar.

Görüntüler, belge kümeniz içerisinde bir `/media` klasöründe depolanmalıdır. Görüntüler için varsayılan olarak aşağıdaki dosya türleri desteklenir:

- .jpg
- .png

Diğer görüntü türlerini belge kümenizin docfx.json dosyasına<!--add link to reference when available--> kaynak olarak ekleyerek bunlar için de destek sağlayabilirsiniz.

## <a name="links"></a>Bağlantılar

Docs çoğu zaman diğer dosya ve sayfalara gitmek için standart Markdown bağlantılarını kullanır. Bağlantı türleri, aşağıdaki alt bölümlerde açıklanmıştır.

> [!TIP]
> VS Code için Docs Yazma Paketi, yolları bulmakla uğraşmadan göreli bağlantıları ve yer işaretlerini doğru şekilde eklemenize yardımcı olabilir.

> [!IMPORTANT]
> Belgelerinize eklediğiniz Microsoft site bağlantılarına tr-tr gibi yerel ayar kodlarını dahil etmeyin. Sabit kodlanmış yerel ayar kodları, yerelleştirilmiş içeriğin işlenmesini önler ve bu durum, diğer yerel ayarlara sahip kullanıcılar için kötü bir müşteri deneyimi sağlamakla kalmayıp yüksek yerelleştirme maliyetlerine yol açar. Bir tarayıcıdan URL kopyaladığınızda URL’de varsayılan olarak yerel ayar kodu bulunur; bağlantınızı oluştururken bu kodu el ile silmeniz gerekir. Örneğin şunu kullanın:
>
> `[Microsoft](https://www.microsoft.com)`
>
> Şunu değil:
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>Aynı belge kümesindeki dosyalara giden göreli bağlantılar

Göreli yol, geçerli dosyayla ilgili bir hedef dosyaya ait yoldur. Docs’ta göreli yolları kullanarak aynı belge kümesindeki başka bir dosyaya bağlantı verebilirsiniz. Göreli yollar için söz dizimi aşağıdaki gibidir:

```markdown
[link text](../../folder/filename.md)
```

`../`, hiyerarşideki bir üst düzeyi ifade eder.

- Göreli yol, derleme esnasında .md uzantısının kaldırılması dahil olmak üzere çözümlenir.
- Üst klasördeki bir dosyaya bağlantı sağlamak için “../” kullanabilirsiniz ancak bu klasörün aynı belge kümesinde yer alması gerekir. Farklı bir belge kümesi klasöründeki dosyaya bağlantı vermek için “../” kullanamazsınız.
- Docs ayrıca “~” ile başlayan özel bir göreli yol biçimini de destekler (örneğin ~/foo/bar.md). Bu söz dizimi, bir belge kümesinin kök klasöründe bulunan bir dosyayı gösterir. Bu tür bir yol da derleme sırasında doğrulanıp çözümlenir.

> [!IMPORTANT]
> Dosya uzantısını göreli yola dahil edin. Derleme, bu göreli yola ait hedef dosyanın varlığını doğrular. Ve göreli yolda dosya uzantısı yoksa derlemenin bozuk bağlantı uyarısı raporlaması olasıdır. Örneğin şunu kullanın:
>
> `[link text](../../folder/filename.md)`
>
> Şunu değil:
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a>Docs’taki diğer dosyalara giden site göreli bağlantıları

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

Dosya uzantısını (.md) dahil etmeyin. Uzantı, Azure “makaleler” belge kümesinin dışındaki Linux genel bakış dosyasına bağlantı verir.

### <a name="links-to-external-sites"></a>Harici sitelere giden bağlantılar

```markdown
[Microsoft](https://www.microsoft.com)
```

Başka bir Web sayfasına giden URL temelli bağlantı (https:// içermelidir).

### <a name="bookmark-links"></a>Yer işareti bağlantıları

Aynı depodaki farklı bir dosyada bulunan bölüm başlığına giden yer işareti bağlantısı:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

Geçerli dosyadaki bölüm başlığına giden yer işareti bağlantısı:

```markdown
[Managed Disks](#managed-disks)
```

Bir diyez etiketi, ardından noktalama işaretleri kaldırılmış ve boşluklar yerine kısa çizgi getirilmiş bölüm başlığı adını kullanın.

### <a name="explicit-anchor-links"></a>Açık yer işareti bağlantıları

`<a>` HTML etiketinin kullanan açık yer işareti bağlantıları, hub veya giriş sayfaları harici **gerekli değildir veya önerilmez**. Yer işaretlerini yukarıdaki genel Markdown dosyalarında açıklandığı şekilde kullanın. Hub ve giriş sayfaları için yer işaretlerini aşağıdaki gibi kullanın:

`## <a id="AnchorText"> </a>Header text` veya `## <a name="AnchorText"> </a>Header text`

Açık yer işaretlerine bağlantı vermek için şu söz dizimini kullanın:

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>XREF (çapraz başvuru) bağlantıları

Geçerli veya farklı bir dosya kümesindeki otomatik oluşturulmuş API başvurularına bağlantı vermek için benzersiz kimlik (UID) ile XREF bağlantıları kullanın.

> [!NOTE]
> Diğer belge kümelerindeki API başvurularına başvurmak için `xrefService` dosyasına `docfx.json` yapılandırmasını eklemeniz gerekir.
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

UID, tam nitelikli sınıf ve üye adına karşılık gelir. UID’den sonra bir * eklerseniz bağlantı belirli bir API’yi değil, aşırı yükleme sayfasını gösterir. Örneğin `List<T>.BinarySearch(T, IComparer<T>)` gibi bir aşırı yükleme sayfasında bağlantı vermek yerine İkili Arama Yöntemi sayfasına bağlantı vermek için `List<T>.BinarySearch*` kullanın.

Şu söz dizimlerinden birini kullanabilirsiniz:

- Otomatik bağlantı: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  İsteğe bağlı `displayProperty` sorgu parametresi, tam nitelikli bir bağlantı metni üretir. Varsayılan olarak, bağlantı metni yalnızca üyenin veya türün adını gösterir.

- Markdown bağlantısı: `[link text](xref:UID)`
  
  Görüntülenen bağlantı metnini özelleştirmek istediğinizde kullanın.

Örnekler:

- `<xref:System.String>`, “String” olarak işlenir.
- `<xref:System.String?displayProperty=nameWithType>`, “System.String” olarak işlenir.
- `[String class](xref:System.String)`, “String class” olarak işlenir.

Şu an için UID’leri bulmanın kolay bir yolu yoktur. <!-- ? -->Bir API UID’sini bulmanın en iyi yolu, bağlantı oluşturmak istediğiniz API sayfasına ilişkin kaynağı görüntülemek ve ms.assetid değerini bulmaktır. Aşırı yükleme değerleri kaynakta tek tek gösterilmez. İleride daha iyi bir sistem sunmak için çalışıyoruz.

UID; \`, \# veya \* özel karakterlerini içerdiğinde UID değerinin sırasıyla `%60`, `%23` ve `%2A` olarak kodlanmış HTML olması gerekir. Bazen parantezlerin kodlandığını görürsünüz ancak bu, zorunlu değildir.

Örnekler:

- System.Threading.Tasks.Task\`1, `System.Threading.Tasks.Task%601` olur
- System.Exception.\#ctor, `System.Exception.%23ctor` olur
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode), `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29` olur

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a>Listeler (Numaralandırılmış, Madde İşaretli, Denetim Listesi)

### <a name="numbered-list"></a>Numaralı liste

Numaralandırılmış liste oluşturmak için yalnızca 1 sayısını kullanabilirsiniz, belge yayımlandığında bunlar sıralı bir liste olarak işlenir. Kaynak okunurluğunu artırmak için artışlı liste oluşturabilirsiniz.

Bu listelerde (iç içe geçmiş listeler dahil) harf kullanmayın. Bunlar, Docs’ta yayımlandığında düzgün işlenmez. Sayıların kullanıldığı iç içe geçmiş listeler, yayımlandığında küçük harfli listeler olarak işlenir. Örneğin:

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

Bu, şu şekilde işlenir:

1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)

### <a name="bulleted-list"></a>Madde işaretli liste

Madde işaretli liste oluşturmak için her satırın başında `-` ve ardından boşluk kullanın:

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

Bu, şu şekilde işlenir:

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

### <a name="checklist"></a>Denetim listesi

Denetim listeleri, (yalnızca) docs.microsoft.com’da özel bir Markdown uzantısı yoluyla kullanılabilir:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Bu örnek, docs.microsoft.com’da şu şekilde işlenir:

> [!div class="checklist"]
> * Liste öğesi 1
> * Liste öğesi 2
> * Liste öğesi 3

Denetim listelerini bir makalenin başında veya sonunda, “Öğrenecekleriniz” veya “Öğrendikleriniz” içeriklerini özetlemek için kullanın. Makaleniz içerisinde denetim listelerini rastgele kullanmayın.
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>Sonraki adım eylemi

(Yalnızca) docs.microsoft.com’daki sayfalara sonraki adım eylemi düğmesi eklemek için özel bir uzantı kullanabilirsiniz.

Söz dizimi aşağıdaki gibidir:

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Örneğin:

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

Bu, şu şekilde işlenir:

> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)

Bir sonraki adım eyleminde desteklenen tüm bağlantıları kullanabilirsiniz, buna farklı bir Web sayfasına ait Markdown bağlantısı da dahildir. Sonraki adım eylemi çoğu zaman aynı belge kümesindeki farklı bir dosyaya giden göreli bağlantıdır.

## <a name="section-definition"></a>Bölüm tanımı

<!-- more info about this would be helpful! --> Bazı bölümleri tanımlamanız gerekebilir. Bu söz dizimi daha çok kod tabloları için kullanılır.
Aşağıdaki örneğe bakın:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

Yukarıdaki alıntı bloğu Markdown metni şu şekilde işlenir:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a>Seçiciler

<!-- could be more clear! --> Aynı makalede farklı sayfaları bağlamak istiyorsanız seçici kullanabilirsiniz. Böylelikle okuyucular, belirttiğiniz sayfalar arasında geçiş yapabilirler.

> [!NOTE]
> Bu uzantı, docs.microsoft.com ve MSDN’de farklı çalışır. <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a>Tek seçici

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

... şu şekilde işlenir:

> [!div class="op_single_selector"]
> - [Evrensel Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a>Çoklu seçici

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

... şu şekilde işlenir:

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows evrensel C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows evrensel C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

## <a name="tables"></a>eğlence

Markdown’da bir tablo oluşturmanın en kolay yolu, kanallar ve çizgiler kullanmaktır. Üst bilgisi olan standart bir tablo oluşturmak için ilk satırın altına kısa çizgilerden oluşan bir satır ekleyin:

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

Bu, şu şekilde işlenir:

|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!||

Üst bilgisiz bir tablo da oluşturabilirsiniz. Örneğin, çok sütunlu bir liste oluşturmak için:

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

Bu, şu şekilde işlenir:

|   |   |
| - | - |
| This | table |
| has no | header |

İki nokta üst üste kullanarak sütunları hizalayabilirsiniz:

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

Şu şekilde işlenir:

|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|

> [!TIP]
> VS Code için Docs Yazma Uzantısı, temel Markdown dosyalarını eklemeyi kolaylaştırır!
>
> [Çevrimiçi tablo oluşturucu](http://www.tablesgenerator.com/markdown_tables) da kullanabilirsiniz.

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> Bu, yalnızca docs.microsoft.com sitesinde çalışır.

Markdown’da tablo oluşturursanız, bu tablo sağ gezinti alanına doğru genişleyebilir ve okunmaz duruma gelir. Docs işlemenin, gerektiğinde tabloyu bölmesine izin vererek bu sorunu çözebilirsiniz. Yalnızca tabloyu `[!div class="mx-tdBreakAll"]` özel sınıfıyla sarmalayın.

Sınıf adı `mx-tdBreakAll` olan bir `div` tarafından sarmalanacak üç satırlı bir tablonun Markdown örneği aşağıdadır.

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

Şöyle işlenir:

> [!div class="mx-tdBreakAll"]
> |Ad|Söz Dizimi|Sessiz yükleme için gerekli mi?|Açıklama|
> |-------------|----------|---------|---------|
> |Sessiz|/quiet|Evet|Hiçbir kullanıcı arabirimi veya komut istemi görüntülemeden yükleyiciyi çalıştırır.|
> |NoRestart|/norestart|Hayır|Herhangi bir yeniden başlatma denemesini engeller. Varsayılan olarak kullanıcı arabirimi, yeniden başlatmadan önce sorar.|
> |Yardım|/help|Hayır|Yardım ve hızlı başvuru sağlar. Tüm seçenek ve davranışların listesiyle birlikte, kurulum komutunun doğru kullanımını gösterir.|

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> Bu, yalnızca docs.microsoft.com sitesinde çalışır.

Bazen, tablonun ikinci sütununa çok uzun sözcükler girebilirsiniz. Bunların düzgün bir şekilde bölünmesi için daha önce gösterildiği gibi `div` sarmalayıcı söz dizimini kullanarak `mx-tdCol2BreakAll` sınıfını uygulayabilirsiniz.

### <a name="html-tables"></a>HTML Tabloları

Docs.microsoft.com’da HTML tabloları önerilmez. Bu tablolar, Markdown’ın temel prensibine aykırı olarak kaynakta okunabilir değildir.

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>Videolar

### <a name="embedding-videos-into-a-markdown-page"></a>Markdown sayfalarına video ekleme

Docs şu anda şu üç konumda yayımlanmış videoları desteklemektedir:

- YouTube
- Channel 9
- Microsoft’un kendi “One Player” sistemi

Aşağıdaki söz dizimiyle videoyu ekleyebilirsiniz. Docs bu videoyu işler.

```markdown
> [!VIDEO <embedded_video_link>]
```

Örnek:

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

...şu şekilde işlenir:

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

Yayımlanan sayfalarda da şöyle görüntülenir:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> CH9 video URL’si `https` ile başlayıp `/player` ile bitmelidir. Aksi takdirde, yalnızca video yerine tüm sayfa eklenir.

### <a name="uploading-new-videos"></a>Yeni video yükleme

Yeni bir video, şu süreci takip ederek karşıya yüklenmelidir:

1. IDWEB’deki **docs_video_users** grubuna katılın.
1. https://aka.ms/VideoUploadRequest adresine gidin ve videonuzun ayrıntılarını belirtin. Şunlara ihtiyacınız olacaktır (bu öğelerden hiçbiri diğer kişilere görünür olmayacaktır):
    1. Videonuz için başlık.
    1. Videonuzun ilgili olduğu ürünler/hizmetler listesi.
    1. Videonuzun barınacağı hedef sayfa veya (sayfanız henüz yoksa) belge kümesi.
    1. Videonuzun MP4 dosyasına ait bağlantı (dosyayı koyacak konumunuz yoksa geçici olarak şuraya koyabilirsiniz:   `\\scratch2\scratch\apex`). MP4 dosyaları en az 720p olmalıdır.
    1. Videonun açıklaması.
1. Bu öğeyi gönderin (kaydedin).
1. İki iş günü içerisinde videonuz yüklenecektir. Videoyu eklemeniz için gereken bağlantı iş öğesine eklenecektir ve bu bağlantı, *tekrar size* çözümlenecektir.
1. Video bağlantısını aldıktan sonra iş öğesini kapatın.
1. Artık video bağlantısını gönderinize ekleyebilirsiniz. Bunun için şu söz dizimini kullanın:

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
