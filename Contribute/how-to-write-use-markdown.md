---
title: Docs’ta makale yazmak için Markdown kullanma
description: Bu makale, docs.microsoft.com makalelerinde kullanılan Markdown dilinin temellerini ve başvuru bilgilerini sağlar.
ms.date: 07/13/2017
ms.openlocfilehash: ef75ffd59b75db5757822642f651d863906cf14c
ms.sourcegitcommit: 18c271ebec920bb976a4bc901f4ab8c1d36b02fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53615847"
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Docs’ta makale yazmak için Markdown kullanma

[Docs.microsoft.com](http://docs.microsoft.com) makaleleri, [Markdown](https://daringfireball.net/projects/markdown/) adı verilen hafif biçimlendirme dilinde yazılır. Bu dilin okunması ve öğrenilmesi kolaydır. O nedenle bu dil kısa sürede endüstri standardı haline gelmiştir.

Docs içerikleri GitHub’da depolandığı için [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) adlı bir Markdown üst kümesi kullanabilir. GFM, yaygın biçimlendirme ihtiyaçları için ilave işlevler sağlar. Ayrıca Open Publishing Services (OPS), Markdig Markdown Ayrıştırıcısı’nı uygular. Markdig, GFM ile yüksek uyumluluğa sahip olduğu için Docs’a özgü özellikleri etkinleştirmek için ek işlevsellik sağlar.

* Markdig; .NET için hızlı, güçlü, CommonMark uyumlu, genişletilebilir Markdown işlemcisidir.
* https://github.com/lunet-io/markdig
* Daha iyi topluluk desteği
* Daha iyi standartlar desteği

## <a name="markdown-basics"></a>Markdown temel bilgileri

### <a name="headings"></a>Bölüm başlıkları

Bir bölüm başlığı oluşturmak için karma işaretini (#) aşağıdaki gibi kullanırsınız:

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

Bölüm başlıkları, atx-style kullanılarak hazırlanmalıdır. Yani satırın başında, arkasından gelen kısmın bölüm başlığı olduğunu belirtmek için H1-H6 HTML başlık düzeyine karşılık gelecek şekilde 1-6 kare karakter (#) kullanın. Bir ila dördüncü düzey bölüm başlığı örnekleri yukarıda verilmiştir.

Konunuz içerisinde yalnızca bir adet birinci düzey bölüm başlığı (H1) **olmalıdır** ve bu, sayfa başlığı olarak görüntülenir.

Başlığınız `#` karakteriyle bitiyorsa başlığın doğru işlenmesi için sonuna fazladan bir `#` karakteri eklemeniz gerekir. Örneğin `# Async Programming in F# #`.

İkinci düzey bölüm başlıkları, sayfa başlığının altındaki “Bu makalede” bölümünde yer alan İçindekiler (TOC) bölümünü oluşturur.

### <a name="bold-and-italic-text"></a>Kalın ve italik metin

Bir metni **kalın** olarak biçimlendirmek için iki yıldız işareti arasına alırsınız:

```markdown
This text is **bold**.
```

Bir metni *italik* olarak biçimlendirmek için bir yıldız işareti arasına alırsınız:

```markdown
This text is *italic*.
```

Bir metni ***kalın ve italik*** olarak biçimlendirmek için üç yıldız işareti arasına alırsınız:

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a>Blok alıntılar

Blok alıntılar, `>` karakteri kullanılarak oluşturulur:

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

Yukarıdaki örnek, şu şekilde işlenir:

> Kuraklık, on milyon yıldır devam ediyordu ve korkunç kertenkelelerin egemenliği çoktan sona ermişti. Burada, Ekvator’da, günün birinde Afrika olarak anılacak bu kıtada, var olmak için verilen savaşta vahşetin yeni bir zirvesine ulaşılmıştı ve ortada henüz bir galip yoktu. Bu kıraç ve kuru topraklarda, yalnızca küçük, hızlı veya vahşi olanlar büyüyebilirdi, ya da hayatta kalmayı umut edebilirdi.

### <a name="lists"></a>Listeler

#### <a name="unordered-list"></a>Sırasız liste

Sırasız/madde işaretli bir listeyi biçimlendirmek için yıldız işaretleri veya tireler kullanabilirsiniz. Örneğin, şu Markdown:

```markdown
- List item 1
- List item 2
- List item 3
```

şu şekilde oluşturulur:

- Liste öğesi 1
- Liste öğesi 2
- Liste öğesi 3

Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın. Örneğin, şu Markdown:

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

şu şekilde oluşturulur:

- Liste öğesi 1
  - Liste öğesi A
  - Liste öğesi B
- Liste öğesi 2

#### <a name="ordered-list"></a>Sıralı liste

Sıralı/adımlı bir listeyi biçimlendirmek için sıra numaraları kullanırsınız. Örneğin, şu Markdown:

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

şu şekilde oluşturulur:

1. İlk yönerge
2. İkinci yönerge
3. Üçüncü yönerge

Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın. Örneğin, şu Markdown:

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

şu şekilde oluşturulur:

1. İlk yönerge
   1. Alt yönerge
   2. Alt yönerge
2. İkinci yönerge

Tüm girişler için “1.” kullandığımıza dikkat edin. Böylece sonraki güncelleştirmelerde yeni adımlar eklendiğinde veya mevcut adımlar çıkarıldığında, değişiklikleri gözden geçirmek kolaylaşır.

### <a name="tables"></a>eğlence

Tablolar, temel Markdown belirtiminin parçası değildir, ancak GFM tarafından desteklenir. Düz çizgi (|) ve kısa çizgi (-) karakterlerini kullanarak tablolar oluşturabilirsiniz. Kısa çizgiler sütunların üst bilgisini oluştururken düz çizgiler sütunları birbirinden ayırır. Tablonun doğru işlenebilmesi için başına boş bir satır ekleyin.

Örneğin, şu Markdown:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

şu şekilde oluşturulur:

| Tablolar                  | Şununla:                 | eğlence          |
| :------------------- | -------------------: |:---------------:|
| sola hizalanmış sütun  | sağa hizalanmış sütun | ortalanmış sütun |
| 100 $                 | 100 $                 | 100 $            |
| 10 $                  | 10 $                  | 10 $             |
| 1 $                   | 1 $                   | 1 $              |

Tablo oluşturma hakkında daha fazla bilgi için şunlara bakın:

- Geniş tabloların biçimlendirmesinde yardımcı olabilecek Markdig [tablo sarmalama özelliği](#table-wrapping).
- GitHub’ın [Tablolarla bilgi düzenleme](https://help.github.com/articles/organizing-information-with-tables/) makalesi.
- [Markdown Tablo Oluşturucu](https://www.tablesgenerator.com/markdown_tables) web uygulaması.
- [Adam Pritchard - Markdown Hızlı Başvuru Kılavuzu](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).
- [Michel Fortin - Markdown Ekstra](https://michelf.ca/projects/php-markdown/extra/#table).
- [HTML tablolarını Markdown’a dönüştürme](https://jmalarcon.github.io/markdowntables/).

### <a name="links"></a>Bağlantılar

Satır içi bağlantılarda Markdown söz dizimi, köprü bağlantısı eklenecek `[link text]` metni ve bağlantı verilen URL ya da dosya adı olan `(file-name.md)` kısımlarından oluşur:

 `[link text](file-name.md)`

Bağlantı verme hakkında daha fazla bilgi için bkz.

- Markdown’ın temel bağlantı desteği konusunda ayrıntılar için [Markdown söz dizimi kılavuzu](https://daringfireball.net/projects/markdown/syntax#link).
- Markdig tarafından sağlanan ilave bağlayıcı söz dizimi hakkında ayrıntılar için bu kılavuzun [Bağlantılar](how-to-write-links.md) bölümü.

### <a name="code-snippets"></a>Kod parçacıkları

Markdown, hem bir cümlede satır içi olarak hem de cümleler arasında ayrı “çevrelenmiş” bir blok halinde kod parçacıkları yerleştirilmesini destekler. Ayrıntılar için bkz.

- [Kod blokları için yerel Markdown desteği](https://daringfireball.net/projects/markdown/syntax#precode)
- [Kod çevreleme ve söz dizimi vurgulama için GFM desteği](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

Çevrelenmiş kod blokları, kod parçacıklarınız için söz dizimi vurgulamasını etkinleştirmenin kolay bir yoludur. Çevrelenmiş kod bloklarının biçimi genelde şöyledir:

    ```alias
    ...
    your code goes in here
    ...
    ```

İlk üç ters tırnak (`) karakterinden sonra gelen diğer ad, kullanılacak söz dizimi vurgulamasını belirtir. Docs içeriğinde yaygın olarak kullanılan programlama dilleri ve bunların etiketleri aşağıdaki gibidir:

Bu diller, kolay as desteğine ve dil vurgulamasına sahiptir.

|Ad|Markdown Etiketi|
|-----|-------|
|.NET Konsolu|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI’si|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|Tarayıcıda C#|csharp-interactive|
|Konsol|konsol|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|PowerApps (nokta ondalık ayırıcısı)|powerapps-dot|
|PowerApps (virgül ondalık ayırıcısı)|powerapps-comma|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|R|r|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|VSTS CLI|vstscli|
|XAML|xaml|
|XML|xml|

`csharp-interactive` adı, C# bilgisayar dilini ve tarayıcıdan örnek çalıştırma becerisini belirtir. Bu kod parçacıkları, bir Docker kapsayıcısında derlenir ve yürütülür. Bu program yürütüldüğünde ortaya çıkan sonuçlar kullanıcının tarayıcı penceresinde görüntülenir.

#### <a name="example-c"></a>Örnek: C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__İşleme__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a>Örnek: SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__İşleme__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a>OPS özel Markdown uzantıları

> [!NOTE]
> Open Publishing Services (OPS), GitHub Flavored Markdown (GFM) ile yüksek uyumluluğa sahip olan Markdown için Markdig Ayrıştırıcısı’nı uygular. Markdig, Markdown uzantıları aracılığıyla ilave işlevsellik sağlar. Bu nedenle, tam OPS Yazma Kılavuzundan bazı makaleler başvuru için bu kılavuza dahil edilmiştir. (Örneğin, içindekiler bölümünde "Markdig ve Markdown uzantıları" ile "Kod parçacıkları" kısımlarına bakın.)

Docs makaleleri çoğu zaman paragraflar, bağlantılar, listeler ve bölüm başlıkları gibi makale biçimlendirmeleri için GFM’yi kullanır. Makaleler, daha zengin biçimlendirme için aşağıdakiler gibi Markdig özelliklerini kullanabilir:

- Not blokları
- Dosyaları dahil et
- Seçiciler
- Ekli videolar
- Kod parçacıkları/örnekleri

Tam bir liste için içerikler bölümünde “Markdig ve Markdown uzantıları” ve “Kod parçacıkları” kısmına bakın.

### <a name="note-blocks"></a>Not blokları

İlgiyi belirli bir içeriğe çekmek için dört çeşit not blokundan birini seçebilirsiniz:

- NOT
- UYARI
- İPUCU
- ÖNEMLİ

Genel olarak not bloklarını fazla kullanmaktan kaçınmalısınız, dikkat dağıtıcı olabilir. Not bloklarında kod blokları, görüntüler, listeler ve bağlantılar destekleniyor olsa da bunları olabildiğince sade ve düz bir şekilde oluşturun.

Örnekler:

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

Bunlar aşağıdaki gibi işlenir:

> [!NOTE]
> Bu bir NOT’tur

> [!WARNING]
> Bu bir UYARI’dır

> [!TIP]
> Bu bir İPUCU’dur

> [!IMPORTANT]
> Bu ÖNEMLİ’dir

### <a name="include-files"></a>Dosyaları dahil et

Makale dosyalarına dahil edilmesi gereken yeniden kullanılabilir metin veya görüntü dosyalarınız varsa dosyayı Markdig dosya dahil etme özelliği ile “dahil etmek” için bir başvuru kullanabilirsiniz. Bu özellik, verilen dosyayı makalenize derleme sırasında “eklemesi” için OPS’yi yönlendirir, böylece dosya da yayımlanan makalenizin bir parçası olur. İçerikleri tekrar kullanmanıza imkan veren üç tür ekleme başvurusu vardır:

- Satır İçi: Genel bir metin parçacığını başka bir cümlede satır içinde yeniden kullanın.
- Blok: Makalenin bir bölümündeki bütün bir Markdown dosyasını yeniden kullanın.
- Görüntü: Docs’ta standart görüntü ekleme yoludur.

Satır içi ve blok ekleme dosyaları, basit birer Markdown (.md) dosyasıdır. Bu dosyalar, herhangi bir geçerli Markdown barındırabilir. Tüm ekleme Markdown dosyaları, depo kökünde [ortak bir `/includes` alt dizinine](git-github-fundamentals.md#includes-subdirectory) yerleştirilmelidir. Makale yayımlandığında, eklenen dosya makaleyle sorunsuz bir şekilde tümleşmiş olur.

Ekleme dosyalarına yönelik gereksinimler ve önemli konular şunlardır:

- Aynı metni birden fazla makalede kullanmanız gerektiği zaman ekleme dosyalarını kullanın.
- Bir veya iki paragraf, paylaşılan bir yordam veya paylaşılan bir bölüm gibi büyük içeriklerde blok ekleme başvurusunu kullanın. Ancak bir cümleden daha küçük şeyler için kullanmayın.
- Ekleme başvuruları, Markdig uzantılarına bağlı olduğu için makalenizin GitHub tarafından işlenmiş görünümünde işlenmez. Bunlar yalnızca yayın sonrasında oluşturulur.
- Ekleme dosyasına başvuran makalelerdeki ekleme dosyalarında bütün metnin, öncesinde veya sonrasında gelen metinden bağımsız tam cümleler veya ifadeler şeklinde olmasına dikkat edin. Bu kılavuzu dikkate almamak, makalede çevrilemeyen bir satır oluşturur ve yerelleştirme deneyimini bozar.
- Ekleme başvurularını diğer ekleme dosyalarına eklemeyin. Bu, desteklenmeyen bir durumdur.
- Medya dosyalarını ekleme alt dizinine özgü bir medya klasörüne yerleştirin, örneğin `<repo>`/eklemeler/medya klasörü. Medya dizini, kökünde hiçbir görüntü barındırmamalıdır. Ekleme dosyasında görüntü yoksa buna karşılık gelecek bir medya dizini gerekli değildir.
- Normal makalelerde olduğu gibi, ekleme dosyaları arasında medya paylaşmayın. Her bir ekleme dosyası ve makale için benzersiz ada sahip ayrı dosyalar kullanın. Medya dosyasını, ekleme dosyasıyla ilişkili medya klasöründe depolayın.
- Ekleme dosyalarını bir makaledeki tek içerik olacak şekilde kullanmayın.  Ekleme dosyaları, makaledeki diğer içerikleri tamamlayıcı niteliktedir.

Örnek:

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a>Seçiciler

Seçicileri teknik makalelerde, aynı makalenin farklı bölümlerini yazdığınızda teknolojiler veya platformlar arasındaki uygulama farklılıklarına değinirken kullanın. Bu genellikle geliştiriciler için mobil platform içeriklerimizde kullanılır. Markdig’de şu anda iki farklı türde seçici vardır; tekli seçici ve çoklu seçici.

Seçimdeki her bir makaleye aynı seçici Markdown gittiği için makalenizin seçicisini bir ekleme dosyasına koymanız önerilir. Daha sonra aynı seçiciyi kullanan tüm makalelerinizde bu ekleme dosyasına başvurabilirsiniz.

Aşağıdaki kodda bir seçici örneği gösterilmektedir:

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

[Azure belgelerinde](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic) seçicilerin nasıl kullanıldığının örneklerini bulabilirsiniz.

### <a name="code-include-references"></a>Kod ekleme başvuruları

Markdig, bir makaleye kod parçacığı uzantısı aracılığıyla gelişmiş kod eklemeyi destekler. Programlama dili seçimi ve söz dizimi renklendirme gibi GFM özellikleri üzerinde ortaya çıkan gelişmiş işleme seçenekleri sağlar, bunların yanında aşağıdaki gibi kullanışlı özellikler de getirir:

- Bir dış depodan gelen merkezi kod örnekleri/parçacıklarının eklenmesi.
- Kod örneklerinin farklı dillerdeki birçok çeşidini gösteren sekmeli kullanıcı arabirimi.

## <a name="gotchas-and-troubleshooting"></a>Tuzaklar ve sorun giderme

### <a name="alt-text"></a>Alternatif metin

Alt çizgi içeren alternatif metin düzgün bir şekilde işlenmez. Örneğin, şunu kullanmak yerine:

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Şunun gibi alt çizgilerden kaçının:

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>Kesme işareti ve tırnak işaretleri

Word dosyasından Markdown editörüne bir şey kopyalarsanız kopyaladığınız metin “akıllı” (kıvrık) kesme işaretleri veya tırnak işaretleri içerebilir. Bunların kodlanması veya kesme işareti ya da tırnak işaretlerine dönüştürülmesi gerekir. Aksi takdirde, dosya yayımlandığında şöyle karakterler görebilirsiniz: Itâ€™s

Bu noktalama işaretlerinin “akıllı” olanları için kodlamalar aşağıdaki gibidir:

- Sol (açma) tırnak işareti: `&#8220;`
- Sağ (kapatma) tırnak işareti: `&#8221;`
- Sağ (kapatma) tekli tırnak işareti veya kesme işareti: `&#8217;`
- Sağ (açma) tekli tırnak işareti (nadiren kullanılır): `&#8216;`

### <a name="angle-brackets"></a>Açılı ayraçlar

Bir yer tutucuyu ifade etmek için köşeli ayraç kullanımı yaygındır. Metinde (kodda değil) bunu yaptığınızda, köşeli ayraçları kodlamanız gerekir. Aksi takdirde Markdown bunların HTML etiketleri olması gerektiğini düşünür.

Örneğin `<script name>` öğesini `&lt;script name&gt;` şeklinde kodlayın

## <a name="see-also"></a>Ayrıca bkz.:

### <a name="markdown-resources"></a>Markdown kaynakları

- [Markdown’a Giriş](https://daringfireball.net/projects/markdown/syntax)
- [Docs Markdown kural sayfası](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [GitHub Markdown Temel Bilgileri](https://help.github.com/articles/markdown-basics/)
- [Markdown Kılavuzu](https://www.markdownguide.org/)
