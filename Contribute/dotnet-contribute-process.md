---
title: .NET belge depolarına katkıda bulunma süreci
description: Bu makale, .NET belge depolarına katkıda bulunma sürecini kısaca tanıtır. Kullanılan depoları, içerik düzenleme sürecini ve kod örnekleri ile diğer varlıkları yönetme ilkelerini öğrenirsiniz.
ms.date: 11/07/2018
ms.openlocfilehash: b83a3080f1abd4df8caaa9d10859760006216e86
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609774"
---
# <a name="process-for-contributing-to-net-docs"></a>.NET belgelerine katkıda bulunma süreci

Belgelere yapılan topluluk katkıları için minnettarız. Aşağıdaki listede .NET belgelerine katkıda bulunurken göz önünde bulundurmanız gereken bazı rehber kurallar gösterilmiştir:

- **YAPMAYIN**: Büyük çekme istekleriyle bizi şaşırtmayın. Uzun vakitler harcamadan önce, izlemeniz gereken yol hakkında bir anlaşmaya varabilmemiz için karşılaştığınız sorunu bildirin ve bir tartışma başlatın.
- **YAPIN**: Buradaki talimatları ve [üslup ve ton](dotnet-voice-tone.md) yönergelerini izleyin.
- **YAPIN**: Çalışmanızın başlangıç noktası olarak [şablon](dotnet-style-guide.md) dosyayı kullanın.
- **YAPIN**: Makaleler üzerinde çalışmaya başlamadan önce çatalınızda ayrı bir dal oluşturun.
- **YAPIN**: [GitHub Flow iş akışını](https://guides.github.com/introduction/flow/) takip edin.
- **YAPIN**: Katkılarınız hakkında sık sık blog gönderisi yazın, tweet atın veya herhangi bir şekilde haber verin.

Bu yönergeleri izleyerek hem kendiniz hem de bizim için daha iyi bir deneyim sağlarsınız.

## <a name="make-a-contribution-to-net-docs"></a>.NET belgelerine katkıda bulunma

**1. Adım:** Küçük değişikliklerde bu adımı atlayın. Yeni içerik yazmak veya mevcut bir içeriği kapsamlı şekilde düzenlemek istiyorsanız yapmak istediğinizi açıklayan bir [sorun](https://github.com/dotnet/docs/issues) açın.

**Belgeler** klasöründeki içerik, İçindekiler’de (TOC) belirtilen bölümlere ayrılır. İçeriğin bu tablonun neresinde yer alacağını belirtin. Teklifiniz hakkında geri bildirim alın.

-veya-

Topluluğun katkıda bulunabileceği mevcut sorunlardan birini de seçebilirsiniz. [.NET Topluluğuna katkıda bulunanlar için projeler](https://github.com/dotnet/docs/projects/35) bölümünde topluluk katkılarına yönelik pek çok konu verilmiştir. İlgi alanınıza ve ayırmak istediğiniz zamana göre şu sorun kategorileri arasından seçim yapabilirsiniz:

- **Bakım**. Bu kategori; bozuk veya hatalı bağlantıları düzeltmek, eksik kod örneklerini eklemek veya sınırlı içerik sorunlarıyla ilgilenmek gibi oldukça basit katkıları içerir. Bazı durumlarda bu sorunlar, çok sayıda dosyayı ilgilendirebilir. Bu durumda, başlamadan önce bize ne üzerinde çalışmak istediğinizi bildirmelisiniz. Bir soruna yorum ekleyerek bunun üzerinde çalıştığınızı belirtin.

- **İçerik güncelleştirmeleri**. Belge kümesi oldukça büyük olduğundan içerikler kolaylıkla güncelliğini kaybedebiliyor ve düzenlemeler gerekebiliyor. Ayrıca çeşitli nedenlerle bazı içerikler iki ve hatta üç kere eklenmiş olabiliyor. İçeriğin güncelleştirilmesi, ayrı ayrı konuların güncel tutulmasını sağlamayı veya tekrarı önlemek ve tüm benzersiz içeriğin daha küçük belge kümelerinde saklanmak için bir özellik alanındaki içeriğin düzenlenmesini içerir.

- **Yeni içerik yazma**. Kendi seçtiğiniz bir konu hakkında makale yazmak istiyorsanız bu sorunlar arasında, belge kümemize eklemek istediğimiz konuları bulabilirsiniz. Ancak bir konu üzerinde çalışmaya başlamadan önce bize haber verin. Burada belirtilmemiş bir konuda makale yazmak istiyorsanız bir sorun açın.

Dilerseniz [açık sorunlar](https://github.com/dotnet/docs/issues) listemize bakıp ilginizi çeken konular üzerinde çalışmak üzere gönüllü olabilirsiniz. Topluluk katkısı için belirlenmiş sorunlar için [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) etiketini kullanıyoruz. Bunlar genelde olabildiğince az bağlam gerektirir ve ilk sorunlar için uygundur. Topluluğumuzdaki deneyimli katkıda bulunanlara, ilgilerini çekebilecek sorunlara bakmalarını öneririz. İlgilenmek istediğiniz bir sorun bulursanız sorunun açık olup olmadığını sormak için bir yorum ekleyin.

Üzerinde çalışacak bir görev seçtikten sonra bir GitHub hesabı oluşturmak ve ortamınızı ayarlamak için [başlarken](get-started-setup-github.md) kılavuzunu takip edin.

**2. Adım:** İhtiyaca göre `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs` veya `dotnet/ml-api-docs` depolarının çatalını oluşturun ve değişiklikleriniz için bir dal oluşturun.

Küçük değişiklikler için katkıda bulunan kılavuzunun [giriş sayfasındaki](index.md#quick-edits-to-existing-documents) GitHub’ı düzenleme yönergelerine bakın.

**3. Adım:** Değişiklikleri bu yeni dalda yapın.

Yeni bir konu üzerine yazıyorsanız başlangıç noktası olarak bu [şablon dosyayı](dotnet-style-guide.md) kullanabilirsiniz. Dosya, yazma yönergelerini içerir ve her bir makale için gerekli olan yazar bilgisi gibi meta verileri açıklar.

1. adımda makaleniz için belirlenen TOC konumuna karşılık gelen klasöre gidin. Bu klasör, bu bölümdeki tüm makalelerin Markdown dosyalarını barındırır. Gerekiyorsa içeriğinize ait dosyaları koyacağınız yeni bir klasör oluşturun. Bu bölümün ana makalesinin adı *index.md*’dir. Görüntüler ve diğer statik kaynaklar için makalenizin bulunduğu klasör içerisinde **medya** adlı bir alt klasör yoksa yenisini oluşturun. **Medya** klasöründe makale adını taşıyan bir alt klasör oluşturun (dizin dosyası hariç). Örnek kod, `dotnet/samples`örnekler[ bölümünde açıklandığı gibi ](#contributing-to-samples) deposunda olmalıdır.

Doğru Markdown söz dizimini izlediğinize emin olun. Yaygın kullanılan söz dizimleri için [şablon ve Markdown başvuru sayfasına](dotnet-style-guide.md) bakın.

## <a name="example-structure"></a>Örnek yapı

    docs
      /about
      /core
        /porting
          porting-overview.md
          /media
            /porting-overview
                portability_report.png

**4. Adım:** Kendi dalınızdan ana dala bir Çekme İsteği (PR) gönderin.

> [!IMPORTANT]
> [Yorum otomasyonu](how-to-write-workflows-major.md#review-and-sign-off) işlevi, şu anda .NET belge depolarının hiçbirinde kullanılamamaktadır. .NET belgeleri ekibinin üyeleri, PR’nizi gözden geçirip birleştirecektir.

Her bir PR, yalnızca bir sorunu ele almalıdır. PR, bir veya birden fazla dosyayı değiştirebilir. Farklı dosyalardaki birden fazla düzeltmeyle ilgileniyorsanız, ayrı PR’ler göndermeniz tercih edilir. Hem örnek oluşturuyor hem de Markdown güncelleştiriyorsanız örnekler için ayrı bir PR oluşturmanız gerekecektir.

PR’niz mevcut bir sorunu düzeltiyorsa işleme iletisine veya PR açıklamasına `Fixes #Issue_Number` anahtar sözcüğünü ekleyin. Böylece PR birleştirildiğinde sorun otomatik olarak kapatılır. Daha fazla bilgi için bkz. [İşleme iletisi yoluyla sorunları kapatma](https://help.github.com/articles/closing-issues-via-commit-messages/).

.NET ekibi, PR’nizi inceleyecek ve PR’nin onaylanması için yapılması gereken başka güncelleştirme/değişiklik olup olmadığını size bildirecektir.

**5. Adım:** Ekiple konuşulduğu şekilde gerekli güncelleştirmeleri dalınıza uygulayın.

Geri bildirim uygulandığında ve değişikliğiniz onaylandığında bakımcılar, PR’nizi ana dalla birleştirecektir.

Tüm işlemeleri ana daldan yayımlanmış dala düzenli olarak gönderiyoruz. böylece katkınızın yayımlanmış halini https://docs.microsoft.com/dotnet/ adresinde görebilirsiniz. Çalışma haftalarında katkıları genellikle günlük olarak yayımlıyoruz. Bakım etkinlikleri, yayımlamayı birkaç gün geciktirebilir.

## <a name="contributing-to-samples"></a>Örneklere katkıda bulunma

[dotnet/samples](https://github.com/dotnet/samples) deposu, .NET belgeleri altındaki herhangi bir konunun parçası olan tüm örnek kodları içerir. Alt klasörlere ayrılmış birkaç farklı proje vardır. Bu alt klasörler, .NET belgelerinin düzenine benzer şekilde düzenlenmiştir.

Depomuzda bulunan kodlar için şu ayrımı yaparız:

- Örnekler: Okuyucular örnekleri indirebilir ve çalıştırabilir. Örneklerin tümü, tam uygulamalar veya kitaplıklar olmalıdır. Örnek, bir kitaplık oluşturuyorsa bu kitaplık, birim testleri veya okuyucuların kodu çalıştırmasını sağlayan bir uygulama içermelidir. Okuyucular genellikle birden fazla teknoloji, özellik veya araç seti kullanır. Her bir örneğin readme.md dosyası, makaleye başvurmalıdır, böylece örneklerde geçen kavramlar hakkında daha fazla şey okuyabilirsiniz.
- Kod parçacıkları: Daha küçük bir kavramı veya görevi betimler. Bunlar derlenebilir, ancak tam uygulamalar olmaları beklenmez. Düzgün çalışabilirler, ancak tipik bir senaryo için örnek uygulama değildirler. Bunun yerine, tek bir kavramı veya özelliği gösterecek kadar küçük tasarlanmıştır. Kod parçacıkları tek kodluk bir ekrandan büyük olmamalıdır.

Tüm kodlar, [dotnet/samples](https://github.com/dotnet/samples) deposunda bulunur. Örnekler klasörünün yapısının belgeler klasörünün yapısıyla eşleştiği bir model üzerinde çalışıyoruz. İzlediğimiz standartlar şunlardır:

- Üst düzey *kod parçacıkları* klasörü, küçük ve odaklanmış örnekleri barındırır.
- API başvurusu örnekleri, şu deseni izleyen bir klasörde bulunur: *kodparçacıkları/\<dil>/api/\<adalanı>/\<apiadı>*.
- Diğer üst düzey klasörler, *belgeler* deposundaki üst düzey klasörlerle eşleşmektedir. Örneğin belgeler deposunda bir *machine-learning/tutorials* klasörü varsa makine öğrenimi öğreticileri *samples/machine-learning/tutorials* klasöründedir.

Ayrıca *temel* ve *standart* klasörlerindeki tüm örnekler, .NET Core tarafından desteklenen tüm platformlarda derlenmeli ve çalışmalıdır. CI derleme sistemimiz bunu zorunlu kılar. Üst düzey *çerçeve* klasörü, yalnızca Windows’ta derlenen ve doğrulanan örnekleri barındırır.

Herhangi bir örnek için örnek projeler, mümkün olan en geniş platformlar kümesinde derlenmeli ve çalışmalıdır. Pratikte bu, mümkünse .NET Core tabanlı konsol uygulamaları derlemek anlamına gelir. Web’e veya bir kullanıcı arabirimi çerçevesine özgü olan örneklerde bu araçlar gerektiği gibi eklenmelidir. Web uygulamaları, mobil uygulamalar, WPF veya WinForms uygulamaları gibi öğeler örnekleri oluşturur.

Tüm kodlar için bir CI sistemi oluşturmaya yönelik olarak çalışıyoruz. Örnekleri güncelleştirdiğinizde, her bir güncelleştirmenin derlenebilir bir projenin parçası olduğundan emin olun. Örneklere doğruluk testleri eklenmesi idealdir.

Oluşturduğunuz her bir tam örnekte bir *readme.md* dosyası olmalıdır. Bu dosya, örneğin kısa bir açıklamasını içermelidir (bir veya iki paragraf). *readme.md* dosyanız, okuyuculara bu örneği keşfederek ne öğreneceklerini anlatmalıdır. *readme.md* dosyası ayrıca [.NET belgeleri sitesindeki](https://docs.microsoft.com/dotnet/welcome) yayımlanmış belgeye yönlendiren bir bağlantı da içermelidir. Depodaki herhangi bir dosyanın bu siteyle eşlenip eşlenmediğini belirlemek için depo yolundaki `/docs` öğesini `http://docs.microsoft.com/dotnet` ile değiştirin.

Konunuzun içinde de örneğe yönlendiren bağlantılar olacaktır. Doğrudan örneğin GitHub’daki klasörüne bağlantı verin.

### <a name="writing-a-new-snippet-or-sample"></a>Yeni bir kod parçacığı veya örnek yazma

1. Örneğinizin **derlenebilir bir projenin parçası olması gerekir**. Mümkünse projeler, .NET Core tarafından desteklenen tüm platformlarda derlenmelidir. Platforma özgü bir özellik veya platforma özgü bir araç gösteren örnekler özel durumlardır.

2. Tutarlılığı korumak adına örneğiniz, [corefx kodlama stiline](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md) uygun olmalıdır.

    - Ayrıca, yeni bir nesne örneği oluşturmaya gerek olmayan bir şeyi gösterirken örnek metotların yerine `static` metotlarının kullanılmasını tercih ediyoruz.

3. Örneğinizde **uygun özel durum işlemeleri** olmalıdır. Örneğiniz, örnek bağlamında oluşabilecek tüm özel durumları işleyebilmelidir. Örneğin, kullanıcı girişini almak için [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) yöntemine çağrı yapan bir örnek, giriş dizesi bir metoda bağımsız değişken olarak geçirildiğinde uygun özel durum işlemesini kullanmalıdır. Benzer şekilde, örneğiniz bir metot çağrısının başarısız olmasını bekliyorsa sonuçta ortaya çıkan özel durum işlenmelidir. Her zaman, [Exception](https://docs.microsoft.com/dotnet/api/system.exception) veya [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception) gibi temel sınıf özel durumlar yerine metot tarafından oluşturulan belirli özel durumları işleyin.

4. Örneğiniz tek başına bir paket derliyorsa örneğiniz tarafından kullanılan çalışma zamanlarına ek olarak, CI derleme sistemimiz tarafından kullanılan çalışma zamanlarını eklemeniz gerekir:
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

Yakın zamanda bu projeleri derlemek için bir CI sistemimiz olacak.

Örnek oluşturmak için:

1. [Sorun](https://github.com/dotnet/docs/issues) bildirin veya mevcut bir soruna üzerine çalıştığınıza dair bir yorum ekleyin.
2. Örneğinizde gösterilen kavramları açıklayan konuyu yazın (örneğin: `docs/standard/linq/where-clause.md`).
3. Örneğinizi yazın (örneğin: `WhereClause-Sample1.cs`).
4. Örneklerinize çağrı yapan bir Ana giriş noktası içeren bir Program.cs oluşturun. Bu zaten varsa çağrıyı örneğinize ekleyin:
    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```
Tüm .NET Core kod parçacıklarını .NET Core CLI kullanarak derlersiniz. Bunu, [.NET Core SDK’sı](https://www.microsoft.com/net/download) ile yükleyebilirsiniz. Örneğinizi derlemek ve çalıştırmak için:

1. Örnek klasörüne ve derlemesine giderek hataları denetleyin:

    ```console
    dotnet build
    ```
2. Örneğinizi çalıştırın:

    ```console
    dotnet run
    ```

3. Örneğinizin kök dizinine bir readme.md dosyası ekleyin. 

   Bu dosya, kodun kısa açıklamasını içermeli ve kişileri örneğe başvuran makaleye yönlendirmelidir.

Aksi belirtilmediği durumlarda tüm örnekler, .NET Core tarafından desteklenen herhangi bir platformda komut satırından derlenir. Visual Studio’ya özgü olan ve Visual Studio 2017 veya üzerini gerektiren bazı örnekler vardır. Ayrıca bazı örnekler, platforma özgü özellikler gösterir ve belirli bir platform gerektirir. Diğer örnekler ve kod parçacıkları .NET Framework gerektirir ve Windows platformlarında çalışır. Bunlar hedef Framework sürümü için Geliştirici Paketi’ni gerektirir.

## <a name="the-c-interactive-experience"></a>Etkileşimli C# deneyimi

Bir makaleye eklenen tüm örnekler, kaynak dili belirtmek adına bir [bilgisayar dili etiketi](how-to-write-use-markdown.md#code-snippets) kullanır. C# dilindeki kısa kod örnekleri, tarayıcıda çalışan bir C# örneğini belirtmek için `csharp-interactive` bilgisayar dili etiketini kullanabilir. (Satır içi kod örnekleri `csharp-interactive` etiketini kullanır, kaynaktan eklenen kod parçacıkları için `code-csharp-interactive` etiketini kullanın.) Bu kod örnekleri, makalede bir kod penceresi ve çıkış penceresi gösterir. Çıkış penceresi, örnek kullanıcı tarafından çalıştırdığında etkileşimli kodun yürütülmesinden ortaya çıkan çıkışları gösterir.

Etkileşimli C# deneyimi, örneklerle çalışma şeklimizi değiştirir. Ziyaretçiler, sonuçları görmek için örneği çalıştırabilirler. Örneğin veya örneğe karşılık gelen metnin çıkış bilgilerini içerip içermeyeceğini belirlemeye yardım eden birkaç etken vardır.

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a>Örnek çalıştırılmadan beklenen çıkışın gösterileceği durumlar

- Yeni başlayanlara yönelik makaleler, okuyucunun kendi sonuçlarıyla beklenen yanıtı kıyaslayabilmesi için çıkış sağlamalıdır.
- Çıkışın konu için önemli olduğu örneklerde bu çıkış gösterilmelidir. Örneğin, biçimlendirilmiş metinle ilgili makalelerde örnek çalıştırılmadan metin biçimi gösterilmelidir.
- Hem örnek hem de beklenen çıkış kısa olduğunda çıkışı göstermek göz önünde bulundurulabilir. Bu, bir miktar zaman tasarrufu sağlar.
- Geçerli kültür veya sabit kültürün çıkışı nasıl etkilediğini açıklayan makalelerde beklenen çıkış açıklanmalıdır. Etkileşimli REPL (Oku Değerlendir Yazdır Döngüsü), Linux tabanlı bir ana bilgisayarda çalışır. Varsayılan kültür ve sabit kültür, farklı işletim sistemlerinde ve makinelerde farklı sonuçlar üretir. Bu makalede Windows, Linux ve Mac sistemlerindeki çıkış açıklanmıştır.

### <a name="when-to-exclude-expected-output-from-the-sample"></a>Beklenen çıkışın örneğe eklenmeyeceği durumlar

- Örneğin büyük bir çıkış oluşturduğu makalelerde bu çıkış, açıklamalarda olmamalıdır. Bu, örnek çalıştırıldığında kodu anlaşılmaz hale getirir.
- Örneğin bir konuyu gösterdiği ancak çıkışın konu için önemli olmadığı makalelerde. Örneğin, sorgu söz dizimini açıklamak için bir LINQ sorgusu çalıştıran ve daha sonra tüm öğeleri çıkış koleksiyonunda görüntüleyen kodlar.

> [!NOTE]
> Konulardan bazılarının şu anda burada belirtilen yönergelere uymadığını fark edebilirsiniz. Site genelinde tutarlılığı sağlamak adına çalışıyoruz. Bu amaçla izlediğimiz [açık sorunlar](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) listesine göz atın.

## <a name="contributor-license-agreement"></a>Katkıda bulunan lisans sözleşmesi

PR’niz birleştirilmeden önce [.NET Foundation Katılım Lisans Sözleşmesi’ni (CLA)](https://cla.dotnetfoundation.org) imzalamanız gerekir. Bu, .NET Foundation projeleri için tek seferlik bir gereksinimdir. [Katılım Lisans Sözleşmeleri (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) hakkında Wikipedia’dan daha fazla bilgi edinebilirsiniz.

Sözleşme: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

Sözleşmeyi önceden imzalamanız gerekmez. PR’nizin kopyalama, gönderme, çatalını oluşturma işlemlerini her zamanki gibi yapabilirsiniz. PR’niz oluşturulduğunda, bir CLA botu tarafından sınıflandırılır. Değişiklik büyük değilse (örneğin bir yazım hatasını düzelttiyseniz) PR `cla-not-required` olarak etiketlenir. Büyük değişikliklerde ise `cla-required` olarak sınıflandırılır. CLA’yı imzaladıktan sonra geçerli ve gelecek tüm çekme istekleri `cla-signed` olarak etiketlenir.
