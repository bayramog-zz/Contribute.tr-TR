---
title: .NET makaleleri için şablon ve başvuru sayfası
description: Bu makale, .NET belge depoları için yeni makaleler oluştururken işinize yarayacak bir şablon içerir
ms.date: 11/07/2018
ms.openlocfilehash: 08c8e19c858e7417d49cc2de543c67f330b93e89
ms.sourcegitcommit: b0556fc33803358009a030ac9efcaed23f562868
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53264514"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a>.NET belgeleri için meta veriler ve Markdown şablonu

Bu dotnet/belgeler şablonu, Markdown söz dizimi örneklerinin yanında meta verileri ayarlama rehberi içerir.

Bir Markdown dosyası oluştururken, eklenen şablonu yeni bir dosyaya kopyalamalı, meta verileri aşağıda belirtildiği gibi doldurmalı ve H1 bölüm başlığını makalenin başlığı olarak yukarıda ayarlamalısınız.

## <a name="metadata"></a>Meta veriler

Gereken meta veri bloğu, aşağıdaki örnek meta veri bloğundadır:

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- İki nokta (:) ile meta veri öğesi arasına bir boşluk koymanız **zorunludur**.
- Bir değerdeki (örneğin başlıktaki) iki nokta işareti, meta veri ayrıştırıcısını keser. Bu durumda başlığın başına ve sonuna tırnak işareti koyun (örneğin `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **title (başlık)**: Arama altyapısı sonuçlarında görünür. Başlık, H1 başlığınızla aynı olmamalı ve en fazla 60 karakterden oluşmalıdır.
- **description (açıklama)**: Makalenin içeriğini özetler. Genellikle arama sonuçları sayfasında görüntülenir ancak arama sıralaması için kullanılmaz. Açıklama uzunluğu, boşluklu 115-145 karakter olmalıdır.
- **author (yazar)**: Yazar alanı, yazarın **GitHub kullanıcı adını** içermelidir.
- **ms.date**: En son yapılan önemli güncelleştirmenin tarihi. Tüm makaleyi gözden geçirip güncelleştirdiyseniz mevcut makalelerde bunu da güncelleştirin. Yazım hataları gibi küçük düzeltmeler güncelleştirme gerektirmez.

Diğer meta veriler makalelere eklenir, ancak çoğu meta veri değeri, **docfx.json** klasöründe belirtilen klasör düzeyinde uygulanır.

## <a name="basic-markdown-gfm-and-special-characters"></a>Temel Markdown, GFM ve özel karakterler

Markdown, GitHub Flavored Markdown (GFM) ve OPS’ye özgü uzantılar hakkında temel bilgileri [Markdown](how-to-write-use-markdown.md) ve [Markdown başvurusu](markdown-reference.md) hakkındaki genel makalelerden edinebilirsiniz.

Markdown, \*, \` ve \# gibi özel karakterleri biçimlendirme için kullanır. İçeriğinizde bu karakterlerden birine yer vermek isterseniz şu ikisinden birini yapmalısınız:

- Özel karakterden önce “kaçış” karakteri kullanmak (örneğin \* elde etmek için `\*` yazmak)
- Karakter için [HTML varlık kodunu](http://www.ascii.cl/htmlcodes.htm) kullanmak (örneğin &#42; elde etmek için `&#42;` yazmak).

## <a name="file-names"></a>Dosya adları

Dosya adlarında şu kuralları takip edin:

* Ad içerisinde yalnızca küçük harf, sayı ve kısa çizgi kullanın.
* Boşluk veya noktalama işareti kullanmayın. Dosya adındaki sözcük ve sayıları birbirinden ayırmak için kısa çizgi kullanın.
* Geliştir, satın al, oluştur, sorun gider gibi belirgin eylem fiillerini kullanın. -ing (İngilizcede) ile biten sözcük kullanmayın.
* Kısa kelimeler kullanmayın; bir, ve, veya gibi sözcükler eklemeyin.
* Ad, Markdown biçiminde olmalı ve .md dosya uzantısını kullanmalıdır.
* Dosya adlarını olabildiğince kısa tutun. Adlar, makale URL’lerinin bir parçasıdır.

## <a name="headings"></a>Bölüm başlıkları

Cümle stili büyük harf kullanımını uygulayın. Başlığın ilk harfini her zaman büyük yazın.

## <a name="text-styling"></a>Metin stili

*İtalik* Dosyalar, klasörler, yollar (uzun öğeleri kendi satırlarına göre ayırın) ve yeni terimler için kullanın.

**Kalın** Kullanıcı arabirimi öğeleri için kullanın.

`Code` Satır içi kod, bilgisayar dili anahtar sözcükleri, NuGet paket adları, komut satırı komutları, veritabanı tablosu ve sütun adları ile tıklanabilir olmasını istemediğiniz URL’ler için kullanın.

## <a name="links"></a>Bağlantılar

Yer işaretleri, dahili bağlantılar, diğer belgelere giden bağlantılar, kod eklemeleri ve harici bağlantılar için [Bağlantılar](how-to-write-links.md) genel makalesine bakın.

.NET belgeleri ekibi, şu kuralları kullanır:

- Çoğu durumda göreli bağlantılar kullanırız ve göreli bağlantılar GitHub’daki kaynakta çözümlendiğinden, bağlantılarda `~/` kullanımını önermeyiz. Ancak bağımlı bir depodaki dosyalara bağlantı verdiğimizde, yolu sağlamak için `~/` karakterini kullanırız. Bağımlı depolardaki dosyalar GitHub’da farklı bir konumda olduğundan, nasıl yazıldıkları fark etmeksizin bağlantılar göreli bağlantılarla doğru çözümlenmez.
- C# bilgisayar dili belirtimi ve Visual Basic bilgisayar dili belirtimi, bilgisayar dili depolarından kaynak eklenerek .NET dosyalarına eklenir. Markdown kaynakları, [csharplang](https://github.com/dotnet/csharplang) ve [vblang](https://github.com/dotnet/vblang) depolarında yönetilir.

Belirtimlere yönlendiren bağlantılar, belirtimlerin bulunduğu kaynak dizinlere işaret etmelidir. Bunlar, C# için **~/_csharplang/spec** ve VB için **~/_vblang/spec** dizinleridir. Şu örnekte görebilirsiniz:

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a>API’lere giden bağlantılar

Derleme sistemi, dahili bağlantılar kullanmaya gerek kalmadan .NET API’lerine bağlantı vermemizi sağlayan bazı uzantılara sahiptir. Şu söz dizimlerinden birini kullanın:

1. Otomatik bağlantı: `<xref:UID>` veya `<xref:UID?displayProperty=nameWithType>`

   `displayProperty` sorgu parametresi, tam nitelikli bir bağlantı metni üretir. Varsayılan olarak, bağlantı metni yalnızca üyenin veya türün adını gösterir.

2. Markdown bağlantısı: `[link text](xref:UID)`

   Görüntülenen bağlantı metnini özelleştirmek istediğinizde kullanın.

Örnekler:

- `<xref:System.String>`, [String](https://docs.microsoft.com/dotnet/api/system.string) olarak işlenir
- `<xref:System.String?displayProperty=nameWithType>`, [System.String](https://docs.microsoft.com/dotnet/api/system.string) olarak işlenir
- `[String class](xref:System.String)`, [String sınıfı](https://docs.microsoft.com/dotnet/api/system.string) olarak işlenir

Bu gösterimi kullanma hakkında daha fazla bilgi için bkz. [Çapraz başvuruyu kullanma](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).

Bazı UID’ler \`, \# veya \* özel karakterlerini içerir, bu durumda UID değerinin sırasıyla `%60`, `%23` ve `%2A` olarak kodlanmış HTML olması gerekir. Bazen parantezlerin kodlandığını görürsünüz ancak bu, zorunlu değildir.

Örnekler:

- System.Threading.Tasks.Task\`1, `System.Threading.Tasks.Task%601` olur
- System.Exception.\#ctor, `System.Exception.%23ctor` olur
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode), `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29` olur

Türlerin, üye aşırı yükleme listesinin veya belirli bir aşırı yüklenmiş üyenin UID’sini `https://xref.docs.microsoft.com/autocomplete` adresinden bulabilirsiniz. `?text=*\<type-member-name>*` sorgu satırı, UID’sini görmek istediğiniz türü veya üyeyi belirler. Örneğin `https://xref.docs.microsoft.com/autocomplete?text=string.format`, [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) aşırı yüklemelerini alır. Araç, sağlanan `text` sorgu parametresini UID’nin herhangi bir bölümünde arar. Örneğin üye adı (ToString), kısmi üye adı (ToStri), tür ve üye adı (Double.ToString) gibi bilgileri arayabilirsiniz.

UID’den sonra bir \* (veya `%2A`) eklerseniz bağlantı belirli bir API’yi değil, aşırı yükleme sayfasını gösterir. Örneğin, [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_) gibi belirli bir aşırı yükleme yerine genel bir şekilde [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) sayfasına bağlantı oluşturmak istediğinizde bunu kullanabilirsiniz. Üye aşırı yüklü olmadığında üye sayfasına bağlantı vermek için bir \* sembolünü de kullanabilirsiniz, böylece parametre listesini UID’ye eklemenize gerek kalmaz.

Belirli bir metot aşırı yüklemesine bağlantı vermek için her bir metot parametresinin tam tür adını eklemeniz gerekir. Örneğin, \<xref:System.DateTime.ToString>, parametresiz [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) metoduna bağlantı verirken \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)>, [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) metoduna bağlantı verir.

[System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1) gibi genel bir türe bağlantı vermek için \` (`%60`) karakterini ve ardından genel tür parametrelerinin sayısını kullanırsınız. Örneğin, `<xref:System.Nullable%601>`, [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) türüne bağlantı verirken `<xref:System.Func%602>` ise [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) temsilcisine bağlantı verir.

## <a name="code"></a>Kod

Kod eklemenin en iyi yolu, çalışan bir örnekten kod parçacığı eklemektir. [.NET’e katkıda bulunma](dotnet-contribute-process.md#contributing-to-samples) makalesindeki yönergeleri izleyerek örneğinizi oluşturun. Kod eklemenin temel kuralları, [kod](how-to-write-use-markdown.md#code-includes) hakkındaki genel rehberde yer almaktadır.

Şu söz dizimini kullanarak kod ekleyebilirsiniz:

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* `-<language>` (*isteğe bağlı* ancak *önerilen*)
  * Başvurulan kod parçacığının bilgisayar dili. Desteklenen değerlerin listesi için bkz. [Desteklenen diller](#supported-languages).

* `<name>` (*isteğe bağlı*)
  * Kod parçacığı için ad. Bu başlığın çıkış HTML’si üzerinde hiçbir etkisi yoktur ancak Markdown kaynağınızın okunabilirliğini geliştirmek için başlık kullanabilirsiniz.

* `<pathToFile>` (*zorunlu*)
  * Dosya sisteminde, başvurulacak kod parçacığı dosyasını gösteren göreli yol. .NET belgeler kümesini oluşturan farklı depolar nedeniyle bu yol karmaşık olabilir. .NET örnekleri, dotnet/samples deposundadır. Tüm kod parçacığı yolları `~/samples` ile başlar, yolun devamı ise bu deponun kökündeki kaynağın yoludur.

* `<queryoption>` (*isteğe bağlı*)
  * Kodun dosyadan nasıl alınacağını belirtmek için kullanılır:
    * `#`:  `#{tagname}` (etiket adı) *veya* `#L{startlinenumber}-L{endlinenumber}` (satır aralığı).
    Bozulması kolay olduğu için satır numarası kullanımını önermiyoruz. Etiket adı, kod parçacıklarına başvurmak için tercih edilen yoldur. Anlamlı etiket adları kullanın. (Pek çok kod parçacığı önceki platformdan geçirilmiştir ve etiketlerin `Snippet1` ve `Snippet2` gibi adları vardır. Bunu devam ettirmek daha zordur.)
    * `range`: `?range=1,3-5` Satır aralığı. Bu örnek 1, 3, 4 ve 5. satırları ekler.

Mümkünse etiket adı seçeneğinin kullanılmasını öneririz. Etiket adı, kaynak kodunda bulunan ve `Snippettagname` biçimindeki bir bölge adı veya kod açıklamasıdır. Aşağıdaki örnek, `BasicThrow` etiket adına nasıl başvurulacağını göstermektedir:

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

**dotnet/samples** deposundaki kaynağın göreli yolu, `~/samples` yolunu izler.

Kod parçacığı etiketlerinin yapısını [bu kaynak dosyada](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs) görebilirsiniz. Dile göre kod parçacığı kaynak dosyalarındaki etiket adı gösterimi hakkında ayrıntılı bilgi için, [DocFX yönergelerine](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file) bakın.

Aşağıdaki örnek, üç .NET dilinde de ekli olan kodu göstermektedir:

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

Tam programlardan kod parçacığı eklendiğinde, tüm kodların Sürekli Tümleştirme (CI) sistemimizde çalışması sağlanır. Ancak derleme zamanı veya çalışma zamanı hatalarına sebep olan bir durum göstermek istiyorsanız satır içi kod bloklarını kullanabilirsiniz.

## <a name="images"></a>Görüntüler

### <a name="static-image-or-animated-gif"></a>Statik görüntü veya animasyonlu GIF

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a>Bağlantı verilen görüntü

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a>Videolar

Şu anda hem Channel 9 hem de YouTube videolarını şu söz dizimi ile ekleyebilirsiniz:

### <a name="channel-9"></a>Channel 9

```markdown
> [!VIDEO <channel9_video_link>]
```

Videoya ait doğru URL’yi almak için video çerçevesindeki **Ekle** sekmesini seçin ve `<iframe>` öğesinden URL’yi kopyalayın. Örneğin:

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a>YouTube

Videoya ait doğru URL’yi almak için videoya sağ tıklayın, **Ekleme Kodunu Kopyala**’ya tıklayın ve `<iframe>` öğesinden URL’yi kopyalayın.

```markdown
> [!VIDEO <youtube_video_link>]
```

Örneğin:

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a>docs.microsoft uzantıları

docs.microsoft, GitHub Flavored Markdown’a birkaç ek uzantı sağlar.

### <a name="checked-lists"></a>İşaretli listeler

Listeler için özel bir stil kullanılabilir. Listeleri yeşil onay işaretleriyle işleyebilirsiniz.

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

Bu, şu şekilde işlenir:

> [!div class="checklist"]
> * .NET Core uygulaması oluşturma
> * Microsoft.XmlSerializer.Generator paketine başvuru ekleme
> * Bağımlılık eklemek için MyApp.csproj dosyanızı düzenleme
> * Sınıf ve XmlSerializer ekleme
> * Uygulamayı derleme ve çalıştırma

[.NET Core belgelerinde](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator), işaretli maddelerin nasıl kullanıldığının örneklerini bulabilirsiniz.

### <a name="buttons"></a>Düğmeler

Düğme bağlantıları:

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

Bu, şu şekilde işlenir:

> [!div class="button"]
> [düğme bağlantıları](dotnet-contribute.md)

[Visual Studio belgelerinde](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio), düğmelerin nasıl kullanıldığının örneklerini bulabilirsiniz.

### <a name="step-by-steps"></a>Adım adım açıklamalar

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

[C# Kılavuzunda](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure), adım adım açıklamaların nasıl kullanıldığının örneklerini bulabilirsiniz.
