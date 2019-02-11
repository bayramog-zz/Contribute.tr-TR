---
title: .NET makaleleri için şablon ve başvuru sayfası
description: Bu makale, .NET belge depoları için yeni makaleler oluştururken işinize yarayacak bir şablon içerir
ms.date: 11/07/2018
ms.openlocfilehash: e342373a09b623dc71aadd63e8d8627d154ec8b6
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55712936"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="ea476-103">.NET belgeleri için meta veriler ve Markdown şablonu</span><span class="sxs-lookup"><span data-stu-id="ea476-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="ea476-104">Bu dotnet/belgeler şablonu, Markdown söz dizimi örneklerinin yanında meta verileri ayarlama rehberi içerir.</span><span class="sxs-lookup"><span data-stu-id="ea476-104">This dotnet/docs template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>

<span data-ttu-id="ea476-105">Bir Markdown dosyası oluştururken, eklenen şablonu yeni bir dosyaya kopyalamalı, meta verileri aşağıda belirtildiği gibi doldurmalı ve H1 bölüm başlığını makalenin başlığı olarak yukarıda ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="ea476-105">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="ea476-106">Meta veriler</span><span class="sxs-lookup"><span data-stu-id="ea476-106">Metadata</span></span>

<span data-ttu-id="ea476-107">Gereken meta veri bloğu, aşağıdaki örnek meta veri bloğundadır:</span><span class="sxs-lookup"><span data-stu-id="ea476-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="ea476-108">İki nokta (:) ile meta veri öğesi arasına bir boşluk koymanız **zorunludur**.</span><span class="sxs-lookup"><span data-stu-id="ea476-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="ea476-109">Bir değerdeki (örneğin başlıktaki) iki nokta işareti, meta veri ayrıştırıcısını keser.</span><span class="sxs-lookup"><span data-stu-id="ea476-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="ea476-110">Bu durumda başlığın başına ve sonuna tırnak işareti koyun (örneğin `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="ea476-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="ea476-111">**title (başlık)**: Arama altyapısı sonuçlarında görünür.</span><span class="sxs-lookup"><span data-stu-id="ea476-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="ea476-112">Başlık, H1 başlığınızla aynı olmamalı ve en fazla 60 karakterden oluşmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ea476-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="ea476-113">**description (açıklama)**: Makalenin içeriğini özetler.</span><span class="sxs-lookup"><span data-stu-id="ea476-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="ea476-114">Genellikle arama sonuçları sayfasında görüntülenir ancak arama sıralaması için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="ea476-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="ea476-115">Açıklama uzunluğu, boşluklu 115-145 karakter olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ea476-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="ea476-116">**author (yazar)**: Yazar alanı, yazarın **GitHub kullanıcı adını** içermelidir.</span><span class="sxs-lookup"><span data-stu-id="ea476-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="ea476-117">**ms.date**: En son yapılan önemli güncelleştirmenin tarihi.</span><span class="sxs-lookup"><span data-stu-id="ea476-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="ea476-118">Tüm makaleyi gözden geçirip güncelleştirdiyseniz mevcut makalelerde bunu da güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="ea476-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="ea476-119">Yazım hataları gibi küçük düzeltmeler güncelleştirme gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="ea476-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="ea476-120">Diğer meta veriler makalelere eklenir, ancak çoğu meta veri değeri, **docfx.json** klasöründe belirtilen klasör düzeyinde uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ea476-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="ea476-121">Temel Markdown, GFM ve özel karakterler</span><span class="sxs-lookup"><span data-stu-id="ea476-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="ea476-122">Markdown, GitHub Flavored Markdown (GFM) ve OPS’ye özgü uzantılar hakkında temel bilgileri [Markdown](how-to-write-use-markdown.md) ve [Markdown başvurusu](markdown-reference.md) hakkındaki genel makalelerden edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](how-to-write-use-markdown.md) and [Markdown reference](markdown-reference.md).</span></span>

