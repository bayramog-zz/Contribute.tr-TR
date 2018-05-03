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
ms.openlocfilehash: 96d00abc052c3b23ca62201dccdbe590a927e72d
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="74588-103">Docs’ta makale yazmak için Markdown kullanma</span><span class="sxs-lookup"><span data-stu-id="74588-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="74588-104">Docs.microsoft.com makaleleri [Markdown](https://daringfireball.net/projects/markdown/) adı verilen hafif biçimlendirme dilinde yazılır, bu dilin okunması ve öğrenilmesi kolaydır.</span><span class="sxs-lookup"><span data-stu-id="74588-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="74588-105">O nedenle bu dil kısa sürede endüstri standardı haline gelmiştir.</span><span class="sxs-lookup"><span data-stu-id="74588-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="74588-106">Docs içerikleri GitHub’da depolandığı için [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) adlı bir Markdown üst kümesi kullanabilir. GFM, yaygın biçimlendirme ihtiyaçları için ilave işlevler sağlar.</span><span class="sxs-lookup"><span data-stu-id="74588-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="74588-107">Ayrıca, Open Publishing Services (OPS) DocFX Flavored Markdown (DFM) uygular.</span><span class="sxs-lookup"><span data-stu-id="74588-107">Additionally, Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="74588-108">DFM, GitHub Flavored Markdown (GFM) ile yüksek oranda uyumludur ve Docs’a özgü özellikleri etkinleştiren işlevler ekler.</span><span class="sxs-lookup"><span data-stu-id="74588-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="74588-109">Markdown temel bilgileri</span><span class="sxs-lookup"><span data-stu-id="74588-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="74588-110">Bölüm başlıkları</span><span class="sxs-lookup"><span data-stu-id="74588-110">Headings</span></span>

