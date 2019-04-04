---
title: Docs’ta makale yazmak için Markdown kullanma
description: Bu makale, docs.microsoft.com makalelerinde kullanılan Markdown dilinin temellerini ve başvuru bilgilerini sağlar.
ms.date: 03/26/2019
ms.openlocfilehash: eeb49961fbf530676b55ae4e42d4fca7b8d7edf7
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637495"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="f0553-103">Docs’ta makale yazmak için Markdown kullanma</span><span class="sxs-lookup"><span data-stu-id="f0553-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="f0553-104">[Docs.microsoft.com](http://docs.microsoft.com) makaleleri, [Markdown](https://daringfireball.net/projects/markdown/) adı verilen hafif biçimlendirme dilinde yazılır. Bu dilin okunması ve öğrenilmesi kolaydır.</span><span class="sxs-lookup"><span data-stu-id="f0553-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="f0553-105">O nedenle bu dil kısa sürede endüstri standardı haline gelmiştir.</span><span class="sxs-lookup"><span data-stu-id="f0553-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="f0553-106">Belgeler sitesi Markdown’ın [Markdig varyantını](#markdown-flavor) kullanır.</span><span class="sxs-lookup"><span data-stu-id="f0553-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="f0553-107">Markdown temel bilgileri</span><span class="sxs-lookup"><span data-stu-id="f0553-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="f0553-108">Bölüm başlıkları</span><span class="sxs-lookup"><span data-stu-id="f0553-108">Headings</span></span>

<span data-ttu-id="f0553-109">Bir bölüm başlığı oluşturmak için karma işaretini (#) aşağıdaki gibi kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="f0553-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="f0553-110">Bölüm başlıkları, atx-style kullanılarak hazırlanmalıdır. Yani satırın başında, arkasından gelen kısmın bölüm başlığı olduğunu belirtmek için H1-H6 HTML başlık düzeyine karşılık gelecek şekilde 1-6 kare karakter (#) kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0553-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="f0553-111">Bir ila dördüncü düzey bölüm başlığı örnekleri yukarıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="f0553-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="f0553-112">Konunuz içerisinde yalnızca bir adet birinci düzey bölüm başlığı (H1) **olmalıdır** ve bu, sayfa başlığı olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f0553-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="f0553-113">Başlığınız `#` karakteriyle bitiyorsa başlığın doğru işlenmesi için sonuna fazladan bir `#` karakteri eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f0553-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="f0553-114">Örneğin `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="f0553-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="f0553-115">İkinci düzey bölüm başlıkları, sayfa başlığının altındaki “Bu makalede” bölümünde yer alan İçindekiler (TOC) bölümünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0553-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="f0553-116">Kalın ve italik metin</span><span class="sxs-lookup"><span data-stu-id="f0553-116">Bold and italic text</span></span>

<span data-ttu-id="f0553-117">Bir metni **kalın** olarak biçimlendirmek için iki yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="f0553-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="f0553-118">Bir metni *italik* olarak biçimlendirmek için bir yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="f0553-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="f0553-119">Bir metni ***kalın ve italik*** olarak biçimlendirmek için üç yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="f0553-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="f0553-120">Blok alıntılar</span><span class="sxs-lookup"><span data-stu-id="f0553-120">Blockquotes</span></span>

<span data-ttu-id="f0553-121">Blok alıntılar, `>` karakteri kullanılarak oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="f0553-121">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="f0553-122">Yukarıdaki örnek, şu şekilde işlenir:</span><span class="sxs-lookup"><span data-stu-id="f0553-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="f0553-123">Kuraklık, on milyon yıldır devam ediyordu ve korkunç kertenkelelerin egemenliği çoktan sona ermişti.</span><span class="sxs-lookup"><span data-stu-id="f0553-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="f0553-124">Burada, Ekvator’da, günün birinde Afrika olarak anılacak bu kıtada, var olmak için verilen savaşta vahşetin yeni bir zirvesine ulaşılmıştı ve ortada henüz bir galip yoktu.</span><span class="sxs-lookup"><span data-stu-id="f0553-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="f0553-125">Bu kıraç ve kuru topraklarda, yalnızca küçük, hızlı veya vahşi olanlar büyüyebilirdi, ya da hayatta kalmayı umut edebilirdi.</span><span class="sxs-lookup"><span data-stu-id="f0553-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="f0553-126">Listeler</span><span class="sxs-lookup"><span data-stu-id="f0553-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="f0553-127">Sırasız liste</span><span class="sxs-lookup"><span data-stu-id="f0553-127">Unordered list</span></span>

<span data-ttu-id="f0553-128">Sırasız/madde işaretli bir listeyi biçimlendirmek için yıldız işaretleri veya tireler kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0553-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="f0553-129">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="f0553-129">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="f0553-130">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="f0553-130">will be rendered as:</span></span>

- <span data-ttu-id="f0553-131">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="f0553-131">List item 1</span></span>
- <span data-ttu-id="f0553-132">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="f0553-132">List item 2</span></span>
- <span data-ttu-id="f0553-133">Liste öğesi 3</span><span class="sxs-lookup"><span data-stu-id="f0553-133">List item 3</span></span>

<span data-ttu-id="f0553-134">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="f0553-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="f0553-135">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="f0553-135">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="f0553-136">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="f0553-136">will be rendered as:</span></span>

- <span data-ttu-id="f0553-137">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="f0553-137">List item 1</span></span>
  - <span data-ttu-id="f0553-138">Liste öğesi A</span><span class="sxs-lookup"><span data-stu-id="f0553-138">List item A</span></span>
  - <span data-ttu-id="f0553-139">Liste öğesi B</span><span class="sxs-lookup"><span data-stu-id="f0553-139">List item B</span></span>
- <span data-ttu-id="f0553-140">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="f0553-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="f0553-141">Sıralı liste</span><span class="sxs-lookup"><span data-stu-id="f0553-141">Ordered list</span></span>

<span data-ttu-id="f0553-142">Sıralı/adımlı bir listeyi biçimlendirmek için sıra numaraları kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="f0553-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="f0553-143">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="f0553-143">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="f0553-144">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="f0553-144">will be rendered as:</span></span>

1. <span data-ttu-id="f0553-145">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="f0553-145">First instruction</span></span>
2. <span data-ttu-id="f0553-146">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="f0553-146">Second instruction</span></span>
3. <span data-ttu-id="f0553-147">Üçüncü yönerge</span><span class="sxs-lookup"><span data-stu-id="f0553-147">Third instruction</span></span>

<span data-ttu-id="f0553-148">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="f0553-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="f0553-149">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="f0553-149">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="f0553-150">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="f0553-150">will be rendered as:</span></span>

1. <span data-ttu-id="f0553-151">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="f0553-151">First instruction</span></span>
   1. <span data-ttu-id="f0553-152">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="f0553-152">Sub-instruction</span></span>
   2. <span data-ttu-id="f0553-153">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="f0553-153">Sub-instruction</span></span>
2. <span data-ttu-id="f0553-154">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="f0553-154">Second instruction</span></span>

<span data-ttu-id="f0553-155">Tüm girişler için “1.”</span><span class="sxs-lookup"><span data-stu-id="f0553-155">Note that we use '1.'</span></span> <span data-ttu-id="f0553-156">kullandığımıza dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f0553-156">for all entries.</span></span> <span data-ttu-id="f0553-157">Böylece sonraki güncelleştirmelerde yeni adımlar eklendiğinde veya mevcut adımlar çıkarıldığında, değişiklikleri gözden geçirmek kolaylaşır.</span><span class="sxs-lookup"><span data-stu-id="f0553-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="f0553-158">eğlence</span><span class="sxs-lookup"><span data-stu-id="f0553-158">Tables</span></span>

<span data-ttu-id="f0553-159">Tablolar, temel Markdown belirtiminin parçası değildir, ancak GFM tarafından desteklenir.</span><span class="sxs-lookup"><span data-stu-id="f0553-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="f0553-160">Düz çizgi (|) ve kısa çizgi (-) karakterlerini kullanarak tablolar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0553-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="f0553-161">Kısa çizgiler sütunların üst bilgisini oluştururken düz çizgiler sütunları birbirinden ayırır.</span><span class="sxs-lookup"><span data-stu-id="f0553-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="f0553-162">Tablonun doğru işlenebilmesi için başına boş bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f0553-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="f0553-163">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="f0553-163">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="f0553-164">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="f0553-164">will be rendered as:</span></span>

| <span data-ttu-id="f0553-165">Tablolar</span><span class="sxs-lookup"><span data-stu-id="f0553-165">Fun</span></span>                  | <span data-ttu-id="f0553-166">Şununla:</span><span class="sxs-lookup"><span data-stu-id="f0553-166">With</span></span>                 | <span data-ttu-id="f0553-167">eğlence</span><span class="sxs-lookup"><span data-stu-id="f0553-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="f0553-168">sola hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="f0553-168">left-aligned column</span></span>  | <span data-ttu-id="f0553-169">sağa hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="f0553-169">right-aligned column</span></span> | <span data-ttu-id="f0553-170">ortalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="f0553-170">centered column</span></span> |
| <span data-ttu-id="f0553-171">100 $</span><span class="sxs-lookup"><span data-stu-id="f0553-171">$100</span></span>                 | <span data-ttu-id="f0553-172">100 $</span><span class="sxs-lookup"><span data-stu-id="f0553-172">$100</span></span>                 | <span data-ttu-id="f0553-173">100 $</span><span class="sxs-lookup"><span data-stu-id="f0553-173">$100</span></span>            |
| <span data-ttu-id="f0553-174">10 $</span><span class="sxs-lookup"><span data-stu-id="f0553-174">$10</span></span>                  | <span data-ttu-id="f0553-175">10 $</span><span class="sxs-lookup"><span data-stu-id="f0553-175">$10</span></span>                  | <span data-ttu-id="f0553-176">10 $</span><span class="sxs-lookup"><span data-stu-id="f0553-176">$10</span></span>             |
| <span data-ttu-id="f0553-177">1 $</span><span class="sxs-lookup"><span data-stu-id="f0553-177">$1</span></span>                   | <span data-ttu-id="f0553-178">1 $</span><span class="sxs-lookup"><span data-stu-id="f0553-178">$1</span></span>                   | <span data-ttu-id="f0553-179">1 $</span><span class="sxs-lookup"><span data-stu-id="f0553-179">$1</span></span>              |

<span data-ttu-id="f0553-180">Tablo oluşturma hakkında daha fazla bilgi için şunlara bakın:</span><span class="sxs-lookup"><span data-stu-id="f0553-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="f0553-181">GitHub’ın [Tablolarla bilgi düzenleme](https://help.github.com/articles/organizing-information-with-tables/) makalesi.</span><span class="sxs-lookup"><span data-stu-id="f0553-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="f0553-182">[Markdown Tablo Oluşturucu](https://www.tablesgenerator.com/markdown_tables) web uygulaması.</span><span class="sxs-lookup"><span data-stu-id="f0553-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="f0553-183">[Adam Pritchard - Markdown Hızlı Başvuru Kılavuzu](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span><span class="sxs-lookup"><span data-stu-id="f0553-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="f0553-184">[Michel Fortin - Markdown Ekstra](https://michelf.ca/projects/php-markdown/extra/#table).</span><span class="sxs-lookup"><span data-stu-id="f0553-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="f0553-185">[HTML tablolarını Markdown’a dönüştürme](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="f0553-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="f0553-186">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="f0553-186">Links</span></span>

<span data-ttu-id="f0553-187">Satır içi bağlantılarda Markdown söz dizimi, köprü bağlantısı eklenecek `[link text]` metni ve bağlantı verilen URL ya da dosya adı olan `(file-name.md)` kısımlarından oluşur:</span><span class="sxs-lookup"><span data-stu-id="f0553-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="f0553-188">Bağlantı verme hakkında daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="f0553-188">For more information on linking, see:</span></span>

- <span data-ttu-id="f0553-189">Markdown’ın temel bağlantı desteği konusunda ayrıntılar için [Markdown söz dizimi kılavuzu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="f0553-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="f0553-190">Markdig tarafından sağlanan ilave bağlayıcı söz dizimi hakkında ayrıntılar için bu kılavuzun [Bağlantılar](how-to-write-links.md) bölümü.</span><span class="sxs-lookup"><span data-stu-id="f0553-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="f0553-191">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="f0553-191">Code snippets</span></span>

<span data-ttu-id="f0553-192">Markdown, hem bir cümlede satır içi olarak hem de cümleler arasında ayrı “çevrelenmiş” bir blok halinde kod parçacıkları yerleştirilmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="f0553-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="f0553-193">Ayrıntılar için bkz.</span><span class="sxs-lookup"><span data-stu-id="f0553-193">For details, see:</span></span>

- [<span data-ttu-id="f0553-194">Kod blokları için yerel Markdown desteği</span><span class="sxs-lookup"><span data-stu-id="f0553-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="f0553-195">Kod çevreleme ve söz dizimi vurgulama için GFM desteği</span><span class="sxs-lookup"><span data-stu-id="f0553-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="f0553-196">Çevrelenmiş kod blokları, kod parçacıklarınız için söz dizimi vurgulamasını etkinleştirmenin kolay bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="f0553-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="f0553-197">Çevrelenmiş kod bloklarının biçimi genelde şöyledir:</span><span class="sxs-lookup"><span data-stu-id="f0553-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="f0553-198">İlk üç ters tırnak (\`) karakterinden sonra gelen diğer ad, kullanılacak söz dizimi vurgulamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0553-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="f0553-199">Docs içeriğinde yaygın olarak kullanılan programlama dilleri ve bunların etiketleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="f0553-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="f0553-200">Bu diller, kolay as desteğine ve dil vurgulamasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="f0553-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="f0553-201">Ad</span><span class="sxs-lookup"><span data-stu-id="f0553-201">Name</span></span>|<span data-ttu-id="f0553-202">Markdown Etiketi</span><span class="sxs-lookup"><span data-stu-id="f0553-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="f0553-203">.NET Konsolu</span><span class="sxs-lookup"><span data-stu-id="f0553-203">.NET Console</span></span>|<span data-ttu-id="f0553-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="f0553-204">dotnetcli</span></span>|
|<span data-ttu-id="f0553-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="f0553-205">ASP.NET (C#)</span></span>|<span data-ttu-id="f0553-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="f0553-206">aspx-csharp</span></span>|
|<span data-ttu-id="f0553-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="f0553-207">ASP.NET (VB)</span></span>|<span data-ttu-id="f0553-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="f0553-208">aspx-vb</span></span>|
|<span data-ttu-id="f0553-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="f0553-209">AzCopy</span></span>|<span data-ttu-id="f0553-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="f0553-210">azcopy</span></span>|
|<span data-ttu-id="f0553-211">Azure CLI’si</span><span class="sxs-lookup"><span data-stu-id="f0553-211">Azure CLI</span></span>|<span data-ttu-id="f0553-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="f0553-212">azurecli</span></span>|
|<span data-ttu-id="f0553-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0553-213">Azure PowerShell</span></span>|<span data-ttu-id="f0553-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="f0553-214">azurepowershell</span></span>|
|<span data-ttu-id="f0553-215">Bash</span><span class="sxs-lookup"><span data-stu-id="f0553-215">Bash</span></span>|<span data-ttu-id="f0553-216">bash</span><span class="sxs-lookup"><span data-stu-id="f0553-216">bash</span></span>|
|<span data-ttu-id="f0553-217">C++</span><span class="sxs-lookup"><span data-stu-id="f0553-217">C++</span></span>|<span data-ttu-id="f0553-218">cpp</span><span class="sxs-lookup"><span data-stu-id="f0553-218">cpp</span></span>|
|<span data-ttu-id="f0553-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="f0553-219">C++/CX</span></span>|<span data-ttu-id="f0553-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="f0553-220">cppcx</span></span>|
|<span data-ttu-id="f0553-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="f0553-221">C++/WinRT</span></span>|<span data-ttu-id="f0553-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="f0553-222">cppwinrt</span></span>|
|<span data-ttu-id="f0553-223">C#</span><span class="sxs-lookup"><span data-stu-id="f0553-223">C#</span></span>|<span data-ttu-id="f0553-224">csharp</span><span class="sxs-lookup"><span data-stu-id="f0553-224">csharp</span></span>|
|<span data-ttu-id="f0553-225">Tarayıcıda C#</span><span class="sxs-lookup"><span data-stu-id="f0553-225">C# in browser</span></span>|<span data-ttu-id="f0553-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="f0553-226">csharp-interactive</span></span>|
|<span data-ttu-id="f0553-227">Konsol</span><span class="sxs-lookup"><span data-stu-id="f0553-227">Console</span></span>|<span data-ttu-id="f0553-228">konsol</span><span class="sxs-lookup"><span data-stu-id="f0553-228">console</span></span>|
|<span data-ttu-id="f0553-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="f0553-229">CSHTML</span></span>|<span data-ttu-id="f0553-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="f0553-230">cshtml</span></span>|
|<span data-ttu-id="f0553-231">DAX</span><span class="sxs-lookup"><span data-stu-id="f0553-231">DAX</span></span>|<span data-ttu-id="f0553-232">dax</span><span class="sxs-lookup"><span data-stu-id="f0553-232">dax</span></span>|
|<span data-ttu-id="f0553-233">Docker</span><span class="sxs-lookup"><span data-stu-id="f0553-233">Docker</span></span>|<span data-ttu-id="f0553-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="f0553-234">dockerfile</span></span>|
|<span data-ttu-id="f0553-235">F#</span><span class="sxs-lookup"><span data-stu-id="f0553-235">F#</span></span>|<span data-ttu-id="f0553-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="f0553-236">fsharp</span></span>|
|<span data-ttu-id="f0553-237">Go</span><span class="sxs-lookup"><span data-stu-id="f0553-237">Go</span></span>|<span data-ttu-id="f0553-238">go</span><span class="sxs-lookup"><span data-stu-id="f0553-238">go</span></span>|
|<span data-ttu-id="f0553-239">HTML</span><span class="sxs-lookup"><span data-stu-id="f0553-239">HTML</span></span>|<span data-ttu-id="f0553-240">html</span><span class="sxs-lookup"><span data-stu-id="f0553-240">html</span></span>|
|<span data-ttu-id="f0553-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="f0553-241">HTTP</span></span>|<span data-ttu-id="f0553-242">http</span><span class="sxs-lookup"><span data-stu-id="f0553-242">http</span></span>|
|<span data-ttu-id="f0553-243">Java</span><span class="sxs-lookup"><span data-stu-id="f0553-243">Java</span></span>|<span data-ttu-id="f0553-244">java</span><span class="sxs-lookup"><span data-stu-id="f0553-244">java</span></span>|
|<span data-ttu-id="f0553-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="f0553-245">JavaScript</span></span>|<span data-ttu-id="f0553-246">javascript</span><span class="sxs-lookup"><span data-stu-id="f0553-246">javascript</span></span>|
|<span data-ttu-id="f0553-247">JSON</span><span class="sxs-lookup"><span data-stu-id="f0553-247">JSON</span></span>|<span data-ttu-id="f0553-248">json</span><span class="sxs-lookup"><span data-stu-id="f0553-248">json</span></span>|
|<span data-ttu-id="f0553-249">Kusto Sorgu Dili</span><span class="sxs-lookup"><span data-stu-id="f0553-249">Kusto Query Language</span></span>|<span data-ttu-id="f0553-250">kusto</span><span class="sxs-lookup"><span data-stu-id="f0553-250">kusto</span></span>|
|<span data-ttu-id="f0553-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="f0553-251">Markdown</span></span>|<span data-ttu-id="f0553-252">md</span><span class="sxs-lookup"><span data-stu-id="f0553-252">md</span></span>|
|<span data-ttu-id="f0553-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="f0553-253">Objective-C</span></span>|<span data-ttu-id="f0553-254">objc</span><span class="sxs-lookup"><span data-stu-id="f0553-254">objc</span></span>|
|<span data-ttu-id="f0553-255">OData</span><span class="sxs-lookup"><span data-stu-id="f0553-255">OData</span></span>|<span data-ttu-id="f0553-256">odata</span><span class="sxs-lookup"><span data-stu-id="f0553-256">odata</span></span>|
|<span data-ttu-id="f0553-257">PHP</span><span class="sxs-lookup"><span data-stu-id="f0553-257">PHP</span></span>|<span data-ttu-id="f0553-258">php</span><span class="sxs-lookup"><span data-stu-id="f0553-258">php</span></span>|
|<span data-ttu-id="f0553-259">PowerApps (nokta ondalık ayırıcısı)</span><span class="sxs-lookup"><span data-stu-id="f0553-259">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="f0553-260">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="f0553-260">powerapps-dot</span></span>|
|<span data-ttu-id="f0553-261">PowerApps (virgül ondalık ayırıcısı)</span><span class="sxs-lookup"><span data-stu-id="f0553-261">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="f0553-262">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="f0553-262">powerapps-comma</span></span>|
|<span data-ttu-id="f0553-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0553-263">PowerShell</span></span>|<span data-ttu-id="f0553-264">powershell</span><span class="sxs-lookup"><span data-stu-id="f0553-264">powershell</span></span>|
|<span data-ttu-id="f0553-265">Python</span><span class="sxs-lookup"><span data-stu-id="f0553-265">Python</span></span>|<span data-ttu-id="f0553-266">python</span><span class="sxs-lookup"><span data-stu-id="f0553-266">python</span></span>|
|<span data-ttu-id="f0553-267">Q#</span><span class="sxs-lookup"><span data-stu-id="f0553-267">Q#</span></span>|<span data-ttu-id="f0553-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="f0553-268">qsharp</span></span>|
|<span data-ttu-id="f0553-269">R</span><span class="sxs-lookup"><span data-stu-id="f0553-269">R</span></span>|<span data-ttu-id="f0553-270">r</span><span class="sxs-lookup"><span data-stu-id="f0553-270">r</span></span>|
|<span data-ttu-id="f0553-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="f0553-271">Ruby</span></span>|<span data-ttu-id="f0553-272">ruby</span><span class="sxs-lookup"><span data-stu-id="f0553-272">ruby</span></span>|
|<span data-ttu-id="f0553-273">SQL</span><span class="sxs-lookup"><span data-stu-id="f0553-273">SQL</span></span>|<span data-ttu-id="f0553-274">sql</span><span class="sxs-lookup"><span data-stu-id="f0553-274">sql</span></span>|
|<span data-ttu-id="f0553-275">Swift</span><span class="sxs-lookup"><span data-stu-id="f0553-275">Swift</span></span>|<span data-ttu-id="f0553-276">swift</span><span class="sxs-lookup"><span data-stu-id="f0553-276">swift</span></span>|
|<span data-ttu-id="f0553-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="f0553-277">TypeScript</span></span>|<span data-ttu-id="f0553-278">typescript</span><span class="sxs-lookup"><span data-stu-id="f0553-278">typescript</span></span>|
|<span data-ttu-id="f0553-279">VB</span><span class="sxs-lookup"><span data-stu-id="f0553-279">VB</span></span>|<span data-ttu-id="f0553-280">vb</span><span class="sxs-lookup"><span data-stu-id="f0553-280">vb</span></span>|
|<span data-ttu-id="f0553-281">XAML</span><span class="sxs-lookup"><span data-stu-id="f0553-281">XAML</span></span>|<span data-ttu-id="f0553-282">xaml</span><span class="sxs-lookup"><span data-stu-id="f0553-282">xaml</span></span>|
|<span data-ttu-id="f0553-283">XML</span><span class="sxs-lookup"><span data-stu-id="f0553-283">XML</span></span>|<span data-ttu-id="f0553-284">xml</span><span class="sxs-lookup"><span data-stu-id="f0553-284">xml</span></span>|

<span data-ttu-id="f0553-285">`csharp-interactive` adı, C# bilgisayar dilini ve tarayıcıdan örnek çalıştırma becerisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0553-285">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="f0553-286">Bu kod parçacıkları, bir Docker kapsayıcısında derlenir ve yürütülür. Bu program yürütüldüğünde ortaya çıkan sonuçlar kullanıcının tarayıcı penceresinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f0553-286">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="f0553-287">Örnek: C\#</span><span class="sxs-lookup"><span data-stu-id="f0553-287">Example: C\#</span></span>

<span data-ttu-id="f0553-288">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="f0553-288">__Markdown__</span></span>

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

<span data-ttu-id="f0553-289">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="f0553-289">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="f0553-290">Örnek: SQL</span><span class="sxs-lookup"><span data-stu-id="f0553-290">Example: SQL</span></span>

<span data-ttu-id="f0553-291">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="f0553-291">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="f0553-292">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="f0553-292">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="f0553-293">OPS özel Markdown uzantıları</span><span class="sxs-lookup"><span data-stu-id="f0553-293">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="f0553-294">Open Publishing Services (OPS), GitHub Flavored Markdown (GFM) ile yüksek uyumluluğa sahip olan Markdown için Markdig Ayrıştırıcısı’nı uygular.</span><span class="sxs-lookup"><span data-stu-id="f0553-294">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="f0553-295">Markdig, Markdown uzantıları aracılığıyla ilave işlevsellik sağlar.</span><span class="sxs-lookup"><span data-stu-id="f0553-295">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="f0553-296">Bu nedenle, tam OPS Yazma Kılavuzundan bazı makaleler başvuru için bu kılavuza dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="f0553-296">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="f0553-297">(Örneğin, içindekiler bölümünde "Markdig ve Markdown uzantıları" ile "Kod parçacıkları" kısımlarına bakın.)</span><span class="sxs-lookup"><span data-stu-id="f0553-297">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="f0553-298">Docs makaleleri çoğu zaman paragraflar, bağlantılar, listeler ve bölüm başlıkları gibi makale biçimlendirmeleri için GFM’yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="f0553-298">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="f0553-299">Makaleler, daha zengin biçimlendirme için aşağıdakiler gibi Markdig özelliklerini kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="f0553-299">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="f0553-300">Not blokları</span><span class="sxs-lookup"><span data-stu-id="f0553-300">Note blocks</span></span>
- <span data-ttu-id="f0553-301">Dosyaları dahil et</span><span class="sxs-lookup"><span data-stu-id="f0553-301">Include files</span></span>
- <span data-ttu-id="f0553-302">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="f0553-302">Selectors</span></span>
- <span data-ttu-id="f0553-303">Ekli videolar</span><span class="sxs-lookup"><span data-stu-id="f0553-303">Embedded videos</span></span>
- <span data-ttu-id="f0553-304">Kod parçacıkları/örnekleri</span><span class="sxs-lookup"><span data-stu-id="f0553-304">Code snippets/samples</span></span>

<span data-ttu-id="f0553-305">Tam bir liste için içerikler bölümünde “Markdig ve Markdown uzantıları” ve “Kod parçacıkları” kısmına bakın.</span><span class="sxs-lookup"><span data-stu-id="f0553-305">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="f0553-306">Not blokları</span><span class="sxs-lookup"><span data-stu-id="f0553-306">Note blocks</span></span>

<span data-ttu-id="f0553-307">İlgiyi belirli bir içeriğe çekmek için dört çeşit not blokundan birini seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f0553-307">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="f0553-308">NOT</span><span class="sxs-lookup"><span data-stu-id="f0553-308">NOTE</span></span>
- <span data-ttu-id="f0553-309">UYARI</span><span class="sxs-lookup"><span data-stu-id="f0553-309">WARNING</span></span>
- <span data-ttu-id="f0553-310">İPUCU</span><span class="sxs-lookup"><span data-stu-id="f0553-310">TIP</span></span>
- <span data-ttu-id="f0553-311">ÖNEMLİ</span><span class="sxs-lookup"><span data-stu-id="f0553-311">IMPORTANT</span></span>

<span data-ttu-id="f0553-312">Genel olarak not bloklarını fazla kullanmaktan kaçınmalısınız, dikkat dağıtıcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="f0553-312">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="f0553-313">Not bloklarında kod blokları, görüntüler, listeler ve bağlantılar destekleniyor olsa da bunları olabildiğince sade ve düz bir şekilde oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f0553-313">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="f0553-314">Örnekler:</span><span class="sxs-lookup"><span data-stu-id="f0553-314">Examples:</span></span>

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

<span data-ttu-id="f0553-315">Bunlar aşağıdaki gibi işlenir:</span><span class="sxs-lookup"><span data-stu-id="f0553-315">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="f0553-316">Bu bir NOT’tur</span><span class="sxs-lookup"><span data-stu-id="f0553-316">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="f0553-317">Bu bir UYARI’dır</span><span class="sxs-lookup"><span data-stu-id="f0553-317">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="f0553-318">Bu bir İPUCU’dur</span><span class="sxs-lookup"><span data-stu-id="f0553-318">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0553-319">Bu ÖNEMLİ’dir</span><span class="sxs-lookup"><span data-stu-id="f0553-319">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="f0553-320">Dosyaları dahil et</span><span class="sxs-lookup"><span data-stu-id="f0553-320">Include files</span></span>

<span data-ttu-id="f0553-321">Makale dosyalarına dahil edilmesi gereken yeniden kullanılabilir metin veya görüntü dosyalarınız varsa dosyayı Markdig dosya dahil etme özelliği ile “dahil etmek” için bir başvuru kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0553-321">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="f0553-322">Bu özellik, verilen dosyayı makalenize derleme sırasında “eklemesi” için OPS’yi yönlendirir, böylece dosya da yayımlanan makalenizin bir parçası olur.</span><span class="sxs-lookup"><span data-stu-id="f0553-322">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="f0553-323">İçerikleri tekrar kullanmanıza imkan veren üç tür ekleme başvurusu vardır:</span><span class="sxs-lookup"><span data-stu-id="f0553-323">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="f0553-324">Satır İçi: Genel bir metin parçacığını başka bir cümlede satır içinde yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0553-324">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="f0553-325">Blok: Makalenin bir bölümündeki bütün bir Markdown dosyasını yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0553-325">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="f0553-326">Görüntü: Docs’ta standart görüntü ekleme yoludur.</span><span class="sxs-lookup"><span data-stu-id="f0553-326">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="f0553-327">Satır içi ve blok ekleme dosyaları, basit birer Markdown (.md) dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="f0553-327">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="f0553-328">Bu dosyalar, herhangi bir geçerli Markdown barındırabilir.</span><span class="sxs-lookup"><span data-stu-id="f0553-328">It can contain any valid Markdown.</span></span> <span data-ttu-id="f0553-329">Tüm ekleme Markdown dosyaları, depo kökünde [ortak bir `/includes` alt dizinine](git-github-fundamentals.md#includes-subdirectory) yerleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f0553-329">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="f0553-330">Makale yayımlandığında, eklenen dosya makaleyle sorunsuz bir şekilde tümleşmiş olur.</span><span class="sxs-lookup"><span data-stu-id="f0553-330">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="f0553-331">Ekleme dosyalarına yönelik gereksinimler ve önemli konular şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f0553-331">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="f0553-332">Aynı metni birden fazla makalede kullanmanız gerektiği zaman ekleme dosyalarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0553-332">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="f0553-333">Bir veya iki paragraf, paylaşılan bir yordam veya paylaşılan bir bölüm gibi büyük içeriklerde blok ekleme başvurusunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0553-333">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="f0553-334">Ancak bir cümleden daha küçük şeyler için kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="f0553-334">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="f0553-335">Ekleme başvuruları, Markdig uzantılarına bağlı olduğu için makalenizin GitHub tarafından işlenmiş görünümünde işlenmez.</span><span class="sxs-lookup"><span data-stu-id="f0553-335">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="f0553-336">Bunlar yalnızca yayın sonrasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f0553-336">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="f0553-337">Ekleme dosyasına başvuran makalelerdeki ekleme dosyalarında bütün metnin, öncesinde veya sonrasında gelen metinden bağımsız tam cümleler veya ifadeler şeklinde olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f0553-337">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="f0553-338">Bu kılavuzu dikkate almamak, makalede çevrilemeyen bir satır oluşturur ve yerelleştirme deneyimini bozar.</span><span class="sxs-lookup"><span data-stu-id="f0553-338">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="f0553-339">Ekleme başvurularını diğer ekleme dosyalarına eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="f0553-339">Don't embed include references within other include files.</span></span> <span data-ttu-id="f0553-340">Bu, desteklenmeyen bir durumdur.</span><span class="sxs-lookup"><span data-stu-id="f0553-340">They are not supported.</span></span>
- <span data-ttu-id="f0553-341">Medya dosyalarını ekleme alt dizinine özgü bir medya klasörüne yerleştirin, örneğin `<repo>`/eklemeler/medya klasörü.</span><span class="sxs-lookup"><span data-stu-id="f0553-341">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="f0553-342">Medya dizini, kökünde hiçbir görüntü barındırmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="f0553-342">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="f0553-343">Ekleme dosyasında görüntü yoksa buna karşılık gelecek bir medya dizini gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="f0553-343">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="f0553-344">Normal makalelerde olduğu gibi, ekleme dosyaları arasında medya paylaşmayın.</span><span class="sxs-lookup"><span data-stu-id="f0553-344">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="f0553-345">Her bir ekleme dosyası ve makale için benzersiz ada sahip ayrı dosyalar kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0553-345">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="f0553-346">Medya dosyasını, ekleme dosyasıyla ilişkili medya klasöründe depolayın.</span><span class="sxs-lookup"><span data-stu-id="f0553-346">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="f0553-347">Ekleme dosyalarını bir makaledeki tek içerik olacak şekilde kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="f0553-347">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="f0553-348">Ekleme dosyaları, makaledeki diğer içerikleri tamamlayıcı niteliktedir.</span><span class="sxs-lookup"><span data-stu-id="f0553-348">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="f0553-349">Örnek:</span><span class="sxs-lookup"><span data-stu-id="f0553-349">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="f0553-350">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="f0553-350">Selectors</span></span>

<span data-ttu-id="f0553-351">Seçicileri teknik makalelerde, aynı makalenin farklı bölümlerini yazdığınızda teknolojiler veya platformlar arasındaki uygulama farklılıklarına değinirken kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0553-351">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="f0553-352">Bu genellikle geliştiriciler için mobil platform içeriklerimizde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f0553-352">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="f0553-353">Markdig’de şu anda iki farklı türde seçici vardır; tekli seçici ve çoklu seçici.</span><span class="sxs-lookup"><span data-stu-id="f0553-353">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="f0553-354">Seçimdeki her bir makaleye aynı seçici Markdown gittiği için makalenizin seçicisini bir ekleme dosyasına koymanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="f0553-354">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="f0553-355">Daha sonra aynı seçiciyi kullanan tüm makalelerinizde bu ekleme dosyasına başvurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0553-355">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="f0553-356">Aşağıdaki kodda bir seçici örneği gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="f0553-356">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="f0553-357">[Azure belgelerinde](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic) seçicilerin nasıl kullanıldığının örneklerini bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0553-357">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="f0553-358">Kod ekleme başvuruları</span><span class="sxs-lookup"><span data-stu-id="f0553-358">Code include references</span></span>

<span data-ttu-id="f0553-359">Markdig, bir makaleye kod parçacığı uzantısı aracılığıyla gelişmiş kod eklemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="f0553-359">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="f0553-360">Programlama dili seçimi ve söz dizimi renklendirme gibi GFM özellikleri üzerinde ortaya çıkan gelişmiş işleme seçenekleri sağlar, bunların yanında aşağıdaki gibi kullanışlı özellikler de getirir:</span><span class="sxs-lookup"><span data-stu-id="f0553-360">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="f0553-361">Bir dış depodan gelen merkezi kod örnekleri/parçacıklarının eklenmesi.</span><span class="sxs-lookup"><span data-stu-id="f0553-361">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="f0553-362">Kod örneklerinin farklı dillerdeki birçok çeşidini gösteren sekmeli kullanıcı arabirimi.</span><span class="sxs-lookup"><span data-stu-id="f0553-362">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="f0553-363">Tuzaklar ve sorun giderme</span><span class="sxs-lookup"><span data-stu-id="f0553-363">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="f0553-364">Alternatif metin</span><span class="sxs-lookup"><span data-stu-id="f0553-364">Alt text</span></span>

<span data-ttu-id="f0553-365">Alt çizgi içeren alternatif metin düzgün bir şekilde işlenmez.</span><span class="sxs-lookup"><span data-stu-id="f0553-365">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="f0553-366">Örneğin, şunu kullanmak yerine:</span><span class="sxs-lookup"><span data-stu-id="f0553-366">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="f0553-367">Şunun gibi alt çizgilerden kaçının:</span><span class="sxs-lookup"><span data-stu-id="f0553-367">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="f0553-368">Kesme işareti ve tırnak işaretleri</span><span class="sxs-lookup"><span data-stu-id="f0553-368">Apostrophes and quotation marks</span></span>

<span data-ttu-id="f0553-369">Word dosyasından Markdown editörüne bir şey kopyalarsanız kopyaladığınız metin “akıllı” (kıvrık) kesme işaretleri veya tırnak işaretleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="f0553-369">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="f0553-370">Bunların kodlanması veya kesme işareti ya da tırnak işaretlerine dönüştürülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f0553-370">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="f0553-371">Aksi takdirde, dosya yayımlandığında şöyle karakterler görebilirsiniz: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="f0553-371">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="f0553-372">Bu noktalama işaretlerinin “akıllı” olanları için kodlamalar aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="f0553-372">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="f0553-373">Sol (açma) tırnak işareti: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="f0553-373">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="f0553-374">Sağ (kapatma) tırnak işareti: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="f0553-374">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="f0553-375">Sağ (kapatma) tekli tırnak işareti veya kesme işareti: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="f0553-375">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="f0553-376">Sağ (açma) tekli tırnak işareti (nadiren kullanılır): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="f0553-376">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="f0553-377">Açılı ayraçlar</span><span class="sxs-lookup"><span data-stu-id="f0553-377">Angle brackets</span></span>

<span data-ttu-id="f0553-378">Bir yer tutucuyu ifade etmek için köşeli ayraç kullanımı yaygındır.</span><span class="sxs-lookup"><span data-stu-id="f0553-378">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="f0553-379">Metinde (kodda değil) bunu yaptığınızda, köşeli ayraçları kodlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f0553-379">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="f0553-380">Aksi takdirde Markdown bunların HTML etiketleri olması gerektiğini düşünür.</span><span class="sxs-lookup"><span data-stu-id="f0553-380">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="f0553-381">Örneğin `<script name>` öğesini `&lt;script name&gt;` şeklinde kodlayın</span><span class="sxs-lookup"><span data-stu-id="f0553-381">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="f0553-382">Markdown varyantı</span><span class="sxs-lookup"><span data-stu-id="f0553-382">Markdown flavor</span></span>

<span data-ttu-id="f0553-383">docs.microsoft.com sitesi arka ucu, [Markdig](https://github.com/lunet-io/markdig) ayrıştırma altyapısı aracılığıyla ayrıştırılan [CommonMark](https://commonmark.org/) uyumlu markdown’ı destekleyen Open Publishing Services (OPS) kullanır.</span><span class="sxs-lookup"><span data-stu-id="f0553-383">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="f0553-384">Çoğu belge GitHub’da depolanıp burada düzenlenebildiği için bu markdown varyantı çoğunlukla [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="f0553-384">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="f0553-385">Markdown uzantıları ile ilave işlevler eklenir.</span><span class="sxs-lookup"><span data-stu-id="f0553-385">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0553-386">Ayrıca bkz.:</span><span class="sxs-lookup"><span data-stu-id="f0553-386">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="f0553-387">Markdown kaynakları</span><span class="sxs-lookup"><span data-stu-id="f0553-387">Markdown resources</span></span>

- [<span data-ttu-id="f0553-388">Markdown’a Giriş</span><span class="sxs-lookup"><span data-stu-id="f0553-388">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="f0553-389">Docs Markdown kural sayfası</span><span class="sxs-lookup"><span data-stu-id="f0553-389">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="f0553-390">GitHub Markdown Temel Bilgileri</span><span class="sxs-lookup"><span data-stu-id="f0553-390">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="f0553-391">Markdown Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="f0553-391">The Markdown Guide</span></span>](https://www.markdownguide.org/)