<span data-ttu-id="ea476-123">Markdown, \*, \` ve \# gibi özel karakterleri biçimlendirme için kullanır.</span><span class="sxs-lookup"><span data-stu-id="ea476-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="ea476-124">İçeriğinizde bu karakterlerden birine yer vermek isterseniz şu ikisinden birini yapmalısınız:</span><span class="sxs-lookup"><span data-stu-id="ea476-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="ea476-125">Özel karakterden önce “kaçış” karakteri kullanmak (örneğin \* elde etmek için `\*` yazmak)</span><span class="sxs-lookup"><span data-stu-id="ea476-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="ea476-126">Karakter için [HTML varlık kodunu](http://www.ascii.cl/htmlcodes.htm) kullanmak (örneğin &#42; elde etmek için `&#42;` yazmak).</span><span class="sxs-lookup"><span data-stu-id="ea476-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="ea476-127">Dosya adları</span><span class="sxs-lookup"><span data-stu-id="ea476-127">File names</span></span>

<span data-ttu-id="ea476-128">Dosya adlarında şu kuralları takip edin:</span><span class="sxs-lookup"><span data-stu-id="ea476-128">File names use the following rules:</span></span>

* <span data-ttu-id="ea476-129">Ad içerisinde yalnızca küçük harf, sayı ve kısa çizgi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea476-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="ea476-130">Boşluk veya noktalama işareti kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="ea476-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="ea476-131">Dosya adındaki sözcük ve sayıları birbirinden ayırmak için kısa çizgi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea476-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="ea476-132">Geliştir, satın al, oluştur, sorun gider gibi belirgin eylem fiillerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea476-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="ea476-133">-ing (İngilizcede) ile biten sözcük kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="ea476-133">No -ing words.</span></span>
* <span data-ttu-id="ea476-134">Kısa kelimeler kullanmayın; bir, ve, veya gibi sözcükler eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="ea476-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="ea476-135">Ad, Markdown biçiminde olmalı ve .md dosya uzantısını kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ea476-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="ea476-136">Dosya adlarını olabildiğince kısa tutun.</span><span class="sxs-lookup"><span data-stu-id="ea476-136">Keep file names reasonably short.</span></span> <span data-ttu-id="ea476-137">Adlar, makale URL’lerinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="ea476-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="ea476-138">Bölüm başlıkları</span><span class="sxs-lookup"><span data-stu-id="ea476-138">Headings</span></span>

<span data-ttu-id="ea476-139">Cümle stili büyük harf kullanımını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="ea476-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="ea476-140">Başlığın ilk harfini her zaman büyük yazın.</span><span class="sxs-lookup"><span data-stu-id="ea476-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="ea476-141">Metin stili</span><span class="sxs-lookup"><span data-stu-id="ea476-141">Text styling</span></span>

<span data-ttu-id="ea476-142">*İtalik* Dosyalar, klasörler, yollar (uzun öğeleri kendi satırlarına göre ayırın) ve yeni terimler için kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea476-142">*Italics* Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="ea476-143">**Kalın** Kullanıcı arabirimi öğeleri için kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea476-143">**Bold** Use for UI elements.</span></span>

<span data-ttu-id="ea476-144">`Code` Satır içi kod, bilgisayar dili anahtar sözcükleri, NuGet paket adları, komut satırı komutları, veritabanı tablosu ve sütun adları ile tıklanabilir olmasını istemediğiniz URL’ler için kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea476-144">`Code` Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="ea476-145">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="ea476-145">Links</span></span>

