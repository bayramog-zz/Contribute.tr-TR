---
title: Belgelerde bağlantı oluşturma
description: Bu makale, docs.microsoft.com’daki içeriklerde bağlantı oluşturma konusunda rehber sağlar.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/29/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1699e57ac6a4dc4c5a1ef099ea183b3cbc6307cd
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/26/2018
---
# <a name="using-links-in-documentation"></a>Belgelerde bağlantı kullanma
Bu makale, docs.microsoft.com’da barınan sayfalardaki bağlantıların nasıl kullanılacağını açıklar. Bağlantılar, çeşitli birkaç kural ile birlikte Markdown’a eklemesi kolay öğelerdir. Bağlantılar kullanıcıları aynı sayfadaki içeriğe, komşu sayfalardaki içeriğe veya harici site ve URL’lere götürebilir.

docs.microsoft.com site arka ucu, DocFX Flavored Markdown (DFM) uygulayan Açık Yayımlama Hizmetleri’ni (OPS) kullanır. DFM, GitHub Flavored Markdown (GFM) ile yüksek uyumluluk sağlar ve Markdown uzantıları yoluyla ek işlevsellik sağlar.

> [!IMPORTANT]
> Hedef desteklediğinde (büyük bir bölümü destekler), tüm bağlantılar güvenli olmalıdır (`https` veya `http`).

## <a name="link-text"></a>Bağlantı metni

Bağlantı metnine eklediğiniz kelimeler kolay olmalıdır. Diğer bir deyişle, bunlar normal Türkçe kelimeler veya bağlantı kurduğunuz sayfanın başlığı olmalıdır.

> [!IMPORTANT]
> "Buraya tıklayın" ifadesini kullanmayın. Bu, SEO açısından kötüdür ve hedefi yeterli derecede açıklamaz.

**Doğru:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

**Yanlış:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Bir makaleden diğerine bağlantı

Bir Docs teknik makalesinden aynı belge kümesinde bulunan bir diğer makaleye satır içi bağlantı oluşturmak için aşağıdaki bağlantı söz dizimini kullanın:

- Bir dizindeki makaleden aynı dizindeki başka makaleye bağlantı oluşturma:

  `[link text](article-name.md)`

- Kök dizinde bir alt dizinden bir makaleye bağlantı oluşturma:

  `[link text](../article-name.md)`

- Kök dizindeki bir makaleden bir alt dizindeki makaleye bağlantı oluşturma:

  `[link text](./directory/article-name.md)`

- Bir alt dizindeki bir makaleden başka alt dizindeki makaleye bağlantı oluşturma:

  `[link text](../directory/article-name.md)`

- Belge kümeleri arası (aynı depoda olsa bile) bağlantı veren bir makale: `[link text](./directory/article-name)`
  
## <a name="links-to-anchors"></a>Yer işaretlerine giden bağlantılar

Yer işaretleri oluşturmanız gerekmez. Yer işaretleri, yayımlanma anında tüm H2 bölüm başlıkları için otomatik olarak oluşturulur. Yapmanız gereken tek şey, H2 bölümlerine bağlantı oluşturmaktır.

- Aynı makaledeki bir bölüm başlığına bağlantı verme:

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- Aynı alt dizindeki başka bir makalede bulunan bir yer işaretine giden bağlantı:

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- Başka bir hizmet alt dizinindeki yer işaretine giden bağlantı:

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a>Eklemelerden bağlantılar

Ekleme dosyaları başka bir dizinde bulunduğu için daha uzun göreli yollar kullanmanız gerekir. Bir ekleme dosyasından bir makaleye bağlantı vermek için şu biçimi kullanın:

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a>Seçicilerde bağlantılar

Bir ekleme işlemine katıştırılmış seçicileriniz varsa (Azure belgeleri takımının olduğu gibi), aşağıdaki bağlantı yapısını kullanın:

    > [AZURE.SEÇİCİ-LİSTESİ(Açılan menü1 | Açılan menü2 )]
    - [(Metin1 | Örnek1)](../articles/folder/article-name1.md)
    - [(Metin1 | Örnek2 )](../articles/folder/article-name2.md)
    - [(Metin2 | Örnek3 )](../articles/folder/article-name3.md)
    - [(Metin2 | Örnek4 )](../articles/folder/article-name4.md) -->

## <a name="reference-style-links"></a>Başvuru stili bağlantıları

