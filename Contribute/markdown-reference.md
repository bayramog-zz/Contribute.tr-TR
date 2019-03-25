---
title: docs.microsoft.com için Markdown başvurusu
description: Markdown özelliklerini ve Microsoft Docs platformunda kullanılan söz dizimini öğrenin.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.openlocfilehash: b4ac631a4ebdf7daf00bc39be80fe2e479720392
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987894"
---
# <a name="markdown-reference"></a><span data-ttu-id="9fe54-103">Markdown Başvurusu</span><span class="sxs-lookup"><span data-stu-id="9fe54-103">Markdown Reference</span></span>

<span data-ttu-id="9fe54-104">Markdown, düz metin biçimli söz dizimine sahip hafif bir biçimlendirme dilidir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="9fe54-105">Docs platformu, Markdown için CommonMark standardını ve docs.microsoft.com’da daha zengin içerik sağlamak üzere tasarlanmış bazı Markdown uzantılarını destekler.</span><span class="sxs-lookup"><span data-stu-id="9fe54-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="9fe54-106">Bu makale, docs.microsoft.com’da Markdown kullanmaya yönelik alfabetik başvuru sağlar.</span><span class="sxs-lookup"><span data-stu-id="9fe54-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="9fe54-107">Markdown yazmak için herhangi bir metin düzenleyiciyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="9fe54-108">Hem standart Markdown söz dizimini hem de özel Docs uzantılarını eklemeyi kolaylaştıran bir düzenleyici olarak [Docs Yazma Paketi](https://aka.ms/DocsAuthoringPack) yükleyip [VS Code](https://code.visualstudio.com/) kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="9fe54-109">Docs, Markdig Markdown altyapısını kullanır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="9fe54-110">[https://babelmark.github.io/](https://babelmark.github.io/) adresine giderek Markdig’e kıyasla diğer altyapılarda Markdown’ın nasıl işlendiğini test edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="9fe54-111">Uyarılar (Not, İpucu, Önemli, Dikkat, Uyarı)</span><span class="sxs-lookup"><span data-stu-id="9fe54-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="9fe54-112">Uyarılar, docs.microsoft.com’da içeriğin önemini belirtmek adına renkler ve simgelerle işlenen blok alıntı oluşturma amaçlı bir Docs Markdown uzantısıdır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="9fe54-113">Aşağıdaki uyarı türleri desteklenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-113">The following alert types are supported:</span></span>

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

<span data-ttu-id="9fe54-114">Bu uyarılar docs.microsoft.com’da şu şekilde görünür:</span><span class="sxs-lookup"><span data-stu-id="9fe54-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="9fe54-115">Kullanıcıların hızlıca göz gezdirirken bile fark etmesi gereken bilgiler.</span><span class="sxs-lookup"><span data-stu-id="9fe54-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="9fe54-116">Kullanıcıların daha başarılı olmasına yardımcı ek bilgiler.</span><span class="sxs-lookup"><span data-stu-id="9fe54-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fe54-117">Kullanıcı başarısı için gerekli bilgiler.</span><span class="sxs-lookup"><span data-stu-id="9fe54-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="9fe54-118">Bir eylemin olası olumsuz sonuçları.</span><span class="sxs-lookup"><span data-stu-id="9fe54-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="9fe54-119">Bir eylemin kesin tehlikeli sonuçları.</span><span class="sxs-lookup"><span data-stu-id="9fe54-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="9fe54-120">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="9fe54-120">Code snippets</span></span>

<span data-ttu-id="9fe54-121">Markdown dosyalarınıza kod parçacıkları ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9fe54-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="9fe54-122">Bölüm başlıkları</span><span class="sxs-lookup"><span data-stu-id="9fe54-122">Headings</span></span>

<span data-ttu-id="9fe54-123">Docs, altı Markdown bölüm başlığı düzeyini destekler:</span><span class="sxs-lookup"><span data-stu-id="9fe54-123">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="9fe54-124">Son `#` ile bölüm başlığı metni arasında bir boşluk olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="9fe54-125">Tüm Markdown dosyalarında yalnızca ve yalnızca bir H1 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="9fe54-126">H1, dosyada YML meta veriler bloğundan sonraki ilk içerik olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="9fe54-127">H2’ler, yayımlanan dosyanın sağ tarafındaki gezinti menüsünde otomatik olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="9fe54-128">Daha düşük düzeydeki bölüm başlıkları burada görüntülenmez; kullanıcıların içeriğinizde gezinmesine yardımcı olmak için H2’leri stratejik olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="9fe54-129">`<h1>` gibi HTML bölüm başlıkları önerilmez ve bazı durumlarda derleme uyarılarına sebep olur.</span><span class="sxs-lookup"><span data-stu-id="9fe54-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="9fe54-130">[Yer işaretleri](#bookmark-links) yoluyla bir dosyadaki bağımsız bölüm başlıklarına bağlantı verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="9fe54-131">HTML</span><span class="sxs-lookup"><span data-stu-id="9fe54-131">HTML</span></span>

<span data-ttu-id="9fe54-132">Markdown satır içi HTML’yi desteklese de Docs yoluyla belge yayımlarken HTML önerilmez ve bazı değerler dışında derleme hatalarına ve uyarılarına sebep olur.</span><span class="sxs-lookup"><span data-stu-id="9fe54-132">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="9fe54-133">Görüntüler</span><span class="sxs-lookup"><span data-stu-id="9fe54-133">Images</span></span>

<span data-ttu-id="9fe54-134">Bir görüntüyü ekleme söz dizimi şu şekildedir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="9fe54-135">`alt text`, görüntünün kısa bir açıklamasını ve `<folder path>`, görüntünün göreli yolunu ifade eder.</span><span class="sxs-lookup"><span data-stu-id="9fe54-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="9fe54-136">Alternatif metin, görme engellilere yönelik ekran okuyucular için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="9fe54-137">Ayrıca görüntünün işlenememesine yol açan bir site hatası durumunda işe yarar.</span><span class="sxs-lookup"><span data-stu-id="9fe54-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="9fe54-138">Görüntüler, belge kümeniz içerisinde bir `/media` klasöründe depolanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="9fe54-139">Görüntüler için varsayılan olarak aşağıdaki dosya türleri desteklenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="9fe54-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="9fe54-140">.jpg</span></span>
- <span data-ttu-id="9fe54-141">.png</span><span class="sxs-lookup"><span data-stu-id="9fe54-141">.png</span></span>

<span data-ttu-id="9fe54-142">Diğer görüntü türlerini belge kümenizin docfx.json dosyasına kaynak olarak ekleyerek bunlar için de</span><span class="sxs-lookup"><span data-stu-id="9fe54-142">You can add support for other image types by adding them as resources to the docfx.json file</span></span><!--add link to reference when available--> <span data-ttu-id="9fe54-143">destek sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-143">for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="9fe54-144">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="9fe54-144">Links</span></span>

<span data-ttu-id="9fe54-145">Docs çoğu zaman diğer dosya ve sayfalara gitmek için standart Markdown bağlantılarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-145">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="9fe54-146">Bağlantı türleri, aşağıdaki alt bölümlerde açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-146">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="9fe54-147">VS Code için Docs Yazma Paketi, yolları bulmakla uğraşmadan göreli bağlantıları ve yer işaretlerini doğru şekilde eklemenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-147">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fe54-148">Belgelerinize eklediğiniz Microsoft site bağlantılarına tr-tr gibi yerel ayar kodlarını dahil etmeyin.</span><span class="sxs-lookup"><span data-stu-id="9fe54-148">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="9fe54-149">Sabit kodlanmış yerel ayar kodları, yerelleştirilmiş içeriğin işlenmesini önler ve bu durum, diğer yerel ayarlara sahip kullanıcılar için kötü bir müşteri deneyimi sağlamakla kalmayıp yüksek yerelleştirme maliyetlerine yol açar.</span><span class="sxs-lookup"><span data-stu-id="9fe54-149">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="9fe54-150">Bir tarayıcıdan URL kopyaladığınızda URL’de varsayılan olarak yerel ayar kodu bulunur; bağlantınızı oluştururken bu kodu el ile silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-150">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="9fe54-151">Örneğin şunu kullanın:</span><span class="sxs-lookup"><span data-stu-id="9fe54-151">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="9fe54-152">Şunu değil:</span><span class="sxs-lookup"><span data-stu-id="9fe54-152">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="9fe54-153">Aynı belge kümesindeki dosyalara giden göreli bağlantılar</span><span class="sxs-lookup"><span data-stu-id="9fe54-153">Relative links to files in the same doc set</span></span>

<span data-ttu-id="9fe54-154">Göreli yol, geçerli dosyayla ilgili bir hedef dosyaya ait yoldur.</span><span class="sxs-lookup"><span data-stu-id="9fe54-154">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="9fe54-155">Docs’ta göreli yolları kullanarak aynı belge kümesindeki başka bir dosyaya bağlantı verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-155">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="9fe54-156">Göreli yollar için söz dizimi aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-156">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="9fe54-157">`../`, hiyerarşideki bir üst düzeyi ifade eder.</span><span class="sxs-lookup"><span data-stu-id="9fe54-157">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="9fe54-158">Göreli yol, derleme esnasında .md uzantısının kaldırılması dahil olmak üzere çözümlenir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-158">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="9fe54-159">Üst klasördeki bir dosyaya bağlantı sağlamak için “../” kullanabilirsiniz ancak bu klasörün aynı belge kümesinde yer alması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-159">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="9fe54-160">Farklı bir belge kümesi klasöründeki dosyaya bağlantı vermek için “../” kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="9fe54-160">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="9fe54-161">Docs ayrıca “~” ile başlayan özel bir göreli yol biçimini de destekler (örneğin ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="9fe54-161">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="9fe54-162">Bu söz dizimi, bir belge kümesinin kök klasöründe bulunan bir dosyayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-162">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="9fe54-163">Bu tür bir yol da derleme sırasında doğrulanıp çözümlenir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-163">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fe54-164">Dosya uzantısını göreli yola dahil edin.</span><span class="sxs-lookup"><span data-stu-id="9fe54-164">Include the file extension in the relative path.</span></span> <span data-ttu-id="9fe54-165">Derleme, bu göreli yola ait hedef dosyanın varlığını doğrular.</span><span class="sxs-lookup"><span data-stu-id="9fe54-165">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="9fe54-166">Ve göreli yolda dosya uzantısı yoksa derlemenin bozuk bağlantı uyarısı raporlaması olasıdır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-166">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="9fe54-167">Örneğin şunu kullanın:</span><span class="sxs-lookup"><span data-stu-id="9fe54-167">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="9fe54-168">Şunu değil:</span><span class="sxs-lookup"><span data-stu-id="9fe54-168">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="9fe54-169">Docs’taki diğer dosyalara giden site göreli bağlantıları</span><span class="sxs-lookup"><span data-stu-id="9fe54-169">Site relative links to other files on Docs</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="9fe54-170">Dosya uzantısını (.md) dahil etmeyin.</span><span class="sxs-lookup"><span data-stu-id="9fe54-170">Do not include the file extension (.md).</span></span> <span data-ttu-id="9fe54-171">Uzantı, Azure “makaleler” belge kümesinin dışındaki Linux genel bakış dosyasına bağlantı verir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-171">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="9fe54-172">Harici sitelere giden bağlantılar</span><span class="sxs-lookup"><span data-stu-id="9fe54-172">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="9fe54-173">Başka bir Web sayfasına giden URL temelli bağlantı (https:// içermelidir).</span><span class="sxs-lookup"><span data-stu-id="9fe54-173">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="9fe54-174">Yer işareti bağlantıları</span><span class="sxs-lookup"><span data-stu-id="9fe54-174">Bookmark links</span></span>

<span data-ttu-id="9fe54-175">Aynı depodaki farklı bir dosyada bulunan bölüm başlığına giden yer işareti bağlantısı.</span><span class="sxs-lookup"><span data-stu-id="9fe54-175">Bookmark link to a heading in another file in the same repo.</span></span> <span data-ttu-id="9fe54-176">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="9fe54-176">For example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="9fe54-177">Geçerli dosyadaki bölüm başlığına giden yer işareti bağlantısı:</span><span class="sxs-lookup"><span data-stu-id="9fe54-177">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="9fe54-178">Karma işaretini `#` yazıp ardından başlık sözcüklerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9fe54-178">Use a hash mark `#` followed by the words of the heading.</span></span> <span data-ttu-id="9fe54-179">Başlık metnini bağlantı metni olarak değiştirmek için:</span><span class="sxs-lookup"><span data-stu-id="9fe54-179">To change the heading text into link text:</span></span>
- <span data-ttu-id="9fe54-180">Tamamını küçük harflerle yazın</span><span class="sxs-lookup"><span data-stu-id="9fe54-180">Use all lowercase characters</span></span>
- <span data-ttu-id="9fe54-181">Noktalama işaretlerini kaldırın</span><span class="sxs-lookup"><span data-stu-id="9fe54-181">Remove punctuation</span></span>
- <span data-ttu-id="9fe54-182">Boşluk yerine kısa çizgi kullanın</span><span class="sxs-lookup"><span data-stu-id="9fe54-182">Replace spaces with dashes</span></span>

<span data-ttu-id="9fe54-183">Örneğin, başlık adı "2.2 Güvenlik konuları" ise yer işareti bağlantısı "#22-güvenlik-konuları" olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-183">For example, if the heading name is "2.2 Security concerns", then the bookmark link text will be "#22-security-concerns".</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="9fe54-184">Açık yer işareti bağlantıları</span><span class="sxs-lookup"><span data-stu-id="9fe54-184">Explicit anchor links</span></span>

<span data-ttu-id="9fe54-185">`<a>` HTML etiketinin kullanan açık yer işareti bağlantıları, hub veya giriş sayfaları harici **gerekli değildir veya önerilmez**.</span><span class="sxs-lookup"><span data-stu-id="9fe54-185">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="9fe54-186">Yer işaretlerini yukarıdaki genel Markdown dosyalarında açıklandığı şekilde kullanın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-186">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="9fe54-187">Hub ve giriş sayfaları için yer işaretlerini aşağıdaki gibi kullanın:</span><span class="sxs-lookup"><span data-stu-id="9fe54-187">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="9fe54-188">`## <a id="AnchorText"> </a>Header text` veya `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="9fe54-188">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="9fe54-189">Açık yer işaretlerine bağlantı vermek için şu söz dizimini kullanın:</span><span class="sxs-lookup"><span data-stu-id="9fe54-189">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="9fe54-190">XREF (çapraz başvuru) bağlantıları</span><span class="sxs-lookup"><span data-stu-id="9fe54-190">XREF (cross reference) links</span></span>

<span data-ttu-id="9fe54-191">Geçerli veya farklı bir dosya kümesindeki otomatik oluşturulmuş API başvurularına bağlantı vermek için benzersiz kimlik (UID) ile XREF bağlantıları kullanın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-191">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="9fe54-192">Diğer belge kümelerindeki API başvurularına başvurmak için `xrefService` dosyasına `docfx.json` yapılandırmasını eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-192">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="9fe54-193">UID, tam nitelikli sınıf ve üye adına karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-193">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="9fe54-194">UID’den sonra bir \* eklerseniz bağlantı belirli bir API’yi değil, aşırı yükleme sayfasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-194">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="9fe54-195">Örneğin `List<T>.BinarySearch(T, IComparer<T>)` gibi bir aşırı yükleme sayfasında bağlantı vermek yerine İkili Arama Yöntemi sayfasına bağlantı vermek için `List<T>.BinarySearch*` kullanın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-195">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="9fe54-196">Şu söz dizimlerinden birini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9fe54-196">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="9fe54-197">Otomatik bağlantı: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="9fe54-197">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="9fe54-198">İsteğe bağlı `displayProperty` sorgu parametresi, tam nitelikli bir bağlantı metni üretir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-198">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="9fe54-199">Varsayılan olarak, bağlantı metni yalnızca üyenin veya türün adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-199">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="9fe54-200">Markdown bağlantısı: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="9fe54-200">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="9fe54-201">Görüntülenen bağlantı metnini özelleştirmek istediğinizde kullanın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-201">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="9fe54-202">Örnekler:</span><span class="sxs-lookup"><span data-stu-id="9fe54-202">Examples:</span></span>

- <span data-ttu-id="9fe54-203">`<xref:System.String>`, “String” olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-203">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="9fe54-204">`<xref:System.String?displayProperty=nameWithType>`, “System.String” olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-204">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="9fe54-205">`[String class](xref:System.String)`, “String class” olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-205">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="9fe54-206">Şu an için UID’leri bulmanın kolay bir yolu yoktur.</span><span class="sxs-lookup"><span data-stu-id="9fe54-206">Right now, there is no easy way to find the UIDs.</span></span> <!-- ? --><span data-ttu-id="9fe54-207">Bir API için UID’yi bulmanın en iyi yolu bağlantı oluşturmak istediğiniz API sayfasına ilişkin kaynağı görüntülemek ve ms.assetid değerini bulmaktır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-207">The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="9fe54-208">Aşırı yükleme değerleri kaynakta tek tek gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="9fe54-208">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="9fe54-209">İleride daha iyi bir sistem sunmak için çalışıyoruz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-209">We're working on having a better system in the future.</span></span>

<span data-ttu-id="9fe54-210">UID; \`, \# veya \* özel karakterlerini içerdiğinde UID değerinin sırasıyla `%60`, `%23` ve `%2A` olarak kodlanmış HTML olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-210">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="9fe54-211">Bazen parantezlerin kodlandığını görürsünüz ancak bu, zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-211">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="9fe54-212">Örnekler:</span><span class="sxs-lookup"><span data-stu-id="9fe54-212">Examples:</span></span>

- <span data-ttu-id="9fe54-213">System.Threading.Tasks.Task\`1, `System.Threading.Tasks.Task%601` olur</span><span class="sxs-lookup"><span data-stu-id="9fe54-213">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="9fe54-214">System.Exception.\#ctor, `System.Exception.%23ctor` olur</span><span class="sxs-lookup"><span data-stu-id="9fe54-214">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="9fe54-215">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode), `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29` olur</span><span class="sxs-lookup"><span data-stu-id="9fe54-215">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="9fe54-216">Listeler (Numaralandırılmış, Madde İşaretli, Denetim Listesi)</span><span class="sxs-lookup"><span data-stu-id="9fe54-216">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="9fe54-217">Numaralı liste</span><span class="sxs-lookup"><span data-stu-id="9fe54-217">Numbered list</span></span>

<span data-ttu-id="9fe54-218">Numaralandırılmış liste oluşturmak için yalnızca 1 sayısını kullanabilirsiniz, belge yayımlandığında bunlar sıralı bir liste olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-218">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="9fe54-219">Kaynak okunurluğunu artırmak için artışlı liste oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-219">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="9fe54-220">Bu listelerde (iç içe geçmiş listeler dahil) harf kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-220">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="9fe54-221">Bunlar, Docs’ta yayımlandığında düzgün işlenmez. Sayıların kullanıldığı iç içe geçmiş listeler, yayımlandığında küçük harfli listeler olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-221">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="9fe54-222">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="9fe54-222">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="9fe54-223">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-223">This renders as follows:</span></span>

1. <span data-ttu-id="9fe54-224">This is</span><span class="sxs-lookup"><span data-stu-id="9fe54-224">This is</span></span>
1. <span data-ttu-id="9fe54-225">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="9fe54-225">a parent numbered list</span></span>
   1. <span data-ttu-id="9fe54-226">and this is</span><span class="sxs-lookup"><span data-stu-id="9fe54-226">and this is</span></span>
   1. <span data-ttu-id="9fe54-227">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="9fe54-227">a nested numbered list</span></span>
1. <span data-ttu-id="9fe54-228">(fin)</span><span class="sxs-lookup"><span data-stu-id="9fe54-228">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="9fe54-229">Madde işaretli liste</span><span class="sxs-lookup"><span data-stu-id="9fe54-229">Bulleted list</span></span>

<span data-ttu-id="9fe54-230">Madde işaretli liste oluşturmak için her satırın başında `-` ve ardından boşluk kullanın:</span><span class="sxs-lookup"><span data-stu-id="9fe54-230">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="9fe54-231">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-231">This renders as follows:</span></span>

- <span data-ttu-id="9fe54-232">This is</span><span class="sxs-lookup"><span data-stu-id="9fe54-232">This is</span></span>
- <span data-ttu-id="9fe54-233">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="9fe54-233">a parent bulleted list</span></span>
  - <span data-ttu-id="9fe54-234">and this is</span><span class="sxs-lookup"><span data-stu-id="9fe54-234">and this is</span></span>
  - <span data-ttu-id="9fe54-235">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="9fe54-235">a nested bulleted list</span></span>
- <span data-ttu-id="9fe54-236">All done!</span><span class="sxs-lookup"><span data-stu-id="9fe54-236">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="9fe54-237">Denetim listesi</span><span class="sxs-lookup"><span data-stu-id="9fe54-237">Checklist</span></span>

<span data-ttu-id="9fe54-238">Denetim listeleri, (yalnızca) docs.microsoft.com’da özel bir Markdown uzantısı yoluyla kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-238">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="9fe54-239">Bu örnek, docs.microsoft.com’da şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-239">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="9fe54-240">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="9fe54-240">List item 1</span></span>
> * <span data-ttu-id="9fe54-241">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="9fe54-241">List item 2</span></span>
> * <span data-ttu-id="9fe54-242">Liste öğesi 3</span><span class="sxs-lookup"><span data-stu-id="9fe54-242">List item 3</span></span>

<span data-ttu-id="9fe54-243">Denetim listelerini bir makalenin başında veya sonunda, “Öğrenecekleriniz” veya “Öğrendikleriniz” içeriklerini özetlemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-243">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="9fe54-244">Makaleniz içerisinde denetim listelerini rastgele kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-244">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="9fe54-245">Sonraki adım eylemi</span><span class="sxs-lookup"><span data-stu-id="9fe54-245">Next step action</span></span>

<span data-ttu-id="9fe54-246">(Yalnızca) docs.microsoft.com’daki sayfalara sonraki adım eylemi düğmesi eklemek için özel bir uzantı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-246">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="9fe54-247">Söz dizimi aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-247">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="9fe54-248">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="9fe54-248">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="9fe54-249">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-249">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="9fe54-250">Learn about basic style</span><span class="sxs-lookup"><span data-stu-id="9fe54-250">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="9fe54-251">Bir sonraki adım eyleminde desteklenen tüm bağlantıları kullanabilirsiniz, buna farklı bir Web sayfasına ait Markdown bağlantısı da dahildir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-251">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="9fe54-252">Sonraki adım eylemi çoğu zaman aynı belge kümesindeki farklı bir dosyaya giden göreli bağlantıdır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-252">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="9fe54-253">Bölüm tanımı</span><span class="sxs-lookup"><span data-stu-id="9fe54-253">Section definition</span></span>

<!-- more info about this would be helpful! -->
<span data-ttu-id="9fe54-254">Bir bölümü tanımlaması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-254">You might need to define a section.</span></span> <span data-ttu-id="9fe54-255">Bu söz dizimi daha çok kod tabloları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-255">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="9fe54-256">Aşağıdaki örneğe bakın:</span><span class="sxs-lookup"><span data-stu-id="9fe54-256">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="9fe54-257">Yukarıdaki alıntı bloğu Markdown metni şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-257">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="9fe54-258">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="9fe54-258">Selectors</span></span>

<!-- could be more clear! -->
<span data-ttu-id="9fe54-259">Aynı makalede farklı sayfaları bağlamak için seçici kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-259">You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="9fe54-260">Böylelikle okuyucular, belirttiğiniz sayfalar arasında geçiş yapabilirler.</span><span class="sxs-lookup"><span data-stu-id="9fe54-260">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="9fe54-261">Bu uzantı, docs.microsoft.com ve MSDN’de farklı çalışır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-261">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="9fe54-262">Tek seçici</span><span class="sxs-lookup"><span data-stu-id="9fe54-262">Single selector</span></span>

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

<span data-ttu-id="9fe54-263">... şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-263">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Evrensel Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="9fe54-272">Çoklu seçici</span><span class="sxs-lookup"><span data-stu-id="9fe54-272">Multi-selector</span></span>

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

<span data-ttu-id="9fe54-273">... şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-273">... will be rendered like this:</span></span>

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

## <a name="tables"></a><span data-ttu-id="9fe54-284">eğlence</span><span class="sxs-lookup"><span data-stu-id="9fe54-284">Tables</span></span>

<span data-ttu-id="9fe54-285">Markdown’da bir tablo oluşturmanın en kolay yolu, kanallar ve çizgiler kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-285">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="9fe54-286">Üst bilgisi olan standart bir tablo oluşturmak için ilk satırın altına kısa çizgilerden oluşan bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="9fe54-286">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="9fe54-287">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-287">This renders as follows:</span></span>

|<span data-ttu-id="9fe54-288">This is</span><span class="sxs-lookup"><span data-stu-id="9fe54-288">This is</span></span>   |<span data-ttu-id="9fe54-289">a simple</span><span class="sxs-lookup"><span data-stu-id="9fe54-289">a simple</span></span>   |<span data-ttu-id="9fe54-290">table header</span><span class="sxs-lookup"><span data-stu-id="9fe54-290">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="9fe54-291">table</span><span class="sxs-lookup"><span data-stu-id="9fe54-291">table</span></span>     |<span data-ttu-id="9fe54-292">data</span><span class="sxs-lookup"><span data-stu-id="9fe54-292">data</span></span>       |<span data-ttu-id="9fe54-293">here</span><span class="sxs-lookup"><span data-stu-id="9fe54-293">here</span></span>        |
|<span data-ttu-id="9fe54-294">it doesn't</span><span class="sxs-lookup"><span data-stu-id="9fe54-294">it doesn't</span></span>|<span data-ttu-id="9fe54-295">actually</span><span class="sxs-lookup"><span data-stu-id="9fe54-295">actually</span></span>   |<span data-ttu-id="9fe54-296">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="9fe54-296">have to line up nicely!</span></span>||

<span data-ttu-id="9fe54-297">Üst bilgisiz bir tablo da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-297">You can also create a table without a header.</span></span> <span data-ttu-id="9fe54-298">Örneğin, çok sütunlu bir liste oluşturmak için:</span><span class="sxs-lookup"><span data-stu-id="9fe54-298">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="9fe54-299">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-299">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="9fe54-300">This</span><span class="sxs-lookup"><span data-stu-id="9fe54-300">This</span></span> | <span data-ttu-id="9fe54-301">table</span><span class="sxs-lookup"><span data-stu-id="9fe54-301">table</span></span> |
| <span data-ttu-id="9fe54-302">has no</span><span class="sxs-lookup"><span data-stu-id="9fe54-302">has no</span></span> | <span data-ttu-id="9fe54-303">header</span><span class="sxs-lookup"><span data-stu-id="9fe54-303">header</span></span> |

<span data-ttu-id="9fe54-304">İki nokta üst üste kullanarak sütunları hizalayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9fe54-304">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="9fe54-305">Şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-305">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="9fe54-306">right aligned:</span><span class="sxs-lookup"><span data-stu-id="9fe54-306">right aligned:</span></span>|
|<span data-ttu-id="9fe54-307">:left aligned</span><span class="sxs-lookup"><span data-stu-id="9fe54-307">:left aligned</span></span>     |
|<span data-ttu-id="9fe54-308">:centered        :</span><span class="sxs-lookup"><span data-stu-id="9fe54-308">:centered        :</span></span>|

> [!TIP]
> VS Code için Docs Yazma Uzantısı, temel Markdown dosyalarını eklemeyi kolaylaştırır!
>
> [Çevrimiçi tablo oluşturucu](http://www.tablesgenerator.com/markdown_tables) da kullanabilirsiniz.

### <a name="mx-tdbreakall"></a><span data-ttu-id="9fe54-311">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="9fe54-311">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Bu, yalnızca docs.microsoft.com sitesinde çalışır.

<span data-ttu-id="9fe54-313">Markdown’da tablo oluşturursanız, bu tablo sağ gezinti alanına doğru genişleyebilir ve okunmaz duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-313">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="9fe54-314">Docs işlemenin, gerektiğinde tabloyu bölmesine izin vererek bu sorunu çözebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-314">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="9fe54-315">Yalnızca tabloyu `[!div class="mx-tdBreakAll"]` özel sınıfıyla sarmalayın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-315">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="9fe54-316">Sınıf adı `mx-tdBreakAll` olan bir `div` tarafından sarmalanacak üç satırlı bir tablonun Markdown örneği aşağıdadır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-316">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="9fe54-317">Şöyle işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-317">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="9fe54-318">Ad</span><span class="sxs-lookup"><span data-stu-id="9fe54-318">Name</span></span>|<span data-ttu-id="9fe54-319">Söz Dizimi</span><span class="sxs-lookup"><span data-stu-id="9fe54-319">Syntax</span></span>|<span data-ttu-id="9fe54-320">Sessiz yükleme için gerekli mi?</span><span class="sxs-lookup"><span data-stu-id="9fe54-320">Mandatory for silent installation?</span></span>|<span data-ttu-id="9fe54-321">Açıklama</span><span class="sxs-lookup"><span data-stu-id="9fe54-321">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="9fe54-322">Sessiz</span><span class="sxs-lookup"><span data-stu-id="9fe54-322">Quiet</span></span>|<span data-ttu-id="9fe54-323">/quiet</span><span class="sxs-lookup"><span data-stu-id="9fe54-323">/quiet</span></span>|<span data-ttu-id="9fe54-324">Evet</span><span class="sxs-lookup"><span data-stu-id="9fe54-324">Yes</span></span>|<span data-ttu-id="9fe54-325">Hiçbir kullanıcı arabirimi veya komut istemi görüntülemeden yükleyiciyi çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-325">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="9fe54-326">NoRestart</span><span class="sxs-lookup"><span data-stu-id="9fe54-326">NoRestart</span></span>|<span data-ttu-id="9fe54-327">/norestart</span><span class="sxs-lookup"><span data-stu-id="9fe54-327">/norestart</span></span>|<span data-ttu-id="9fe54-328">Hayır</span><span class="sxs-lookup"><span data-stu-id="9fe54-328">No</span></span>|<span data-ttu-id="9fe54-329">Herhangi bir yeniden başlatma denemesini engeller.</span><span class="sxs-lookup"><span data-stu-id="9fe54-329">Suppresses any attempts to restart.</span></span> <span data-ttu-id="9fe54-330">Varsayılan olarak kullanıcı arabirimi, yeniden başlatmadan önce sorar.</span><span class="sxs-lookup"><span data-stu-id="9fe54-330">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="9fe54-331">Yardım</span><span class="sxs-lookup"><span data-stu-id="9fe54-331">Help</span></span>|<span data-ttu-id="9fe54-332">/help</span><span class="sxs-lookup"><span data-stu-id="9fe54-332">/help</span></span>|<span data-ttu-id="9fe54-333">Hayır</span><span class="sxs-lookup"><span data-stu-id="9fe54-333">No</span></span>|<span data-ttu-id="9fe54-334">Yardım ve hızlı başvuru sağlar.</span><span class="sxs-lookup"><span data-stu-id="9fe54-334">Provides help and quick reference.</span></span> <span data-ttu-id="9fe54-335">Tüm seçenek ve davranışların listesiyle birlikte, kurulum komutunun doğru kullanımını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-335">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="9fe54-336">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="9fe54-336">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fe54-337">Bu, yalnızca docs.microsoft.com sitesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-337">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="9fe54-338">Bazen, tablonun ikinci sütununa çok uzun sözcükler girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-338">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="9fe54-339">Bunların düzgün bir şekilde bölünmesi için daha önce gösterildiği gibi `div` sarmalayıcı söz dizimini kullanarak `mx-tdCol2BreakAll` sınıfını uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9fe54-339">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="9fe54-340">HTML Tabloları</span><span class="sxs-lookup"><span data-stu-id="9fe54-340">HTML Tables</span></span>

<span data-ttu-id="9fe54-341">Docs.microsoft.com’da HTML tabloları önerilmez.</span><span class="sxs-lookup"><span data-stu-id="9fe54-341">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="9fe54-342">Bu tablolar, Markdown’ın temel prensibine aykırı olarak kaynakta okunabilir değildir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-342">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="9fe54-343">Videolar</span><span class="sxs-lookup"><span data-stu-id="9fe54-343">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="9fe54-344">Markdown sayfalarına video ekleme</span><span class="sxs-lookup"><span data-stu-id="9fe54-344">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="9fe54-345">Docs şu anda şu üç konumda yayımlanmış videoları desteklemektedir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-345">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="9fe54-346">YouTube</span><span class="sxs-lookup"><span data-stu-id="9fe54-346">YouTube</span></span>
- <span data-ttu-id="9fe54-347">Channel 9</span><span class="sxs-lookup"><span data-stu-id="9fe54-347">Channel 9</span></span>
- <span data-ttu-id="9fe54-348">Microsoft’un kendi “One Player” sistemi</span><span class="sxs-lookup"><span data-stu-id="9fe54-348">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="9fe54-349">Aşağıdaki söz dizimiyle videoyu ekleyebilirsiniz. Docs bu videoyu işler.</span><span class="sxs-lookup"><span data-stu-id="9fe54-349">You can embed a video with the following syntax, and Docs will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="9fe54-350">Örnek:</span><span class="sxs-lookup"><span data-stu-id="9fe54-350">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="9fe54-351">...şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-351">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="9fe54-352">Yayımlanan sayfalarda da şöyle görüntülenir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-352">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="9fe54-353">CH9 video URL’si `https` ile başlayıp `/player` ile bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-353">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="9fe54-354">Aksi takdirde, yalnızca video yerine tüm sayfa eklenir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-354">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="9fe54-355">Yeni video yükleme</span><span class="sxs-lookup"><span data-stu-id="9fe54-355">Uploading new videos</span></span>

<span data-ttu-id="9fe54-356">Yeni bir video, şu süreci takip ederek karşıya yüklenmelidir:</span><span class="sxs-lookup"><span data-stu-id="9fe54-356">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="9fe54-357">IDWEB’deki **docs_video_users** grubuna katılın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-357">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="9fe54-358">[https://aka.ms/VideoUploadRequest](https://aka.ms/VideoUploadRequest) adresine gidin ve videonuzun ayrıntılarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="9fe54-358">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="9fe54-359">Şunlara ihtiyacınız olacaktır (bu öğelerden hiçbiri diğer kişilere görünür olmayacaktır):</span><span class="sxs-lookup"><span data-stu-id="9fe54-359">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="9fe54-360">Videonuz için başlık.</span><span class="sxs-lookup"><span data-stu-id="9fe54-360">A title for your video.</span></span>
    1. <span data-ttu-id="9fe54-361">Videonuzun ilgili olduğu ürünler/hizmetler listesi.</span><span class="sxs-lookup"><span data-stu-id="9fe54-361">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="9fe54-362">Videonuzun barınacağı hedef sayfa veya (sayfanız henüz yoksa) belge kümesi.</span><span class="sxs-lookup"><span data-stu-id="9fe54-362">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="9fe54-363">Videonuzun MP4 dosyasına ait bağlantı (dosyayı koyacak konumunuz yoksa geçici olarak şuraya koyabilirsiniz:   `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="9fe54-363">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="9fe54-364">MP4 dosyaları en az 720p olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9fe54-364">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="9fe54-365">Videonun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="9fe54-365">A description of the video.</span></span>
1. <span data-ttu-id="9fe54-366">Bu öğeyi gönderin (kaydedin).</span><span class="sxs-lookup"><span data-stu-id="9fe54-366">Submit (save) that item.</span></span>
1. <span data-ttu-id="9fe54-367">İki iş günü içerisinde videonuz yüklenecektir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-367">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="9fe54-368">Videoyu eklemeniz için gereken bağlantı iş öğesine eklenecektir ve bu bağlantı, *tekrar size* çözümlenecektir.</span><span class="sxs-lookup"><span data-stu-id="9fe54-368">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="9fe54-369">Video bağlantısını aldıktan sonra iş öğesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="9fe54-369">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="9fe54-370">Artık video bağlantısını gönderinize ekleyebilirsiniz. Bunun için şu söz dizimini kullanın:</span><span class="sxs-lookup"><span data-stu-id="9fe54-370">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
