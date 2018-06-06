---
title: Docs’ta makale yazmak için Markdown kullanma
description: Bu makale, docs.microsoft.com makalelerinde kullanılan Markdown dilinin temellerini ve başvuru bilgilerini sağlar.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 041398361aef90c44bdf3a0dad4aaa2d40a38289
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469958"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="a5605-103">Docs’ta makale yazmak için Markdown kullanma</span><span class="sxs-lookup"><span data-stu-id="a5605-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="a5605-104">Docs.microsoft.com makaleleri [Markdown](https://daringfireball.net/projects/markdown/) adı verilen hafif biçimlendirme dilinde yazılır, bu dilin okunması ve öğrenilmesi kolaydır.</span><span class="sxs-lookup"><span data-stu-id="a5605-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="a5605-105">O nedenle bu dil kısa sürede endüstri standardı haline gelmiştir.</span><span class="sxs-lookup"><span data-stu-id="a5605-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="a5605-106">Docs içerikleri GitHub’da depolandığı için [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) adlı bir Markdown üst kümesi kullanabilir. GFM, yaygın biçimlendirme ihtiyaçları için ilave işlevler sağlar.</span><span class="sxs-lookup"><span data-stu-id="a5605-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="a5605-107">Ayrıca Open Publishing Services (OPS), Markdig Markdown Ayrıştırıcısı’nı uygular.</span><span class="sxs-lookup"><span data-stu-id="a5605-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="a5605-108">Markdig, GitHub Flavored Markdown (GFM) ile son derece uyumlu olduğu için Docs’a özgü özellikleri etkinleştirmek için ek işlevsellik sağlar.</span><span class="sxs-lookup"><span data-stu-id="a5605-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="a5605-109">Markdig; .NET için hızlı, güçlü, CommonMark uyumlu, genişletilebilir Markdown işlemcisidir.</span><span class="sxs-lookup"><span data-stu-id="a5605-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="a5605-110">Daha iyi topluluk desteği</span><span class="sxs-lookup"><span data-stu-id="a5605-110">Better community support</span></span>
* <span data-ttu-id="a5605-111">Daha iyi standartlar desteği</span><span class="sxs-lookup"><span data-stu-id="a5605-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="a5605-112">Markdown temel bilgileri</span><span class="sxs-lookup"><span data-stu-id="a5605-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="a5605-113">Bölüm başlıkları</span><span class="sxs-lookup"><span data-stu-id="a5605-113">Headings</span></span>

<span data-ttu-id="a5605-114">Bir bölüm başlığı oluşturmak için karma işaretini (#) aşağıdaki gibi kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="a5605-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="a5605-115">Kalın ve italik metin</span><span class="sxs-lookup"><span data-stu-id="a5605-115">Bold and italic text</span></span>

<span data-ttu-id="a5605-116">Bir metni **kalın** olarak biçimlendirmek için iki yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="a5605-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="a5605-117">Bir metni *italik* olarak biçimlendirmek için bir yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="a5605-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="a5605-118">Bir metni ***kalın ve italik*** olarak biçimlendirmek için üç yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="a5605-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="a5605-119">Listeler</span><span class="sxs-lookup"><span data-stu-id="a5605-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="a5605-120">Sırasız liste</span><span class="sxs-lookup"><span data-stu-id="a5605-120">Unordered list</span></span>

<span data-ttu-id="a5605-121">Sırasız/madde işaretli bir listeyi biçimlendirmek için yıldız işaretleri veya tireler kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5605-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="a5605-122">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="a5605-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="a5605-123">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="a5605-123">will be rendered as:</span></span>

- <span data-ttu-id="a5605-124">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="a5605-124">List item 1</span></span>
- <span data-ttu-id="a5605-125">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="a5605-125">List item 2</span></span>
- <span data-ttu-id="a5605-126">Liste öğesi 3</span><span class="sxs-lookup"><span data-stu-id="a5605-126">List item 3</span></span>

<span data-ttu-id="a5605-127">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="a5605-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="a5605-128">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="a5605-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="a5605-129">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="a5605-129">will be rendered as:</span></span>

- <span data-ttu-id="a5605-130">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="a5605-130">List item 1</span></span>
  - <span data-ttu-id="a5605-131">Liste öğesi A</span><span class="sxs-lookup"><span data-stu-id="a5605-131">List item A</span></span>
  - <span data-ttu-id="a5605-132">Liste öğesi B</span><span class="sxs-lookup"><span data-stu-id="a5605-132">List item B</span></span>
- <span data-ttu-id="a5605-133">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="a5605-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="a5605-134">Sıralı liste</span><span class="sxs-lookup"><span data-stu-id="a5605-134">Ordered list</span></span>

<span data-ttu-id="a5605-135">Sıralı/adımlı bir listeyi biçimlendirmek için sıra numaraları kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="a5605-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="a5605-136">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="a5605-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="a5605-137">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="a5605-137">will be rendered as:</span></span>

1. <span data-ttu-id="a5605-138">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="a5605-138">First instruction</span></span>
2. <span data-ttu-id="a5605-139">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="a5605-139">Second instruction</span></span>
3. <span data-ttu-id="a5605-140">Üçüncü yönerge</span><span class="sxs-lookup"><span data-stu-id="a5605-140">Third instruction</span></span>

<span data-ttu-id="a5605-141">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="a5605-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="a5605-142">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="a5605-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="a5605-143">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="a5605-143">will be rendered as:</span></span>

1. <span data-ttu-id="a5605-144">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="a5605-144">First instruction</span></span>
    1. <span data-ttu-id="a5605-145">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="a5605-145">Sub-instruction</span></span>
    2. <span data-ttu-id="a5605-146">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="a5605-146">Sub-instruction</span></span>
2. <span data-ttu-id="a5605-147">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="a5605-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="a5605-148">eğlence</span><span class="sxs-lookup"><span data-stu-id="a5605-148">Tables</span></span>

<span data-ttu-id="a5605-149">Tablolar, temel Markdown belirtiminin parçası değildir, ancak GFM tarafından desteklenir.</span><span class="sxs-lookup"><span data-stu-id="a5605-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="a5605-150">Düz çizgi (|) ve kısa çizgi (-) karakterlerini kullanarak tablolar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5605-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="a5605-151">Kısa çizgiler sütunların üst bilgisini oluştururken düz çizgiler sütunları birbirinden ayırır.</span><span class="sxs-lookup"><span data-stu-id="a5605-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="a5605-152">Tablonun doğru işlenebilmesi için başına boş bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a5605-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="a5605-153">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="a5605-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="a5605-154">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="a5605-154">will be rendered as:</span></span>

| <span data-ttu-id="a5605-155">Tablolar</span><span class="sxs-lookup"><span data-stu-id="a5605-155">Fun</span></span>                  | <span data-ttu-id="a5605-156">Şununla:</span><span class="sxs-lookup"><span data-stu-id="a5605-156">With</span></span>                 | <span data-ttu-id="a5605-157">eğlence</span><span class="sxs-lookup"><span data-stu-id="a5605-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="a5605-158">sola hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="a5605-158">left-aligned column</span></span>  | <span data-ttu-id="a5605-159">sağa hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="a5605-159">right-aligned column</span></span> | <span data-ttu-id="a5605-160">ortalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="a5605-160">centered column</span></span> |
| <span data-ttu-id="a5605-161">100 $</span><span class="sxs-lookup"><span data-stu-id="a5605-161">$100</span></span>                 | <span data-ttu-id="a5605-162">100 $</span><span class="sxs-lookup"><span data-stu-id="a5605-162">$100</span></span>                 | <span data-ttu-id="a5605-163">100 $</span><span class="sxs-lookup"><span data-stu-id="a5605-163">$100</span></span>            |
| <span data-ttu-id="a5605-164">10 $</span><span class="sxs-lookup"><span data-stu-id="a5605-164">$10</span></span>                  | <span data-ttu-id="a5605-165">10 $</span><span class="sxs-lookup"><span data-stu-id="a5605-165">$10</span></span>                  | <span data-ttu-id="a5605-166">10 $</span><span class="sxs-lookup"><span data-stu-id="a5605-166">$10</span></span>             |
| <span data-ttu-id="a5605-167">1 $</span><span class="sxs-lookup"><span data-stu-id="a5605-167">$1</span></span>                   | <span data-ttu-id="a5605-168">1 $</span><span class="sxs-lookup"><span data-stu-id="a5605-168">$1</span></span>                   | <span data-ttu-id="a5605-169">1 $</span><span class="sxs-lookup"><span data-stu-id="a5605-169">$1</span></span>              |

<span data-ttu-id="a5605-170">Tablo oluşturma hakkında daha fazla bilgi için şunlara bakın:</span><span class="sxs-lookup"><span data-stu-id="a5605-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="a5605-171">Geniş tabloların biçimlendirmesinde yardımcı olabilecek Markdig [tablo sarmalama özelliği](#table-wrapping)</span><span class="sxs-lookup"><span data-stu-id="a5605-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="a5605-172">GitHub’ın [Tablolarla bilgi düzenleme](https://help.github.com/articles/organizing-information-with-tables/) makalesi</span><span class="sxs-lookup"><span data-stu-id="a5605-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="a5605-173">[Markdown Tablo Oluşturucu](https://www.tablesgenerator.com/markdown_tables) web uygulaması</span><span class="sxs-lookup"><span data-stu-id="a5605-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="a5605-174">Adam Pritchard - Markdown Kural Sayfası</span><span class="sxs-lookup"><span data-stu-id="a5605-174">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="a5605-175">Michel Fortin - Markdown Ekstra</span><span class="sxs-lookup"><span data-stu-id="a5605-175">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="a5605-176">HTML tablolarını Markdown’a dönüştürme</span><span class="sxs-lookup"><span data-stu-id="a5605-176">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="a5605-177">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="a5605-177">Links</span></span>

<span data-ttu-id="a5605-178">Satır içi bağlantılarda Markdown söz dizimi, köprü bağlantısı eklenecek `[link text]` metni ve bağlantı verilen URL ya da dosya adı olan `(file-name.md)` kısımlarından oluşur:</span><span class="sxs-lookup"><span data-stu-id="a5605-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="a5605-179">Bağlantı verme hakkında daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="a5605-179">For more information on linking, see:</span></span>

- <span data-ttu-id="a5605-180">Markdown’ın temel bağlantı desteği konusunda ayrıntılar için [Markdown söz dizimi kılavuzu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="a5605-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="a5605-181">Markdig tarafından sağlanan ilave bağlayıcı söz dizimi hakkında ayrıntılar için bu kılavuzun [Bağlantılar](how-to-write-links.md) bölümü.</span><span class="sxs-lookup"><span data-stu-id="a5605-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="a5605-182">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="a5605-182">Code snippets</span></span>

<span data-ttu-id="a5605-183">Markdown, hem bir cümlede satır içi olarak hem de cümleler arasında ayrı “çevrelenmiş” bir blok halinde kod parçacıkları yerleştirilmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="a5605-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="a5605-184">Ayrıntılar için bkz.</span><span class="sxs-lookup"><span data-stu-id="a5605-184">For details, see:</span></span>

- [<span data-ttu-id="a5605-185">Kod blokları için yerel Markdown desteği</span><span class="sxs-lookup"><span data-stu-id="a5605-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="a5605-186">Kod çevreleme ve söz dizimi vurgulama için GFM desteği</span><span class="sxs-lookup"><span data-stu-id="a5605-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="a5605-187">Çevrelenmiş kod blokları, kod parçacıklarınız için söz dizimi vurgulamasını etkinleştirmenin kolay bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="a5605-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="a5605-188">Çevrelenmiş kod bloklarının biçimi genelde şöyledir:</span><span class="sxs-lookup"><span data-stu-id="a5605-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="a5605-189">İlk üç ters tırnak (\`) karakterinden sonra gelen diğer ad, kullanılacak söz dizimi vurgulamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5605-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="a5605-190">Docs içeriğinde yaygın olarak kullanılan programlama dilleri ve bunların etiketleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="a5605-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="a5605-191">Bu diller, kolay as desteğine ve dil vurgulamasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="a5605-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="a5605-192">Ad</span><span class="sxs-lookup"><span data-stu-id="a5605-192">Name</span></span>|<span data-ttu-id="a5605-193">Markdown Etiketi</span><span class="sxs-lookup"><span data-stu-id="a5605-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="a5605-194">.NET Konsolu</span><span class="sxs-lookup"><span data-stu-id="a5605-194">.NET Console</span></span>|<span data-ttu-id="a5605-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="a5605-195">dotnetcli</span></span>|
|<span data-ttu-id="a5605-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="a5605-196">ASP.NET (C#)</span></span>|<span data-ttu-id="a5605-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="a5605-197">aspx-csharp</span></span>|
|<span data-ttu-id="a5605-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="a5605-198">ASP.NET (VB)</span></span>|<span data-ttu-id="a5605-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="a5605-199">aspx-vb</span></span>|
|<span data-ttu-id="a5605-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="a5605-200">AzCopy</span></span>|<span data-ttu-id="a5605-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="a5605-201">azcopy</span></span>|
|<span data-ttu-id="a5605-202">Azure CLI’si</span><span class="sxs-lookup"><span data-stu-id="a5605-202">Azure CLI</span></span>|<span data-ttu-id="a5605-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="a5605-203">azurecli</span></span>|
|<span data-ttu-id="a5605-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5605-204">Azure PowerShell</span></span>|<span data-ttu-id="a5605-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="a5605-205">azurepowershell</span></span>|
|<span data-ttu-id="a5605-206">C++</span><span class="sxs-lookup"><span data-stu-id="a5605-206">C++</span></span>|<span data-ttu-id="a5605-207">cpp</span><span class="sxs-lookup"><span data-stu-id="a5605-207">cpp</span></span>|
|<span data-ttu-id="a5605-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="a5605-208">C++/CX</span></span>|<span data-ttu-id="a5605-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="a5605-209">cppcx</span></span>|
|<span data-ttu-id="a5605-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="a5605-210">C++/WinRT</span></span>|<span data-ttu-id="a5605-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="a5605-211">cppwinrt</span></span>|
|<span data-ttu-id="a5605-212">C#</span><span class="sxs-lookup"><span data-stu-id="a5605-212">C#</span></span>|<span data-ttu-id="a5605-213">csharp</span><span class="sxs-lookup"><span data-stu-id="a5605-213">csharp</span></span>|
|<span data-ttu-id="a5605-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="a5605-214">CSHTML</span></span>|<span data-ttu-id="a5605-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="a5605-215">cshtml</span></span>|
|<span data-ttu-id="a5605-216">DAX</span><span class="sxs-lookup"><span data-stu-id="a5605-216">DAX</span></span>|<span data-ttu-id="a5605-217">dax</span><span class="sxs-lookup"><span data-stu-id="a5605-217">dax</span></span>|
|<span data-ttu-id="a5605-218">F#</span><span class="sxs-lookup"><span data-stu-id="a5605-218">F#</span></span>|<span data-ttu-id="a5605-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="a5605-219">fsharp</span></span>|
|<span data-ttu-id="a5605-220">Go</span><span class="sxs-lookup"><span data-stu-id="a5605-220">Go</span></span>|<span data-ttu-id="a5605-221">go</span><span class="sxs-lookup"><span data-stu-id="a5605-221">go</span></span>|
|<span data-ttu-id="a5605-222">HTML</span><span class="sxs-lookup"><span data-stu-id="a5605-222">HTML</span></span>|<span data-ttu-id="a5605-223">html</span><span class="sxs-lookup"><span data-stu-id="a5605-223">html</span></span>|
|<span data-ttu-id="a5605-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="a5605-224">HTTP</span></span>|<span data-ttu-id="a5605-225">http</span><span class="sxs-lookup"><span data-stu-id="a5605-225">http</span></span>|
|<span data-ttu-id="a5605-226">Java</span><span class="sxs-lookup"><span data-stu-id="a5605-226">Java</span></span>|<span data-ttu-id="a5605-227">java</span><span class="sxs-lookup"><span data-stu-id="a5605-227">java</span></span>|
|<span data-ttu-id="a5605-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="a5605-228">JavaScript</span></span>|<span data-ttu-id="a5605-229">javascript</span><span class="sxs-lookup"><span data-stu-id="a5605-229">javascript</span></span>|
|<span data-ttu-id="a5605-230">JSON</span><span class="sxs-lookup"><span data-stu-id="a5605-230">JSON</span></span>|<span data-ttu-id="a5605-231">json</span><span class="sxs-lookup"><span data-stu-id="a5605-231">json</span></span>|
|<span data-ttu-id="a5605-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="a5605-232">Markdown</span></span>|<span data-ttu-id="a5605-233">md</span><span class="sxs-lookup"><span data-stu-id="a5605-233">md</span></span>|
|<span data-ttu-id="a5605-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="a5605-234">NodeJS</span></span>|<span data-ttu-id="a5605-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="a5605-235">nodejs</span></span>|
|<span data-ttu-id="a5605-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="a5605-236">Objective-C</span></span>|<span data-ttu-id="a5605-237">objc</span><span class="sxs-lookup"><span data-stu-id="a5605-237">objc</span></span>|
|<span data-ttu-id="a5605-238">OData</span><span class="sxs-lookup"><span data-stu-id="a5605-238">OData</span></span>|<span data-ttu-id="a5605-239">odata</span><span class="sxs-lookup"><span data-stu-id="a5605-239">odata</span></span>|
|<span data-ttu-id="a5605-240">PHP</span><span class="sxs-lookup"><span data-stu-id="a5605-240">PHP</span></span>|<span data-ttu-id="a5605-241">php</span><span class="sxs-lookup"><span data-stu-id="a5605-241">php</span></span>|
|<span data-ttu-id="a5605-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="a5605-242">Power Apps Formula</span></span>|<span data-ttu-id="a5605-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="a5605-243">powerappsfl</span></span>|
|<span data-ttu-id="a5605-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5605-244">PowerShell</span></span>|<span data-ttu-id="a5605-245">powershell</span><span class="sxs-lookup"><span data-stu-id="a5605-245">powershell</span></span>|
|<span data-ttu-id="a5605-246">Python</span><span class="sxs-lookup"><span data-stu-id="a5605-246">Python</span></span>|<span data-ttu-id="a5605-247">python</span><span class="sxs-lookup"><span data-stu-id="a5605-247">python</span></span>|
|<span data-ttu-id="a5605-248">Q#</span><span class="sxs-lookup"><span data-stu-id="a5605-248">Q#</span></span>|<span data-ttu-id="a5605-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="a5605-249">qsharp</span></span>|
|<span data-ttu-id="a5605-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="a5605-250">Ruby</span></span>|<span data-ttu-id="a5605-251">ruby</span><span class="sxs-lookup"><span data-stu-id="a5605-251">ruby</span></span>|
|<span data-ttu-id="a5605-252">SQL</span><span class="sxs-lookup"><span data-stu-id="a5605-252">SQL</span></span>|<span data-ttu-id="a5605-253">sql</span><span class="sxs-lookup"><span data-stu-id="a5605-253">sql</span></span>|
|<span data-ttu-id="a5605-254">Swift</span><span class="sxs-lookup"><span data-stu-id="a5605-254">Swift</span></span>|<span data-ttu-id="a5605-255">swift</span><span class="sxs-lookup"><span data-stu-id="a5605-255">swift</span></span>|
|<span data-ttu-id="a5605-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="a5605-256">TypeScript</span></span>|<span data-ttu-id="a5605-257">typescript</span><span class="sxs-lookup"><span data-stu-id="a5605-257">typescript</span></span>|
|<span data-ttu-id="a5605-258">VB</span><span class="sxs-lookup"><span data-stu-id="a5605-258">VB</span></span>|<span data-ttu-id="a5605-259">vb</span><span class="sxs-lookup"><span data-stu-id="a5605-259">vb</span></span>|
|<span data-ttu-id="a5605-260">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="a5605-260">VSTS CLI</span></span>|<span data-ttu-id="a5605-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="a5605-261">vstscli</span></span>|
|<span data-ttu-id="a5605-262">XAML</span><span class="sxs-lookup"><span data-stu-id="a5605-262">XAML</span></span>|<span data-ttu-id="a5605-263">xaml</span><span class="sxs-lookup"><span data-stu-id="a5605-263">xaml</span></span>|
|<span data-ttu-id="a5605-264">XML</span><span class="sxs-lookup"><span data-stu-id="a5605-264">XML</span></span>|<span data-ttu-id="a5605-265">xml</span><span class="sxs-lookup"><span data-stu-id="a5605-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="a5605-266">Örnek: C\#</span><span class="sxs-lookup"><span data-stu-id="a5605-266">Example: C\#</span></span>

<span data-ttu-id="a5605-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="a5605-267">__Markdown__</span></span>

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

<span data-ttu-id="a5605-268">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="a5605-268">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="a5605-269">Örnek: SQL</span><span class="sxs-lookup"><span data-stu-id="a5605-269">Example: SQL</span></span>

<span data-ttu-id="a5605-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="a5605-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="a5605-271">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="a5605-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="a5605-272">OPS özel Markdown uzantıları</span><span class="sxs-lookup"><span data-stu-id="a5605-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="a5605-273">Open Publishing Services (OPS), GitHub Flavored Markdown (GFM) ile yüksek uyumluluğa sahip olan Markdown için Markdig Ayrıştırıcısı’nı uygular.</span><span class="sxs-lookup"><span data-stu-id="a5605-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="a5605-274">Markdig, Markdown uzantıları aracılığıyla ilave işlevsellik sağlar.</span><span class="sxs-lookup"><span data-stu-id="a5605-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="a5605-275">Bu nedenle, tam OPS Yazma Kılavuzundan bazı makaleler başvuru için bu kılavuza dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a5605-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="a5605-276">(Örneğin, içindekiler bölümünde "Markdig ve Markdown uzantıları" ile "Kod parçacıkları" kısımlarına bakın.)</span><span class="sxs-lookup"><span data-stu-id="a5605-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="a5605-277">Docs makaleleri çoğu zaman paragraflar, bağlantılar, listeler ve bölüm başlıkları gibi makale biçimlendirmeleri için GFM’yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="a5605-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="a5605-278">Makaleler, daha zengin biçimlendirme için aşağıdakiler gibi Markdig özelliklerini kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="a5605-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="a5605-279">Not blokları</span><span class="sxs-lookup"><span data-stu-id="a5605-279">Note blocks</span></span>
- <span data-ttu-id="a5605-280">Eklemeler</span><span class="sxs-lookup"><span data-stu-id="a5605-280">Includes</span></span>
- <span data-ttu-id="a5605-281">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="a5605-281">Selectors</span></span>
- <span data-ttu-id="a5605-282">Ekli videolar</span><span class="sxs-lookup"><span data-stu-id="a5605-282">Embedded videos</span></span>
- <span data-ttu-id="a5605-283">Kod parçacıkları/örnekleri</span><span class="sxs-lookup"><span data-stu-id="a5605-283">Code snippets/samples</span></span>

<span data-ttu-id="a5605-284">Tam bir liste için içerikler bölümünde “Markdig ve Markdown uzantıları” ve “Kod parçacıkları” kısmına bakın.</span><span class="sxs-lookup"><span data-stu-id="a5605-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="a5605-285">Not blokları</span><span class="sxs-lookup"><span data-stu-id="a5605-285">Note blocks</span></span>

<span data-ttu-id="a5605-286">İlgiyi belirli bir içeriğe çekmek için dört çeşit not blokundan birini seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a5605-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="a5605-287">NOT</span><span class="sxs-lookup"><span data-stu-id="a5605-287">NOTE</span></span>
- <span data-ttu-id="a5605-288">UYARI</span><span class="sxs-lookup"><span data-stu-id="a5605-288">WARNING</span></span>
- <span data-ttu-id="a5605-289">İPUCU</span><span class="sxs-lookup"><span data-stu-id="a5605-289">TIP</span></span>
- <span data-ttu-id="a5605-290">ÖNEMLİ</span><span class="sxs-lookup"><span data-stu-id="a5605-290">IMPORTANT</span></span>

<span data-ttu-id="a5605-291">Genel olarak not bloklarını fazla kullanmaktan kaçınmalısınız, dikkat dağıtıcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="a5605-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="a5605-292">Not bloklarında kod blokları, görüntüler, listeler ve bağlantılar destekleniyor olsa da bunları olabildiğince sade ve düz bir şekilde oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5605-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="a5605-293">Eklemeler</span><span class="sxs-lookup"><span data-stu-id="a5605-293">Includes</span></span>

<span data-ttu-id="a5605-294">Makale dosyalarına dahil edilmesi gereken yeniden kullanılabilir metin veya görüntü dosyalarınız varsa dosyayı Markdig dosya dahil etme özelliği ile “dahil etmek” için bir başvuru kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5605-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="a5605-295">Bu özellik, verilen dosyayı makalenize derleme sırasında “eklemesi” için OPS’yi yönlendirir, böylece dosya da yayımlanan makalenizin bir parçası olur.</span><span class="sxs-lookup"><span data-stu-id="a5605-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="a5605-296">İçerikleri tekrar kullanmanıza imkan veren üç tür ekleme vardır:</span><span class="sxs-lookup"><span data-stu-id="a5605-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="a5605-297">Satır içi: Genel bir metin parçacığını başka bir cümlede satır içinde yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5605-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="a5605-298">Blok: Makalenin bir bölümündeki bütün bir Markdown dosyasını yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5605-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="a5605-299">Görüntüler: Docs’ta standart görüntü ekleme yoludur.</span><span class="sxs-lookup"><span data-stu-id="a5605-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="a5605-300">Satır içi ve blok eklemeleri, basit birer Markdown (.md) dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="a5605-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="a5605-301">Bu dosyalar, herhangi bir geçerli Markdown barındırabilir.</span><span class="sxs-lookup"><span data-stu-id="a5605-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="a5605-302">Tüm ekleme Markdown dosyaları, depo kökünde [ortak bir `/includes` alt dizinine](git-github-fundamentals.md#includes-subdirectory) yerleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a5605-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="a5605-303">Makale yayımlandığında, eklenen dosya makaleyle sorunsuz bir şekilde tümleşmiş olur.</span><span class="sxs-lookup"><span data-stu-id="a5605-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="a5605-304">Eklemelere yönelik gereksinimler ve önemli konular şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a5605-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="a5605-305">Aynı metni birden fazla makalede kullanmanız gerektiği zaman eklemeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5605-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="a5605-306">Blok eklemeleri bir veya iki paragraf, paylaşılan bir yordam veya paylaşılan bir kısım gibi büyük içeriklerle kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5605-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="a5605-307">Ancak bir cümleden daha küçük şeyler için kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="a5605-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="a5605-308">Eklenen dosyalar, makalenizin GitHub tarafından işlenmiş görünümünde işlenmez çünkü bunlar, Markdig uzantılarına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a5605-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="a5605-309">Bunlar yalnızca yayın sonrasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a5605-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="a5605-310">Eklemeye başvuran makaledeki bir eklemede bütün metnin, tam cümlelerden oluşmasına veya öncesinde ya da sonrasındaki metne bağlı olmayan tümcecikler halinde olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="a5605-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="a5605-311">Bu kılavuzu dikkate almamak, makalede çevrilemeyen bir satır oluşturur ve yerelleştirme deneyimini bozar.</span><span class="sxs-lookup"><span data-stu-id="a5605-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="a5605-312">Eklemeleri birbirine eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="a5605-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="a5605-313">Bu, desteklenmeyen bir durumdur.</span><span class="sxs-lookup"><span data-stu-id="a5605-313">They are not supported.</span></span>
- <span data-ttu-id="a5605-314">Medya dosyalarını ekleme alt dizinine özgü bir medya klasörüne yerleştirin, örneğin `<repo>`/eklemeler/medya klasörü.</span><span class="sxs-lookup"><span data-stu-id="a5605-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="a5605-315">Medya dizini, kökünde hiçbir görüntü barındırmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="a5605-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="a5605-316">Eklemede görüntü yoksa buna karşılık gelecek bir medya dizini gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="a5605-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="a5605-317">Normal makalelerde olduğu gibi, ekleme dosyaları arasında medya paylaşmayın.</span><span class="sxs-lookup"><span data-stu-id="a5605-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="a5605-318">Her bir ekleme ve makale için benzersiz ada sahip ayrı dosyalar kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5605-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="a5605-319">Medya dosyasını, eklemeyle ilişkili medya klasöründe depolayın.</span><span class="sxs-lookup"><span data-stu-id="a5605-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="a5605-320">Eklemeleri, bir makalenin tek içeriği olarak kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="a5605-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="a5605-321">Eklemelerin, makaledeki diğer içerikleri tamamlayıcı görevi vardır.</span><span class="sxs-lookup"><span data-stu-id="a5605-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="a5605-322">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="a5605-322">Selectors</span></span>

<span data-ttu-id="a5605-323">Seçicileri; teknik makalelerde, aynı makalenin farklı bölümlerini yazdığınızda teknolojiler veya platformlar arasındaki uygulama farklılıklarına değinirken kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5605-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="a5605-324">Bu genellikle geliştiriciler için mobil platform içeriklerimizde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a5605-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="a5605-325">Markdig’de şu anda iki farklı türde seçici vardır; tekli seçici ve çoklu seçici.</span><span class="sxs-lookup"><span data-stu-id="a5605-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="a5605-326">Aynı seçici Markdown, seçimdeki her bir makaleye gittiği için makalenizin seçicisini bir eklemeye yerleştirmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="a5605-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="a5605-327">Daha sonra tüm makalelerinizde aynı seçiciyi kullanan eklemeye başvurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5605-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="a5605-328">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="a5605-328">Code snippets</span></span>

<span data-ttu-id="a5605-329">Markdig, bir makaleye kod parçacığı uzantısı aracılığıyla gelişmiş kod eklemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="a5605-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="a5605-330">Programlama dili seçimi ve söz dizimi renklendirme gibi GFM özellikleri üzerinde ortaya çıkan gelişmiş işleme seçenekleri sağlar, bunların yanında aşağıdaki gibi kullanışlı özellikler de getirir:</span><span class="sxs-lookup"><span data-stu-id="a5605-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="a5605-331">Bir dış depodan gelen merkezi kod örnekleri/parçacıklarının eklenmesi.</span><span class="sxs-lookup"><span data-stu-id="a5605-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="a5605-332">Kod örneklerinin farklı dillerdeki birçok çeşidini gösteren sekmeli kullanıcı arabirimi.</span><span class="sxs-lookup"><span data-stu-id="a5605-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="a5605-333">Tuzaklar ve sorun giderme</span><span class="sxs-lookup"><span data-stu-id="a5605-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="a5605-334">Alternatif metin</span><span class="sxs-lookup"><span data-stu-id="a5605-334">Alt text</span></span>

<span data-ttu-id="a5605-335">Alt çizgi içeren alternatif metin düzgün bir şekilde işlenmez.</span><span class="sxs-lookup"><span data-stu-id="a5605-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="a5605-336">Örneğin, şunu kullanmak yerine:</span><span class="sxs-lookup"><span data-stu-id="a5605-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="a5605-337">Şunun gibi alt çizgilerden kaçının:</span><span class="sxs-lookup"><span data-stu-id="a5605-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="a5605-338">Kesme işareti ve tırnak işaretleri</span><span class="sxs-lookup"><span data-stu-id="a5605-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="a5605-339">Word dosyasından Markdown editörüne bir şey kopyalarsanız kopyaladığınız metin “akıllı” (kıvrık) kesme işaretleri veya tırnak işaretleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="a5605-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="a5605-340">Bunların kodlanması veya kesme işareti ya da tırnak işaretlerine dönüştürülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a5605-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="a5605-341">Aksi takdirde, dosya yayımlandığında şu karakterleri görebilirsiniz: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="a5605-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="a5605-342">Bu noktalama işaretlerinin “akıllı” olanları için kodlamalar aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="a5605-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="a5605-343">Sol (açma) tırnak işareti: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="a5605-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="a5605-344">Sağ (kapatma) tırnak işareti: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="a5605-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="a5605-345">Sağ (kapatma) tekli tırnak işareti veya kesme işareti: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="a5605-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="a5605-346">Sağ (açma) tekli tırnak işareti (nadiren kullanılır): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="a5605-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="a5605-347">Açılı ayraçlar</span><span class="sxs-lookup"><span data-stu-id="a5605-347">Angle brackets</span></span>

<span data-ttu-id="a5605-348">Dosyanızın metninde (kodunda değil), yer tutucuları göstermek gibi bir amaçla açılı ayraç kullanıyorsanız bu ayraçları el ile kodlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a5605-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="a5605-349">Aksi takdirde Markdown bunların HTML etiketleri olması gerektiğini düşünür.</span><span class="sxs-lookup"><span data-stu-id="a5605-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="a5605-350">Örneğin `<script name>` öğesini `&lt;script name&gt;` şeklinde kodlayın</span><span class="sxs-lookup"><span data-stu-id="a5605-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="a5605-351">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="a5605-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="a5605-352">Markdown kaynakları</span><span class="sxs-lookup"><span data-stu-id="a5605-352">Markdown resources</span></span>

- [<span data-ttu-id="a5605-353">Markdown’a Giriş</span><span class="sxs-lookup"><span data-stu-id="a5605-353">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="a5605-354">Docs Markdown kural sayfası</span><span class="sxs-lookup"><span data-stu-id="a5605-354">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="a5605-355">GitHub Markdown Temel Bilgileri</span><span class="sxs-lookup"><span data-stu-id="a5605-355">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
