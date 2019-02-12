---
title: Belgelerde bağlantı oluşturma
description: Bu makale, docs.microsoft.com’daki içeriklerde bağlantı oluşturma konusunda rehber sağlar.
author: gewarren
ms.author: gewarren
ms.date: 10/31/2018
ms.openlocfilehash: 9dc1b6dc2ac19b8f28a5a137817245f9a8c34eaf
ms.sourcegitcommit: fbdd61ae4fb3761aec072732eefcbf2c2dca8011
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55887264"
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="ec7bd-103">Belgelerde bağlantı kullanma</span><span class="sxs-lookup"><span data-stu-id="ec7bd-103">Using links in documentation</span></span>
<span data-ttu-id="ec7bd-104">Bu makale, docs.microsoft.com’da barınan sayfalardaki bağlantıların nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="ec7bd-105">Bağlantılar, çeşitli birkaç kural ile birlikte Markdown’a eklemesi kolay öğelerdir.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="ec7bd-106">Bağlantılar kullanıcıları aynı sayfadaki içeriğe, komşu sayfalardaki içeriğe veya harici site ve URL’lere götürebilir.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-106">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="ec7bd-107">docs.microsoft.com sitesi arka ucu, [Markdig](https://github.com/lunet-io/markdig) ile ayrıştırılan [CommonMark](https://commonmark.org/) uyumlu markdown’ı destekleyen Open Publishing Services (OPS) kullanır ve aynı zamanda [DocFX Flavored Markdown’ı (DFM)](https://dotnet.github.io/docfx/) destekler.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through [Markdig](https://github.com/lunet-io/markdig) and also supports [DocFX Flavored Markdown (DFM)](https://dotnet.github.io/docfx/).</span></span> <span data-ttu-id="ec7bd-108">Çoğu belge GitHub’da depolanıp burada düzenlenebildiği için bu markdown özellikleri çoğunlukla [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-108">These markdown flavors are mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="ec7bd-109">Markdown uzantıları ile ilave işlevler eklenir.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec7bd-110">Hedef desteklediğinde (büyük bir bölümü destekler), tüm bağlantılar güvenli olmalıdır (`https` veya `http`).</span><span class="sxs-lookup"><span data-stu-id="ec7bd-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="ec7bd-111">Bağlantı metni</span><span class="sxs-lookup"><span data-stu-id="ec7bd-111">Link text</span></span>

<span data-ttu-id="ec7bd-112">Bağlantı metnine eklediğiniz kelimeler kolay olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="ec7bd-113">Diğer bir deyişle, bunlar normal Türkçe kelimeler veya bağlantı kurduğunuz sayfanın başlığı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec7bd-114">"Buraya tıklayın" ifadesini kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-114">Do not use "click here."</span></span> <span data-ttu-id="ec7bd-115">Bu, arama alt yapısı iyileştirmesi açısından kötüdür ve hedefi yeterli derecede açıklamaz.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-115">It's bad for search engine optimization, and doesn't adequately describe the target.</span></span>

<span data-ttu-id="ec7bd-116">**Doğru:**</span><span class="sxs-lookup"><span data-stu-id="ec7bd-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="ec7bd-117">**Yanlış:**</span><span class="sxs-lookup"><span data-stu-id="ec7bd-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="ec7bd-118">Bir makaleden diğerine bağlantı</span><span class="sxs-lookup"><span data-stu-id="ec7bd-118">Links from one article to another</span></span>

