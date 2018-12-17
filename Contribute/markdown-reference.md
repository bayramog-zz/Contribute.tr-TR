---
title: docs.microsoft.com için Markdown başvurusu
description: Docs platformu Markdown kılavuzu.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: 1023f3036e5c1facd0bcd4c31069e6faf3c95483
ms.sourcegitcommit: 21c9ac71e1abff946466cddf17a1ee97bc349ec5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245884"
---
# <a name="markdown-reference"></a><span data-ttu-id="d0aa0-103">Markdown Başvurusu</span><span class="sxs-lookup"><span data-stu-id="d0aa0-103">Markdown Reference</span></span>

<span data-ttu-id="d0aa0-104">Markdown, düz metin biçimli söz dizimine sahip hafif bir biçimlendirme dilidir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="d0aa0-105">Docs platformu, Markdown için CommonMark standardını ve docs.microsoft.com’da daha zengin içerik sağlamak üzere tasarlanmış bazı Markdown uzantılarını destekler.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="d0aa0-106">Bu makale, docs.microsoft.com’da Markdown kullanmaya yönelik alfabetik başvuru sağlar.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="d0aa0-107">Markdown yazmak için herhangi bir metin düzenleyiciyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="d0aa0-108">Hem standart Markdown söz dizimini hem de özel Docs uzantılarını eklemeyi kolaylaştıran bir düzenleyici olarak [Docs Yazma Paketi](https://aka.ms/DocsAuthoringPack) yükleyip [VS Code](https://code.visualstudio.com/) kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="d0aa0-109">Docs, Markdig Markdown altyapısını kullanır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="d0aa0-110">[https://babelmark.github.io/](https://babelmark.github.io/) adresine giderek Markdig’e kıyasla diğer altyapılarda Markdown’ın nasıl işlendiğini test edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="d0aa0-111">Uyarılar (Not, İpucu, Önemli, Dikkat, Uyarı)</span><span class="sxs-lookup"><span data-stu-id="d0aa0-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="d0aa0-112">Uyarılar, docs.microsoft.com’da içeriğin önemini belirtmek adına renkler ve simgelerle işlenen blok alıntı oluşturma amaçlı bir Docs Markdown uzantısıdır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="d0aa0-113">Aşağıdaki uyarı türleri desteklenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-113">The following alert types are supported:</span></span>

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

<span data-ttu-id="d0aa0-114">Bu uyarılar docs.microsoft.com’da şu şekilde görünür:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="d0aa0-115">Kullanıcıların hızlıca göz gezdirirken bile fark etmesi gereken bilgiler.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="d0aa0-116">Kullanıcıların daha başarılı olmasına yardımcı ek bilgiler.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0aa0-117">Kullanıcı başarısı için gerekli bilgiler.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="d0aa0-118">Bir eylemin olası olumsuz sonuçları.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="d0aa0-119">Bir eylemin kesin tehlikeli sonuçları.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="d0aa0-120">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="d0aa0-120">Code snippets</span></span>

<span data-ttu-id="d0aa0-121">Markdown dosyalarınıza kod parçacıkları ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="d0aa0-122">Bölüm başlıkları</span><span class="sxs-lookup"><span data-stu-id="d0aa0-122">Headings</span></span>

<span data-ttu-id="d0aa0-123">Docs, altı Markdown bölüm başlığı düzeyini destekler:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-123">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="d0aa0-124">Son `#` ile bölüm başlığı metni arasında bir boşluk olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="d0aa0-125">Tüm Markdown dosyalarında yalnızca ve yalnızca bir H1 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="d0aa0-126">H1, dosyada YML meta veriler bloğundan sonraki ilk içerik olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="d0aa0-127">H2’ler, yayımlanan dosyanın sağ tarafındaki gezinti menüsünde otomatik olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="d0aa0-128">Daha düşük düzeydeki bölüm başlıkları burada görüntülenmez; kullanıcıların içeriğinizde gezinmesine yardımcı olmak için H2’leri stratejik olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="d0aa0-129">`<h1>` gibi HTML bölüm başlıkları önerilmez ve bazı durumlarda derleme uyarılarına sebep olur.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="d0aa0-130">[Yer işaretleri](#bookmark-links) yoluyla bir dosyadaki bağımsız bölüm başlıklarına bağlantı verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="d0aa0-131">HTML</span><span class="sxs-lookup"><span data-stu-id="d0aa0-131">HTML</span></span>

<span data-ttu-id="d0aa0-132">Markdown satır içi HTML’yi desteklese de Docs yoluyla belge yayımlarken HTML önerilmez ve bazı değerler dışında derleme hatalarına ve uyarılarına sebep olur.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-132">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="d0aa0-133">Görüntüler</span><span class="sxs-lookup"><span data-stu-id="d0aa0-133">Images</span></span>

<span data-ttu-id="d0aa0-134">Bir görüntüyü ekleme söz dizimi şu şekildedir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="d0aa0-135">`alt text`, görüntünün kısa bir açıklamasını ve `<folder path>`, görüntünün göreli yolunu ifade eder.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="d0aa0-136">Alternatif metin, görme engellilere yönelik ekran okuyucular için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="d0aa0-137">Ayrıca görüntünün işlenememesine yol açan bir site hatası durumunda işe yarar.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="d0aa0-138">Görüntüler, belge kümeniz içerisinde bir `/media` klasöründe depolanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="d0aa0-139">Görüntüler için varsayılan olarak aşağıdaki dosya türleri desteklenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="d0aa0-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="d0aa0-140">.jpg</span></span>
- <span data-ttu-id="d0aa0-141">.png</span><span class="sxs-lookup"><span data-stu-id="d0aa0-141">.png</span></span>

<span data-ttu-id="d0aa0-142">Diğer görüntü türlerini belge kümenizin docfx.json dosyasına<!--add link to reference when available--> kaynak olarak ekleyerek bunlar için de destek sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="d0aa0-143">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="d0aa0-143">Links</span></span>

<span data-ttu-id="d0aa0-144">Docs çoğu zaman diğer dosya ve sayfalara gitmek için standart Markdown bağlantılarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-144">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="d0aa0-145">Bağlantı türleri, aşağıdaki alt bölümlerde açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="d0aa0-146">VS Code için Docs Yazma Paketi, yolları bulmakla uğraşmadan göreli bağlantıları ve yer işaretlerini doğru şekilde eklemenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0aa0-147">Belgelerinize eklediğiniz Microsoft site bağlantılarına tr-tr gibi yerel ayar kodlarını dahil etmeyin.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="d0aa0-148">Sabit kodlanmış yerel ayar kodları, yerelleştirilmiş içeriğin işlenmesini önler ve bu durum, diğer yerel ayarlara sahip kullanıcılar için kötü bir müşteri deneyimi sağlamakla kalmayıp yüksek yerelleştirme maliyetlerine yol açar.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="d0aa0-149">Bir tarayıcıdan URL kopyaladığınızda URL’de varsayılan olarak yerel ayar kodu bulunur; bağlantınızı oluştururken bu kodu el ile silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="d0aa0-150">Örneğin şunu kullanın:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="d0aa0-151">Şunu değil:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="d0aa0-152">Aynı belge kümesindeki dosyalara giden göreli bağlantılar</span><span class="sxs-lookup"><span data-stu-id="d0aa0-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="d0aa0-153">Göreli yol, geçerli dosyayla ilgili bir hedef dosyaya ait yoldur.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="d0aa0-154">Docs’ta göreli yolları kullanarak aynı belge kümesindeki başka bir dosyaya bağlantı verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-154">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="d0aa0-155">Göreli yollar için söz dizimi aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="d0aa0-156">`../`, hiyerarşideki bir üst düzeyi ifade eder.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="d0aa0-157">Göreli yol, derleme esnasında .md uzantısının kaldırılması dahil olmak üzere çözümlenir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="d0aa0-158">Üst klasördeki bir dosyaya bağlantı sağlamak için “../” kullanabilirsiniz ancak bu klasörün aynı belge kümesinde yer alması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="d0aa0-159">Farklı bir belge kümesi klasöründeki dosyaya bağlantı vermek için “../” kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="d0aa0-160">Docs ayrıca “~” ile başlayan özel bir göreli yol biçimini de destekler (örneğin ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="d0aa0-160">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="d0aa0-161">Bu söz dizimi, bir belge kümesinin kök klasöründe bulunan bir dosyayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="d0aa0-162">Bu tür bir yol da derleme sırasında doğrulanıp çözümlenir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0aa0-163">Dosya uzantısını göreli yola dahil edin.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="d0aa0-164">Derleme, bu göreli yola ait hedef dosyanın varlığını doğrular.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="d0aa0-165">Ve göreli yolda dosya uzantısı yoksa derlemenin bozuk bağlantı uyarısı raporlaması olasıdır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="d0aa0-166">Örneğin şunu kullanın:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="d0aa0-167">Şunu değil:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="d0aa0-168">Docs’taki diğer dosyalara giden site göreli bağlantıları</span><span class="sxs-lookup"><span data-stu-id="d0aa0-168">Site relative links to other files on Docs</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="d0aa0-169">Dosya uzantısını (.md) dahil etmeyin.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="d0aa0-170">Uzantı, Azure “makaleler” belge kümesinin dışındaki Linux genel bakış dosyasına bağlantı verir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="d0aa0-171">Harici sitelere giden bağlantılar</span><span class="sxs-lookup"><span data-stu-id="d0aa0-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="d0aa0-172">Başka bir Web sayfasına giden URL temelli bağlantı (https:// içermelidir).</span><span class="sxs-lookup"><span data-stu-id="d0aa0-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="d0aa0-173">Yer işareti bağlantıları</span><span class="sxs-lookup"><span data-stu-id="d0aa0-173">Bookmark links</span></span>

<span data-ttu-id="d0aa0-174">Aynı depodaki farklı bir dosyada bulunan bölüm başlığına giden yer işareti bağlantısı:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="d0aa0-175">Geçerli dosyadaki bölüm başlığına giden yer işareti bağlantısı:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="d0aa0-176">Bir diyez etiketi, ardından noktalama işaretleri kaldırılmış ve boşluklar yerine kısa çizgi getirilmiş bölüm başlığı adını kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="d0aa0-177">Açık yer işareti bağlantıları</span><span class="sxs-lookup"><span data-stu-id="d0aa0-177">Explicit anchor links</span></span>

<span data-ttu-id="d0aa0-178">`<a>` HTML etiketinin kullanan açık yer işareti bağlantıları, hub veya giriş sayfaları harici **gerekli değildir veya önerilmez**.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="d0aa0-179">Yer işaretlerini yukarıdaki genel Markdown dosyalarında açıklandığı şekilde kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="d0aa0-180">Hub ve giriş sayfaları için yer işaretlerini aşağıdaki gibi kullanın:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="d0aa0-181">`## <a id="AnchorText"> </a>Header text` veya `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="d0aa0-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="d0aa0-182">Açık yer işaretlerine bağlantı vermek için şu söz dizimini kullanın:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="d0aa0-183">XREF (çapraz başvuru) bağlantıları</span><span class="sxs-lookup"><span data-stu-id="d0aa0-183">XREF (cross reference) links</span></span>

<span data-ttu-id="d0aa0-184">Geçerli veya farklı bir dosya kümesindeki otomatik oluşturulmuş API başvurularına bağlantı vermek için benzersiz kimlik (UID) ile XREF bağlantıları kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="d0aa0-185">Diğer belge kümelerindeki API başvurularına başvurmak için `xrefService` dosyasına `docfx.json` yapılandırmasını eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-185">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="d0aa0-186">UID, tam nitelikli sınıf ve üye adına karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="d0aa0-187">UID’den sonra bir \* eklerseniz bağlantı belirli bir API’yi değil, aşırı yükleme sayfasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="d0aa0-188">Örneğin `List<T>.BinarySearch(T, IComparer<T>)` gibi bir aşırı yükleme sayfasında bağlantı vermek yerine İkili Arama Yöntemi sayfasına bağlantı vermek için `List<T>.BinarySearch*` kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="d0aa0-189">Şu söz dizimlerinden birini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="d0aa0-190">Otomatik bağlantı: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="d0aa0-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="d0aa0-191">İsteğe bağlı `displayProperty` sorgu parametresi, tam nitelikli bir bağlantı metni üretir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="d0aa0-192">Varsayılan olarak, bağlantı metni yalnızca üyenin veya türün adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="d0aa0-193">Markdown bağlantısı: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="d0aa0-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="d0aa0-194">Görüntülenen bağlantı metnini özelleştirmek istediğinizde kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="d0aa0-195">Örnekler:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-195">Examples:</span></span>

- <span data-ttu-id="d0aa0-196">`<xref:System.String>`, “String” olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="d0aa0-197">`<xref:System.String?displayProperty=nameWithType>`, “System.String” olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="d0aa0-198">`[String class](xref:System.String)`, “String class” olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="d0aa0-199">Şu an için UID’leri bulmanın kolay bir yolu yoktur.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="d0aa0-200"><!-- ? -->Bir API UID’sini bulmanın en iyi yolu, bağlantı oluşturmak istediğiniz API sayfasına ilişkin kaynağı görüntülemek ve ms.assetid değerini bulmaktır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="d0aa0-201">Aşırı yükleme değerleri kaynakta tek tek gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="d0aa0-202">İleride daha iyi bir sistem sunmak için çalışıyoruz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="d0aa0-203">UID; \`, \# veya \* özel karakterlerini içerdiğinde UID değerinin sırasıyla `%60`, `%23` ve `%2A` olarak kodlanmış HTML olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="d0aa0-204">Bazen parantezlerin kodlandığını görürsünüz ancak bu, zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="d0aa0-205">Örnekler:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-205">Examples:</span></span>

- <span data-ttu-id="d0aa0-206">System.Threading.Tasks.Task\`1, `System.Threading.Tasks.Task%601` olur</span><span class="sxs-lookup"><span data-stu-id="d0aa0-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="d0aa0-207">System.Exception.\#ctor, `System.Exception.%23ctor` olur</span><span class="sxs-lookup"><span data-stu-id="d0aa0-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="d0aa0-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode), `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29` olur</span><span class="sxs-lookup"><span data-stu-id="d0aa0-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="d0aa0-209">Listeler (Numaralandırılmış, Madde İşaretli, Denetim Listesi)</span><span class="sxs-lookup"><span data-stu-id="d0aa0-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="d0aa0-210">Numaralı liste</span><span class="sxs-lookup"><span data-stu-id="d0aa0-210">Numbered list</span></span>

<span data-ttu-id="d0aa0-211">Numaralandırılmış liste oluşturmak için yalnızca 1 sayısını kullanabilirsiniz, belge yayımlandığında bunlar sıralı bir liste olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="d0aa0-212">Kaynak okunurluğunu artırmak için artışlı liste oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="d0aa0-213">Bu listelerde (iç içe geçmiş listeler dahil) harf kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="d0aa0-214">Bunlar, Docs’ta yayımlandığında düzgün işlenmez. Sayıların kullanıldığı iç içe geçmiş listeler, yayımlandığında küçük harfli listeler olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-214">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="d0aa0-215">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-215">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="d0aa0-216">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-216">This renders as follows:</span></span>

1. <span data-ttu-id="d0aa0-217">This is</span><span class="sxs-lookup"><span data-stu-id="d0aa0-217">This is</span></span>
1. <span data-ttu-id="d0aa0-218">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="d0aa0-218">a parent numbered list</span></span>
   1. <span data-ttu-id="d0aa0-219">and this is</span><span class="sxs-lookup"><span data-stu-id="d0aa0-219">and this is</span></span>
   1. <span data-ttu-id="d0aa0-220">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="d0aa0-220">a nested numbered list</span></span>
1. <span data-ttu-id="d0aa0-221">(fin)</span><span class="sxs-lookup"><span data-stu-id="d0aa0-221">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="d0aa0-222">Madde işaretli liste</span><span class="sxs-lookup"><span data-stu-id="d0aa0-222">Bulleted list</span></span>

<span data-ttu-id="d0aa0-223">Madde işaretli liste oluşturmak için her satırın başında `-` ve ardından boşluk kullanın:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-223">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="d0aa0-224">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-224">This renders as follows:</span></span>

- <span data-ttu-id="d0aa0-225">This is</span><span class="sxs-lookup"><span data-stu-id="d0aa0-225">This is</span></span>
- <span data-ttu-id="d0aa0-226">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="d0aa0-226">a parent bulleted list</span></span>
  - <span data-ttu-id="d0aa0-227">and this is</span><span class="sxs-lookup"><span data-stu-id="d0aa0-227">and this is</span></span>
  - <span data-ttu-id="d0aa0-228">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="d0aa0-228">a nested bulleted list</span></span>
- <span data-ttu-id="d0aa0-229">All done!</span><span class="sxs-lookup"><span data-stu-id="d0aa0-229">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="d0aa0-230">Denetim listesi</span><span class="sxs-lookup"><span data-stu-id="d0aa0-230">Checklist</span></span>

<span data-ttu-id="d0aa0-231">Denetim listeleri, (yalnızca) docs.microsoft.com’da özel bir Markdown uzantısı yoluyla kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-231">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="d0aa0-232">Bu örnek, docs.microsoft.com’da şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-232">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="d0aa0-233">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="d0aa0-233">List item 1</span></span>
> * <span data-ttu-id="d0aa0-234">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="d0aa0-234">List item 2</span></span>
> * <span data-ttu-id="d0aa0-235">Liste öğesi 3</span><span class="sxs-lookup"><span data-stu-id="d0aa0-235">List item 3</span></span>

<span data-ttu-id="d0aa0-236">Denetim listelerini bir makalenin başında veya sonunda, “Öğrenecekleriniz” veya “Öğrendikleriniz” içeriklerini özetlemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-236">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="d0aa0-237">Makaleniz içerisinde denetim listelerini rastgele kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-237">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="d0aa0-238">Sonraki adım eylemi</span><span class="sxs-lookup"><span data-stu-id="d0aa0-238">Next step action</span></span>

<span data-ttu-id="d0aa0-239">(Yalnızca) docs.microsoft.com’daki sayfalara sonraki adım eylemi düğmesi eklemek için özel bir uzantı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-239">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="d0aa0-240">Söz dizimi aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-240">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="d0aa0-241">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-241">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="d0aa0-242">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-242">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d0aa0-243">Learn about basic style</span><span class="sxs-lookup"><span data-stu-id="d0aa0-243">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="d0aa0-244">Bir sonraki adım eyleminde desteklenen tüm bağlantıları kullanabilirsiniz, buna farklı bir Web sayfasına ait Markdown bağlantısı da dahildir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-244">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="d0aa0-245">Sonraki adım eylemi çoğu zaman aynı belge kümesindeki farklı bir dosyaya giden göreli bağlantıdır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-245">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="d0aa0-246">Bölüm tanımı</span><span class="sxs-lookup"><span data-stu-id="d0aa0-246">Section definition</span></span>

<span data-ttu-id="d0aa0-247"><!-- more info about this would be helpful! --> Bazı bölümleri tanımlamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-247"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="d0aa0-248">Bu söz dizimi daha çok kod tabloları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-248">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="d0aa0-249">Aşağıdaki örneğe bakın:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-249">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="d0aa0-250">Yukarıdaki alıntı bloğu Markdown metni şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-250">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="d0aa0-251">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="d0aa0-251">Selectors</span></span>

<span data-ttu-id="d0aa0-252"><!-- could be more clear! --> Aynı makalede farklı sayfaları bağlamak istiyorsanız seçici kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-252"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="d0aa0-253">Böylelikle okuyucular, belirttiğiniz sayfalar arasında geçiş yapabilirler.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-253">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="d0aa0-254">Bu uzantı, docs.microsoft.com ve MSDN’de farklı çalışır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-254">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="d0aa0-255">Tek seçici</span><span class="sxs-lookup"><span data-stu-id="d0aa0-255">Single selector</span></span>

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

<span data-ttu-id="d0aa0-256">... şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-256">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Evrensel Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="d0aa0-265">Çoklu seçici</span><span class="sxs-lookup"><span data-stu-id="d0aa0-265">Multi-selector</span></span>

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

<span data-ttu-id="d0aa0-266">... şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-266">... will be rendered like this:</span></span>

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

## <a name="tables"></a><span data-ttu-id="d0aa0-277">eğlence</span><span class="sxs-lookup"><span data-stu-id="d0aa0-277">Tables</span></span>

<span data-ttu-id="d0aa0-278">Markdown’da bir tablo oluşturmanın en kolay yolu, kanallar ve çizgiler kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-278">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="d0aa0-279">Üst bilgisi olan standart bir tablo oluşturmak için ilk satırın altına kısa çizgilerden oluşan bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-279">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="d0aa0-280">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-280">This renders as follows:</span></span>

|<span data-ttu-id="d0aa0-281">This is</span><span class="sxs-lookup"><span data-stu-id="d0aa0-281">This is</span></span>   |<span data-ttu-id="d0aa0-282">a simple</span><span class="sxs-lookup"><span data-stu-id="d0aa0-282">a simple</span></span>   |<span data-ttu-id="d0aa0-283">table header</span><span class="sxs-lookup"><span data-stu-id="d0aa0-283">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="d0aa0-284">table</span><span class="sxs-lookup"><span data-stu-id="d0aa0-284">table</span></span>     |<span data-ttu-id="d0aa0-285">data</span><span class="sxs-lookup"><span data-stu-id="d0aa0-285">data</span></span>       |<span data-ttu-id="d0aa0-286">here</span><span class="sxs-lookup"><span data-stu-id="d0aa0-286">here</span></span>        |
|<span data-ttu-id="d0aa0-287">it doesn't</span><span class="sxs-lookup"><span data-stu-id="d0aa0-287">it doesn't</span></span>|<span data-ttu-id="d0aa0-288">actually</span><span class="sxs-lookup"><span data-stu-id="d0aa0-288">actually</span></span>   |<span data-ttu-id="d0aa0-289">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="d0aa0-289">have to line up nicely!</span></span>||

<span data-ttu-id="d0aa0-290">Üst bilgisiz bir tablo da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-290">You can also create a table without a header.</span></span> <span data-ttu-id="d0aa0-291">Örneğin, çok sütunlu bir liste oluşturmak için:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-291">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="d0aa0-292">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-292">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="d0aa0-293">This</span><span class="sxs-lookup"><span data-stu-id="d0aa0-293">This</span></span> | <span data-ttu-id="d0aa0-294">table</span><span class="sxs-lookup"><span data-stu-id="d0aa0-294">table</span></span> |
| <span data-ttu-id="d0aa0-295">has no</span><span class="sxs-lookup"><span data-stu-id="d0aa0-295">has no</span></span> | <span data-ttu-id="d0aa0-296">header</span><span class="sxs-lookup"><span data-stu-id="d0aa0-296">header</span></span> |

<span data-ttu-id="d0aa0-297">İki nokta üst üste kullanarak sütunları hizalayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-297">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="d0aa0-298">Şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-298">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="d0aa0-299">right aligned:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-299">right aligned:</span></span>|
|<span data-ttu-id="d0aa0-300">:left aligned</span><span class="sxs-lookup"><span data-stu-id="d0aa0-300">:left aligned</span></span>     |
|<span data-ttu-id="d0aa0-301">:centered        :</span><span class="sxs-lookup"><span data-stu-id="d0aa0-301">:centered        :</span></span>|

> [!TIP]
> VS Code için Docs Yazma Uzantısı, temel Markdown dosyalarını eklemeyi kolaylaştırır!
>
> [Çevrimiçi tablo oluşturucu](http://www.tablesgenerator.com/markdown_tables) da kullanabilirsiniz.

### <a name="mx-tdbreakall"></a><span data-ttu-id="d0aa0-304">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="d0aa0-304">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Bu, yalnızca docs.microsoft.com sitesinde çalışır.

<span data-ttu-id="d0aa0-306">Markdown’da tablo oluşturursanız, bu tablo sağ gezinti alanına doğru genişleyebilir ve okunmaz duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-306">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="d0aa0-307">Docs işlemenin, gerektiğinde tabloyu bölmesine izin vererek bu sorunu çözebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-307">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="d0aa0-308">Yalnızca tabloyu `[!div class="mx-tdBreakAll"]` özel sınıfıyla sarmalayın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-308">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="d0aa0-309">Sınıf adı `mx-tdBreakAll` olan bir `div` tarafından sarmalanacak üç satırlı bir tablonun Markdown örneği aşağıdadır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-309">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="d0aa0-310">Şöyle işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-310">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="d0aa0-311">Ad</span><span class="sxs-lookup"><span data-stu-id="d0aa0-311">Name</span></span>|<span data-ttu-id="d0aa0-312">Söz Dizimi</span><span class="sxs-lookup"><span data-stu-id="d0aa0-312">Syntax</span></span>|<span data-ttu-id="d0aa0-313">Sessiz yükleme için gerekli mi?</span><span class="sxs-lookup"><span data-stu-id="d0aa0-313">Mandatory for silent installation?</span></span>|<span data-ttu-id="d0aa0-314">Açıklama</span><span class="sxs-lookup"><span data-stu-id="d0aa0-314">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="d0aa0-315">Sessiz</span><span class="sxs-lookup"><span data-stu-id="d0aa0-315">Quiet</span></span>|<span data-ttu-id="d0aa0-316">/quiet</span><span class="sxs-lookup"><span data-stu-id="d0aa0-316">/quiet</span></span>|<span data-ttu-id="d0aa0-317">Evet</span><span class="sxs-lookup"><span data-stu-id="d0aa0-317">Yes</span></span>|<span data-ttu-id="d0aa0-318">Hiçbir kullanıcı arabirimi veya komut istemi görüntülemeden yükleyiciyi çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-318">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="d0aa0-319">NoRestart</span><span class="sxs-lookup"><span data-stu-id="d0aa0-319">NoRestart</span></span>|<span data-ttu-id="d0aa0-320">/norestart</span><span class="sxs-lookup"><span data-stu-id="d0aa0-320">/norestart</span></span>|<span data-ttu-id="d0aa0-321">Hayır</span><span class="sxs-lookup"><span data-stu-id="d0aa0-321">No</span></span>|<span data-ttu-id="d0aa0-322">Herhangi bir yeniden başlatma denemesini engeller.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-322">Suppresses any attempts to restart.</span></span> <span data-ttu-id="d0aa0-323">Varsayılan olarak kullanıcı arabirimi, yeniden başlatmadan önce sorar.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-323">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="d0aa0-324">Yardım</span><span class="sxs-lookup"><span data-stu-id="d0aa0-324">Help</span></span>|<span data-ttu-id="d0aa0-325">/help</span><span class="sxs-lookup"><span data-stu-id="d0aa0-325">/help</span></span>|<span data-ttu-id="d0aa0-326">Hayır</span><span class="sxs-lookup"><span data-stu-id="d0aa0-326">No</span></span>|<span data-ttu-id="d0aa0-327">Yardım ve hızlı başvuru sağlar.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-327">Provides help and quick reference.</span></span> <span data-ttu-id="d0aa0-328">Tüm seçenek ve davranışların listesiyle birlikte, kurulum komutunun doğru kullanımını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-328">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="d0aa0-329">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="d0aa0-329">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0aa0-330">Bu, yalnızca docs.microsoft.com sitesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-330">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="d0aa0-331">Bazen, tablonun ikinci sütununa çok uzun sözcükler girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-331">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="d0aa0-332">Bunların düzgün bir şekilde bölünmesi için daha önce gösterildiği gibi `div` sarmalayıcı söz dizimini kullanarak `mx-tdCol2BreakAll` sınıfını uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-332">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="d0aa0-333">HTML Tabloları</span><span class="sxs-lookup"><span data-stu-id="d0aa0-333">HTML Tables</span></span>

<span data-ttu-id="d0aa0-334">Docs.microsoft.com’da HTML tabloları önerilmez.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-334">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="d0aa0-335">Bu tablolar, Markdown’ın temel prensibine aykırı olarak kaynakta okunabilir değildir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-335">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="d0aa0-336">Videolar</span><span class="sxs-lookup"><span data-stu-id="d0aa0-336">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="d0aa0-337">Markdown sayfalarına video ekleme</span><span class="sxs-lookup"><span data-stu-id="d0aa0-337">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="d0aa0-338">Docs şu anda şu üç konumda yayımlanmış videoları desteklemektedir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-338">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="d0aa0-339">YouTube</span><span class="sxs-lookup"><span data-stu-id="d0aa0-339">YouTube</span></span>
- <span data-ttu-id="d0aa0-340">Channel 9</span><span class="sxs-lookup"><span data-stu-id="d0aa0-340">Channel 9</span></span>
- <span data-ttu-id="d0aa0-341">Microsoft’un kendi “One Player” sistemi</span><span class="sxs-lookup"><span data-stu-id="d0aa0-341">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="d0aa0-342">Aşağıdaki söz dizimiyle videoyu ekleyebilirsiniz. Docs bu videoyu işler.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-342">You can embed a video with the following syntax, and Docs will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="d0aa0-343">Örnek:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-343">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="d0aa0-344">...şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-344">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="d0aa0-345">Yayımlanan sayfalarda da şöyle görüntülenir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-345">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="d0aa0-346">CH9 video URL’si `https` ile başlayıp `/player` ile bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-346">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="d0aa0-347">Aksi takdirde, yalnızca video yerine tüm sayfa eklenir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-347">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="d0aa0-348">Yeni video yükleme</span><span class="sxs-lookup"><span data-stu-id="d0aa0-348">Uploading new videos</span></span>

<span data-ttu-id="d0aa0-349">Yeni bir video, şu süreci takip ederek karşıya yüklenmelidir:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-349">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="d0aa0-350">IDWEB’deki **docs_video_users** grubuna katılın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-350">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="d0aa0-351">https://aka.ms/VideoUploadRequest adresine gidin ve videonuzun ayrıntılarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-351">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="d0aa0-352">Şunlara ihtiyacınız olacaktır (bu öğelerden hiçbiri diğer kişilere görünür olmayacaktır):</span><span class="sxs-lookup"><span data-stu-id="d0aa0-352">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="d0aa0-353">Videonuz için başlık.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-353">A title for your video.</span></span>
    1. <span data-ttu-id="d0aa0-354">Videonuzun ilgili olduğu ürünler/hizmetler listesi.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-354">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="d0aa0-355">Videonuzun barınacağı hedef sayfa veya (sayfanız henüz yoksa) belge kümesi.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-355">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="d0aa0-356">Videonuzun MP4 dosyasına ait bağlantı (dosyayı koyacak konumunuz yoksa geçici olarak şuraya koyabilirsiniz:   `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="d0aa0-356">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="d0aa0-357">MP4 dosyaları en az 720p olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-357">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="d0aa0-358">Videonun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-358">A description of the video.</span></span>
1. <span data-ttu-id="d0aa0-359">Bu öğeyi gönderin (kaydedin).</span><span class="sxs-lookup"><span data-stu-id="d0aa0-359">Submit (save) that item.</span></span>
1. <span data-ttu-id="d0aa0-360">İki iş günü içerisinde videonuz yüklenecektir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-360">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="d0aa0-361">Videoyu eklemeniz için gereken bağlantı iş öğesine eklenecektir ve bu bağlantı, *tekrar size* çözümlenecektir.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-361">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="d0aa0-362">Video bağlantısını aldıktan sonra iş öğesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="d0aa0-362">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="d0aa0-363">Artık video bağlantısını gönderinize ekleyebilirsiniz. Bunun için şu söz dizimini kullanın:</span><span class="sxs-lookup"><span data-stu-id="d0aa0-363">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
