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
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="955b4-103">Docs’ta makale yazmak için Markdown kullanma</span><span class="sxs-lookup"><span data-stu-id="955b4-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="955b4-104">[Docs.microsoft.com](http://docs.microsoft.com) makaleleri, [Markdown](https://daringfireball.net/projects/markdown/) adı verilen hafif biçimlendirme dilinde yazılır. Bu dilin okunması ve öğrenilmesi kolaydır.</span><span class="sxs-lookup"><span data-stu-id="955b4-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="955b4-105">O nedenle bu dil kısa sürede endüstri standardı haline gelmiştir.</span><span class="sxs-lookup"><span data-stu-id="955b4-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="955b4-106">Docs içerikleri GitHub’da depolandığı için [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) adlı bir Markdown üst kümesi kullanabilir. GFM, yaygın biçimlendirme ihtiyaçları için ilave işlevler sağlar.</span><span class="sxs-lookup"><span data-stu-id="955b4-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="955b4-107">Ayrıca Open Publishing Services (OPS), Markdig Markdown Ayrıştırıcısı’nı uygular.</span><span class="sxs-lookup"><span data-stu-id="955b4-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="955b4-108">Markdig, GFM ile yüksek uyumluluğa sahip olduğu için Docs’a özgü özellikleri etkinleştirmek için ek işlevsellik sağlar.</span><span class="sxs-lookup"><span data-stu-id="955b4-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="955b4-109">Markdig; .NET için hızlı, güçlü, CommonMark uyumlu, genişletilebilir Markdown işlemcisidir.</span><span class="sxs-lookup"><span data-stu-id="955b4-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="955b4-110">Daha iyi topluluk desteği</span><span class="sxs-lookup"><span data-stu-id="955b4-110">Better community support</span></span>
* <span data-ttu-id="955b4-111">Daha iyi standartlar desteği</span><span class="sxs-lookup"><span data-stu-id="955b4-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="955b4-112">Markdown temel bilgileri</span><span class="sxs-lookup"><span data-stu-id="955b4-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="955b4-113">Bölüm başlıkları</span><span class="sxs-lookup"><span data-stu-id="955b4-113">Headings</span></span>