<span data-ttu-id="ec7bd-119">Bir Docs teknik makalesinden aynı belge kümesinde bulunan bir diğer makaleye satır içi bağlantı oluşturmak için aşağıdaki bağlantı söz dizimini kullanın:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-119">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="ec7bd-120">Bir dizindeki makaleden aynı dizindeki başka makaleye bağlantı oluşturma:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-120">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="ec7bd-121">Kök dizinde bir alt dizinden bir makaleye bağlantı oluşturma:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-121">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="ec7bd-122">Kök dizindeki bir makaleden bir alt dizindeki makaleye bağlantı oluşturma:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-122">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="ec7bd-123">Bir alt dizindeki bir makaleden başka alt dizindeki makaleye bağlantı oluşturma:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-123">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="ec7bd-124">Belge kümeleri arası (aynı depoda olsa bile) bağlantı veren bir makale:  `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="ec7bd-124">An article linking across docsets (even if in the same repository):  `[link text](./directory/article-name)`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec7bd-125">Yukarıdaki örneklerin hiçbiri `~/` öğesini bağlantının bir bölümü olarak kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-125">None of the above examples use the `~/` as part of the link.</span></span> <span data-ttu-id="ec7bd-126">Deponun kökündeki bir yola bağlanıyorsanız `/` ile başlayın.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-126">If you are linking to a path at the root of the repository, start with the `/`.</span></span> <span data-ttu-id="ec7bd-127">`~/` dahil olmak üzere GitHub'daki kaynak depolarında gezinirken geçersiz bağlantılar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-127">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="ec7bd-128">Yolu `/` ile başlatmak doğru bir şekilde çözer.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-128">Starting the path with `/` resolves correctly.</span></span>

## <a name="links-to-anchors"></a><span data-ttu-id="ec7bd-129">Yer işaretlerine giden bağlantılar</span><span class="sxs-lookup"><span data-stu-id="ec7bd-129">Links to anchors</span></span>

<span data-ttu-id="ec7bd-130">Yer işaretleri oluşturmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-130">You do not have to create anchors.</span></span> <span data-ttu-id="ec7bd-131">Yer işaretleri, yayımlanma anında tüm H2 bölüm başlıkları için otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-131">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="ec7bd-132">Yapmanız gereken tek şey, H2 bölümlerine bağlantı oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-132">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="ec7bd-133">Aynı makaledeki bir bölüm başlığına bağlantı verme:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-133">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="ec7bd-134">Aynı alt dizindeki başka bir makalede bulunan bir yer işaretine giden bağlantı:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-134">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="ec7bd-135">Başka bir hizmet alt dizinindeki yer işaretine giden bağlantı:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-135">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="ec7bd-136">Eklemelerden bağlantılar</span><span class="sxs-lookup"><span data-stu-id="ec7bd-136">Links from includes</span></span>

<span data-ttu-id="ec7bd-137">Ekleme dosyaları başka bir dizinde bulunduğu için daha uzun göreli yollar kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-137">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="ec7bd-138">Bir ekleme dosyasından bir makaleye bağlantı vermek için şu biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-138">To link to an article from an include file, use this format:</span></span>

   ```markdown
   [link text](../articles/folder/article-name.md)
   ```

## <a name="links-in-selectors"></a><span data-ttu-id="ec7bd-139">Seçicilerde bağlantılar</span><span class="sxs-lookup"><span data-stu-id="ec7bd-139">Links in selectors</span></span>

<span data-ttu-id="ec7bd-140">Seçici, bir belgeler makalesinde açılan liste olarak görüntülenen bir gezinti bileşenidir.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-140">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="ec7bd-141">Okuyucu, açılan listeden bir değer seçtiğinde tarayıcı, seçili makaleyi açar.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-141">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="ec7bd-142">Seçiciler genellikle bir makaleyle yakından ilgisi olan, aynı konunun birden fazla bilgisayar dilinde ele alındığı veya ilgili bir dizi başka makale gibi diğer makalelere yönlendiren bağlantıları içerir.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-142">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span> 