İçeriğinizin daha kolay okunması için başvuru stili bağlantıları kullanabilirsiniz. Başvuru stili bağlantıları; satır içi bağlantı söz dizimini, uzun URL’leri makale sonuna taşımanıza izin veren basitleştirilmiş söz dizimi ile değiştirir. Aşağıda [Daring Fireball](https://daringfireball.net/projects/markdown/) örneği verilmiştir:

Satır içi metin:

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

Makale sonunda başvuru bağlantıları:

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

Bağlantıdan önce, iki nokta üst üste işaretinin sonuna boşluk koymayı unutmayın. Bu boşluğu unutursanız makale yayımlandığında diğer teknik makalelere verdiğiniz bağlantı bozuk olacaktır.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Teknik belgeler kümesine ait olmayan sayfaların bağlantıları

Başka bir tür Microsoft sayfasına (fiyatlandırma sayfası, SLA sayfası gibi belge makalesi olmayan herhangi bir şey) bağlantı vermek için bir mutlak URL kullanın, ancak yerel ayarı çıkarın. Burada amaç, bağlantıların GitHub’da ve işlenmiş sitede çalışmasını sağlamaktır:

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a>Üçüncü taraf sitelerin bağlantıları

En iyi kullanıcı deneyimi, kullanıcıları başka sitelere göndermekten olabildiğince uzak durarak sağlanır. Ancak bazen bunu yapmamız gerekir, bu durumda üçüncü taraf sitelere giden bağlantıları şu bilgiler temelinde oluşturun:

- **Sorumluluk:** Paylaşmak istediğiniz bilgi üçüncü tarafa aitse üçüncü taraf içeriğine bağlantı verin. Örneğin, Android geliştirici araçlarını kullanmayı anlatmak Microsoft’un işi değildir, bu görev Google’a düşer. Gerekirse Android geliştirici araçlarının Azure *ile birlikte* nasıl kullanılacağını anlatabiliriz ancak kendi araçlarının kullanımı açıklamak yine Google’ın işidir.
- **PM oturum kapatma**: Microsoft’un üçüncü taraf içerikte oturum kapatmasını isteyin. Bağlantı vererek, bağlantı verdiğimiz siteye güvendiğimizi ve insanlar bu yönergeleri izlediğinde üzerimize düşen yükümlülüğün farkında olduğumuzu belirtmiş oluruz.
- **Güncellik gözden geçirmeleri:** Üçüncü taraf bilgilerinin hala geçerli, doğru, alakalı olduğundan ve bağlantının değişmediğinden emin olun.
- **Site dışı:** Kullanıcıların başka bir siteye gittiklerini fark etmelerini sağlayın. Bağlam bunu açıklamıyorsa belirleyici bir ifade ekleyin. Örneğin: “Önkoşullar arasında Android Geliştirici Araçları vardır, bunları Android Studio sitesinden indirebilirsiniz.”
- **Sonraki adımlar:** “Sonraki adımlar” bölümünde, örneğin bir MVP bloguna bağlantı verilebilir. Yalnızca kullanıcıların siteden ayrıldıklarını fark etmelerini sağlayın.
- **Yasal:** Her ms.com sayfasının alt bilgisinde bulunan **Kullanım Koşulları**’nda, **Üçüncü Taraf Site Bağlantıları**’na yasal olarak bağlıyız.

## <a name="links-to-msdn-or-technet"></a>MSDN veya TechNet bağlantıları

MSDN veya TechNet’e bağlantı vermeniz gerektiğinde, konunun tam bağlantısını alın ve “tr-tr” dil yerel ayarını kaldırın.

## <a name="links-to-azure-powershell-reference-content"></a>Azure PowerShell başvuru içeriklerinin bağlantıları

Kasım 2016 tarihinden beri Azure PowerShell başvuru içeriği pek çok değişiklik yaşamıştır. docs.microsoft.com’daki diğer makalelerden bu içeriğe bağlantı vermek için aşağıdaki kılavuzu izleyin.

URL yapısı:

* cmdletler için:
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* Kavramsal konular için:
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

&lt;moniker-name&gt; (bilinen ad) kısmı isteğe bağlıdır. Çıkarılırsa içeriğin son sürümüne yönlendirilirsiniz. &lt;service-name&gt; kısmı, aşağıdaki temel URL’lerde gösterilen örneklerden biridir:

- Azure PowerShell (AzureRM) içeriği: https://docs.microsoft.com/powershell/azure/
- Azure PowerShell (ASM) içeriği: https://docs.microsoft.com/powershell/azure/_servicemanagement_
- Azure Active Directory (AzureAD) PowerShell içeriği: https://docs.microsoft.com/powershell/azure/ _active-directory_
- Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_
- Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_
- Azure Elastik Veritabanı İşleri PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_

Bu URL’leri kullandığınızda, içeriğin son sürümüne yönlendirilirsiniz. Böylece sürüm bilinen adını belirtmeniz gerekmez. Ayrıca, sürüm değiştiğinde güncelleştirilmesi gereken kavramsal içeriğe bağlantı vermezsiniz.

Doğru bağlantıyı oluşturmak için bağlantı vermek istediğiniz sayfayı tarayıcınızda açın ve URL’yi kopyalayın.
Ardından "https://docs.microsoft.com" ve yerel ayar bilgilerini kaldırın.

Bir İçindekiler Tablosu’ndan bağlantı verirken, yerel ayar bilgisini çıkararak tam URL’yi kullanmanız gerekir.

Örnek markdown:

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```