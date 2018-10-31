---
title: Docs’ta makale yazmak için Markdown kullanma
description: Bu makale, docs.microsoft.com makalelerinde kullanılan Markdown dilinin temellerini ve başvuru bilgilerini sağlar.
ms.date: 07/13/2017
ms.openlocfilehash: 6bb8a1fa20957512addb07dda0e68abec4b0a83f
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805747"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="7419f-103">Docs’ta makale yazmak için Markdown kullanma</span><span class="sxs-lookup"><span data-stu-id="7419f-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="7419f-104">[Docs.microsoft.com](http://docs.microsoft.com) makaleleri, [Markdown](https://daringfireball.net/projects/markdown/) adı verilen hafif biçimlendirme dilinde yazılır. Bu dilin okunması ve öğrenilmesi kolaydır.</span><span class="sxs-lookup"><span data-stu-id="7419f-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="7419f-105">O nedenle bu dil kısa sürede endüstri standardı haline gelmiştir.</span><span class="sxs-lookup"><span data-stu-id="7419f-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="7419f-106">Docs içerikleri GitHub’da depolandığı için [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) adlı bir Markdown üst kümesi kullanabilir. GFM, yaygın biçimlendirme ihtiyaçları için ilave işlevler sağlar.</span><span class="sxs-lookup"><span data-stu-id="7419f-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="7419f-107">Ayrıca Open Publishing Services (OPS), Markdig Markdown Ayrıştırıcısı’nı uygular.</span><span class="sxs-lookup"><span data-stu-id="7419f-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="7419f-108">Markdig, GFM ile yüksek uyumluluğa sahip olduğu için Docs’a özgü özellikleri etkinleştirmek için ek işlevsellik sağlar.</span><span class="sxs-lookup"><span data-stu-id="7419f-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="7419f-109">Markdig; .NET için hızlı, güçlü, CommonMark uyumlu, genişletilebilir Markdown işlemcisidir.</span><span class="sxs-lookup"><span data-stu-id="7419f-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="7419f-110">Daha iyi topluluk desteği</span><span class="sxs-lookup"><span data-stu-id="7419f-110">Better community support</span></span>
* <span data-ttu-id="7419f-111">Daha iyi standartlar desteği</span><span class="sxs-lookup"><span data-stu-id="7419f-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="7419f-112">Markdown temel bilgileri</span><span class="sxs-lookup"><span data-stu-id="7419f-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="7419f-113">Bölüm başlıkları</span><span class="sxs-lookup"><span data-stu-id="7419f-113">Headings</span></span>

<span data-ttu-id="7419f-114">Bir bölüm başlığı oluşturmak için karma işaretini (#) aşağıdaki gibi kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="7419f-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="7419f-115">Kalın ve italik metin</span><span class="sxs-lookup"><span data-stu-id="7419f-115">Bold and italic text</span></span>

<span data-ttu-id="7419f-116">Bir metni **kalın** olarak biçimlendirmek için iki yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="7419f-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="7419f-117">Bir metni *italik* olarak biçimlendirmek için bir yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="7419f-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="7419f-118">Bir metni ***kalın ve italik*** olarak biçimlendirmek için üç yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="7419f-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="7419f-119">Listeler</span><span class="sxs-lookup"><span data-stu-id="7419f-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="7419f-120">Sırasız liste</span><span class="sxs-lookup"><span data-stu-id="7419f-120">Unordered list</span></span>

<span data-ttu-id="7419f-121">Sırasız/madde işaretli bir listeyi biçimlendirmek için yıldız işaretleri veya tireler kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7419f-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="7419f-122">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="7419f-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="7419f-123">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="7419f-123">will be rendered as:</span></span>

- <span data-ttu-id="7419f-124">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="7419f-124">List item 1</span></span>
- <span data-ttu-id="7419f-125">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="7419f-125">List item 2</span></span>
- <span data-ttu-id="7419f-126">Liste öğesi 3</span><span class="sxs-lookup"><span data-stu-id="7419f-126">List item 3</span></span>

<span data-ttu-id="7419f-127">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="7419f-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="7419f-128">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="7419f-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="7419f-129">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="7419f-129">will be rendered as:</span></span>

- <span data-ttu-id="7419f-130">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="7419f-130">List item 1</span></span>
  - <span data-ttu-id="7419f-131">Liste öğesi A</span><span class="sxs-lookup"><span data-stu-id="7419f-131">List item A</span></span>
  - <span data-ttu-id="7419f-132">Liste öğesi B</span><span class="sxs-lookup"><span data-stu-id="7419f-132">List item B</span></span>
- <span data-ttu-id="7419f-133">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="7419f-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="7419f-134">Sıralı liste</span><span class="sxs-lookup"><span data-stu-id="7419f-134">Ordered list</span></span>

<span data-ttu-id="7419f-135">Sıralı/adımlı bir listeyi biçimlendirmek için sıra numaraları kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="7419f-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="7419f-136">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="7419f-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="7419f-137">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="7419f-137">will be rendered as:</span></span>

1. <span data-ttu-id="7419f-138">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="7419f-138">First instruction</span></span>
2. <span data-ttu-id="7419f-139">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="7419f-139">Second instruction</span></span>
3. <span data-ttu-id="7419f-140">Üçüncü yönerge</span><span class="sxs-lookup"><span data-stu-id="7419f-140">Third instruction</span></span>

<span data-ttu-id="7419f-141">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="7419f-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="7419f-142">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="7419f-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="7419f-143">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="7419f-143">will be rendered as:</span></span>

1. <span data-ttu-id="7419f-144">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="7419f-144">First instruction</span></span>
   1. <span data-ttu-id="7419f-145">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="7419f-145">Sub-instruction</span></span>
   2. <span data-ttu-id="7419f-146">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="7419f-146">Sub-instruction</span></span>
2. <span data-ttu-id="7419f-147">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="7419f-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="7419f-148">eğlence</span><span class="sxs-lookup"><span data-stu-id="7419f-148">Tables</span></span>

<span data-ttu-id="7419f-149">Tablolar, temel Markdown belirtiminin parçası değildir, ancak GFM tarafından desteklenir.</span><span class="sxs-lookup"><span data-stu-id="7419f-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="7419f-150">Düz çizgi (|) ve kısa çizgi (-) karakterlerini kullanarak tablolar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7419f-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="7419f-151">Kısa çizgiler sütunların üst bilgisini oluştururken düz çizgiler sütunları birbirinden ayırır.</span><span class="sxs-lookup"><span data-stu-id="7419f-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="7419f-152">Tablonun doğru işlenebilmesi için başına boş bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7419f-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="7419f-153">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="7419f-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="7419f-154">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="7419f-154">will be rendered as:</span></span>

| <span data-ttu-id="7419f-155">Tablolar</span><span class="sxs-lookup"><span data-stu-id="7419f-155">Fun</span></span>                  | <span data-ttu-id="7419f-156">Şununla:</span><span class="sxs-lookup"><span data-stu-id="7419f-156">With</span></span>                 | <span data-ttu-id="7419f-157">eğlence</span><span class="sxs-lookup"><span data-stu-id="7419f-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="7419f-158">sola hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="7419f-158">left-aligned column</span></span>  | <span data-ttu-id="7419f-159">sağa hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="7419f-159">right-aligned column</span></span> | <span data-ttu-id="7419f-160">ortalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="7419f-160">centered column</span></span> |
| <span data-ttu-id="7419f-161">100 $</span><span class="sxs-lookup"><span data-stu-id="7419f-161">$100</span></span>                 | <span data-ttu-id="7419f-162">100 $</span><span class="sxs-lookup"><span data-stu-id="7419f-162">$100</span></span>                 | <span data-ttu-id="7419f-163">100 $</span><span class="sxs-lookup"><span data-stu-id="7419f-163">$100</span></span>            |
| <span data-ttu-id="7419f-164">10 $</span><span class="sxs-lookup"><span data-stu-id="7419f-164">$10</span></span>                  | <span data-ttu-id="7419f-165">10 $</span><span class="sxs-lookup"><span data-stu-id="7419f-165">$10</span></span>                  | <span data-ttu-id="7419f-166">10 $</span><span class="sxs-lookup"><span data-stu-id="7419f-166">$10</span></span>             |
| <span data-ttu-id="7419f-167">1 $</span><span class="sxs-lookup"><span data-stu-id="7419f-167">$1</span></span>                   | <span data-ttu-id="7419f-168">1 $</span><span class="sxs-lookup"><span data-stu-id="7419f-168">$1</span></span>                   | <span data-ttu-id="7419f-169">1 $</span><span class="sxs-lookup"><span data-stu-id="7419f-169">$1</span></span>              |

<span data-ttu-id="7419f-170">Tablo oluşturma hakkında daha fazla bilgi için şunlara bakın:</span><span class="sxs-lookup"><span data-stu-id="7419f-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="7419f-171">Geniş tabloların biçimlendirmesinde yardımcı olabilecek Markdig [tablo sarmalama özelliği](#table-wrapping).</span><span class="sxs-lookup"><span data-stu-id="7419f-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="7419f-172">GitHub’ın [Tablolarla bilgi düzenleme](https://help.github.com/articles/organizing-information-with-tables/) makalesi.</span><span class="sxs-lookup"><span data-stu-id="7419f-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="7419f-173">[Markdown Tablo Oluşturucu](https://www.tablesgenerator.com/markdown_tables) web uygulaması.</span><span class="sxs-lookup"><span data-stu-id="7419f-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="7419f-174">[Adam Pritchard - Markdown Hızlı Başvuru Kılavuzu](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span><span class="sxs-lookup"><span data-stu-id="7419f-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="7419f-175">[Michel Fortin - Markdown Ekstra](https://michelf.ca/projects/php-markdown/extra/#table).</span><span class="sxs-lookup"><span data-stu-id="7419f-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="7419f-176">[HTML tablolarını Markdown’a dönüştürme](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="7419f-176">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="7419f-177">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="7419f-177">Links</span></span>

<span data-ttu-id="7419f-178">Satır içi bağlantılarda Markdown söz dizimi, köprü bağlantısı eklenecek `[link text]` metni ve bağlantı verilen URL ya da dosya adı olan `(file-name.md)` kısımlarından oluşur:</span><span class="sxs-lookup"><span data-stu-id="7419f-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="7419f-179">Bağlantı verme hakkında daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="7419f-179">For more information on linking, see:</span></span>

- <span data-ttu-id="7419f-180">Markdown’ın temel bağlantı desteği konusunda ayrıntılar için [Markdown söz dizimi kılavuzu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="7419f-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="7419f-181">Markdig tarafından sağlanan ilave bağlayıcı söz dizimi hakkında ayrıntılar için bu kılavuzun [Bağlantılar](how-to-write-links.md) bölümü.</span><span class="sxs-lookup"><span data-stu-id="7419f-181">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="7419f-182">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="7419f-182">Code snippets</span></span>

<span data-ttu-id="7419f-183">Markdown, hem bir cümlede satır içi olarak hem de cümleler arasında ayrı “çevrelenmiş” bir blok halinde kod parçacıkları yerleştirilmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="7419f-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="7419f-184">Ayrıntılar için bkz.</span><span class="sxs-lookup"><span data-stu-id="7419f-184">For details, see:</span></span>

- [<span data-ttu-id="7419f-185">Kod blokları için yerel Markdown desteği</span><span class="sxs-lookup"><span data-stu-id="7419f-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="7419f-186">Kod çevreleme ve söz dizimi vurgulama için GFM desteği</span><span class="sxs-lookup"><span data-stu-id="7419f-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="7419f-187">Çevrelenmiş kod blokları, kod parçacıklarınız için söz dizimi vurgulamasını etkinleştirmenin kolay bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="7419f-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="7419f-188">Çevrelenmiş kod bloklarının biçimi genelde şöyledir:</span><span class="sxs-lookup"><span data-stu-id="7419f-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="7419f-189">İlk üç ters tırnak (\`) karakterinden sonra gelen diğer ad, kullanılacak söz dizimi vurgulamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7419f-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="7419f-190">Docs içeriğinde yaygın olarak kullanılan programlama dilleri ve bunların etiketleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="7419f-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="7419f-191">Bu diller, kolay as desteğine ve dil vurgulamasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="7419f-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="7419f-192">Ad</span><span class="sxs-lookup"><span data-stu-id="7419f-192">Name</span></span>|<span data-ttu-id="7419f-193">Markdown Etiketi</span><span class="sxs-lookup"><span data-stu-id="7419f-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="7419f-194">.NET Konsolu</span><span class="sxs-lookup"><span data-stu-id="7419f-194">.NET Console</span></span>|<span data-ttu-id="7419f-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="7419f-195">dotnetcli</span></span>|
|<span data-ttu-id="7419f-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="7419f-196">ASP.NET (C#)</span></span>|<span data-ttu-id="7419f-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="7419f-197">aspx-csharp</span></span>|
|<span data-ttu-id="7419f-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="7419f-198">ASP.NET (VB)</span></span>|<span data-ttu-id="7419f-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="7419f-199">aspx-vb</span></span>|
|<span data-ttu-id="7419f-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="7419f-200">AzCopy</span></span>|<span data-ttu-id="7419f-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="7419f-201">azcopy</span></span>|
|<span data-ttu-id="7419f-202">Azure CLI’si</span><span class="sxs-lookup"><span data-stu-id="7419f-202">Azure CLI</span></span>|<span data-ttu-id="7419f-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="7419f-203">azurecli</span></span>|
|<span data-ttu-id="7419f-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7419f-204">Azure PowerShell</span></span>|<span data-ttu-id="7419f-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="7419f-205">azurepowershell</span></span>|
|<span data-ttu-id="7419f-206">C++</span><span class="sxs-lookup"><span data-stu-id="7419f-206">C++</span></span>|<span data-ttu-id="7419f-207">cpp</span><span class="sxs-lookup"><span data-stu-id="7419f-207">cpp</span></span>|
|<span data-ttu-id="7419f-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="7419f-208">C++/CX</span></span>|<span data-ttu-id="7419f-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="7419f-209">cppcx</span></span>|
|<span data-ttu-id="7419f-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="7419f-210">C++/WinRT</span></span>|<span data-ttu-id="7419f-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="7419f-211">cppwinrt</span></span>|
|<span data-ttu-id="7419f-212">C#</span><span class="sxs-lookup"><span data-stu-id="7419f-212">C#</span></span>|<span data-ttu-id="7419f-213">csharp</span><span class="sxs-lookup"><span data-stu-id="7419f-213">csharp</span></span>|
|<span data-ttu-id="7419f-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="7419f-214">CSHTML</span></span>|<span data-ttu-id="7419f-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="7419f-215">cshtml</span></span>|
|<span data-ttu-id="7419f-216">DAX</span><span class="sxs-lookup"><span data-stu-id="7419f-216">DAX</span></span>|<span data-ttu-id="7419f-217">dax</span><span class="sxs-lookup"><span data-stu-id="7419f-217">dax</span></span>|
|<span data-ttu-id="7419f-218">F#</span><span class="sxs-lookup"><span data-stu-id="7419f-218">F#</span></span>|<span data-ttu-id="7419f-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="7419f-219">fsharp</span></span>|
|<span data-ttu-id="7419f-220">Go</span><span class="sxs-lookup"><span data-stu-id="7419f-220">Go</span></span>|<span data-ttu-id="7419f-221">go</span><span class="sxs-lookup"><span data-stu-id="7419f-221">go</span></span>|
|<span data-ttu-id="7419f-222">HTML</span><span class="sxs-lookup"><span data-stu-id="7419f-222">HTML</span></span>|<span data-ttu-id="7419f-223">html</span><span class="sxs-lookup"><span data-stu-id="7419f-223">html</span></span>|
|<span data-ttu-id="7419f-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="7419f-224">HTTP</span></span>|<span data-ttu-id="7419f-225">http</span><span class="sxs-lookup"><span data-stu-id="7419f-225">http</span></span>|
|<span data-ttu-id="7419f-226">Java</span><span class="sxs-lookup"><span data-stu-id="7419f-226">Java</span></span>|<span data-ttu-id="7419f-227">java</span><span class="sxs-lookup"><span data-stu-id="7419f-227">java</span></span>|
|<span data-ttu-id="7419f-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7419f-228">JavaScript</span></span>|<span data-ttu-id="7419f-229">javascript</span><span class="sxs-lookup"><span data-stu-id="7419f-229">javascript</span></span>|
|<span data-ttu-id="7419f-230">JSON</span><span class="sxs-lookup"><span data-stu-id="7419f-230">JSON</span></span>|<span data-ttu-id="7419f-231">json</span><span class="sxs-lookup"><span data-stu-id="7419f-231">json</span></span>|
|<span data-ttu-id="7419f-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="7419f-232">Markdown</span></span>|<span data-ttu-id="7419f-233">md</span><span class="sxs-lookup"><span data-stu-id="7419f-233">md</span></span>|
|<span data-ttu-id="7419f-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="7419f-234">NodeJS</span></span>|<span data-ttu-id="7419f-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="7419f-235">nodejs</span></span>|
|<span data-ttu-id="7419f-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="7419f-236">Objective-C</span></span>|<span data-ttu-id="7419f-237">objc</span><span class="sxs-lookup"><span data-stu-id="7419f-237">objc</span></span>|
|<span data-ttu-id="7419f-238">OData</span><span class="sxs-lookup"><span data-stu-id="7419f-238">OData</span></span>|<span data-ttu-id="7419f-239">odata</span><span class="sxs-lookup"><span data-stu-id="7419f-239">odata</span></span>|
|<span data-ttu-id="7419f-240">PHP</span><span class="sxs-lookup"><span data-stu-id="7419f-240">PHP</span></span>|<span data-ttu-id="7419f-241">php</span><span class="sxs-lookup"><span data-stu-id="7419f-241">php</span></span>|
|<span data-ttu-id="7419f-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="7419f-242">Power Apps Formula</span></span>|<span data-ttu-id="7419f-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="7419f-243">powerappsfl</span></span>|
|<span data-ttu-id="7419f-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7419f-244">PowerShell</span></span>|<span data-ttu-id="7419f-245">powershell</span><span class="sxs-lookup"><span data-stu-id="7419f-245">powershell</span></span>|
|<span data-ttu-id="7419f-246">Python</span><span class="sxs-lookup"><span data-stu-id="7419f-246">Python</span></span>|<span data-ttu-id="7419f-247">python</span><span class="sxs-lookup"><span data-stu-id="7419f-247">python</span></span>|
|<span data-ttu-id="7419f-248">Q#</span><span class="sxs-lookup"><span data-stu-id="7419f-248">Q#</span></span>|<span data-ttu-id="7419f-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="7419f-249">qsharp</span></span>|
|<span data-ttu-id="7419f-250">R</span><span class="sxs-lookup"><span data-stu-id="7419f-250">R</span></span>|<span data-ttu-id="7419f-251">r</span><span class="sxs-lookup"><span data-stu-id="7419f-251">r</span></span>|
|<span data-ttu-id="7419f-252">Ruby</span><span class="sxs-lookup"><span data-stu-id="7419f-252">Ruby</span></span>|<span data-ttu-id="7419f-253">ruby</span><span class="sxs-lookup"><span data-stu-id="7419f-253">ruby</span></span>|
|<span data-ttu-id="7419f-254">SQL</span><span class="sxs-lookup"><span data-stu-id="7419f-254">SQL</span></span>|<span data-ttu-id="7419f-255">sql</span><span class="sxs-lookup"><span data-stu-id="7419f-255">sql</span></span>|
|<span data-ttu-id="7419f-256">Swift</span><span class="sxs-lookup"><span data-stu-id="7419f-256">Swift</span></span>|<span data-ttu-id="7419f-257">swift</span><span class="sxs-lookup"><span data-stu-id="7419f-257">swift</span></span>|
|<span data-ttu-id="7419f-258">TypeScript</span><span class="sxs-lookup"><span data-stu-id="7419f-258">TypeScript</span></span>|<span data-ttu-id="7419f-259">typescript</span><span class="sxs-lookup"><span data-stu-id="7419f-259">typescript</span></span>|
|<span data-ttu-id="7419f-260">VB</span><span class="sxs-lookup"><span data-stu-id="7419f-260">VB</span></span>|<span data-ttu-id="7419f-261">vb</span><span class="sxs-lookup"><span data-stu-id="7419f-261">vb</span></span>|
|<span data-ttu-id="7419f-262">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="7419f-262">VSTS CLI</span></span>|<span data-ttu-id="7419f-263">vstscli</span><span class="sxs-lookup"><span data-stu-id="7419f-263">vstscli</span></span>|
|<span data-ttu-id="7419f-264">XAML</span><span class="sxs-lookup"><span data-stu-id="7419f-264">XAML</span></span>|<span data-ttu-id="7419f-265">xaml</span><span class="sxs-lookup"><span data-stu-id="7419f-265">xaml</span></span>|
|<span data-ttu-id="7419f-266">XML</span><span class="sxs-lookup"><span data-stu-id="7419f-266">XML</span></span>|<span data-ttu-id="7419f-267">xml</span><span class="sxs-lookup"><span data-stu-id="7419f-267">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="7419f-268">Örnek: C\#</span><span class="sxs-lookup"><span data-stu-id="7419f-268">Example: C\#</span></span>

<span data-ttu-id="7419f-269">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="7419f-269">__Markdown__</span></span>

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

<span data-ttu-id="7419f-270">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="7419f-270">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="7419f-271">Örnek: SQL</span><span class="sxs-lookup"><span data-stu-id="7419f-271">Example: SQL</span></span>

<span data-ttu-id="7419f-272">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="7419f-272">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="7419f-273">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="7419f-273">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="7419f-274">OPS özel Markdown uzantıları</span><span class="sxs-lookup"><span data-stu-id="7419f-274">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="7419f-275">Open Publishing Services (OPS), GitHub Flavored Markdown (GFM) ile yüksek uyumluluğa sahip olan Markdown için Markdig Ayrıştırıcısı’nı uygular.</span><span class="sxs-lookup"><span data-stu-id="7419f-275">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="7419f-276">Markdig, Markdown uzantıları aracılığıyla ilave işlevsellik sağlar.</span><span class="sxs-lookup"><span data-stu-id="7419f-276">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="7419f-277">Bu nedenle, tam OPS Yazma Kılavuzundan bazı makaleler başvuru için bu kılavuza dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7419f-277">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="7419f-278">(Örneğin, içindekiler bölümünde "Markdig ve Markdown uzantıları" ile "Kod parçacıkları" kısımlarına bakın.)</span><span class="sxs-lookup"><span data-stu-id="7419f-278">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="7419f-279">Docs makaleleri çoğu zaman paragraflar, bağlantılar, listeler ve bölüm başlıkları gibi makale biçimlendirmeleri için GFM’yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="7419f-279">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="7419f-280">Makaleler, daha zengin biçimlendirme için aşağıdakiler gibi Markdig özelliklerini kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="7419f-280">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="7419f-281">Not blokları</span><span class="sxs-lookup"><span data-stu-id="7419f-281">Note blocks</span></span>
- <span data-ttu-id="7419f-282">Eklemeler</span><span class="sxs-lookup"><span data-stu-id="7419f-282">Includes</span></span>
- <span data-ttu-id="7419f-283">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="7419f-283">Selectors</span></span>
- <span data-ttu-id="7419f-284">Ekli videolar</span><span class="sxs-lookup"><span data-stu-id="7419f-284">Embedded videos</span></span>
- <span data-ttu-id="7419f-285">Kod parçacıkları/örnekleri</span><span class="sxs-lookup"><span data-stu-id="7419f-285">Code snippets/samples</span></span>

<span data-ttu-id="7419f-286">Tam bir liste için içerikler bölümünde “Markdig ve Markdown uzantıları” ve “Kod parçacıkları” kısmına bakın.</span><span class="sxs-lookup"><span data-stu-id="7419f-286">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="7419f-287">Not blokları</span><span class="sxs-lookup"><span data-stu-id="7419f-287">Note blocks</span></span>

<span data-ttu-id="7419f-288">İlgiyi belirli bir içeriğe çekmek için dört çeşit not blokundan birini seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7419f-288">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="7419f-289">NOT</span><span class="sxs-lookup"><span data-stu-id="7419f-289">NOTE</span></span>
- <span data-ttu-id="7419f-290">UYARI</span><span class="sxs-lookup"><span data-stu-id="7419f-290">WARNING</span></span>
- <span data-ttu-id="7419f-291">İPUCU</span><span class="sxs-lookup"><span data-stu-id="7419f-291">TIP</span></span>
- <span data-ttu-id="7419f-292">ÖNEMLİ</span><span class="sxs-lookup"><span data-stu-id="7419f-292">IMPORTANT</span></span>

<span data-ttu-id="7419f-293">Genel olarak not bloklarını fazla kullanmaktan kaçınmalısınız, dikkat dağıtıcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="7419f-293">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="7419f-294">Not bloklarında kod blokları, görüntüler, listeler ve bağlantılar destekleniyor olsa da bunları olabildiğince sade ve düz bir şekilde oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7419f-294">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="7419f-295">Eklemeler</span><span class="sxs-lookup"><span data-stu-id="7419f-295">Includes</span></span>

<span data-ttu-id="7419f-296">Makale dosyalarına dahil edilmesi gereken yeniden kullanılabilir metin veya görüntü dosyalarınız varsa dosyayı Markdig dosya dahil etme özelliği ile “dahil etmek” için bir başvuru kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7419f-296">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="7419f-297">Bu özellik, verilen dosyayı makalenize derleme sırasında “eklemesi” için OPS’yi yönlendirir, böylece dosya da yayımlanan makalenizin bir parçası olur.</span><span class="sxs-lookup"><span data-stu-id="7419f-297">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="7419f-298">İçerikleri tekrar kullanmanıza imkan veren üç tür ekleme vardır:</span><span class="sxs-lookup"><span data-stu-id="7419f-298">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="7419f-299">Satır içi: Genel bir metin parçacığını başka bir cümlede satır içinde yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="7419f-299">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="7419f-300">Blok: Makalenin bir bölümündeki bütün bir Markdown dosyasını yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="7419f-300">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="7419f-301">Görüntüler: Docs’ta standart görüntü ekleme yoludur.</span><span class="sxs-lookup"><span data-stu-id="7419f-301">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="7419f-302">Satır içi ve blok eklemeleri, basit birer Markdown (.md) dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="7419f-302">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="7419f-303">Bu dosyalar, herhangi bir geçerli Markdown barındırabilir.</span><span class="sxs-lookup"><span data-stu-id="7419f-303">It can contain any valid Markdown.</span></span> <span data-ttu-id="7419f-304">Tüm ekleme Markdown dosyaları, depo kökünde [ortak bir `/includes` alt dizinine](git-github-fundamentals.md#includes-subdirectory) yerleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7419f-304">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="7419f-305">Makale yayımlandığında, eklenen dosya makaleyle sorunsuz bir şekilde tümleşmiş olur.</span><span class="sxs-lookup"><span data-stu-id="7419f-305">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="7419f-306">Eklemelere yönelik gereksinimler ve önemli konular şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7419f-306">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="7419f-307">Aynı metni birden fazla makalede kullanmanız gerektiği zaman eklemeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="7419f-307">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="7419f-308">Blok eklemeleri bir veya iki paragraf, paylaşılan bir yordam veya paylaşılan bir kısım gibi büyük içeriklerle kullanın.</span><span class="sxs-lookup"><span data-stu-id="7419f-308">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="7419f-309">Ancak bir cümleden daha küçük şeyler için kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="7419f-309">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="7419f-310">Eklenen dosyalar, makalenizin GitHub tarafından işlenmiş görünümünde işlenmez çünkü bunlar, Markdig uzantılarına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7419f-310">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="7419f-311">Bunlar yalnızca yayın sonrasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7419f-311">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="7419f-312">Eklemeye başvuran makaledeki bir eklemede bütün metnin, tam cümlelerden oluşmasına veya öncesinde ya da sonrasındaki metne bağlı olmayan tümcecikler halinde olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7419f-312">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="7419f-313">Bu kılavuzu dikkate almamak, makalede çevrilemeyen bir satır oluşturur ve yerelleştirme deneyimini bozar.</span><span class="sxs-lookup"><span data-stu-id="7419f-313">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="7419f-314">Eklemeleri birbirine eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="7419f-314">Don't embed includes within other includes.</span></span> <span data-ttu-id="7419f-315">Bu, desteklenmeyen bir durumdur.</span><span class="sxs-lookup"><span data-stu-id="7419f-315">They are not supported.</span></span>
- <span data-ttu-id="7419f-316">Medya dosyalarını ekleme alt dizinine özgü bir medya klasörüne yerleştirin, örneğin `<repo>`/eklemeler/medya klasörü.</span><span class="sxs-lookup"><span data-stu-id="7419f-316">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="7419f-317">Medya dizini, kökünde hiçbir görüntü barındırmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="7419f-317">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="7419f-318">Eklemede görüntü yoksa buna karşılık gelecek bir medya dizini gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="7419f-318">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="7419f-319">Normal makalelerde olduğu gibi, ekleme dosyaları arasında medya paylaşmayın.</span><span class="sxs-lookup"><span data-stu-id="7419f-319">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="7419f-320">Her bir ekleme ve makale için benzersiz ada sahip ayrı dosyalar kullanın.</span><span class="sxs-lookup"><span data-stu-id="7419f-320">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="7419f-321">Medya dosyasını, eklemeyle ilişkili medya klasöründe depolayın.</span><span class="sxs-lookup"><span data-stu-id="7419f-321">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="7419f-322">Eklemeleri, bir makalenin tek içeriği olarak kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="7419f-322">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="7419f-323">Eklemelerin, makaledeki diğer içerikleri tamamlayıcı görevi vardır.</span><span class="sxs-lookup"><span data-stu-id="7419f-323">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="7419f-324">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="7419f-324">Selectors</span></span>

<span data-ttu-id="7419f-325">Seçicileri; teknik makalelerde, aynı makalenin farklı bölümlerini yazdığınızda teknolojiler veya platformlar arasındaki uygulama farklılıklarına değinirken kullanın.</span><span class="sxs-lookup"><span data-stu-id="7419f-325">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="7419f-326">Bu genellikle geliştiriciler için mobil platform içeriklerimizde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7419f-326">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="7419f-327">Markdig’de şu anda iki farklı türde seçici vardır; tekli seçici ve çoklu seçici.</span><span class="sxs-lookup"><span data-stu-id="7419f-327">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="7419f-328">Aynı seçici Markdown, seçimdeki her bir makaleye gittiği için makalenizin seçicisini bir eklemeye yerleştirmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="7419f-328">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="7419f-329">Daha sonra tüm makalelerinizde aynı seçiciyi kullanan eklemeye başvurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7419f-329">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="7419f-330">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="7419f-330">Code snippets</span></span>

<span data-ttu-id="7419f-331">Markdig, bir makaleye kod parçacığı uzantısı aracılığıyla gelişmiş kod eklemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="7419f-331">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="7419f-332">Programlama dili seçimi ve söz dizimi renklendirme gibi GFM özellikleri üzerinde ortaya çıkan gelişmiş işleme seçenekleri sağlar, bunların yanında aşağıdaki gibi kullanışlı özellikler de getirir:</span><span class="sxs-lookup"><span data-stu-id="7419f-332">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="7419f-333">Bir dış depodan gelen merkezi kod örnekleri/parçacıklarının eklenmesi.</span><span class="sxs-lookup"><span data-stu-id="7419f-333">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="7419f-334">Kod örneklerinin farklı dillerdeki birçok çeşidini gösteren sekmeli kullanıcı arabirimi.</span><span class="sxs-lookup"><span data-stu-id="7419f-334">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="7419f-335">Tuzaklar ve sorun giderme</span><span class="sxs-lookup"><span data-stu-id="7419f-335">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="7419f-336">Alternatif metin</span><span class="sxs-lookup"><span data-stu-id="7419f-336">Alt text</span></span>

<span data-ttu-id="7419f-337">Alt çizgi içeren alternatif metin düzgün bir şekilde işlenmez.</span><span class="sxs-lookup"><span data-stu-id="7419f-337">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="7419f-338">Örneğin, şunu kullanmak yerine:</span><span class="sxs-lookup"><span data-stu-id="7419f-338">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="7419f-339">Şunun gibi alt çizgilerden kaçının:</span><span class="sxs-lookup"><span data-stu-id="7419f-339">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="7419f-340">Kesme işareti ve tırnak işaretleri</span><span class="sxs-lookup"><span data-stu-id="7419f-340">Apostrophes and quotation marks</span></span>

<span data-ttu-id="7419f-341">Word dosyasından Markdown editörüne bir şey kopyalarsanız kopyaladığınız metin “akıllı” (kıvrık) kesme işaretleri veya tırnak işaretleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="7419f-341">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="7419f-342">Bunların kodlanması veya kesme işareti ya da tırnak işaretlerine dönüştürülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="7419f-342">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span>
<span data-ttu-id="7419f-343">Aksi takdirde, dosya yayımlandığında şu karakterleri görebilirsiniz: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="7419f-343">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="7419f-344">Bu noktalama işaretlerinin “akıllı” olanları için kodlamalar aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="7419f-344">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="7419f-345">Sol (açma) tırnak işareti: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="7419f-345">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="7419f-346">Sağ (kapatma) tırnak işareti: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="7419f-346">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="7419f-347">Sağ (kapatma) tekli tırnak işareti veya kesme işareti: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="7419f-347">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="7419f-348">Sağ (açma) tekli tırnak işareti (nadiren kullanılır): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="7419f-348">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="7419f-349">Açılı ayraçlar</span><span class="sxs-lookup"><span data-stu-id="7419f-349">Angle brackets</span></span>

<span data-ttu-id="7419f-350">Bir yer tutucuyu ifade etmek için köşeli ayraç kullanımı yaygındır.</span><span class="sxs-lookup"><span data-stu-id="7419f-350">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="7419f-351">Metinde (kodda değil) bunu yaptığınızda, köşeli ayraçları kodlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7419f-351">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="7419f-352">Aksi takdirde Markdown bunların HTML etiketleri olması gerektiğini düşünür.</span><span class="sxs-lookup"><span data-stu-id="7419f-352">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="7419f-353">Örneğin `<script name>` öğesini `&lt;script name&gt;` şeklinde kodlayın</span><span class="sxs-lookup"><span data-stu-id="7419f-353">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="7419f-354">Ayrıca bkz.:</span><span class="sxs-lookup"><span data-stu-id="7419f-354">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="7419f-355">Markdown kaynakları</span><span class="sxs-lookup"><span data-stu-id="7419f-355">Markdown resources</span></span>

- [<span data-ttu-id="7419f-356">Markdown’a Giriş</span><span class="sxs-lookup"><span data-stu-id="7419f-356">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="7419f-357">Docs Markdown kural sayfası</span><span class="sxs-lookup"><span data-stu-id="7419f-357">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="7419f-358">GitHub Markdown Temel Bilgileri</span><span class="sxs-lookup"><span data-stu-id="7419f-358">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="7419f-359">Markdown Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="7419f-359">The Markdown Guide</span></span>](https://www.markdownguide.org/)