<span data-ttu-id="ec7bd-143">Bir ekleme işlemine eklenmiş seçicileriniz varsa aşağıdaki bağlantı yapısını kullanın:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-143">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->
   ```

## <a name="reference-style-links"></a><span data-ttu-id="ec7bd-144">Başvuru stili bağlantıları</span><span class="sxs-lookup"><span data-stu-id="ec7bd-144">Reference-style links</span></span>

<span data-ttu-id="ec7bd-145">İçeriğinizin daha kolay okunması için başvuru stili bağlantıları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-145">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="ec7bd-146">Başvuru stili bağlantıları; satır içi bağlantı söz dizimini, uzun URL’leri makale sonuna taşımanıza izin veren basitleştirilmiş söz dizimi ile değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-146">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="ec7bd-147">Aşağıda [Daring Fireball](https://daringfireball.net/projects/markdown/) örneği verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-147">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="ec7bd-148">Satır içi metin:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-148">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="ec7bd-149">Makale sonunda başvuru bağlantıları:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-149">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```
   
<span data-ttu-id="ec7bd-150">Bağlantıdan önce, iki nokta üst üste işaretinin sonuna boşluk koymayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-150">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="ec7bd-151">Bu boşluğu unutursanız makale yayımlandığında diğer teknik makalelere verdiğiniz bağlantı bozuk olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-151">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="ec7bd-152">Teknik belgeler kümesine ait olmayan sayfaların bağlantıları</span><span class="sxs-lookup"><span data-stu-id="ec7bd-152">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="ec7bd-153">Başka bir tür Microsoft sayfasına (fiyatlandırma sayfası, SLA sayfası gibi belge makalesi olmayan herhangi bir şey) bağlantı vermek için bir mutlak URL kullanın, ancak yerel ayarı çıkarın.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-153">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="ec7bd-154">Burada amaç, bağlantıların GitHub’da ve işlenmiş sitede çalışmasını sağlamaktır:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-154">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```
   
## <a name="links-to-third-party-sites"></a><span data-ttu-id="ec7bd-155">Üçüncü taraf sitelerin bağlantıları</span><span class="sxs-lookup"><span data-stu-id="ec7bd-155">Links to third-party sites</span></span>

<span data-ttu-id="ec7bd-156">En iyi kullanıcı deneyimi, kullanıcıları başka sitelere göndermekten olabildiğince uzak durarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-156">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="ec7bd-157">Ancak bazen bunu yapmamız gerekir, bu durumda üçüncü taraf sitelere giden bağlantıları şu bilgiler temelinde oluşturun:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-157">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="ec7bd-158">**Sorumluluk**: Paylaşmak istediğiniz bilgi üçüncü tarafa aitse, üçüncü taraf içeriğine yönlendiren bir bağlantı verin.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-158">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="ec7bd-159">Örneğin, Android geliştirici araçlarını kullanmayı anlatmak Microsoft’un işi değildir, bu görev Google’a düşer.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-159">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="ec7bd-160">Gerekirse Android geliştirici araçlarının Azure *ile birlikte* nasıl kullanılacağını anlatabiliriz ancak kendi araçlarının kullanımı açıklamak yine Google’ın işidir.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-160">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="ec7bd-161">**PM oturum kapatma**: Microsoft’un üçüncü taraf içerikte oturum kapatmasını isteyin.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-161">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="ec7bd-162">Bağlantı vererek, bağlantı verdiğimiz siteye güvendiğimizi ve insanlar bu yönergeleri izlediğinde üzerimize düşen yükümlülüğün farkında olduğumuzu belirtmiş oluruz.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-162">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="ec7bd-163">**Güncellik gözden geçirmeleri**: Üçüncü taraf bilgilerinin hala geçerli, doğru, alakalı olduğundan ve bağlantının değişmediğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-163">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="ec7bd-164">**Site dışı**: Kullanıcıların başka bir siteye gittiklerini fark etmelerini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-164">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="ec7bd-165">Bağlam bunu açıklamıyorsa belirleyici bir ifade ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-165">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="ec7bd-166">Örneğin: “Önkoşullar arasında Android Geliştirici Araçları vardır. Bunları Android Studio sitesinden indirebilirsiniz.”</span><span class="sxs-lookup"><span data-stu-id="ec7bd-166">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="ec7bd-167">**Sonraki adımlar**: “Sonraki adımlar” bölümünde, örneğin bir MVP bloguna bağlantı verilebilir.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-167">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="ec7bd-168">Yalnızca kullanıcıların siteden ayrıldıklarını fark etmelerini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-168">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="ec7bd-169">**Yasal**: Her ms.com sayfasının alt bilgisinde bulunan **Kullanım Koşulları**’nda, **Üçüncü Taraf Site Bağlantıları**’na yasal olarak bağlıyız.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-169">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="ec7bd-170">MSDN veya TechNet bağlantıları</span><span class="sxs-lookup"><span data-stu-id="ec7bd-170">Links to MSDN or TechNet</span></span>

<span data-ttu-id="ec7bd-171">MSDN veya TechNet’e bağlantı vermeniz gerektiğinde, konunun tam bağlantısını alın ve “tr-tr” dil yerel ayarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-171">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="ec7bd-172">Azure PowerShell başvuru içeriklerinin bağlantıları</span><span class="sxs-lookup"><span data-stu-id="ec7bd-172">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="ec7bd-173">Kasım 2016 tarihinden beri Azure PowerShell başvuru içeriği pek çok değişiklik yaşamıştır.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-173">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="ec7bd-174">docs.microsoft.com’daki diğer makalelerden bu içeriğe bağlantı vermek için aşağıdaki kılavuzu izleyin.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-174">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="ec7bd-175">URL yapısı:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-175">Structure of the URL:</span></span>

* <span data-ttu-id="ec7bd-176">cmdletler için:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-176">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="ec7bd-177">Kavramsal konular için:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-177">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="ec7bd-178">`<moniker-name>` kısmı isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-178">The `<moniker-name>` portion is optional.</span></span> <span data-ttu-id="ec7bd-179">Çıkarılırsa içeriğin son sürümüne yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-179">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="ec7bd-180">`<service-name>` kısmı, aşağıdaki temel URL’lerde gösterilen örneklerden biridir:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-180">The `<service-name>` portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="ec7bd-181">Azure PowerShell (AzureRM) içeriği: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="ec7bd-181">Azure PowerShell (AzureRM) content: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span></span>
- <span data-ttu-id="ec7bd-182">Azure PowerShell (ASM) içeriği: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span><span class="sxs-lookup"><span data-stu-id="ec7bd-182">Azure PowerShell (ASM) content: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span></span>
- <span data-ttu-id="ec7bd-183">Azure Active Directory (AzureAD) PowerShell içeriği: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span><span class="sxs-lookup"><span data-stu-id="ec7bd-183">Azure Active Directory (AzureAD) PowerShell content: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span></span>
- <span data-ttu-id="ec7bd-184">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span><span class="sxs-lookup"><span data-stu-id="ec7bd-184">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span></span>
- <span data-ttu-id="ec7bd-185">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span><span class="sxs-lookup"><span data-stu-id="ec7bd-185">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span></span>
- <span data-ttu-id="ec7bd-186">Azure Elastik Veritabanı İşleri PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span><span class="sxs-lookup"><span data-stu-id="ec7bd-186">Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span></span>

<span data-ttu-id="ec7bd-187">Bu URL’leri kullandığınızda, içeriğin son sürümüne yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-187">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="ec7bd-188">Böylece sürüm bilinen adını belirtmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-188">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="ec7bd-189">Ayrıca, sürüm değiştiğinde güncelleştirilmesi gereken kavramsal içeriğe bağlantı vermezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-189">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="ec7bd-190">Doğru bağlantıyı oluşturmak için bağlantı vermek istediğiniz sayfayı tarayıcınızda açın ve URL’yi kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-190">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="ec7bd-191">Ardından `https://docs.microsoft.com` kısmını ve yerel ayar bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-191">Then, remove  `https://docs.microsoft.com` and the locale info.</span></span>

<span data-ttu-id="ec7bd-192">Bir İçindekiler Tablosu’ndan bağlantı verirken, yerel ayar bilgisini çıkararak tam URL’yi kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-192">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="ec7bd-193">Örnek markdown:</span><span class="sxs-lookup"><span data-stu-id="ec7bd-193">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