<span data-ttu-id="74588-111">Bir bölüm başlığı oluşturmak için karma işaretini (#) aşağıdaki gibi kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="74588-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="74588-112">Kalın ve italik metin</span><span class="sxs-lookup"><span data-stu-id="74588-112">Bold and italic text</span></span>

<span data-ttu-id="74588-113">Bir metni **kalın** olarak biçimlendirmek için iki yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="74588-113">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="74588-114">Bir metni *italik* olarak biçimlendirmek için bir yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="74588-114">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="74588-115">Bir metni ***kalın ve italik*** olarak biçimlendirmek için üç yıldız işareti arasına alırsınız:</span><span class="sxs-lookup"><span data-stu-id="74588-115">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="74588-116">Listeler</span><span class="sxs-lookup"><span data-stu-id="74588-116">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="74588-117">Sırasız liste</span><span class="sxs-lookup"><span data-stu-id="74588-117">Unordered list</span></span>

<span data-ttu-id="74588-118">Sırasız/madde işaretli bir listeyi biçimlendirmek için yıldız işaretleri veya tireler kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="74588-118">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="74588-119">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="74588-119">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="74588-120">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="74588-120">will be rendered as:</span></span>

- <span data-ttu-id="74588-121">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="74588-121">List item 1</span></span>
- <span data-ttu-id="74588-122">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="74588-122">List item 2</span></span>
- <span data-ttu-id="74588-123">Liste öğesi 3</span><span class="sxs-lookup"><span data-stu-id="74588-123">List item 3</span></span>

<span data-ttu-id="74588-124">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="74588-124">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="74588-125">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="74588-125">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="74588-126">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="74588-126">will be rendered as:</span></span>

- <span data-ttu-id="74588-127">Liste öğesi 1</span><span class="sxs-lookup"><span data-stu-id="74588-127">List item 1</span></span>
  - <span data-ttu-id="74588-128">Liste öğesi A</span><span class="sxs-lookup"><span data-stu-id="74588-128">List item A</span></span>
  - <span data-ttu-id="74588-129">Liste öğesi B</span><span class="sxs-lookup"><span data-stu-id="74588-129">List item B</span></span>
- <span data-ttu-id="74588-130">Liste öğesi 2</span><span class="sxs-lookup"><span data-stu-id="74588-130">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="74588-131">Sıralı liste</span><span class="sxs-lookup"><span data-stu-id="74588-131">Ordered list</span></span>

<span data-ttu-id="74588-132">Sıralı/adımlı bir listeyi biçimlendirmek için sıra numaraları kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="74588-132">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="74588-133">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="74588-133">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="74588-134">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="74588-134">will be rendered as:</span></span>

1. <span data-ttu-id="74588-135">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="74588-135">First instruction</span></span>
2. <span data-ttu-id="74588-136">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="74588-136">Second instruction</span></span>
3. <span data-ttu-id="74588-137">Üçüncü yönerge</span><span class="sxs-lookup"><span data-stu-id="74588-137">Third instruction</span></span>

<span data-ttu-id="74588-138">Bir listeyi diğerinin içine yerleştirmek için alt lise öğelerini girintili olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="74588-138">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="74588-139">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="74588-139">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="74588-140">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="74588-140">will be rendered as:</span></span>

1. <span data-ttu-id="74588-141">İlk yönerge</span><span class="sxs-lookup"><span data-stu-id="74588-141">First instruction</span></span>
    1. <span data-ttu-id="74588-142">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="74588-142">Sub-instruction</span></span>
    2. <span data-ttu-id="74588-143">Alt yönerge</span><span class="sxs-lookup"><span data-stu-id="74588-143">Sub-instruction</span></span>
2. <span data-ttu-id="74588-144">İkinci yönerge</span><span class="sxs-lookup"><span data-stu-id="74588-144">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="74588-145">eğlence</span><span class="sxs-lookup"><span data-stu-id="74588-145">Tables</span></span>

<span data-ttu-id="74588-146">Tablolar, temel Markdown belirtiminin parçası değildir, ancak GFM tarafından desteklenir.</span><span class="sxs-lookup"><span data-stu-id="74588-146">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="74588-147">Düz çizgi (|) ve kısa çizgi (-) karakterlerini kullanarak tablolar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="74588-147">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="74588-148">Kısa çizgiler sütunların üst bilgisini oluştururken düz çizgiler sütunları birbirinden ayırır.</span><span class="sxs-lookup"><span data-stu-id="74588-148">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="74588-149">Tablonun doğru işlenebilmesi için başına boş bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="74588-149">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="74588-150">Örneğin, şu Markdown:</span><span class="sxs-lookup"><span data-stu-id="74588-150">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="74588-151">şu şekilde oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="74588-151">will be rendered as:</span></span>

| <span data-ttu-id="74588-152">Tablolar</span><span class="sxs-lookup"><span data-stu-id="74588-152">Fun</span></span>                  | <span data-ttu-id="74588-153">Şununla:</span><span class="sxs-lookup"><span data-stu-id="74588-153">With</span></span>                 | <span data-ttu-id="74588-154">eğlence</span><span class="sxs-lookup"><span data-stu-id="74588-154">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="74588-155">sola hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="74588-155">left-aligned column</span></span>  | <span data-ttu-id="74588-156">sağa hizalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="74588-156">right-aligned column</span></span> | <span data-ttu-id="74588-157">ortalanmış sütun</span><span class="sxs-lookup"><span data-stu-id="74588-157">centered column</span></span> |
| <span data-ttu-id="74588-158">100 $</span><span class="sxs-lookup"><span data-stu-id="74588-158">$100</span></span>                 | <span data-ttu-id="74588-159">100 $</span><span class="sxs-lookup"><span data-stu-id="74588-159">$100</span></span>                 | <span data-ttu-id="74588-160">100 $</span><span class="sxs-lookup"><span data-stu-id="74588-160">$100</span></span>            |
| <span data-ttu-id="74588-161">10 $</span><span class="sxs-lookup"><span data-stu-id="74588-161">$10</span></span>                  | <span data-ttu-id="74588-162">10 $</span><span class="sxs-lookup"><span data-stu-id="74588-162">$10</span></span>                  | <span data-ttu-id="74588-163">10 $</span><span class="sxs-lookup"><span data-stu-id="74588-163">$10</span></span>             |
| <span data-ttu-id="74588-164">1 $</span><span class="sxs-lookup"><span data-stu-id="74588-164">$1</span></span>                   | <span data-ttu-id="74588-165">1 $</span><span class="sxs-lookup"><span data-stu-id="74588-165">$1</span></span>                   | <span data-ttu-id="74588-166">1 $</span><span class="sxs-lookup"><span data-stu-id="74588-166">$1</span></span>              |

<span data-ttu-id="74588-167">Tablo oluşturma hakkında daha fazla bilgi için şunlara bakın:</span><span class="sxs-lookup"><span data-stu-id="74588-167">For more information on creating tables, see:</span></span>

- <span data-ttu-id="74588-168">Geniş tabloların biçimlendirmesinde yardımcı olabilecek DFM [tablo sarmalama özelliği](#table-wrapping)</span><span class="sxs-lookup"><span data-stu-id="74588-168">The DFM [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="74588-169">GitHub’ın [Tablolarla bilgi düzenleme](https://help.github.com/articles/organizing-information-with-tables/) makalesi</span><span class="sxs-lookup"><span data-stu-id="74588-169">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="74588-170">[Markdown Tablo Oluşturucu](https://www.tablesgenerator.com/markdown_tables) web uygulaması</span><span class="sxs-lookup"><span data-stu-id="74588-170">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="74588-171">Adam Pritchard - Markdown Kural Sayfası</span><span class="sxs-lookup"><span data-stu-id="74588-171">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="74588-172">Michel Fortin - Markdown Ekstra</span><span class="sxs-lookup"><span data-stu-id="74588-172">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="74588-173">HTML tablolarını Markdown’a dönüştürme</span><span class="sxs-lookup"><span data-stu-id="74588-173">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="74588-174">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="74588-174">Links</span></span>

<span data-ttu-id="74588-175">Satır içi bağlantılarda Markdown söz dizimi, köprü bağlantısı eklenecek `[link text]` metni ve bağlantı verilen URL ya da dosya adı olan `(file-name.md)` kısımlarından oluşur:</span><span class="sxs-lookup"><span data-stu-id="74588-175">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="74588-176">Bağlantı verme hakkında daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="74588-176">For more information on linking, see:</span></span>

- <span data-ttu-id="74588-177">Markdown’ın temel bağlantı desteği konusunda ayrıntılar için [Markdown söz dizimi kılavuzu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="74588-177">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="74588-178">DFM tarafından sağlanan ilave bağlama söz dizimi hakkında ayrıntılar için bu kılavuzun [Bağlantılar](how-to-write-links.md) bölümü.</span><span class="sxs-lookup"><span data-stu-id="74588-178">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that DFM provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="74588-179">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="74588-179">Code snippets</span></span>

<span data-ttu-id="74588-180">Markdown, hem bir cümlede satır içi olarak hem de cümleler arasında ayrı “çevrelenmiş” bir blok halinde kod parçacıkları yerleştirilmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="74588-180">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="74588-181">Ayrıntılar için bkz.</span><span class="sxs-lookup"><span data-stu-id="74588-181">For details, see:</span></span>

- [<span data-ttu-id="74588-182">Kod blokları için yerel Markdown desteği</span><span class="sxs-lookup"><span data-stu-id="74588-182">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="74588-183">Kod çevreleme ve söz dizimi vurgulama için GFM desteği</span><span class="sxs-lookup"><span data-stu-id="74588-183">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="74588-184">Çevrelenmiş kod blokları, kod parçacıklarınız için söz dizimi vurgulamasını etkinleştirmenin kolay bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="74588-184">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="74588-185">Çevrelenmiş kod bloklarının biçimi genelde şöyledir:</span><span class="sxs-lookup"><span data-stu-id="74588-185">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="74588-186">İlk üç ters tırnak (\`) karakterinden sonra gelen diğer ad, kullanılacak söz dizimi vurgulamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74588-186">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="74588-187">Docs içeriğinde yaygın olarak kullanılan programlama dilleri ve bunların etiketleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="74588-187">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="74588-188">Bu diller, kolay as desteğine ve dil vurgulamasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="74588-188">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="74588-189">Ad</span><span class="sxs-lookup"><span data-stu-id="74588-189">Name</span></span>|<span data-ttu-id="74588-190">Markdown Etiketi</span><span class="sxs-lookup"><span data-stu-id="74588-190">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="74588-191">.NET Konsolu</span><span class="sxs-lookup"><span data-stu-id="74588-191">.NET Console</span></span>|<span data-ttu-id="74588-192">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="74588-192">dotnetcli</span></span>|
|<span data-ttu-id="74588-193">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="74588-193">ASP.NET (C#)</span></span>|<span data-ttu-id="74588-194">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="74588-194">aspx-csharp</span></span>|
|<span data-ttu-id="74588-195">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="74588-195">ASP.NET (VB)</span></span>|<span data-ttu-id="74588-196">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="74588-196">aspx-vb</span></span>|
|<span data-ttu-id="74588-197">AzCopy</span><span class="sxs-lookup"><span data-stu-id="74588-197">AzCopy</span></span>|<span data-ttu-id="74588-198">azcopy</span><span class="sxs-lookup"><span data-stu-id="74588-198">azcopy</span></span>|
|<span data-ttu-id="74588-199">Azure CLI’si</span><span class="sxs-lookup"><span data-stu-id="74588-199">Azure CLI</span></span>|<span data-ttu-id="74588-200">azurecli</span><span class="sxs-lookup"><span data-stu-id="74588-200">azurecli</span></span>|
|<span data-ttu-id="74588-201">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="74588-201">Azure PowerShell</span></span>|<span data-ttu-id="74588-202">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="74588-202">azurepowershell</span></span>|
|<span data-ttu-id="74588-203">C++</span><span class="sxs-lookup"><span data-stu-id="74588-203">C++</span></span>|<span data-ttu-id="74588-204">cpp</span><span class="sxs-lookup"><span data-stu-id="74588-204">cpp</span></span>|
|<span data-ttu-id="74588-205">C++/CX</span><span class="sxs-lookup"><span data-stu-id="74588-205">C++/CX</span></span>|<span data-ttu-id="74588-206">cppcx</span><span class="sxs-lookup"><span data-stu-id="74588-206">cppcx</span></span>|
|<span data-ttu-id="74588-207">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="74588-207">C++/WinRT</span></span>|<span data-ttu-id="74588-208">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="74588-208">cppwinrt</span></span>|
|<span data-ttu-id="74588-209">C#</span><span class="sxs-lookup"><span data-stu-id="74588-209">C#</span></span>|<span data-ttu-id="74588-210">csharp</span><span class="sxs-lookup"><span data-stu-id="74588-210">csharp</span></span>|
|<span data-ttu-id="74588-211">CSHTML</span><span class="sxs-lookup"><span data-stu-id="74588-211">CSHTML</span></span>|<span data-ttu-id="74588-212">cshtml</span><span class="sxs-lookup"><span data-stu-id="74588-212">cshtml</span></span>|
|<span data-ttu-id="74588-213">DAX</span><span class="sxs-lookup"><span data-stu-id="74588-213">DAX</span></span>|<span data-ttu-id="74588-214">dax</span><span class="sxs-lookup"><span data-stu-id="74588-214">dax</span></span>|
|<span data-ttu-id="74588-215">F#</span><span class="sxs-lookup"><span data-stu-id="74588-215">F#</span></span>|<span data-ttu-id="74588-216">fsharp</span><span class="sxs-lookup"><span data-stu-id="74588-216">fsharp</span></span>|
|<span data-ttu-id="74588-217">Go</span><span class="sxs-lookup"><span data-stu-id="74588-217">Go</span></span>|<span data-ttu-id="74588-218">go</span><span class="sxs-lookup"><span data-stu-id="74588-218">go</span></span>|
|<span data-ttu-id="74588-219">HTML</span><span class="sxs-lookup"><span data-stu-id="74588-219">HTML</span></span>|<span data-ttu-id="74588-220">html</span><span class="sxs-lookup"><span data-stu-id="74588-220">html</span></span>|
|<span data-ttu-id="74588-221">HTTP</span><span class="sxs-lookup"><span data-stu-id="74588-221">HTTP</span></span>|<span data-ttu-id="74588-222">http</span><span class="sxs-lookup"><span data-stu-id="74588-222">http</span></span>|
|<span data-ttu-id="74588-223">Java</span><span class="sxs-lookup"><span data-stu-id="74588-223">Java</span></span>|<span data-ttu-id="74588-224">java</span><span class="sxs-lookup"><span data-stu-id="74588-224">java</span></span>|
|<span data-ttu-id="74588-225">JavaScript</span><span class="sxs-lookup"><span data-stu-id="74588-225">JavaScript</span></span>|<span data-ttu-id="74588-226">javascript</span><span class="sxs-lookup"><span data-stu-id="74588-226">javascript</span></span>|
|<span data-ttu-id="74588-227">JSON</span><span class="sxs-lookup"><span data-stu-id="74588-227">JSON</span></span>|<span data-ttu-id="74588-228">json</span><span class="sxs-lookup"><span data-stu-id="74588-228">json</span></span>|
|<span data-ttu-id="74588-229">Markdown</span><span class="sxs-lookup"><span data-stu-id="74588-229">Markdown</span></span>|<span data-ttu-id="74588-230">md</span><span class="sxs-lookup"><span data-stu-id="74588-230">md</span></span>|
|<span data-ttu-id="74588-231">NodeJS</span><span class="sxs-lookup"><span data-stu-id="74588-231">NodeJS</span></span>|<span data-ttu-id="74588-232">nodejs</span><span class="sxs-lookup"><span data-stu-id="74588-232">nodejs</span></span>|
|<span data-ttu-id="74588-233">Objective-C</span><span class="sxs-lookup"><span data-stu-id="74588-233">Objective-C</span></span>|<span data-ttu-id="74588-234">objc</span><span class="sxs-lookup"><span data-stu-id="74588-234">objc</span></span>|
|<span data-ttu-id="74588-235">OData</span><span class="sxs-lookup"><span data-stu-id="74588-235">OData</span></span>|<span data-ttu-id="74588-236">odata</span><span class="sxs-lookup"><span data-stu-id="74588-236">odata</span></span>|
|<span data-ttu-id="74588-237">PHP</span><span class="sxs-lookup"><span data-stu-id="74588-237">PHP</span></span>|<span data-ttu-id="74588-238">php</span><span class="sxs-lookup"><span data-stu-id="74588-238">php</span></span>|
|<span data-ttu-id="74588-239">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="74588-239">Power Apps Formula</span></span>|<span data-ttu-id="74588-240">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="74588-240">powerappsfl</span></span>|
|<span data-ttu-id="74588-241">PowerShell</span><span class="sxs-lookup"><span data-stu-id="74588-241">PowerShell</span></span>|<span data-ttu-id="74588-242">powershell</span><span class="sxs-lookup"><span data-stu-id="74588-242">powershell</span></span>|
|<span data-ttu-id="74588-243">Python</span><span class="sxs-lookup"><span data-stu-id="74588-243">Python</span></span>|<span data-ttu-id="74588-244">python</span><span class="sxs-lookup"><span data-stu-id="74588-244">python</span></span>|
|<span data-ttu-id="74588-245">Q#</span><span class="sxs-lookup"><span data-stu-id="74588-245">Q#</span></span>|<span data-ttu-id="74588-246">qsharp</span><span class="sxs-lookup"><span data-stu-id="74588-246">qsharp</span></span>|
|<span data-ttu-id="74588-247">Ruby</span><span class="sxs-lookup"><span data-stu-id="74588-247">Ruby</span></span>|<span data-ttu-id="74588-248">ruby</span><span class="sxs-lookup"><span data-stu-id="74588-248">ruby</span></span>|
|<span data-ttu-id="74588-249">SQL</span><span class="sxs-lookup"><span data-stu-id="74588-249">SQL</span></span>|<span data-ttu-id="74588-250">sql</span><span class="sxs-lookup"><span data-stu-id="74588-250">sql</span></span>|
|<span data-ttu-id="74588-251">Swift</span><span class="sxs-lookup"><span data-stu-id="74588-251">Swift</span></span>|<span data-ttu-id="74588-252">swift</span><span class="sxs-lookup"><span data-stu-id="74588-252">swift</span></span>|
|<span data-ttu-id="74588-253">TypeScript</span><span class="sxs-lookup"><span data-stu-id="74588-253">TypeScript</span></span>|<span data-ttu-id="74588-254">typescript</span><span class="sxs-lookup"><span data-stu-id="74588-254">typescript</span></span>|
|<span data-ttu-id="74588-255">VB</span><span class="sxs-lookup"><span data-stu-id="74588-255">VB</span></span>|<span data-ttu-id="74588-256">vb</span><span class="sxs-lookup"><span data-stu-id="74588-256">vb</span></span>|
|<span data-ttu-id="74588-257">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="74588-257">VSTS CLI</span></span>|<span data-ttu-id="74588-258">vstscli</span><span class="sxs-lookup"><span data-stu-id="74588-258">vstscli</span></span>|
|<span data-ttu-id="74588-259">XAML</span><span class="sxs-lookup"><span data-stu-id="74588-259">XAML</span></span>|<span data-ttu-id="74588-260">xaml</span><span class="sxs-lookup"><span data-stu-id="74588-260">xaml</span></span>|
|<span data-ttu-id="74588-261">XML</span><span class="sxs-lookup"><span data-stu-id="74588-261">XML</span></span>|<span data-ttu-id="74588-262">xml</span><span class="sxs-lookup"><span data-stu-id="74588-262">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="74588-263">Örnek: C\#</span><span class="sxs-lookup"><span data-stu-id="74588-263">Example: C\#</span></span>

<span data-ttu-id="74588-264">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="74588-264">__Markdown__</span></span>

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

<span data-ttu-id="74588-265">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="74588-265">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="74588-266">Örnek: SQL</span><span class="sxs-lookup"><span data-stu-id="74588-266">Example: SQL</span></span>

<span data-ttu-id="74588-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="74588-267">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="74588-268">__İşleme__</span><span class="sxs-lookup"><span data-stu-id="74588-268">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="74588-269">OPS özel Markdown uzantıları</span><span class="sxs-lookup"><span data-stu-id="74588-269">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="74588-270">Open Publishing Services (OPS), GitHub Flavored Markdown (GFM) ile yüksek uyumluluğa sahip olan DocFX Flavored Markdown’ı (DFM) uygular.</span><span class="sxs-lookup"><span data-stu-id="74588-270">Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM), which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="74588-271">DFM, Markdown uzantıları aracılığıyla bazı işlevler ekler.</span><span class="sxs-lookup"><span data-stu-id="74588-271">DFM adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="74588-272">Bu nedenle, tam OPS Yazma Kılavuzundan bazı makaleler başvuru için bu kılavuza dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="74588-272">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="74588-273">(Örneğin, içindekiler bölümündeki "DFM ve Markdown uzantıları" ile "Kod parçacıkları" kısımlarına bakın.)</span><span class="sxs-lookup"><span data-stu-id="74588-273">(For example, see "DFM and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="74588-274">Docs makaleleri çoğu zaman paragraflar, bağlantılar, listeler ve bölüm başlıkları gibi makale biçimlendirmeleri için GFM’yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="74588-274">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="74588-275">Makaleler, daha zengin biçimlendirme seçenekleri için aşağıdakiler gibi DFM özelliklerini kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="74588-275">For richer formatting, articles can use DFM features such as:</span></span>

- <span data-ttu-id="74588-276">Not blokları</span><span class="sxs-lookup"><span data-stu-id="74588-276">Note blocks</span></span>
- <span data-ttu-id="74588-277">Eklemeler</span><span class="sxs-lookup"><span data-stu-id="74588-277">Includes</span></span>
- <span data-ttu-id="74588-278">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="74588-278">Selectors</span></span>
- <span data-ttu-id="74588-279">Ekli videolar</span><span class="sxs-lookup"><span data-stu-id="74588-279">Embedded videos</span></span>
- <span data-ttu-id="74588-280">Kod parçacıkları/örnekleri</span><span class="sxs-lookup"><span data-stu-id="74588-280">Code snippets/samples</span></span>

<span data-ttu-id="74588-281">Tam liste için içindekiler tablosunun “DFM ve Markdown uzantıları” ve “Kod parçacıkları” başlıklarına bakın.</span><span class="sxs-lookup"><span data-stu-id="74588-281">For the complete list, refer to "DFM and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="74588-282">Not blokları</span><span class="sxs-lookup"><span data-stu-id="74588-282">Note blocks</span></span>

<span data-ttu-id="74588-283">İlgiyi belirli bir içeriğe çekmek için dört çeşit not blokundan birini seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="74588-283">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="74588-284">NOT</span><span class="sxs-lookup"><span data-stu-id="74588-284">NOTE</span></span>
- <span data-ttu-id="74588-285">UYARI</span><span class="sxs-lookup"><span data-stu-id="74588-285">WARNING</span></span>
- <span data-ttu-id="74588-286">İPUCU</span><span class="sxs-lookup"><span data-stu-id="74588-286">TIP</span></span>
- <span data-ttu-id="74588-287">ÖNEMLİ</span><span class="sxs-lookup"><span data-stu-id="74588-287">IMPORTANT</span></span>

<span data-ttu-id="74588-288">Genel olarak not bloklarını fazla kullanmaktan kaçınmalısınız, dikkat dağıtıcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="74588-288">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="74588-289">Not bloklarında kod blokları, görüntüler, listeler ve bağlantılar destekleniyor olsa da bunları olabildiğince sade ve düz bir şekilde oluşturun.</span><span class="sxs-lookup"><span data-stu-id="74588-289">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="74588-290">Eklemeler</span><span class="sxs-lookup"><span data-stu-id="74588-290">Includes</span></span>

<span data-ttu-id="74588-291">Makale dosyalarına “eklenmesi” gereken yeniden kullanılabilir metin veya görüntüleriniz varsa DFM dosya ekleme özelliği aracılığıyla “ekleme” dosyasına bir başvuru kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="74588-291">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the DFM file include feature.</span></span> <span data-ttu-id="74588-292">Bu özellik, verilen dosyayı makalenize derleme sırasında “eklemesi” için OPS’yi yönlendirir, böylece dosya da yayımlanan makalenizin bir parçası olur.</span><span class="sxs-lookup"><span data-stu-id="74588-292">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="74588-293">İçerikleri tekrar kullanmanıza imkan veren üç tür ekleme vardır:</span><span class="sxs-lookup"><span data-stu-id="74588-293">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="74588-294">Satır içi: Genel bir metin parçacığını başka bir cümlede satır içinde yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="74588-294">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="74588-295">Blok: Makalenin bir bölümündeki bütün bir Markdown dosyasını yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="74588-295">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="74588-296">Görüntüler: Docs’ta standart görüntü ekleme yoludur.</span><span class="sxs-lookup"><span data-stu-id="74588-296">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="74588-297">Satır içi ve blok eklemeleri, basit birer Markdown (.md) dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="74588-297">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="74588-298">Bu dosyalar, herhangi bir geçerli Markdown barındırabilir.</span><span class="sxs-lookup"><span data-stu-id="74588-298">It can contain any valid Markdown.</span></span> <span data-ttu-id="74588-299">Tüm ekleme Markdown dosyaları, depo kökünde [ortak bir `/includes` alt dizinine](git-github-fundamentals.md#includes-subdirectory) yerleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="74588-299">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="74588-300">Makale yayımlandığında, eklenen dosya makaleyle sorunsuz bir şekilde tümleşmiş olur.</span><span class="sxs-lookup"><span data-stu-id="74588-300">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="74588-301">Eklemelere yönelik gereksinimler ve önemli konular şunlardır:</span><span class="sxs-lookup"><span data-stu-id="74588-301">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="74588-302">Aynı metni birden fazla makalede kullanmanız gerektiği zaman eklemeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="74588-302">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="74588-303">Blok eklemeleri bir veya iki paragraf, paylaşılan bir yordam veya paylaşılan bir kısım gibi büyük içeriklerle kullanın.</span><span class="sxs-lookup"><span data-stu-id="74588-303">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="74588-304">Ancak bir cümleden daha küçük şeyler için kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="74588-304">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="74588-305">Eklemeler, makalenizin GitHub işlenmiş görüntüsünde işlenmez, çünkü DFM uzantılarıyla çalışır.</span><span class="sxs-lookup"><span data-stu-id="74588-305">Includes won't be rendered in the GitHub rendered view of your article, because they rely on DFM extensions.</span></span> <span data-ttu-id="74588-306">Bunlar yalnızca yayın sonrasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="74588-306">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="74588-307">Eklemeye başvuran makaledeki bir eklemede bütün metnin, tam cümlelerden oluşmasına veya öncesinde ya da sonrasındaki metne bağlı olmayan tümcecikler halinde olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="74588-307">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="74588-308">Bu kılavuzu dikkate almamak, makalede çevrilemeyen bir satır oluşturur ve yerelleştirme deneyimini bozar.</span><span class="sxs-lookup"><span data-stu-id="74588-308">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="74588-309">Eklemeleri birbirine eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="74588-309">Don't embed includes within other includes.</span></span> <span data-ttu-id="74588-310">Bu, desteklenmeyen bir durumdur.</span><span class="sxs-lookup"><span data-stu-id="74588-310">They are not supported.</span></span>
- <span data-ttu-id="74588-311">Medya dosyalarını ekleme alt dizinine özgü bir medya klasörüne yerleştirin, örneğin `<repo>`/eklemeler/medya klasörü.</span><span class="sxs-lookup"><span data-stu-id="74588-311">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="74588-312">Medya dizini, kökünde hiçbir görüntü barındırmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="74588-312">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="74588-313">Eklemede görüntü yoksa buna karşılık gelecek bir medya dizini gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="74588-313">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="74588-314">Normal makalelerde olduğu gibi, ekleme dosyaları arasında medya paylaşmayın.</span><span class="sxs-lookup"><span data-stu-id="74588-314">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="74588-315">Her bir ekleme ve makale için benzersiz ada sahip ayrı dosyalar kullanın.</span><span class="sxs-lookup"><span data-stu-id="74588-315">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="74588-316">Medya dosyasını, eklemeyle ilişkili medya klasöründe depolayın.</span><span class="sxs-lookup"><span data-stu-id="74588-316">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="74588-317">Eklemeleri, bir makalenin tek içeriği olarak kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="74588-317">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="74588-318">Eklemelerin, makaledeki diğer içerikleri tamamlayıcı görevi vardır.</span><span class="sxs-lookup"><span data-stu-id="74588-318">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="74588-319">Seçiciler</span><span class="sxs-lookup"><span data-stu-id="74588-319">Selectors</span></span>

<span data-ttu-id="74588-320">Seçicileri; teknik makalelerde, aynı makalenin farklı bölümlerini yazdığınızda teknolojiler veya platformlar arasındaki uygulama farklılıklarına değinirken kullanın.</span><span class="sxs-lookup"><span data-stu-id="74588-320">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="74588-321">Bu genellikle geliştiriciler için mobil platform içeriklerimizde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="74588-321">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="74588-322">DFM’de şu anda iki farklı tür seçici vardır: Tekli seçici ve çoklu seçici.</span><span class="sxs-lookup"><span data-stu-id="74588-322">There are currently two different types of selectors in DFM, a single selector and a multi-selector.</span></span>

<span data-ttu-id="74588-323">Aynı seçici Markdown, seçimdeki her bir makaleye gittiği için makalenizin seçicisini bir eklemeye yerleştirmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="74588-323">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="74588-324">Daha sonra tüm makalelerinizde aynı seçiciyi kullanan eklemeye başvurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="74588-324">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="74588-325">Kod parçacıkları</span><span class="sxs-lookup"><span data-stu-id="74588-325">Code snippets</span></span>

<span data-ttu-id="74588-326">DFM, kod parçacığı uzantısı yoluyla bir makaleye gelişmiş kod eklemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="74588-326">DFM supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="74588-327">Programlama dili seçimi ve söz dizimi renklendirme gibi GFM özellikleri üzerinde ortaya çıkan gelişmiş işleme seçenekleri sağlar, bunların yanında aşağıdaki gibi kullanışlı özellikler de getirir:</span><span class="sxs-lookup"><span data-stu-id="74588-327">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="74588-328">Bir dış depodan gelen merkezi kod örnekleri/parçacıklarının eklenmesi.</span><span class="sxs-lookup"><span data-stu-id="74588-328">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="74588-329">Kod örneklerinin farklı dillerdeki birçok çeşidini gösteren sekmeli kullanıcı arabirimi.</span><span class="sxs-lookup"><span data-stu-id="74588-329">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="74588-330">Tuzaklar ve sorun giderme</span><span class="sxs-lookup"><span data-stu-id="74588-330">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="74588-331">Alternatif metin</span><span class="sxs-lookup"><span data-stu-id="74588-331">Alt text</span></span>

<span data-ttu-id="74588-332">Alt çizgi içeren alternatif metin düzgün bir şekilde işlenmez.</span><span class="sxs-lookup"><span data-stu-id="74588-332">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="74588-333">Örneğin, şunu kullanmak yerine:</span><span class="sxs-lookup"><span data-stu-id="74588-333">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="74588-334">Şunun gibi alt çizgilerden kaçının:</span><span class="sxs-lookup"><span data-stu-id="74588-334">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="74588-335">Kesme işareti ve tırnak işaretleri</span><span class="sxs-lookup"><span data-stu-id="74588-335">Apostrophes and quotation marks</span></span>

<span data-ttu-id="74588-336">Word dosyasından Markdown editörüne bir şey kopyalarsanız kopyaladığınız metin “akıllı” (kıvrık) kesme işaretleri veya tırnak işaretleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="74588-336">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="74588-337">Bunların kodlanması veya kesme işareti ya da tırnak işaretlerine dönüştürülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="74588-337">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="74588-338">Aksi takdirde, dosya yayımlandığında şu karakterleri görebilirsiniz: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="74588-338">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="74588-339">Bu noktalama işaretlerinin “akıllı” olanları için kodlamalar aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="74588-339">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="74588-340">Sol (açma) tırnak işareti: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="74588-340">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="74588-341">Sağ (kapatma) tırnak işareti: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="74588-341">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="74588-342">Sağ (kapatma) tekli tırnak işareti veya kesme işareti: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="74588-342">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="74588-343">Sağ (açma) tekli tırnak işareti (nadiren kullanılır): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="74588-343">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="74588-344">Açılı ayraçlar</span><span class="sxs-lookup"><span data-stu-id="74588-344">Angle brackets</span></span>

<span data-ttu-id="74588-345">Dosyanızın metninde (kodunda değil), yer tutucuları göstermek gibi bir amaçla açılı ayraç kullanıyorsanız bu ayraçları el ile kodlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="74588-345">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="74588-346">Aksi takdirde Markdown bunların HTML etiketleri olması gerektiğini düşünür.</span><span class="sxs-lookup"><span data-stu-id="74588-346">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="74588-347">Örneğin `<script name>` öğesini `&lt;script name&gt;` şeklinde kodlayın</span><span class="sxs-lookup"><span data-stu-id="74588-347">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="74588-348">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="74588-348">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="74588-349">Markdown kaynakları</span><span class="sxs-lookup"><span data-stu-id="74588-349">Markdown resources</span></span>

- [<span data-ttu-id="74588-350">Markdown’a Giriş</span><span class="sxs-lookup"><span data-stu-id="74588-350">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="74588-351">Docs Markdown kural sayfası</span><span class="sxs-lookup"><span data-stu-id="74588-351">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="74588-352">GitHub Markdown Temel Bilgileri</span><span class="sxs-lookup"><span data-stu-id="74588-352">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