<span data-ttu-id="955b4-114">Bir bölüm başlığı oluşturmak için karma işaretini (#) aşağıdaki gibi kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="955b4-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="955b4-115">Bölüm başlıkları, atx-style kullanılarak hazırlanmalıdır. Yani satırın başında, arkasından gelen kısmın bölüm başlığı olduğunu belirtmek için H1-H6 HTML başlık düzeyine karşılık gelecek şekilde 1-6 kare karakter (#) kullanın.</span><span class="sxs-lookup"><span data-stu-id="955b4-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="955b4-116">Bir ila dördüncü düzey bölüm başlığı örnekleri yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="955b4-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="955b4-117">Konunuz içerisinde yalnızca bir adet birinci düzey bölüm başlığı (H1) **olmalıdır** ve bu, sayfa başlığı olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="955b4-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="955b4-118">Başlığınız `#` karakteriyle bitiyorsa başlığın doğru işlenmesi için sonuna fazladan bir `#` karakteri eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="955b4-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="955b4-119">Örneğin `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="955b4-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="955b4-120">İkinci düzey bölüm başlıkları, sayfa başlığının altındaki “Bu makalede” bölümünde yer alan İçindekiler (TOC) bölümünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="955b4-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="955b4-121">Kalın ve italik metin</span><span class="sxs-lookup"><span data-stu-id="955b4-121">Bold and italic text</span></span>

<span data-ttu-id="955b4-122">Bir metni **kalın** olarak biçimlendirmek için iki yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="955b4-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="955b4-123">Bir metni *italik* olarak biçimlendirmek için bir yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="955b4-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="955b4-124">Bir metni ***kalın ve italik*** olarak biçimlendirmek için üç yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="955b4-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="955b4-125">Blok alıntılar</span><span class="sxs-lookup"><span data-stu-id="955b4-125">Blockquotes</span></span>

<span data-ttu-id="955b4-126">Blok alıntılar, `>` karakteri kullanılarak oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="955b4-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="955b4-127">Yukarıdaki örnek, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="955b4-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="955b4-128">Kuraklık, on milyon yıldır devam ediyordu ve korkunç kertenkelelerin egemenliği çoktan sona ermişti.</span><span class="sxs-lookup"><span data-stu-id="955b4-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="955b4-129">Burada, Ekvator’da, günün birinde Afrika olarak anılacak bu kıtada, var olmak için verilen savaşta vahşetin yeni bir zirvesine ulaşılmıştı ve ortada henüz bir galip yoktu.</span><span class="sxs-lookup"><span data-stu-id="955b4-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="955b4-130">Bu kıraç ve kuru topraklarda, yalnızca küçük, hızlı veya vahşi olanlar büyüyebilirdi, ya da hayatta kalmayı umut edebilirdi.</span><span class="sxs-lookup"><span data-stu-id="955b4-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="955b4-131">Listeler</span><span class="sxs-lookup"><span data-stu-id="955b4-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="955b4-132">Sırasız liste</span><span class="sxs-lookup"><span data-stu-id="955b4-132">Unordered list</span></span>

<span data-ttu-id="955b4-133">Sırasız/madde işaretli bir listeyi biçimlendirmek için yıldız işaretleri veya tireler kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="955b4-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="955b4-134">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="955b4-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="955b4-135">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="955b4-135">will be rendered as:</span></span>

- <span data-ttu-id="955b4-136">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="955b4-136">List item 1</span></span>
- <span data-ttu-id="955b4-137">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="955b4-137">List item 2</span></span>
- <span data-ttu-id="955b4-138">Liste öğesi 3</span><span class="sxs-lookup"><span data-stu-id="955b4-138">List item 3</span></span>

<span data-ttu-id="955b4-139">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="955b4-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="955b4-140">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="955b4-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="955b4-141">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="955b4-141">will be rendered as:</span></span>

- <span data-ttu-id="955b4-142">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="955b4-142">List item 1</span></span>
  - <span data-ttu-id="955b4-143">Liste öğesi A</span><span class="sxs-lookup"><span data-stu-id="955b4-143">List item A</span></span>
  - <span data-ttu-id="955b4-144">Liste öğesi B</span><span class="sxs-lookup"><span data-stu-id="955b4-144">List item B</span></span>
- <span data-ttu-id="955b4-145">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="955b4-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="955b4-146">Sıralı liste</span><span class="sxs-lookup"><span data-stu-id="955b4-146">Ordered list</span></span>

<span data-ttu-id="955b4-147">Sıralı/adımlı bir listeyi biçimlendirmek için sıra numaraları kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="955b4-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="955b4-148">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="955b4-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="955b4-149">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="955b4-149">will be rendered as:</span></span>

1. <span data-ttu-id="955b4-150">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="955b4-150">First instruction</span></span>
2. <span data-ttu-id="955b4-151">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="955b4-151">Second instruction</span></span>
3. <span data-ttu-id="955b4-152">Üçüncü yönerge</span><span class="sxs-lookup"><span data-stu-id="955b4-152">Third instruction</span></span>

<span data-ttu-id="955b4-153">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="955b4-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="955b4-154">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="955b4-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="955b4-155">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="955b4-155">will be rendered as:</span></span>

1. <span data-ttu-id="955b4-156">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="955b4-156">First instruction</span></span>
   1. <span data-ttu-id="955b4-157">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="955b4-157">Sub-instruction</span></span>
   2. <span data-ttu-id="955b4-158">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="955b4-158">Sub-instruction</span></span>
2. <span data-ttu-id="955b4-159">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="955b4-159">Second instruction</span></span>

<span data-ttu-id="955b4-160">Tüm girişler için “1.”</span><span class="sxs-lookup"><span data-stu-id="955b4-160">Note that we use '1.'</span></span> <span data-ttu-id="955b4-161">kullandığımıza dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="955b4-161">for all entries.</span></span> <span data-ttu-id="955b4-162">Böylece sonraki güncelleştirmelerde yeni adımlar eklendiğinde veya mevcut adımlar çıkarıldığında, değişiklikleri gözden geçirmek kolaylaşır.</span><span class="sxs-lookup"><span data-stu-id="955b4-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="955b4-163">eğlence</span><span class="sxs-lookup"><span data-stu-id="955b4-163">Tables</span></span>

<span data-ttu-id="955b4-164">Tablolar, temel Markdown belirtiminin parçası değildir, ancak GFM tarafından desteklenir.</span><span class="sxs-lookup"><span data-stu-id="955b4-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="955b4-165">Düz çizgi (|) ve kısa çizgi (-) karakterlerini kullanarak tablolar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="955b4-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="955b4-166">Kısa çizgiler sütunların üst bilgisini oluştururken düz çizgiler sütunları birbirinden ayırır.</span><span class="sxs-lookup"><span data-stu-id="955b4-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="955b4-167">Tablonun doğru işlenebilmesi için başına boş bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="955b4-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="955b4-168">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="955b4-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="955b4-169">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="955b4-169">will be rendered as:</span></span>

| <span data-ttu-id="955b4-170">Tablolar</span><span class="sxs-lookup"><span data-stu-id="955b4-170">Fun</span></span>                  | <span data-ttu-id="955b4-171">Şununla:</span><span class="sxs-lookup"><span data-stu-id="955b4-171">With</span></span>                 | <span data-ttu-id="955b4-172">eğlence</span><span class="sxs-lookup"><span data-stu-id="955b4-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="955b4-173">sola hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="955b4-173">left-aligned column</span></span>  | <span data-ttu-id="955b4-174">sağa hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="955b4-174">right-aligned column</span></span> | <span data-ttu-id="955b4-175">ortalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="955b4-175">centered column</span></span> |
| <span data-ttu-id="955b4-176">100 $</span><span class="sxs-lookup"><span data-stu-id="955b4-176">$100</span></span>                 | <span data-ttu-id="955b4-177">100 $</span><span class="sxs-lookup"><span data-stu-id="955b4-177">$100</span></span>                 | <span data-ttu-id="955b4-178">100 $</span><span class="sxs-lookup"><span data-stu-id="955b4-178">$100</span></span>            |
| <span data-ttu-id="955b4-179">10 $</span><span class="sxs-lookup"><span data-stu-id="955b4-179">$10</span></span>                  | <span data-ttu-id="955b4-180">10 $</span><span class="sxs-lookup"><span data-stu-id="955b4-180">$10</span></span>                  | <span data-ttu-id="955b4-181">10 $</span><span class="sxs-lookup"><span data-stu-id="955b4-181">$10</span></span>             |
| <span data-ttu-id="955b4-182">1 $</span><span class="sxs-lookup"><span data-stu-id="955b4-182">$1</span></span>                   | <span data-ttu-id="955b4-183">1 $</span><span class="sxs-lookup"><span data-stu-id="955b4-183">$1</span></span>                   | <span data-ttu-id="955b4-184">1 $</span><span class="sxs-lookup"><span data-stu-id="955b4-184">$1</span></span>              |

<span data-ttu-id="955b4-185">Tablo oluşturma hakkında daha fazla bilgi için şunlara bakın:</span><span class="sxs-lookup"><span data-stu-id="955b4-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="955b4-186">Geniş tabloların biçimlendirmesinde yardımcı olabilecek Markdig [tablo sarmalama özelliği](#table-wrapping).</span><span class="sxs-lookup"><span data-stu-id="955b4-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="955b4-187">GitHub’ın [Tablolarla bilgi düzenleme](https://help.github.com/articles/organizing-information-with-tables/) makalesi.</span><span class="sxs-lookup"><span data-stu-id="955b4-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="955b4-188">[Markdown Tablo Oluşturucu](https://www.tablesgenerator.com/markdown_tables) web uygulaması.</span><span class="sxs-lookup"><span data-stu-id="955b4-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="955b4-189">[Adam Pritchard - Markdown Hızlı Başvuru Kılavuzu](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span><span class="sxs-lookup"><span data-stu-id="955b4-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="955b4-190">[Michel Fortin - Markdown Ekstra](https://michelf.ca/projects/php-markdown/extra/#table).</span><span class="sxs-lookup"><span data-stu-id="955b4-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="955b4-191">[HTML tablolarını Markdown’a dönüştürme](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="955b4-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="955b4-192">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="955b4-192">Links</span></span>

<span data-ttu-id="955b4-193">Satır içi bağlantılarda Markdown söz dizimi, köprü bağlantısı eklenecek `[link text]` metni ve bağlantı verilen URL ya da dosya adı olan `(file-name.md)` kısımlarından oluşur:</span><span class="sxs-lookup"><span data-stu-id="955b4-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="955b4-194">Bağlantı verme hakkında daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="955b4-194">For more information on linking, see:</span></span>

- <span data-ttu-id="955b4-195">Markdown’ın temel bağlantı desteği konusunda ayrıntılar için [Markdown söz dizimi kılavuzu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="955b4-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="955b4-196">Markdig tarafından sağlanan ilave bağlayıcı söz dizimi hakkında ayrıntılar için bu kılavuzun [Bağlantılar](how-to-write-links.md) bölümü.</span><span class="sxs-lookup"><span data-stu-id="955b4-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="955b4-197">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="955b4-197">Code snippets</span></span>

<span data-ttu-id="955b4-198">Markdown, hem bir cümlede satır içi olarak hem de cümleler arasında ayrı “çevrelenmiş” bir blok halinde kod parçacıkları yerleştirilmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="955b4-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="955b4-199">Ayrıntılar için bkz.</span><span class="sxs-lookup"><span data-stu-id="955b4-199">For details, see:</span></span>

- [<span data-ttu-id="955b4-200">Kod blokları için yerel Markdown desteği</span><span class="sxs-lookup"><span data-stu-id="955b4-200">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="955b4-201">Kod çevreleme ve söz dizimi vurgulama için GFM desteği</span><span class="sxs-lookup"><span data-stu-id="955b4-201">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="955b4-202">Çevrelenmiş kod blokları, kod parçacıklarınız için söz dizimi vurgulamasını etkinleştirmenin kolay bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="955b4-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="955b4-203">Çevrelenmiş kod bloklarının biçimi genelde şöyledir:</span><span class="sxs-lookup"><span data-stu-id="955b4-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="955b4-204">İlk üç ters tırnak (\`) karakterinden sonra gelen diğer ad, kullanılacak söz dizimi vurgulamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="955b4-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="955b4-205">Docs içeriğinde yaygın olarak kullanılan programlama dilleri ve bunların etiketleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="955b4-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="955b4-206">Bu diller, kolay as desteğine ve dil vurgulamasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="955b4-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="955b4-207">Ad</span><span class="sxs-lookup"><span data-stu-id="955b4-207">Name</span></span>|<span data-ttu-id="955b4-208">Markdown Etiketi</span><span class="sxs-lookup"><span data-stu-id="955b4-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="955b4-209">.NET Konsolu</span><span class="sxs-lookup"><span data-stu-id="955b4-209">.NET Console</span></span>|<span data-ttu-id="955b4-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="955b4-210">dotnetcli</span></span>|
|<span data-ttu-id="955b4-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="955b4-211">ASP.NET (C#)</span></span>|<span data-ttu-id="955b4-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="955b4-212">aspx-csharp</span></span>|
|<span data-ttu-id="955b4-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="955b4-213">ASP.NET (VB)</span></span>|<span data-ttu-id="955b4-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="955b4-214">aspx-vb</span></span>|
|<span data-ttu-id="955b4-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="955b4-215">AzCopy</span></span>|<span data-ttu-id="955b4-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="955b4-216">azcopy</span></span>|
|<span data-ttu-id="955b4-217">Azure CLI’si</span><span class="sxs-lookup"><span data-stu-id="955b4-217">Azure CLI</span></span>|<span data-ttu-id="955b4-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="955b4-218">azurecli</span></span>|
|<span data-ttu-id="955b4-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="955b4-219">Azure PowerShell</span></span>|<span data-ttu-id="955b4-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="955b4-220">azurepowershell</span></span>|
|<span data-ttu-id="955b4-221">C++</span><span class="sxs-lookup"><span data-stu-id="955b4-221">C++</span></span>|<span data-ttu-id="955b4-222">cpp</span><span class="sxs-lookup"><span data-stu-id="955b4-222">cpp</span></span>|
|<span data-ttu-id="955b4-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="955b4-223">C++/CX</span></span>|<span data-ttu-id="955b4-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="955b4-224">cppcx</span></span>|
|<span data-ttu-id="955b4-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="955b4-225">C++/WinRT</span></span>|<span data-ttu-id="955b4-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="955b4-226">cppwinrt</span></span>|
|<span data-ttu-id="955b4-227">C#</span><span class="sxs-lookup"><span data-stu-id="955b4-227">C#</span></span>|<span data-ttu-id="955b4-228">csharp</span><span class="sxs-lookup"><span data-stu-id="955b4-228">csharp</span></span>|
|<span data-ttu-id="955b4-229">Tarayıcıda C#</span><span class="sxs-lookup"><span data-stu-id="955b4-229">C# in browser</span></span>|<span data-ttu-id="955b4-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="955b4-230">csharp-interactive</span></span>|
|<span data-ttu-id="955b4-231">Konsol</span><span class="sxs-lookup"><span data-stu-id="955b4-231">Console</span></span>|<span data-ttu-id="955b4-232">konsol</span><span class="sxs-lookup"><span data-stu-id="955b4-232">console</span></span>|
|<span data-ttu-id="955b4-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="955b4-233">CSHTML</span></span>|<span data-ttu-id="955b4-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="955b4-234">cshtml</span></span>|
|<span data-ttu-id="955b4-235">DAX</span><span class="sxs-lookup"><span data-stu-id="955b4-235">DAX</span></span>|<span data-ttu-id="955b4-236">dax</span><span class="sxs-lookup"><span data-stu-id="955b4-236">dax</span></span>|
|<span data-ttu-id="955b4-237">F#</span><span class="sxs-lookup"><span data-stu-id="955b4-237">F#</span></span>|<span data-ttu-id="955b4-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="955b4-238">fsharp</span></span>|
|<span data-ttu-id="955b4-239">Go</span><span class="sxs-lookup"><span data-stu-id="955b4-239">Go</span></span>|<span data-ttu-id="955b4-240">go</span><span class="sxs-lookup"><span data-stu-id="955b4-240">go</span></span>|
|<span data-ttu-id="955b4-241">HTML</span><span class="sxs-lookup"><span data-stu-id="955b4-241">HTML</span></span>|<span data-ttu-id="955b4-242">html</span><span class="sxs-lookup"><span data-stu-id="955b4-242">html</span></span>|
|<span data-ttu-id="955b4-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="955b4-243">HTTP</span></span>|<span data-ttu-id="955b4-244">http</span><span class="sxs-lookup"><span data-stu-id="955b4-244">http</span></span>|
|<span data-ttu-id="955b4-245">Java</span><span class="sxs-lookup"><span data-stu-id="955b4-245">Java</span></span>|<span data-ttu-id="955b4-246">java</span><span class="sxs-lookup"><span data-stu-id="955b4-246">java</span></span>|
|<span data-ttu-id="955b4-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="955b4-247">JavaScript</span></span>|<span data-ttu-id="955b4-248">javascript</span><span class="sxs-lookup"><span data-stu-id="955b4-248">javascript</span></span>|
|<span data-ttu-id="955b4-249">JSON</span><span class="sxs-lookup"><span data-stu-id="955b4-249">JSON</span></span>|<span data-ttu-id="955b4-250">json</span><span class="sxs-lookup"><span data-stu-id="955b4-250">json</span></span>|
|<span data-ttu-id="955b4-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="955b4-251">Markdown</span></span>|<span data-ttu-id="955b4-252">md</span><span class="sxs-lookup"><span data-stu-id="955b4-252">md</span></span>|
|<span data-ttu-id="955b4-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="955b4-253">NodeJS</span></span>|<span data-ttu-id="955b4-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="955b4-254">nodejs</span></span>|
|<span data-ttu-id="955b4-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="955b4-255">Objective-C</span></span>|<span data-ttu-id="955b4-256">objc</span><span class="sxs-lookup"><span data-stu-id="955b4-256">objc</span></span>|
|<span data-ttu-id="955b4-257">OData</span><span class="sxs-lookup"><span data-stu-id="955b4-257">OData</span></span>|<span data-ttu-id="955b4-258">odata</span><span class="sxs-lookup"><span data-stu-id="955b4-258">odata</span></span>|
|<span data-ttu-id="955b4-259">PHP</span><span class="sxs-lookup"><span data-stu-id="955b4-259">PHP</span></span>|<span data-ttu-id="955b4-260">php</span><span class="sxs-lookup"><span data-stu-id="955b4-260">php</span></span>|
|<span data-ttu-id="955b4-261">PowerApps (nokta ondalık ayırıcısı)</span><span class="sxs-lookup"><span data-stu-id="955b4-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="955b4-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="955b4-262">powerapps-dot</span></span>|
|<span data-ttu-id="955b4-263">PowerApps (virgül ondalık ayırıcısı)</span><span class="sxs-lookup"><span data-stu-id="955b4-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="955b4-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="955b4-264">powerapps-comma</span></span>|
|<span data-ttu-id="955b4-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="955b4-265">PowerShell</span></span>|<span data-ttu-id="955b4-266">powershell</span><span class="sxs-lookup"><span data-stu-id="955b4-266">powershell</span></span>|
|<span data-ttu-id="955b4-267">Python</span><span class="sxs-lookup"><span data-stu-id="955b4-267">Python</span></span>|<span data-ttu-id="955b4-268">python</span><span class="sxs-lookup"><span data-stu-id="955b4-268">python</span></span>|
|<span data-ttu-id="955b4-269">Q#</span><span class="sxs-lookup"><span data-stu-id="955b4-269">Q#</span></span>|<span data-ttu-id="955b4-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="955b4-270">qsharp</span></span>|
|<span data-ttu-id="955b4-271">R</span><span class="sxs-lookup"><span data-stu-id="955b4-271">R</span></span>|<span data-ttu-id="955b4-272">r</span><span class="sxs-lookup"><span data-stu-id="955b4-272">r</span></span>|
|<span data-ttu-id="955b4-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="955b4-273">Ruby</span></span>|<span data-ttu-id="955b4-274">ruby</span><span class="sxs-lookup"><span data-stu-id="955b4-274">ruby</span></span>|
|<span data-ttu-id="955b4-275">SQL</span><span class="sxs-lookup"><span data-stu-id="955b4-275">SQL</span></span>|<span data-ttu-id="955b4-276">sql</span><span class="sxs-lookup"><span data-stu-id="955b4-276">sql</span></span>|
|<span data-ttu-id="955b4-277">Swift</span><span class="sxs-lookup"><span data-stu-id="955b4-277">Swift</span></span>|<span data-ttu-id="955b4-278">swift</span><span class="sxs-lookup"><span data-stu-id="955b4-278">swift</span></span>|
|<span data-ttu-id="955b4-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="955b4-279">TypeScript</span></span>|<span data-ttu-id="955b4-280">typescript</span><span class="sxs-lookup"><span data-stu-id="955b4-280">typescript</span></span>|
|<span data-ttu-id="955b4-281">VB</span><span class="sxs-lookup"><span data-stu-id="955b4-281">VB</span></span>|<span data-ttu-id="955b4-282">vb</span><span class="sxs-lookup"><span data-stu-id="955b4-282">vb</span></span>|
|<span data-ttu-id="955b4-283">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="955b4-283">VSTS CLI</span></span>|<span data-ttu-id="955b4-284">vstscli</span><span class="sxs-lookup"><span data-stu-id="955b4-284">vstscli</span></span>|
|<span data-ttu-id="955b4-285">XAML</span><span class="sxs-lookup"><span data-stu-id="955b4-285">XAML</span></span>|<span data-ttu-id="955b4-286">xaml</span><span class="sxs-lookup"><span data-stu-id="955b4-286">xaml</span></span>|
|<span data-ttu-id="955b4-287">XML</span><span class="sxs-lookup"><span data-stu-id="955b4-287">XML</span></span>|<span data-ttu-id="955b4-288">xml</span><span class="sxs-lookup"><span data-stu-id="955b4-288">xml</span></span>|

<span data-ttu-id="955b4-289">`csharp-interactive` adı, C# bilgisayar dilini ve tarayıcıdan örnek çalıştırma becerisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="955b4-289">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="955b4-290">Bu kod parçacıkları, bir Docker kapsayıcısında derlenir ve yürütülür. Bu program yürütüldüğünde ortaya çıkan sonuçlar kullanıcının tarayıcı penceresinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="955b4-290">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="955b4-291">Örnek: C\#</span><span class="sxs-lookup"><span data-stu-id="955b4-291">Example: C\#</span></span>

<span data-ttu-id="955b4-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="955b4-292">__Markdown__</span></span>

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

<span data-ttu-id="955b4-293">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="955b4-293">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="955b4-294">Örnek: SQL</span><span class="sxs-lookup"><span data-stu-id="955b4-294">Example: SQL</span></span>

<span data-ttu-id="955b4-295">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="955b4-295">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="955b4-296">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="955b4-296">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="955b4-297">OPS özel Markdown uzantıları</span><span class="sxs-lookup"><span data-stu-id="955b4-297">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="955b4-298">Open Publishing Services (OPS), GitHub Flavored Markdown (GFM) ile yüksek uyumluluğa sahip olan Markdown için Markdig Ayrıştırıcısı’nı uygular.</span><span class="sxs-lookup"><span data-stu-id="955b4-298">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="955b4-299">Markdig, Markdown uzantıları aracılığıyla ilave işlevsellik sağlar.</span><span class="sxs-lookup"><span data-stu-id="955b4-299">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="955b4-300">Bu nedenle, tam OPS Yazma Kılavuzundan bazı makaleler başvuru için bu kılavuza dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="955b4-300">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="955b4-301">(Örneğin, içindekiler bölümünde "Markdig ve Markdown uzantıları" ile "Kod parçacıkları" kısımlarına bakın.)</span><span class="sxs-lookup"><span data-stu-id="955b4-301">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="955b4-302">Docs makaleleri çoğu zaman paragraflar, bağlantılar, listeler ve bölüm başlıkları gibi makale biçimlendirmeleri için GFM’yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="955b4-302">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="955b4-303">Makaleler, daha zengin biçimlendirme için aşağıdakiler gibi Markdig özelliklerini kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="955b4-303">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="955b4-304">Not blokları</span><span class="sxs-lookup"><span data-stu-id="955b4-304">Note blocks</span></span>
- <span data-ttu-id="955b4-305">Dosyaları dahil et</span><span class="sxs-lookup"><span data-stu-id="955b4-305">Include files</span></span>
- <span data-ttu-id="955b4-306">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="955b4-306">Selectors</span></span>
- <span data-ttu-id="955b4-307">Ekli videolar</span><span class="sxs-lookup"><span data-stu-id="955b4-307">Embedded videos</span></span>
- <span data-ttu-id="955b4-308">Kod parçacıkları/örnekleri</span><span class="sxs-lookup"><span data-stu-id="955b4-308">Code snippets/samples</span></span>

<span data-ttu-id="955b4-309">Tam bir liste için içerikler bölümünde “Markdig ve Markdown uzantıları” ve “Kod parçacıkları” kısmına bakın.</span><span class="sxs-lookup"><span data-stu-id="955b4-309">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="955b4-310">Not blokları</span><span class="sxs-lookup"><span data-stu-id="955b4-310">Note blocks</span></span>

<span data-ttu-id="955b4-311">İlgiyi belirli bir içeriğe çekmek için dört çeşit not blokundan birini seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="955b4-311">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="955b4-312">NOT</span><span class="sxs-lookup"><span data-stu-id="955b4-312">NOTE</span></span>
- <span data-ttu-id="955b4-313">UYARI</span><span class="sxs-lookup"><span data-stu-id="955b4-313">WARNING</span></span>
- <span data-ttu-id="955b4-314">İPUCU</span><span class="sxs-lookup"><span data-stu-id="955b4-314">TIP</span></span>
- <span data-ttu-id="955b4-315">ÖNEMLİ</span><span class="sxs-lookup"><span data-stu-id="955b4-315">IMPORTANT</span></span>

<span data-ttu-id="955b4-316">Genel olarak not bloklarını fazla kullanmaktan kaçınmalısınız, dikkat dağıtıcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="955b4-316">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="955b4-317">Not bloklarında kod blokları, görüntüler, listeler ve bağlantılar destekleniyor olsa da bunları olabildiğince sade ve düz bir şekilde oluşturun.</span><span class="sxs-lookup"><span data-stu-id="955b4-317">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="955b4-318">Örnekler:</span><span class="sxs-lookup"><span data-stu-id="955b4-318">Examples:</span></span>

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

<span data-ttu-id="955b4-319">Bunlar aşağıdaki gibi işlenir:</span><span class="sxs-lookup"><span data-stu-id="955b4-319">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="955b4-320">Bu bir NOT’tur</span><span class="sxs-lookup"><span data-stu-id="955b4-320">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="955b4-321">Bu bir UYARI’dır</span><span class="sxs-lookup"><span data-stu-id="955b4-321">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="955b4-322">Bu bir İPUCU’dur</span><span class="sxs-lookup"><span data-stu-id="955b4-322">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="955b4-323">Bu ÖNEMLİ’dir</span><span class="sxs-lookup"><span data-stu-id="955b4-323">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="955b4-324">Dosyaları dahil et</span><span class="sxs-lookup"><span data-stu-id="955b4-324">Include files</span></span>

<span data-ttu-id="955b4-325">Makale dosyalarına dahil edilmesi gereken yeniden kullanılabilir metin veya görüntü dosyalarınız varsa dosyayı Markdig dosya dahil etme özelliği ile “dahil etmek” için bir başvuru kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="955b4-325">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="955b4-326">Bu özellik, verilen dosyayı makalenize derleme sırasında “eklemesi” için OPS’yi yönlendirir, böylece dosya da yayımlanan makalenizin bir parçası olur.</span><span class="sxs-lookup"><span data-stu-id="955b4-326">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="955b4-327">İçerikleri tekrar kullanmanıza imkan veren üç tür ekleme başvurusu vardır:</span><span class="sxs-lookup"><span data-stu-id="955b4-327">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="955b4-328">Satır İçi: Genel bir metin parçacığını başka bir cümlede satır içinde yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="955b4-328">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="955b4-329">Blok: Makalenin bir bölümündeki bütün bir Markdown dosyasını yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="955b4-329">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="955b4-330">Görüntü: Docs’ta standart görüntü ekleme yoludur.</span><span class="sxs-lookup"><span data-stu-id="955b4-330">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="955b4-331">Satır içi ve blok ekleme dosyaları, basit birer Markdown (.md) dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="955b4-331">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="955b4-332">Bu dosyalar, herhangi bir geçerli Markdown barındırabilir.</span><span class="sxs-lookup"><span data-stu-id="955b4-332">It can contain any valid Markdown.</span></span> <span data-ttu-id="955b4-333">Tüm ekleme Markdown dosyaları, depo kökünde [ortak bir `/includes` alt dizinine](git-github-fundamentals.md#includes-subdirectory) yerleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="955b4-333">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="955b4-334">Makale yayımlandığında, eklenen dosya makaleyle sorunsuz bir şekilde tümleşmiş olur.</span><span class="sxs-lookup"><span data-stu-id="955b4-334">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="955b4-335">Ekleme dosyalarına yönelik gereksinimler ve önemli konular şunlardır:</span><span class="sxs-lookup"><span data-stu-id="955b4-335">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="955b4-336">Aynı metni birden fazla makalede kullanmanız gerektiği zaman ekleme dosyalarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="955b4-336">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="955b4-337">Bir veya iki paragraf, paylaşılan bir yordam veya paylaşılan bir bölüm gibi büyük içeriklerde blok ekleme başvurusunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="955b4-337">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="955b4-338">Ancak bir cümleden daha küçük şeyler için kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="955b4-338">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="955b4-339">Ekleme başvuruları, Markdig uzantılarına bağlı olduğu için makalenizin GitHub tarafından işlenmiş görünümünde işlenmez.</span><span class="sxs-lookup"><span data-stu-id="955b4-339">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="955b4-340">Bunlar yalnızca yayın sonrasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="955b4-340">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="955b4-341">Ekleme dosyasına başvuran makalelerdeki ekleme dosyalarında bütün metnin, öncesinde veya sonrasında gelen metinden bağımsız tam cümleler veya ifadeler şeklinde olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="955b4-341">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="955b4-342">Bu kılavuzu dikkate almamak, makalede çevrilemeyen bir satır oluşturur ve yerelleştirme deneyimini bozar.</span><span class="sxs-lookup"><span data-stu-id="955b4-342">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="955b4-343">Ekleme başvurularını diğer ekleme dosyalarına eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="955b4-343">Don't embed include references within other include files.</span></span> <span data-ttu-id="955b4-344">Bu, desteklenmeyen bir durumdur.</span><span class="sxs-lookup"><span data-stu-id="955b4-344">They are not supported.</span></span>
- <span data-ttu-id="955b4-345">Medya dosyalarını ekleme alt dizinine özgü bir medya klasörüne yerleştirin, örneğin `<repo>`/eklemeler/medya klasörü.</span><span class="sxs-lookup"><span data-stu-id="955b4-345">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="955b4-346">Medya dizini, kökünde hiçbir görüntü barındırmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="955b4-346">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="955b4-347">Ekleme dosyasında görüntü yoksa buna karşılık gelecek bir medya dizini gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="955b4-347">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="955b4-348">Normal makalelerde olduğu gibi, ekleme dosyaları arasında medya paylaşmayın.</span><span class="sxs-lookup"><span data-stu-id="955b4-348">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="955b4-349">Her bir ekleme dosyası ve makale için benzersiz ada sahip ayrı dosyalar kullanın.</span><span class="sxs-lookup"><span data-stu-id="955b4-349">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="955b4-350">Medya dosyasını, ekleme dosyasıyla ilişkili medya klasöründe depolayın.</span><span class="sxs-lookup"><span data-stu-id="955b4-350">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="955b4-351">Ekleme dosyalarını bir makaledeki tek içerik olacak şekilde kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="955b4-351">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="955b4-352">Ekleme dosyaları, makaledeki diğer içerikleri tamamlayıcı niteliktedir.</span><span class="sxs-lookup"><span data-stu-id="955b4-352">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="955b4-353">Örnek:</span><span class="sxs-lookup"><span data-stu-id="955b4-353">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="955b4-354">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="955b4-354">Selectors</span></span>

<span data-ttu-id="955b4-355">Seçicileri teknik makalelerde, aynı makalenin farklı bölümlerini yazdığınızda teknolojiler veya platformlar arasındaki uygulama farklılıklarına değinirken kullanın.</span><span class="sxs-lookup"><span data-stu-id="955b4-355">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="955b4-356">Bu genellikle geliştiriciler için mobil platform içeriklerimizde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="955b4-356">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="955b4-357">Markdig’de şu anda iki farklı türde seçici vardır; tekli seçici ve çoklu seçici.</span><span class="sxs-lookup"><span data-stu-id="955b4-357">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="955b4-358">Seçimdeki her bir makaleye aynı seçici Markdown gittiği için makalenizin seçicisini bir ekleme dosyasına koymanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="955b4-358">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="955b4-359">Daha sonra aynı seçiciyi kullanan tüm makalelerinizde bu ekleme dosyasına başvurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="955b4-359">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="955b4-360">Aşağıdaki kodda bir seçici örneği gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="955b4-360">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="955b4-361">[Azure belgelerinde](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic) seçicilerin nasıl kullanıldığının örneklerini bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="955b4-361">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="955b4-362">Kod ekleme başvuruları</span><span class="sxs-lookup"><span data-stu-id="955b4-362">Code include references</span></span>

<span data-ttu-id="955b4-363">Markdig, bir makaleye kod parçacığı uzantısı aracılığıyla gelişmiş kod eklemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="955b4-363">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="955b4-364">Programlama dili seçimi ve söz dizimi renklendirme gibi GFM özellikleri üzerinde ortaya çıkan gelişmiş işleme seçenekleri sağlar, bunların yanında aşağıdaki gibi kullanışlı özellikler de getirir:</span><span class="sxs-lookup"><span data-stu-id="955b4-364">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="955b4-365">Bir dış depodan gelen merkezi kod örnekleri/parçacıklarının eklenmesi.</span><span class="sxs-lookup"><span data-stu-id="955b4-365">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="955b4-366">Kod örneklerinin farklı dillerdeki birçok çeşidini gösteren sekmeli kullanıcı arabirimi.</span><span class="sxs-lookup"><span data-stu-id="955b4-366">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="955b4-367">Tuzaklar ve sorun giderme</span><span class="sxs-lookup"><span data-stu-id="955b4-367">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="955b4-368">Alternatif metin</span><span class="sxs-lookup"><span data-stu-id="955b4-368">Alt text</span></span>

<span data-ttu-id="955b4-369">Alt çizgi içeren alternatif metin düzgün bir şekilde işlenmez.</span><span class="sxs-lookup"><span data-stu-id="955b4-369">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="955b4-370">Örneğin, şunu kullanmak yerine:</span><span class="sxs-lookup"><span data-stu-id="955b4-370">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="955b4-371">Şunun gibi alt çizgilerden kaçının:</span><span class="sxs-lookup"><span data-stu-id="955b4-371">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="955b4-372">Kesme işareti ve tırnak işaretleri</span><span class="sxs-lookup"><span data-stu-id="955b4-372">Apostrophes and quotation marks</span></span>

<span data-ttu-id="955b4-373">Word dosyasından Markdown editörüne bir şey kopyalarsanız kopyaladığınız metin “akıllı” (kıvrık) kesme işaretleri veya tırnak işaretleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="955b4-373">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="955b4-374">Bunların kodlanması veya kesme işareti ya da tırnak işaretlerine dönüştürülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="955b4-374">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="955b4-375">Aksi takdirde, dosya yayımlandığında şöyle karakterler görebilirsiniz: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="955b4-375">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="955b4-376">Bu noktalama işaretlerinin “akıllı” olanları için kodlamalar aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="955b4-376">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="955b4-377">Sol (açma) tırnak işareti: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="955b4-377">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="955b4-378">Sağ (kapatma) tırnak işareti: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="955b4-378">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="955b4-379">Sağ (kapatma) tekli tırnak işareti veya kesme işareti: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="955b4-379">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="955b4-380">Sağ (açma) tekli tırnak işareti (nadiren kullanılır): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="955b4-380">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="955b4-381">Açılı ayraçlar</span><span class="sxs-lookup"><span data-stu-id="955b4-381">Angle brackets</span></span>

<span data-ttu-id="955b4-382">Bir yer tutucuyu ifade etmek için köşeli ayraç kullanımı yaygındır.</span><span class="sxs-lookup"><span data-stu-id="955b4-382">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="955b4-383">Metinde (kodda değil) bunu yaptığınızda, köşeli ayraçları kodlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="955b4-383">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="955b4-384">Aksi takdirde Markdown bunların HTML etiketleri olması gerektiğini düşünür.</span><span class="sxs-lookup"><span data-stu-id="955b4-384">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="955b4-385">Örneğin `<script name>` öğesini `&lt;script name&gt;` şeklinde kodlayın</span><span class="sxs-lookup"><span data-stu-id="955b4-385">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="955b4-386">Ayrıca bkz.:</span><span class="sxs-lookup"><span data-stu-id="955b4-386">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="955b4-387">Markdown kaynakları</span><span class="sxs-lookup"><span data-stu-id="955b4-387">Markdown resources</span></span>

- [<span data-ttu-id="955b4-388">Markdown’a Giriş</span><span class="sxs-lookup"><span data-stu-id="955b4-388">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="955b4-389">Docs Markdown kural sayfası</span><span class="sxs-lookup"><span data-stu-id="955b4-389">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="955b4-390">GitHub Markdown Temel Bilgileri</span><span class="sxs-lookup"><span data-stu-id="955b4-390">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="955b4-391">Markdown Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="955b4-391">The Markdown Guide</span></span>](https://www.markdownguide.org/)