<span data-ttu-id="ea476-146">Yer işaretleri, dahili bağlantılar, diğer belgelere giden bağlantılar, kod eklemeleri ve harici bağlantılar için [Bağlantılar](how-to-write-links.md) genel makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="ea476-146">See the general article on [Links](how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="ea476-147">.NET belgeleri ekibi, şu kuralları kullanır:</span><span class="sxs-lookup"><span data-stu-id="ea476-147">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="ea476-148">Çoğu durumda göreli bağlantılar kullanırız ve göreli bağlantılar GitHub’daki kaynakta çözümlendiğinden, bağlantılarda `~/` kullanımını önermeyiz.</span><span class="sxs-lookup"><span data-stu-id="ea476-148">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="ea476-149">Ancak bağımlı bir depodaki dosyalara bağlantı verdiğimizde, yolu sağlamak için `~/` karakterini kullanırız.</span><span class="sxs-lookup"><span data-stu-id="ea476-149">However, whenever we link to a file in a dependent repo, we'll use the `~/` character to provide the path.</span></span> <span data-ttu-id="ea476-150">Bağımlı depolardaki dosyalar GitHub’da farklı bir konumda olduğundan, nasıl yazıldıkları fark etmeksizin bağlantılar göreli bağlantılarla doğru çözümlenmez.</span><span class="sxs-lookup"><span data-stu-id="ea476-150">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="ea476-151">C# bilgisayar dili belirtimi ve Visual Basic bilgisayar dili belirtimi, bilgisayar dili depolarından kaynak eklenerek .NET dosyalarına eklenir.</span><span class="sxs-lookup"><span data-stu-id="ea476-151">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="ea476-152">Markdown kaynakları, [csharplang](https://github.com/dotnet/csharplang) ve [vblang](https://github.com/dotnet/vblang) depolarında yönetilir.</span><span class="sxs-lookup"><span data-stu-id="ea476-152">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="ea476-153">Belirtimlere yönlendiren bağlantılar, belirtimlerin bulunduğu kaynak dizinlere işaret etmelidir.</span><span class="sxs-lookup"><span data-stu-id="ea476-153">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="ea476-154">Bunlar, C# için **~/_csharplang/spec** ve VB için **~/_vblang/spec** dizinleridir. Şu örnekte görebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ea476-154">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="ea476-155">API’lere giden bağlantılar</span><span class="sxs-lookup"><span data-stu-id="ea476-155">Links to APIs</span></span>

<span data-ttu-id="ea476-156">Derleme sistemi, dahili bağlantılar kullanmaya gerek kalmadan .NET API’lerine bağlantı vermemizi sağlayan bazı uzantılara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="ea476-156">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="ea476-157">Şu söz dizimlerinden birini kullanın:</span><span class="sxs-lookup"><span data-stu-id="ea476-157">You use one of the following syntax:</span></span>

1. <span data-ttu-id="ea476-158">Otomatik bağlantı: `<xref:UID>` veya `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="ea476-158">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="ea476-159">`displayProperty` sorgu parametresi, tam nitelikli bir bağlantı metni üretir.</span><span class="sxs-lookup"><span data-stu-id="ea476-159">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="ea476-160">Varsayılan olarak, bağlantı metni yalnızca üyenin veya türün adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea476-160">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="ea476-161">Markdown bağlantısı: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="ea476-161">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="ea476-162">Görüntülenen bağlantı metnini özelleştirmek istediğinizde kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea476-162">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="ea476-163">Örnekler:</span><span class="sxs-lookup"><span data-stu-id="ea476-163">Examples:</span></span>

- <span data-ttu-id="ea476-164">`<xref:System.String>`, [String](https://docs.microsoft.com/dotnet/api/system.string) olarak işlenir</span><span class="sxs-lookup"><span data-stu-id="ea476-164">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="ea476-165">`<xref:System.String?displayProperty=nameWithType>`, [System.String](https://docs.microsoft.com/dotnet/api/system.string) olarak işlenir</span><span class="sxs-lookup"><span data-stu-id="ea476-165">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="ea476-166">`[String class](xref:System.String)`, [String sınıfı](https://docs.microsoft.com/dotnet/api/system.string) olarak işlenir</span><span class="sxs-lookup"><span data-stu-id="ea476-166">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="ea476-167">Bu gösterimi kullanma hakkında daha fazla bilgi için bkz. [Çapraz başvuruyu kullanma](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span><span class="sxs-lookup"><span data-stu-id="ea476-167">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="ea476-168">Bazı UID’ler \`, \# veya \* özel karakterlerini içerir, bu durumda UID değerinin sırasıyla `%60`, `%23` ve `%2A` olarak kodlanmış HTML olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ea476-168">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="ea476-169">Bazen parantezlerin kodlandığını görürsünüz ancak bu, zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="ea476-169">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="ea476-170">Örnekler:</span><span class="sxs-lookup"><span data-stu-id="ea476-170">Examples:</span></span>

- <span data-ttu-id="ea476-171">System.Threading.Tasks.Task\`1, `System.Threading.Tasks.Task%601` olur</span><span class="sxs-lookup"><span data-stu-id="ea476-171">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="ea476-172">System.Exception.\#ctor, `System.Exception.%23ctor` olur</span><span class="sxs-lookup"><span data-stu-id="ea476-172">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="ea476-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode), `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29` olur</span><span class="sxs-lookup"><span data-stu-id="ea476-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="ea476-174">Türlerin, üye aşırı yükleme listesinin veya belirli bir aşırı yüklenmiş üyenin UID’sini `https://xref.docs.microsoft.com/autocomplete` adresinden bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-174">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="ea476-175">`?text=*\<type-member-name>*` sorgu satırı, UID’sini görmek istediğiniz türü veya üyeyi belirler.</span><span class="sxs-lookup"><span data-stu-id="ea476-175">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="ea476-176">Örneğin `https://xref.docs.microsoft.com/autocomplete?text=string.format`, [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) aşırı yüklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="ea476-176">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="ea476-177">Araç, sağlanan `text` sorgu parametresini UID’nin herhangi bir bölümünde arar.</span><span class="sxs-lookup"><span data-stu-id="ea476-177">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="ea476-178">Örneğin üye adı (ToString), kısmi üye adı (ToStri), tür ve üye adı (Double.ToString) gibi bilgileri arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-178">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="ea476-179">UID’den sonra bir \* (veya `%2A`) eklerseniz bağlantı belirli bir API’yi değil, aşırı yükleme sayfasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea476-179">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="ea476-180">Örneğin, [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_) gibi belirli bir aşırı yükleme yerine genel bir şekilde [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) sayfasına bağlantı oluşturmak istediğinizde bunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-180">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="ea476-181">Üye aşırı yüklü olmadığında üye sayfasına bağlantı vermek için bir \* sembolünü de kullanabilirsiniz, böylece parametre listesini UID’ye eklemenize gerek kalmaz.</span><span class="sxs-lookup"><span data-stu-id="ea476-181">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="ea476-182">Belirli bir metot aşırı yüklemesine bağlantı vermek için her bir metot parametresinin tam tür adını eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ea476-182">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="ea476-183">Örneğin, \<xref:System.DateTime.ToString>, parametresiz [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) metoduna bağlantı verirken \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)>, [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) metoduna bağlantı verir.</span><span class="sxs-lookup"><span data-stu-id="ea476-183">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="ea476-184">[System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1) gibi genel bir türe bağlantı vermek için \` (`%60`) karakterini ve ardından genel tür parametrelerinin sayısını kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="ea476-184">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="ea476-185">Örneğin, `<xref:System.Nullable%601>`, [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) türüne bağlantı verirken `<xref:System.Func%602>` ise [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) temsilcisine bağlantı verir.</span><span class="sxs-lookup"><span data-stu-id="ea476-185">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="ea476-186">Kod</span><span class="sxs-lookup"><span data-stu-id="ea476-186">Code</span></span>

<span data-ttu-id="ea476-187">Kod eklemenin en iyi yolu, çalışan bir örnekten kod parçacığı eklemektir.</span><span class="sxs-lookup"><span data-stu-id="ea476-187">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="ea476-188">[.NET’e katkıda bulunma](dotnet-contribute-process.md#contributing-to-samples) makalesindeki yönergeleri izleyerek örneğinizi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ea476-188">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute-process.md#contributing-to-samples) article.</span></span> <span data-ttu-id="ea476-189">Kod eklemenin temel kuralları, [kod](how-to-write-use-markdown.md#code-snippets) hakkındaki genel rehberde yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="ea476-189">The basic rules for including code are located in the general guidance on [code](how-to-write-use-markdown.md#code-snippets).</span></span>

<span data-ttu-id="ea476-190">Şu söz dizimini kullanarak kod ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ea476-190">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="ea476-191">`-<language>` (*isteğe bağlı* ancak *önerilen*)</span><span class="sxs-lookup"><span data-stu-id="ea476-191">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="ea476-192">Başvurulan kod parçacığının bilgisayar dili.</span><span class="sxs-lookup"><span data-stu-id="ea476-192">Language of the code snippet being referenced.</span></span> <span data-ttu-id="ea476-193">Desteklenen değerlerin listesi için bkz. [Desteklenen diller](#supported-languages).</span><span class="sxs-lookup"><span data-stu-id="ea476-193">For a list of supported values, see [Supported languages](#supported-languages).</span></span>

* <span data-ttu-id="ea476-194">`<name>` (*isteğe bağlı*)</span><span class="sxs-lookup"><span data-stu-id="ea476-194">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="ea476-195">Kod parçacığı için ad.</span><span class="sxs-lookup"><span data-stu-id="ea476-195">Name for the code snippet.</span></span> <span data-ttu-id="ea476-196">Bu başlığın çıkış HTML’si üzerinde hiçbir etkisi yoktur ancak Markdown kaynağınızın okunabilirliğini geliştirmek için başlık kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-196">It doesn’t have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="ea476-197">`<pathToFile>` (*zorunlu*)</span><span class="sxs-lookup"><span data-stu-id="ea476-197">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="ea476-198">Dosya sisteminde, başvurulacak kod parçacığı dosyasını gösteren göreli yol.</span><span class="sxs-lookup"><span data-stu-id="ea476-198">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="ea476-199">.NET belgeler kümesini oluşturan farklı depolar nedeniyle bu yol karmaşık olabilir.</span><span class="sxs-lookup"><span data-stu-id="ea476-199">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="ea476-200">.NET örnekleri, dotnet/samples deposundadır.</span><span class="sxs-lookup"><span data-stu-id="ea476-200">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="ea476-201">Tüm kod parçacığı yolları `~/samples` ile başlar, yolun devamı ise bu deponun kökündeki kaynağın yoludur.</span><span class="sxs-lookup"><span data-stu-id="ea476-201">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="ea476-202">`<queryoption>` (*isteğe bağlı*)</span><span class="sxs-lookup"><span data-stu-id="ea476-202">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="ea476-203">Kodun dosyadan nasıl alınacağını belirtmek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="ea476-203">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="ea476-204">`#`:  `#{tagname}` (etiket adı) *veya* `#L{startlinenumber}-L{endlinenumber}` (satır aralığı).</span><span class="sxs-lookup"><span data-stu-id="ea476-204">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="ea476-205">Bozulması kolay olduğu için satır numarası kullanımını önermiyoruz.</span><span class="sxs-lookup"><span data-stu-id="ea476-205">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="ea476-206">Etiket adı, kod parçacıklarına başvurmak için tercih edilen yoldur.</span><span class="sxs-lookup"><span data-stu-id="ea476-206">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="ea476-207">Anlamlı etiket adları kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea476-207">Use meaningful tag names.</span></span> <span data-ttu-id="ea476-208">(Pek çok kod parçacığı önceki platformdan geçirilmiştir ve etiketlerin `Snippet1` ve `Snippet2` gibi adları vardır. Bunu devam ettirmek daha zordur.)</span><span class="sxs-lookup"><span data-stu-id="ea476-208">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="ea476-209">`range`: `?range=1,3-5` Satır aralığı.</span><span class="sxs-lookup"><span data-stu-id="ea476-209">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="ea476-210">Bu örnek 1, 3, 4 ve 5. satırları ekler.</span><span class="sxs-lookup"><span data-stu-id="ea476-210">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="ea476-211">Mümkünse etiket adı seçeneğinin kullanılmasını öneririz.</span><span class="sxs-lookup"><span data-stu-id="ea476-211">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="ea476-212">Etiket adı, kaynak kodunda bulunan ve `Snippettagname` biçimindeki bir bölge adı veya kod açıklamasıdır.</span><span class="sxs-lookup"><span data-stu-id="ea476-212">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="ea476-213">Aşağıdaki örnek, `BasicThrow` etiket adına nasıl başvurulacağını göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="ea476-213">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="ea476-214">**dotnet/samples** deposundaki kaynağın göreli yolu, `~/samples` yolunu izler.</span><span class="sxs-lookup"><span data-stu-id="ea476-214">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="ea476-215">Kod parçacığı etiketlerinin yapısını [bu kaynak dosyada](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs) görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-215">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="ea476-216">Dile göre kod parçacığı kaynak dosyalarındaki etiket adı gösterimi hakkında ayrıntılı bilgi için, [DocFX yönergelerine](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file) bakın.</span><span class="sxs-lookup"><span data-stu-id="ea476-216">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="ea476-217">Aşağıdaki örnek, üç .NET dilinde de ekli olan kodu göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="ea476-217">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

<span data-ttu-id="ea476-218">Tam programlardan kod parçacığı eklendiğinde, tüm kodların Sürekli Tümleştirme (CI) sistemimizde çalışması sağlanır.</span><span class="sxs-lookup"><span data-stu-id="ea476-218">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="ea476-219">Ancak derleme zamanı veya çalışma zamanı hatalarına sebep olan bir durum göstermek istiyorsanız satır içi kod bloklarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-219">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="ea476-220">Görüntüler</span><span class="sxs-lookup"><span data-stu-id="ea476-220">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="ea476-221">Statik görüntü veya animasyonlu GIF</span><span class="sxs-lookup"><span data-stu-id="ea476-221">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="ea476-222">Bağlantı verilen görüntü</span><span class="sxs-lookup"><span data-stu-id="ea476-222">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="ea476-223">Videolar</span><span class="sxs-lookup"><span data-stu-id="ea476-223">Videos</span></span>

<span data-ttu-id="ea476-224">Şu anda hem Channel 9 hem de YouTube videolarını şu söz dizimi ile ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ea476-224">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="ea476-225">Channel 9</span><span class="sxs-lookup"><span data-stu-id="ea476-225">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="ea476-226">Videoya ait doğru URL’yi almak için video çerçevesindeki **Ekle** sekmesini seçin ve `<iframe>` öğesinden URL’yi kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="ea476-226">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="ea476-227">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="ea476-227">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="ea476-228">YouTube</span><span class="sxs-lookup"><span data-stu-id="ea476-228">YouTube</span></span>

<span data-ttu-id="ea476-229">Videoya ait doğru URL’yi almak için videoya sağ tıklayın, **Ekleme Kodunu Kopyala**’ya tıklayın ve `<iframe>` öğesinden URL’yi kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="ea476-229">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="ea476-230">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="ea476-230">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="ea476-231">docs.microsoft uzantıları</span><span class="sxs-lookup"><span data-stu-id="ea476-231">docs.microsoft extensions</span></span>

<span data-ttu-id="ea476-232">docs.microsoft, GitHub Flavored Markdown’a birkaç ek uzantı sağlar.</span><span class="sxs-lookup"><span data-stu-id="ea476-232">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="ea476-233">İşaretli listeler</span><span class="sxs-lookup"><span data-stu-id="ea476-233">Checked lists</span></span>

<span data-ttu-id="ea476-234">Listeler için özel bir stil kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ea476-234">A custom style is available for lists.</span></span> <span data-ttu-id="ea476-235">Listeleri yeşil onay işaretleriyle işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-235">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="ea476-236">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="ea476-236">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="ea476-237">.NET Core uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea476-237">How to create a .NET Core app</span></span>
> * <span data-ttu-id="ea476-238">Microsoft.XmlSerializer.Generator paketine başvuru ekleme</span><span class="sxs-lookup"><span data-stu-id="ea476-238">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="ea476-239">Bağımlılık eklemek için MyApp.csproj dosyanızı düzenleme</span><span class="sxs-lookup"><span data-stu-id="ea476-239">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="ea476-240">Sınıf ve XmlSerializer ekleme</span><span class="sxs-lookup"><span data-stu-id="ea476-240">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="ea476-241">Uygulamayı derleme ve çalıştırma</span><span class="sxs-lookup"><span data-stu-id="ea476-241">How to build and run the application</span></span>

<span data-ttu-id="ea476-242">[.NET Core belgelerinde](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator), işaretli maddelerin nasıl kullanıldığının örneklerini bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-242">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="ea476-243">Düğmeler</span><span class="sxs-lookup"><span data-stu-id="ea476-243">Buttons</span></span>

<span data-ttu-id="ea476-244">Düğme bağlantıları:</span><span class="sxs-lookup"><span data-stu-id="ea476-244">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="ea476-245">Bu, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="ea476-245">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="ea476-246">düğme bağlantıları</span><span class="sxs-lookup"><span data-stu-id="ea476-246">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="ea476-247">[Visual Studio belgelerinde](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio), düğmelerin nasıl kullanıldığının örneklerini bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-247">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="ea476-248">Adım adım açıklamalar</span><span class="sxs-lookup"><span data-stu-id="ea476-248">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="ea476-249">[C# Kılavuzunda](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure), adım adım açıklamaların nasıl kullanıldığının örneklerini bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea476-249">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
