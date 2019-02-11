---
title: Docs’ta makale yazmak için Markdown kullanma
description: Bu makale, docs.microsoft.com makalelerinde kullanılan Markdown dilinin temellerini ve başvuru bilgilerini sağlar.
ms.date: 01/29/2019
ms.openlocfilehash: 5235189d11c8c20ac20c91572d8bafcf525fb7c0
ms.sourcegitcommit: fbdd61ae4fb3761aec072732eefcbf2c2dca8011
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55887310"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="19a11-103">Docs’ta makale yazmak için Markdown kullanma</span><span class="sxs-lookup"><span data-stu-id="19a11-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="19a11-104">[Docs.microsoft.com](http://docs.microsoft.com) makaleleri, [Markdown](https://daringfireball.net/projects/markdown/) adı verilen hafif biçimlendirme dilinde yazılır. Bu dilin okunması ve öğrenilmesi kolaydır.</span><span class="sxs-lookup"><span data-stu-id="19a11-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="19a11-105">O nedenle bu dil kısa sürede endüstri standardı haline gelmiştir.</span><span class="sxs-lookup"><span data-stu-id="19a11-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="19a11-106">docs.microsoft.com sitesi arka ucu, [Markdig](https://github.com/lunet-io/markdig) ile ayrıştırılan [CommonMark](https://commonmark.org/) uyumlu markdown’ı destekleyen Open Publishing Services (OPS) kullanır ve aynı zamanda [DocFX Flavored Markdown’ı (DFM)](https://dotnet.github.io/docfx/) destekler.</span><span class="sxs-lookup"><span data-stu-id="19a11-106">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through [Markdig](https://github.com/lunet-io/markdig) and also supports [DocFX Flavored Markdown (DFM)](https://dotnet.github.io/docfx/).</span></span> <span data-ttu-id="19a11-107">Çoğu belge GitHub’da depolanıp burada düzenlenebildiği için bu markdown özellikleri çoğunlukla [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="19a11-107">These markdown flavors are mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="19a11-108">Markdown uzantıları ile ilave işlevler eklenir.</span><span class="sxs-lookup"><span data-stu-id="19a11-108">Additional functionality is added through Markdown extensions.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="19a11-109">Markdown temel bilgileri</span><span class="sxs-lookup"><span data-stu-id="19a11-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="19a11-110">Bölüm başlıkları</span><span class="sxs-lookup"><span data-stu-id="19a11-110">Headings</span></span>

<span data-ttu-id="19a11-111">Bir bölüm başlığı oluşturmak için karma işaretini (#) aşağıdaki gibi kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="19a11-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="19a11-112">Bölüm başlıkları, atx-style kullanılarak hazırlanmalıdır. Yani satırın başında, arkasından gelen kısmın bölüm başlığı olduğunu belirtmek için H1-H6 HTML başlık düzeyine karşılık gelecek şekilde 1-6 kare karakter (#) kullanın.</span><span class="sxs-lookup"><span data-stu-id="19a11-112">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="19a11-113">Bir ila dördüncü düzey bölüm başlığı örnekleri yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="19a11-113">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="19a11-114">Konunuz içerisinde yalnızca bir adet birinci düzey bölüm başlığı (H1) **olmalıdır** ve bu, sayfa başlığı olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="19a11-114">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="19a11-115">Başlığınız `#` karakteriyle bitiyorsa başlığın doğru işlenmesi için sonuna fazladan bir `#` karakteri eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="19a11-115">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="19a11-116">Örneğin `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="19a11-116">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="19a11-117">İkinci düzey bölüm başlıkları, sayfa başlığının altındaki “Bu makalede” bölümünde yer alan İçindekiler (TOC) bölümünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19a11-117">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="19a11-118">Kalın ve italik metin</span><span class="sxs-lookup"><span data-stu-id="19a11-118">Bold and italic text</span></span>

<span data-ttu-id="19a11-119">Bir metni **kalın** olarak biçimlendirmek için iki yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="19a11-119">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="19a11-120">Bir metni *italik* olarak biçimlendirmek için bir yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="19a11-120">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="19a11-121">Bir metni ***kalın ve italik*** olarak biçimlendirmek için üç yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="19a11-121">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="19a11-122">Blok alıntılar</span><span class="sxs-lookup"><span data-stu-id="19a11-122">Blockquotes</span></span>

<span data-ttu-id="19a11-123">Blok alıntılar, `>` karakteri kullanılarak oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="19a11-123">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="19a11-124">Yukarıdaki örnek, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="19a11-124">The preceding example renders as follows:</span></span>

> <span data-ttu-id="19a11-125">Kuraklık, on milyon yıldır devam ediyordu ve korkunç kertenkelelerin egemenliği çoktan sona ermişti.</span><span class="sxs-lookup"><span data-stu-id="19a11-125">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="19a11-126">Burada, Ekvator’da, günün birinde Afrika olarak anılacak bu kıtada, var olmak için verilen savaşta vahşetin yeni bir zirvesine ulaşılmıştı ve ortada henüz bir galip yoktu.</span><span class="sxs-lookup"><span data-stu-id="19a11-126">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="19a11-127">Bu kıraç ve kuru topraklarda, yalnızca küçük, hızlı veya vahşi olanlar büyüyebilirdi, ya da hayatta kalmayı umut edebilirdi.</span><span class="sxs-lookup"><span data-stu-id="19a11-127">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="19a11-128">Listeler</span><span class="sxs-lookup"><span data-stu-id="19a11-128">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="19a11-129">Sırasız liste</span><span class="sxs-lookup"><span data-stu-id="19a11-129">Unordered list</span></span>

<span data-ttu-id="19a11-130">Sırasız/madde işaretli bir listeyi biçimlendirmek için yıldız işaretleri veya tireler kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a11-130">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="19a11-131">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="19a11-131">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="19a11-132">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="19a11-132">will be rendered as:</span></span>

- <span data-ttu-id="19a11-133">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="19a11-133">List item 1</span></span>
- <span data-ttu-id="19a11-134">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="19a11-134">List item 2</span></span>
- <span data-ttu-id="19a11-135">Liste öğesi 3</span><span class="sxs-lookup"><span data-stu-id="19a11-135">List item 3</span></span>

<span data-ttu-id="19a11-136">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="19a11-136">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="19a11-137">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="19a11-137">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="19a11-138">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="19a11-138">will be rendered as:</span></span>

- <span data-ttu-id="19a11-139">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="19a11-139">List item 1</span></span>
  - <span data-ttu-id="19a11-140">Liste öğesi A</span><span class="sxs-lookup"><span data-stu-id="19a11-140">List item A</span></span>
  - <span data-ttu-id="19a11-141">Liste öğesi B</span><span class="sxs-lookup"><span data-stu-id="19a11-141">List item B</span></span>
- <span data-ttu-id="19a11-142">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="19a11-142">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="19a11-143">Sıralı liste</span><span class="sxs-lookup"><span data-stu-id="19a11-143">Ordered list</span></span>

<span data-ttu-id="19a11-144">Sıralı/adımlı bir listeyi biçimlendirmek için sıra numaraları kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="19a11-144">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="19a11-145">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="19a11-145">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="19a11-146">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="19a11-146">will be rendered as:</span></span>

1. <span data-ttu-id="19a11-147">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="19a11-147">First instruction</span></span>
2. <span data-ttu-id="19a11-148">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="19a11-148">Second instruction</span></span>
3. <span data-ttu-id="19a11-149">Üçüncü yönerge</span><span class="sxs-lookup"><span data-stu-id="19a11-149">Third instruction</span></span>

<span data-ttu-id="19a11-150">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="19a11-150">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="19a11-151">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="19a11-151">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="19a11-152">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="19a11-152">will be rendered as:</span></span>

1. <span data-ttu-id="19a11-153">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="19a11-153">First instruction</span></span>
   1. <span data-ttu-id="19a11-154">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="19a11-154">Sub-instruction</span></span>
   2. <span data-ttu-id="19a11-155">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="19a11-155">Sub-instruction</span></span>
2. <span data-ttu-id="19a11-156">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="19a11-156">Second instruction</span></span>

<span data-ttu-id="19a11-157">Tüm girişler için “1.”</span><span class="sxs-lookup"><span data-stu-id="19a11-157">Note that we use '1.'</span></span> <span data-ttu-id="19a11-158">kullandığımıza dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="19a11-158">for all entries.</span></span> <span data-ttu-id="19a11-159">Böylece sonraki güncelleştirmelerde yeni adımlar eklendiğinde veya mevcut adımlar çıkarıldığında, değişiklikleri gözden geçirmek kolaylaşır.</span><span class="sxs-lookup"><span data-stu-id="19a11-159">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="19a11-160">eğlence</span><span class="sxs-lookup"><span data-stu-id="19a11-160">Tables</span></span>

<span data-ttu-id="19a11-161">Tablolar, temel Markdown belirtiminin parçası değildir, ancak GFM tarafından desteklenir.</span><span class="sxs-lookup"><span data-stu-id="19a11-161">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="19a11-162">Düz çizgi (|) ve kısa çizgi (-) karakterlerini kullanarak tablolar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a11-162">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="19a11-163">Kısa çizgiler sütunların üst bilgisini oluştururken düz çizgiler sütunları birbirinden ayırır.</span><span class="sxs-lookup"><span data-stu-id="19a11-163">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="19a11-164">Tablonun doğru işlenebilmesi için başına boş bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="19a11-164">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="19a11-165">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="19a11-165">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="19a11-166">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="19a11-166">will be rendered as:</span></span>

| <span data-ttu-id="19a11-167">Tablolar</span><span class="sxs-lookup"><span data-stu-id="19a11-167">Fun</span></span>                  | <span data-ttu-id="19a11-168">Şununla:</span><span class="sxs-lookup"><span data-stu-id="19a11-168">With</span></span>                 | <span data-ttu-id="19a11-169">eğlence</span><span class="sxs-lookup"><span data-stu-id="19a11-169">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="19a11-170">sola hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="19a11-170">left-aligned column</span></span>  | <span data-ttu-id="19a11-171">sağa hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="19a11-171">right-aligned column</span></span> | <span data-ttu-id="19a11-172">ortalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="19a11-172">centered column</span></span> |
| <span data-ttu-id="19a11-173">100 $</span><span class="sxs-lookup"><span data-stu-id="19a11-173">$100</span></span>                 | <span data-ttu-id="19a11-174">100 $</span><span class="sxs-lookup"><span data-stu-id="19a11-174">$100</span></span>                 | <span data-ttu-id="19a11-175">100 $</span><span class="sxs-lookup"><span data-stu-id="19a11-175">$100</span></span>            |
| <span data-ttu-id="19a11-176">10 $</span><span class="sxs-lookup"><span data-stu-id="19a11-176">$10</span></span>                  | <span data-ttu-id="19a11-177">10 $</span><span class="sxs-lookup"><span data-stu-id="19a11-177">$10</span></span>                  | <span data-ttu-id="19a11-178">10 $</span><span class="sxs-lookup"><span data-stu-id="19a11-178">$10</span></span>             |
| <span data-ttu-id="19a11-179">1 $</span><span class="sxs-lookup"><span data-stu-id="19a11-179">$1</span></span>                   | <span data-ttu-id="19a11-180">1 $</span><span class="sxs-lookup"><span data-stu-id="19a11-180">$1</span></span>                   | <span data-ttu-id="19a11-181">1 $</span><span class="sxs-lookup"><span data-stu-id="19a11-181">$1</span></span>              |

<span data-ttu-id="19a11-182">Tablo oluşturma hakkında daha fazla bilgi için şunlara bakın:</span><span class="sxs-lookup"><span data-stu-id="19a11-182">For more information on creating tables, see:</span></span>

- <span data-ttu-id="19a11-183">Geniş tabloların biçimlendirmesinde yardımcı olabilecek Markdig [tablo sarmalama özelliği](#table-wrapping).</span><span class="sxs-lookup"><span data-stu-id="19a11-183">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="19a11-184">GitHub’ın [Tablolarla bilgi düzenleme](https://help.github.com/articles/organizing-information-with-tables/) makalesi.</span><span class="sxs-lookup"><span data-stu-id="19a11-184">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="19a11-185">[Markdown Tablo Oluşturucu](https://www.tablesgenerator.com/markdown_tables) web uygulaması.</span><span class="sxs-lookup"><span data-stu-id="19a11-185">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="19a11-186">[Adam Pritchard - Markdown Hızlı Başvuru Kılavuzu](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span><span class="sxs-lookup"><span data-stu-id="19a11-186">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="19a11-187">[Michel Fortin - Markdown Ekstra](https://michelf.ca/projects/php-markdown/extra/#table).</span><span class="sxs-lookup"><span data-stu-id="19a11-187">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="19a11-188">[HTML tablolarını Markdown’a dönüştürme](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="19a11-188">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="19a11-189">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="19a11-189">Links</span></span>

<span data-ttu-id="19a11-190">Satır içi bağlantılarda Markdown söz dizimi, köprü bağlantısı eklenecek `[link text]` metni ve bağlantı verilen URL ya da dosya adı olan `(file-name.md)` kısımlarından oluşur:</span><span class="sxs-lookup"><span data-stu-id="19a11-190">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="19a11-191">Bağlantı verme hakkında daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="19a11-191">For more information on linking, see:</span></span>

- <span data-ttu-id="19a11-192">Markdown’ın temel bağlantı desteği konusunda ayrıntılar için [Markdown söz dizimi kılavuzu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="19a11-192">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="19a11-193">Markdig tarafından sağlanan ilave bağlayıcı söz dizimi hakkında ayrıntılar için bu kılavuzun [Bağlantılar](how-to-write-links.md) bölümü.</span><span class="sxs-lookup"><span data-stu-id="19a11-193">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="19a11-194">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="19a11-194">Code snippets</span></span>

<span data-ttu-id="19a11-195">Markdown, hem bir cümlede satır içi olarak hem de cümleler arasında ayrı “çevrelenmiş” bir blok halinde kod parçacıkları yerleştirilmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="19a11-195">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="19a11-196">Ayrıntılar için bkz.</span><span class="sxs-lookup"><span data-stu-id="19a11-196">For details, see:</span></span>

- [<span data-ttu-id="19a11-197">Kod blokları için yerel Markdown desteği</span><span class="sxs-lookup"><span data-stu-id="19a11-197">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="19a11-198">Kod çevreleme ve söz dizimi vurgulama için GFM desteği</span><span class="sxs-lookup"><span data-stu-id="19a11-198">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="19a11-199">Çevrelenmiş kod blokları, kod parçacıklarınız için söz dizimi vurgulamasını etkinleştirmenin kolay bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="19a11-199">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="19a11-200">Çevrelenmiş kod bloklarının biçimi genelde şöyledir:</span><span class="sxs-lookup"><span data-stu-id="19a11-200">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="19a11-201">İlk üç ters tırnak (\`) karakterinden sonra gelen diğer ad, kullanılacak söz dizimi vurgulamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19a11-201">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="19a11-202">Docs içeriğinde yaygın olarak kullanılan programlama dilleri ve bunların etiketleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="19a11-202">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="19a11-203">Bu diller, kolay as desteğine ve dil vurgulamasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="19a11-203">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="19a11-204">Ad</span><span class="sxs-lookup"><span data-stu-id="19a11-204">Name</span></span>|<span data-ttu-id="19a11-205">Markdown Etiketi</span><span class="sxs-lookup"><span data-stu-id="19a11-205">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="19a11-206">.NET Konsolu</span><span class="sxs-lookup"><span data-stu-id="19a11-206">.NET Console</span></span>|<span data-ttu-id="19a11-207">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="19a11-207">dotnetcli</span></span>|
|<span data-ttu-id="19a11-208">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="19a11-208">ASP.NET (C#)</span></span>|<span data-ttu-id="19a11-209">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="19a11-209">aspx-csharp</span></span>|
|<span data-ttu-id="19a11-210">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="19a11-210">ASP.NET (VB)</span></span>|<span data-ttu-id="19a11-211">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="19a11-211">aspx-vb</span></span>|
|<span data-ttu-id="19a11-212">AzCopy</span><span class="sxs-lookup"><span data-stu-id="19a11-212">AzCopy</span></span>|<span data-ttu-id="19a11-213">azcopy</span><span class="sxs-lookup"><span data-stu-id="19a11-213">azcopy</span></span>|
|<span data-ttu-id="19a11-214">Azure CLI’si</span><span class="sxs-lookup"><span data-stu-id="19a11-214">Azure CLI</span></span>|<span data-ttu-id="19a11-215">azurecli</span><span class="sxs-lookup"><span data-stu-id="19a11-215">azurecli</span></span>|
|<span data-ttu-id="19a11-216">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="19a11-216">Azure PowerShell</span></span>|<span data-ttu-id="19a11-217">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="19a11-217">azurepowershell</span></span>|
|<span data-ttu-id="19a11-218">C++</span><span class="sxs-lookup"><span data-stu-id="19a11-218">C++</span></span>|<span data-ttu-id="19a11-219">cpp</span><span class="sxs-lookup"><span data-stu-id="19a11-219">cpp</span></span>|
|<span data-ttu-id="19a11-220">C++/CX</span><span class="sxs-lookup"><span data-stu-id="19a11-220">C++/CX</span></span>|<span data-ttu-id="19a11-221">cppcx</span><span class="sxs-lookup"><span data-stu-id="19a11-221">cppcx</span></span>|
|<span data-ttu-id="19a11-222">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="19a11-222">C++/WinRT</span></span>|<span data-ttu-id="19a11-223">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="19a11-223">cppwinrt</span></span>|
|<span data-ttu-id="19a11-224">C#</span><span class="sxs-lookup"><span data-stu-id="19a11-224">C#</span></span>|<span data-ttu-id="19a11-225">csharp</span><span class="sxs-lookup"><span data-stu-id="19a11-225">csharp</span></span>|
|<span data-ttu-id="19a11-226">Tarayıcıda C#</span><span class="sxs-lookup"><span data-stu-id="19a11-226">C# in browser</span></span>|<span data-ttu-id="19a11-227">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="19a11-227">csharp-interactive</span></span>|
|<span data-ttu-id="19a11-228">Konsol</span><span class="sxs-lookup"><span data-stu-id="19a11-228">Console</span></span>|<span data-ttu-id="19a11-229">konsol</span><span class="sxs-lookup"><span data-stu-id="19a11-229">console</span></span>|
|<span data-ttu-id="19a11-230">CSHTML</span><span class="sxs-lookup"><span data-stu-id="19a11-230">CSHTML</span></span>|<span data-ttu-id="19a11-231">cshtml</span><span class="sxs-lookup"><span data-stu-id="19a11-231">cshtml</span></span>|
|<span data-ttu-id="19a11-232">DAX</span><span class="sxs-lookup"><span data-stu-id="19a11-232">DAX</span></span>|<span data-ttu-id="19a11-233">dax</span><span class="sxs-lookup"><span data-stu-id="19a11-233">dax</span></span>|
|<span data-ttu-id="19a11-234">Docker</span><span class="sxs-lookup"><span data-stu-id="19a11-234">Docker</span></span>|<span data-ttu-id="19a11-235">dockerfile</span><span class="sxs-lookup"><span data-stu-id="19a11-235">dockerfile</span></span>|
|<span data-ttu-id="19a11-236">F#</span><span class="sxs-lookup"><span data-stu-id="19a11-236">F#</span></span>|<span data-ttu-id="19a11-237">fsharp</span><span class="sxs-lookup"><span data-stu-id="19a11-237">fsharp</span></span>|
|<span data-ttu-id="19a11-238">Go</span><span class="sxs-lookup"><span data-stu-id="19a11-238">Go</span></span>|<span data-ttu-id="19a11-239">go</span><span class="sxs-lookup"><span data-stu-id="19a11-239">go</span></span>|
|<span data-ttu-id="19a11-240">HTML</span><span class="sxs-lookup"><span data-stu-id="19a11-240">HTML</span></span>|<span data-ttu-id="19a11-241">html</span><span class="sxs-lookup"><span data-stu-id="19a11-241">html</span></span>|
|<span data-ttu-id="19a11-242">HTTP</span><span class="sxs-lookup"><span data-stu-id="19a11-242">HTTP</span></span>|<span data-ttu-id="19a11-243">http</span><span class="sxs-lookup"><span data-stu-id="19a11-243">http</span></span>|
|<span data-ttu-id="19a11-244">Java</span><span class="sxs-lookup"><span data-stu-id="19a11-244">Java</span></span>|<span data-ttu-id="19a11-245">java</span><span class="sxs-lookup"><span data-stu-id="19a11-245">java</span></span>|
|<span data-ttu-id="19a11-246">JavaScript</span><span class="sxs-lookup"><span data-stu-id="19a11-246">JavaScript</span></span>|<span data-ttu-id="19a11-247">javascript</span><span class="sxs-lookup"><span data-stu-id="19a11-247">javascript</span></span>|
|<span data-ttu-id="19a11-248">JSON</span><span class="sxs-lookup"><span data-stu-id="19a11-248">JSON</span></span>|<span data-ttu-id="19a11-249">json</span><span class="sxs-lookup"><span data-stu-id="19a11-249">json</span></span>|
|<span data-ttu-id="19a11-250">Kusto Sorgu Dili</span><span class="sxs-lookup"><span data-stu-id="19a11-250">Kusto Query Language</span></span>|<span data-ttu-id="19a11-251">kusto</span><span class="sxs-lookup"><span data-stu-id="19a11-251">kusto</span></span>|
|<span data-ttu-id="19a11-252">Markdown</span><span class="sxs-lookup"><span data-stu-id="19a11-252">Markdown</span></span>|<span data-ttu-id="19a11-253">md</span><span class="sxs-lookup"><span data-stu-id="19a11-253">md</span></span>|
|<span data-ttu-id="19a11-254">Objective-C</span><span class="sxs-lookup"><span data-stu-id="19a11-254">Objective-C</span></span>|<span data-ttu-id="19a11-255">objc</span><span class="sxs-lookup"><span data-stu-id="19a11-255">objc</span></span>|
|<span data-ttu-id="19a11-256">OData</span><span class="sxs-lookup"><span data-stu-id="19a11-256">OData</span></span>|<span data-ttu-id="19a11-257">odata</span><span class="sxs-lookup"><span data-stu-id="19a11-257">odata</span></span>|
|<span data-ttu-id="19a11-258">PHP</span><span class="sxs-lookup"><span data-stu-id="19a11-258">PHP</span></span>|<span data-ttu-id="19a11-259">php</span><span class="sxs-lookup"><span data-stu-id="19a11-259">php</span></span>|
|<span data-ttu-id="19a11-260">PowerApps (nokta ondalık ayırıcısı)</span><span class="sxs-lookup"><span data-stu-id="19a11-260">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="19a11-261">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="19a11-261">powerapps-dot</span></span>|
|<span data-ttu-id="19a11-262">PowerApps (virgül ondalık ayırıcısı)</span><span class="sxs-lookup"><span data-stu-id="19a11-262">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="19a11-263">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="19a11-263">powerapps-comma</span></span>|
|<span data-ttu-id="19a11-264">PowerShell</span><span class="sxs-lookup"><span data-stu-id="19a11-264">PowerShell</span></span>|<span data-ttu-id="19a11-265">powershell</span><span class="sxs-lookup"><span data-stu-id="19a11-265">powershell</span></span>|
|<span data-ttu-id="19a11-266">Python</span><span class="sxs-lookup"><span data-stu-id="19a11-266">Python</span></span>|<span data-ttu-id="19a11-267">python</span><span class="sxs-lookup"><span data-stu-id="19a11-267">python</span></span>|
|<span data-ttu-id="19a11-268">Q#</span><span class="sxs-lookup"><span data-stu-id="19a11-268">Q#</span></span>|<span data-ttu-id="19a11-269">qsharp</span><span class="sxs-lookup"><span data-stu-id="19a11-269">qsharp</span></span>|
|<span data-ttu-id="19a11-270">R</span><span class="sxs-lookup"><span data-stu-id="19a11-270">R</span></span>|<span data-ttu-id="19a11-271">r</span><span class="sxs-lookup"><span data-stu-id="19a11-271">r</span></span>|
|<span data-ttu-id="19a11-272">Ruby</span><span class="sxs-lookup"><span data-stu-id="19a11-272">Ruby</span></span>|<span data-ttu-id="19a11-273">ruby</span><span class="sxs-lookup"><span data-stu-id="19a11-273">ruby</span></span>|
|<span data-ttu-id="19a11-274">SQL</span><span class="sxs-lookup"><span data-stu-id="19a11-274">SQL</span></span>|<span data-ttu-id="19a11-275">sql</span><span class="sxs-lookup"><span data-stu-id="19a11-275">sql</span></span>|
|<span data-ttu-id="19a11-276">Swift</span><span class="sxs-lookup"><span data-stu-id="19a11-276">Swift</span></span>|<span data-ttu-id="19a11-277">swift</span><span class="sxs-lookup"><span data-stu-id="19a11-277">swift</span></span>|
|<span data-ttu-id="19a11-278">TypeScript</span><span class="sxs-lookup"><span data-stu-id="19a11-278">TypeScript</span></span>|<span data-ttu-id="19a11-279">typescript</span><span class="sxs-lookup"><span data-stu-id="19a11-279">typescript</span></span>|
|<span data-ttu-id="19a11-280">VB</span><span class="sxs-lookup"><span data-stu-id="19a11-280">VB</span></span>|<span data-ttu-id="19a11-281">vb</span><span class="sxs-lookup"><span data-stu-id="19a11-281">vb</span></span>|
|<span data-ttu-id="19a11-282">XAML</span><span class="sxs-lookup"><span data-stu-id="19a11-282">XAML</span></span>|<span data-ttu-id="19a11-283">xaml</span><span class="sxs-lookup"><span data-stu-id="19a11-283">xaml</span></span>|
|<span data-ttu-id="19a11-284">XML</span><span class="sxs-lookup"><span data-stu-id="19a11-284">XML</span></span>|<span data-ttu-id="19a11-285">xml</span><span class="sxs-lookup"><span data-stu-id="19a11-285">xml</span></span>|

<span data-ttu-id="19a11-286">`csharp-interactive` adı, C# bilgisayar dilini ve tarayıcıdan örnek çalıştırma becerisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19a11-286">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="19a11-287">Bu kod parçacıkları, bir Docker kapsayıcısında derlenir ve yürütülür. Bu program yürütüldüğünde ortaya çıkan sonuçlar kullanıcının tarayıcı penceresinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="19a11-287">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="19a11-288">Örnek: C\#</span><span class="sxs-lookup"><span data-stu-id="19a11-288">Example: C\#</span></span>

<span data-ttu-id="19a11-289">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="19a11-289">__Markdown__</span></span>

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

<span data-ttu-id="19a11-290">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="19a11-290">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="19a11-291">Örnek: SQL</span><span class="sxs-lookup"><span data-stu-id="19a11-291">Example: SQL</span></span>

<span data-ttu-id="19a11-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="19a11-292">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="19a11-293">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="19a11-293">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="19a11-294">OPS özel Markdown uzantıları</span><span class="sxs-lookup"><span data-stu-id="19a11-294">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="19a11-295">Open Publishing Services (OPS), GitHub Flavored Markdown (GFM) ile yüksek uyumluluğa sahip olan Markdown için Markdig Ayrıştırıcısı’nı uygular.</span><span class="sxs-lookup"><span data-stu-id="19a11-295">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="19a11-296">Markdig, Markdown uzantıları aracılığıyla ilave işlevsellik sağlar.</span><span class="sxs-lookup"><span data-stu-id="19a11-296">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="19a11-297">Bu nedenle, tam OPS Yazma Kılavuzundan bazı makaleler başvuru için bu kılavuza dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="19a11-297">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="19a11-298">(Örneğin, içindekiler bölümünde "Markdig ve Markdown uzantıları" ile "Kod parçacıkları" kısımlarına bakın.)</span><span class="sxs-lookup"><span data-stu-id="19a11-298">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="19a11-299">Docs makaleleri çoğu zaman paragraflar, bağlantılar, listeler ve bölüm başlıkları gibi makale biçimlendirmeleri için GFM’yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="19a11-299">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="19a11-300">Makaleler, daha zengin biçimlendirme için aşağıdakiler gibi Markdig özelliklerini kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="19a11-300">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="19a11-301">Not blokları</span><span class="sxs-lookup"><span data-stu-id="19a11-301">Note blocks</span></span>
- <span data-ttu-id="19a11-302">Dosyaları dahil et</span><span class="sxs-lookup"><span data-stu-id="19a11-302">Include files</span></span>
- <span data-ttu-id="19a11-303">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="19a11-303">Selectors</span></span>
- <span data-ttu-id="19a11-304">Ekli videolar</span><span class="sxs-lookup"><span data-stu-id="19a11-304">Embedded videos</span></span>
- <span data-ttu-id="19a11-305">Kod parçacıkları/örnekleri</span><span class="sxs-lookup"><span data-stu-id="19a11-305">Code snippets/samples</span></span>

<span data-ttu-id="19a11-306">Tam bir liste için içerikler bölümünde “Markdig ve Markdown uzantıları” ve “Kod parçacıkları” kısmına bakın.</span><span class="sxs-lookup"><span data-stu-id="19a11-306">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="19a11-307">Not blokları</span><span class="sxs-lookup"><span data-stu-id="19a11-307">Note blocks</span></span>

<span data-ttu-id="19a11-308">İlgiyi belirli bir içeriğe çekmek için dört çeşit not blokundan birini seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="19a11-308">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="19a11-309">NOT</span><span class="sxs-lookup"><span data-stu-id="19a11-309">NOTE</span></span>
- <span data-ttu-id="19a11-310">UYARI</span><span class="sxs-lookup"><span data-stu-id="19a11-310">WARNING</span></span>
- <span data-ttu-id="19a11-311">İPUCU</span><span class="sxs-lookup"><span data-stu-id="19a11-311">TIP</span></span>
- <span data-ttu-id="19a11-312">ÖNEMLİ</span><span class="sxs-lookup"><span data-stu-id="19a11-312">IMPORTANT</span></span>

<span data-ttu-id="19a11-313">Genel olarak not bloklarını fazla kullanmaktan kaçınmalısınız, dikkat dağıtıcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="19a11-313">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="19a11-314">Not bloklarında kod blokları, görüntüler, listeler ve bağlantılar destekleniyor olsa da bunları olabildiğince sade ve düz bir şekilde oluşturun.</span><span class="sxs-lookup"><span data-stu-id="19a11-314">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="19a11-315">Örnekler:</span><span class="sxs-lookup"><span data-stu-id="19a11-315">Examples:</span></span>

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

<span data-ttu-id="19a11-316">Bunlar aşağıdaki gibi işlenir:</span><span class="sxs-lookup"><span data-stu-id="19a11-316">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="19a11-317">Bu bir NOT’tur</span><span class="sxs-lookup"><span data-stu-id="19a11-317">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="19a11-318">Bu bir UYARI’dır</span><span class="sxs-lookup"><span data-stu-id="19a11-318">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="19a11-319">Bu bir İPUCU’dur</span><span class="sxs-lookup"><span data-stu-id="19a11-319">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19a11-320">Bu ÖNEMLİ’dir</span><span class="sxs-lookup"><span data-stu-id="19a11-320">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="19a11-321">Dosyaları dahil et</span><span class="sxs-lookup"><span data-stu-id="19a11-321">Include files</span></span>

<span data-ttu-id="19a11-322">Makale dosyalarına dahil edilmesi gereken yeniden kullanılabilir metin veya görüntü dosyalarınız varsa dosyayı Markdig dosya dahil etme özelliği ile “dahil etmek” için bir başvuru kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a11-322">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="19a11-323">Bu özellik, verilen dosyayı makalenize derleme sırasında “eklemesi” için OPS’yi yönlendirir, böylece dosya da yayımlanan makalenizin bir parçası olur.</span><span class="sxs-lookup"><span data-stu-id="19a11-323">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="19a11-324">İçerikleri tekrar kullanmanıza imkan veren üç tür ekleme başvurusu vardır:</span><span class="sxs-lookup"><span data-stu-id="19a11-324">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="19a11-325">Satır İçi: Genel bir metin parçacığını başka bir cümlede satır içinde yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="19a11-325">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="19a11-326">Blok: Makalenin bir bölümündeki bütün bir Markdown dosyasını yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="19a11-326">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="19a11-327">Görüntü: Docs’ta standart görüntü ekleme yoludur.</span><span class="sxs-lookup"><span data-stu-id="19a11-327">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="19a11-328">Satır içi ve blok ekleme dosyaları, basit birer Markdown (.md) dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="19a11-328">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="19a11-329">Bu dosyalar, herhangi bir geçerli Markdown barındırabilir.</span><span class="sxs-lookup"><span data-stu-id="19a11-329">It can contain any valid Markdown.</span></span> <span data-ttu-id="19a11-330">Tüm ekleme Markdown dosyaları, depo kökünde [ortak bir `/includes` alt dizinine](git-github-fundamentals.md#includes-subdirectory) yerleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="19a11-330">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="19a11-331">Makale yayımlandığında, eklenen dosya makaleyle sorunsuz bir şekilde tümleşmiş olur.</span><span class="sxs-lookup"><span data-stu-id="19a11-331">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="19a11-332">Ekleme dosyalarına yönelik gereksinimler ve önemli konular şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19a11-332">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="19a11-333">Aynı metni birden fazla makalede kullanmanız gerektiği zaman ekleme dosyalarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="19a11-333">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="19a11-334">Bir veya iki paragraf, paylaşılan bir yordam veya paylaşılan bir bölüm gibi büyük içeriklerde blok ekleme başvurusunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="19a11-334">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="19a11-335">Ancak bir cümleden daha küçük şeyler için kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="19a11-335">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="19a11-336">Ekleme başvuruları, Markdig uzantılarına bağlı olduğu için makalenizin GitHub tarafından işlenmiş görünümünde işlenmez.</span><span class="sxs-lookup"><span data-stu-id="19a11-336">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="19a11-337">Bunlar yalnızca yayın sonrasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="19a11-337">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="19a11-338">Ekleme dosyasına başvuran makalelerdeki ekleme dosyalarında bütün metnin, öncesinde veya sonrasında gelen metinden bağımsız tam cümleler veya ifadeler şeklinde olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="19a11-338">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="19a11-339">Bu kılavuzu dikkate almamak, makalede çevrilemeyen bir satır oluşturur ve yerelleştirme deneyimini bozar.</span><span class="sxs-lookup"><span data-stu-id="19a11-339">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="19a11-340">Ekleme başvurularını diğer ekleme dosyalarına eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="19a11-340">Don't embed include references within other include files.</span></span> <span data-ttu-id="19a11-341">Bu, desteklenmeyen bir durumdur.</span><span class="sxs-lookup"><span data-stu-id="19a11-341">They are not supported.</span></span>
- <span data-ttu-id="19a11-342">Medya dosyalarını ekleme alt dizinine özgü bir medya klasörüne yerleştirin, örneğin `<repo>`/eklemeler/medya klasörü.</span><span class="sxs-lookup"><span data-stu-id="19a11-342">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="19a11-343">Medya dizini, kökünde hiçbir görüntü barındırmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="19a11-343">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="19a11-344">Ekleme dosyasında görüntü yoksa buna karşılık gelecek bir medya dizini gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="19a11-344">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="19a11-345">Normal makalelerde olduğu gibi, ekleme dosyaları arasında medya paylaşmayın.</span><span class="sxs-lookup"><span data-stu-id="19a11-345">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="19a11-346">Her bir ekleme dosyası ve makale için benzersiz ada sahip ayrı dosyalar kullanın.</span><span class="sxs-lookup"><span data-stu-id="19a11-346">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="19a11-347">Medya dosyasını, ekleme dosyasıyla ilişkili medya klasöründe depolayın.</span><span class="sxs-lookup"><span data-stu-id="19a11-347">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="19a11-348">Ekleme dosyalarını bir makaledeki tek içerik olacak şekilde kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="19a11-348">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="19a11-349">Ekleme dosyaları, makaledeki diğer içerikleri tamamlayıcı niteliktedir.</span><span class="sxs-lookup"><span data-stu-id="19a11-349">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="19a11-350">Örnek:</span><span class="sxs-lookup"><span data-stu-id="19a11-350">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="19a11-351">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="19a11-351">Selectors</span></span>

<span data-ttu-id="19a11-352">Seçicileri teknik makalelerde, aynı makalenin farklı bölümlerini yazdığınızda teknolojiler veya platformlar arasındaki uygulama farklılıklarına değinirken kullanın.</span><span class="sxs-lookup"><span data-stu-id="19a11-352">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="19a11-353">Bu genellikle geliştiriciler için mobil platform içeriklerimizde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="19a11-353">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="19a11-354">Markdig’de şu anda iki farklı türde seçici vardır; tekli seçici ve çoklu seçici.</span><span class="sxs-lookup"><span data-stu-id="19a11-354">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="19a11-355">Seçimdeki her bir makaleye aynı seçici Markdown gittiği için makalenizin seçicisini bir ekleme dosyasına koymanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="19a11-355">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="19a11-356">Daha sonra aynı seçiciyi kullanan tüm makalelerinizde bu ekleme dosyasına başvurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a11-356">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="19a11-357">Aşağıdaki kodda bir seçici örneği gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="19a11-357">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="19a11-358">[Azure belgelerinde](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic) seçicilerin nasıl kullanıldığının örneklerini bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a11-358">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="19a11-359">Kod ekleme başvuruları</span><span class="sxs-lookup"><span data-stu-id="19a11-359">Code include references</span></span>

<span data-ttu-id="19a11-360">Markdig, bir makaleye kod parçacığı uzantısı aracılığıyla gelişmiş kod eklemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="19a11-360">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="19a11-361">Programlama dili seçimi ve söz dizimi renklendirme gibi GFM özellikleri üzerinde ortaya çıkan gelişmiş işleme seçenekleri sağlar, bunların yanında aşağıdaki gibi kullanışlı özellikler de getirir:</span><span class="sxs-lookup"><span data-stu-id="19a11-361">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="19a11-362">Bir dış depodan gelen merkezi kod örnekleri/parçacıklarının eklenmesi.</span><span class="sxs-lookup"><span data-stu-id="19a11-362">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="19a11-363">Kod örneklerinin farklı dillerdeki birçok çeşidini gösteren sekmeli kullanıcı arabirimi.</span><span class="sxs-lookup"><span data-stu-id="19a11-363">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="19a11-364">Tuzaklar ve sorun giderme</span><span class="sxs-lookup"><span data-stu-id="19a11-364">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="19a11-365">Alternatif metin</span><span class="sxs-lookup"><span data-stu-id="19a11-365">Alt text</span></span>

<span data-ttu-id="19a11-366">Alt çizgi içeren alternatif metin düzgün bir şekilde işlenmez.</span><span class="sxs-lookup"><span data-stu-id="19a11-366">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="19a11-367">Örneğin, şunu kullanmak yerine:</span><span class="sxs-lookup"><span data-stu-id="19a11-367">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="19a11-368">Şunun gibi alt çizgilerden kaçının:</span><span class="sxs-lookup"><span data-stu-id="19a11-368">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="19a11-369">Kesme işareti ve tırnak işaretleri</span><span class="sxs-lookup"><span data-stu-id="19a11-369">Apostrophes and quotation marks</span></span>

<span data-ttu-id="19a11-370">Word dosyasından Markdown editörüne bir şey kopyalarsanız kopyaladığınız metin “akıllı” (kıvrık) kesme işaretleri veya tırnak işaretleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="19a11-370">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="19a11-371">Bunların kodlanması veya kesme işareti ya da tırnak işaretlerine dönüştürülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="19a11-371">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="19a11-372">Aksi takdirde, dosya yayımlandığında şöyle karakterler görebilirsiniz: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="19a11-372">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="19a11-373">Bu noktalama işaretlerinin “akıllı” olanları için kodlamalar aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="19a11-373">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="19a11-374">Sol (açma) tırnak işareti: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="19a11-374">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="19a11-375">Sağ (kapatma) tırnak işareti: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="19a11-375">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="19a11-376">Sağ (kapatma) tekli tırnak işareti veya kesme işareti: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="19a11-376">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="19a11-377">Sağ (açma) tekli tırnak işareti (nadiren kullanılır): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="19a11-377">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="19a11-378">Açılı ayraçlar</span><span class="sxs-lookup"><span data-stu-id="19a11-378">Angle brackets</span></span>

<span data-ttu-id="19a11-379">Bir yer tutucuyu ifade etmek için köşeli ayraç kullanımı yaygındır.</span><span class="sxs-lookup"><span data-stu-id="19a11-379">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="19a11-380">Metinde (kodda değil) bunu yaptığınızda, köşeli ayraçları kodlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="19a11-380">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="19a11-381">Aksi takdirde Markdown bunların HTML etiketleri olması gerektiğini düşünür.</span><span class="sxs-lookup"><span data-stu-id="19a11-381">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="19a11-382">Örneğin `<script name>` öğesini `&lt;script name&gt;` şeklinde kodlayın</span><span class="sxs-lookup"><span data-stu-id="19a11-382">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="19a11-383">Ayrıca bkz.:</span><span class="sxs-lookup"><span data-stu-id="19a11-383">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="19a11-384">Markdown kaynakları</span><span class="sxs-lookup"><span data-stu-id="19a11-384">Markdown resources</span></span>

- [<span data-ttu-id="19a11-385">Markdown’a Giriş</span><span class="sxs-lookup"><span data-stu-id="19a11-385">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="19a11-386">Docs Markdown kural sayfası</span><span class="sxs-lookup"><span data-stu-id="19a11-386">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="19a11-387">GitHub Markdown Temel Bilgileri</span><span class="sxs-lookup"><span data-stu-id="19a11-387">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="19a11-388">Markdown Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="19a11-388">The Markdown Guide</span></span>](https://www.markdownguide.org/)
