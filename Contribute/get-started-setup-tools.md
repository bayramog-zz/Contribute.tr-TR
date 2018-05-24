---
title: İçerik yazma araçlarını yükleme
description: Bu makale, Git ve markdown dosyalarını düzenlemek için ihtiyacınız olacak istemci araçları indirip yüklemenize yardımcı olur.
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 04/30/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1011c3fc829202a3df134ddc80eb05b8959b7bf6
ms.sourcegitcommit: e046e7aad8ed22bffe5380d63a9d40f0baeecc57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="d8d3f-103">İçerik yazma araçlarını yükleme</span><span class="sxs-lookup"><span data-stu-id="d8d3f-103">Install content authoring tools</span></span>

<span data-ttu-id="d8d3f-104">Bu makalede Git istemci araçlarını ve Visual Studio Code'u etkileşimli olarak yükleme adımları açıklanır.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="d8d3f-105">[Windows için Git](https://git-scm.com/download/win)'i yükleme</span><span class="sxs-lookup"><span data-stu-id="d8d3f-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="d8d3f-106">[Visual Studio Code](https://code.visualstudio.com/)'u yükleme</span><span class="sxs-lookup"><span data-stu-id="d8d3f-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>
> * <span data-ttu-id="d8d3f-107">[Docs Yazma Paketi](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)’ni yükleme</span><span class="sxs-lookup"><span data-stu-id="d8d3f-107">Install [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="d8d3f-108">Bir makalede yalnızca küçük değişiklikler yapıyorsanız bu makaledeki adımları tamamlamanız gerekli *değildir* ve doğrudan [hızlı değişiklikler iş akışı](index.md#quick-edits-to-existing-documents) kısmına gidebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-108">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="d8d3f-109">Büyük katkılarda bulunanların bu adımı tamamlaması önerilir, bu adımdan sonra [büyük/uzun ömürlü değişiklikler iş akışı](how-to-write-workflows-major.md) kısmına geçebilirler.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-109">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="d8d3f-110">Ana depoda yazma izinleriniz olsa bile, önerdiğiniz değişiklikleri çatalınızda depolamak üzere okuma/yazma izinlerinizin olacağı *depo çatalını oluşturmanız ve kopyalamanız kesinlikle önerilir (ve bu makalede öyle yaptığınız varsayılır)*.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-110">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="d8d3f-111">Windows'da Git istemci araçlarını yükleme</span><span class="sxs-lookup"><span data-stu-id="d8d3f-111">Install Git client tools on Windows</span></span>

 <span data-ttu-id="d8d3f-112">[Software Freedom Conservancy’nin Git istemci araçlarının](https://git-scm.com/download/) son sürümünü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-112">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="d8d3f-113">Yükleme, Git sürüm denetim sistemini ve yerel Git deponuzla etkileşim için kullandığınız komut satırı uygulaması olan Git Bash'i içerir.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-113">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="d8d3f-114">Komut satırı arabirimi (CLI) yerine bir grafik kullanıcı arabirimi (GUI) tercih ederseniz popüler seçenekler için [Software Freedom Conservancy’nin uygun GUI İstemcileri sayfası](https://git-scm.com/downloads/guis), [GitHub’ın GitHub Masaüstü](https://desktop.github.com/) veya [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)’a bakın.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-114">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="d8d3f-115">Yükleme ve yapılandırma için seçtiğiniz istemcinin yönergelerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-115">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="d8d3f-116">Sonraki makalede, [yerel Git deponuzu ayarlayacaksınız](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="d8d3f-116">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="d8d3f-117">Ek Git kaynaklarını burada bulabilirsiniz: [Git terminolojisi](https://help.github.com/articles/github-glossary) | [Git temel bilgileri](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Git ve GitHub'ı öğrenme](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span><span class="sxs-lookup"><span data-stu-id="d8d3f-117">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="d8d3f-118">Markdown düzenleyicilerini anlama</span><span class="sxs-lookup"><span data-stu-id="d8d3f-118">Understand Markdown editors</span></span>

<span data-ttu-id="d8d3f-119">Markdown, okuması ve öğrenmesi kolay bir biçimlendirme dilidir.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-119">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="d8d3f-120">Bu nedenle, bu dil kısa sürede endüstri standardı haline gelmiştir.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-120">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="d8d3f-121">Markdown’da makale yazmak için önce bir Markdown düzenleyicisi indirip yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-121">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="d8d3f-122">[Visual Studio Code](https://code.visualstudio.com/), Microsoft'ta Markdown'ı düzenlemek için tercih edilen dildir.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-122">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="d8d3f-123">Markdown'ı düzenlemeye yönelik bir diğer popüler araç da [Atom](https://atom.io)'dur.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-123">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="d8d3f-124">Markdown metinleri, .md uzantılı dosyalara kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-124">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="d8d3f-125">Markdown temel bilgileri ve OPS özel Markdown uzantıları tarafından desteklenen özellikler dahil olmak üzere Markdown ile makale yazmaya yönelik ilave ayrıntılar daha sonra [Markdown kullanımı](how-to-write-use-markdown.md) makalesinde ele alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-125">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="d8d3f-126">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="d8d3f-126">Visual Studio Code</span></span>

<span data-ttu-id="d8d3f-127">VS Code olarak da bilinen [Visual Studio Code](https://code.visualstudio.com/), Windows, Linux ve Mac üzerinde çalışan basit bir düzenleyicidir.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-127">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="d8d3f-128">Git tümleştirmesi ve uzantılar için destek içerir.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-128">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="d8d3f-129">[VS Code](https://code.visualstudio.com/)'u indirin ve yükleyin.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-129">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="d8d3f-130">VS Code giriş sayfasında işletim sisteminiz doğru algılanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-130">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="d8d3f-131">Windows</span><span class="sxs-lookup"><span data-stu-id="d8d3f-131">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="d8d3f-132">Mac</span><span class="sxs-lookup"><span data-stu-id="d8d3f-132">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="d8d3f-133">Linux</span><span class="sxs-lookup"><span data-stu-id="d8d3f-133">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="d8d3f-134">VS Code'u başlatmak ve geçerli klasörü açmak için, komut satırında veya bash kabuğunda `code .` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-134">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="d8d3f-135">Geçerli klasör yerel git deposunun bir parçasıysa, github tümleştirmesi Visual Studio Code'da otomatik olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-135">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="docs-authoring-pack"></a><span data-ttu-id="d8d3f-136">Docs Yazma Paketi</span><span class="sxs-lookup"><span data-stu-id="d8d3f-136">Docs Authoring Pack</span></span>
<span data-ttu-id="d8d3f-137">Visual Studio Code için Docs Yazma Paketi’ni yükleyin.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-137">Install the Docs Authoring Pack for Visual Studio Code.</span></span> <span data-ttu-id="d8d3f-138">Bu uzantı kümesi, Markdown yazarken yardım için temel yazma desteği ve Markdown’ın docs.microsoft.com sitesinde nasıl görüneceğine bakmanız için önizleme özelliği sağlar.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-138">This set of extensions includes basic authoring assistance for help when writing Markdown, and a preview feature, so that you can see what the Markdown looks like in the style of the docs.microsoft.com site.</span></span>

   <span data-ttu-id="d8d3f-139">Bu [market sayfasını](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) ziyaret edin ve **Yükle**’yi seçin veya VS Code penceresindeki uzantılar listenizde `docsmsft.docs-authoring-pack` için arama yapın.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-139">Visit this [marketplace page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and select **Install**, or search for `docsmsft.docs-authoring-pack` in your extensions list in the VS Code window.</span></span> 

   <span data-ttu-id="d8d3f-140">Docs Yazma Paketi’ne VS Code’da Alt+M tuşlarına basarak ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-140">The Docs Authoring Pack is accessible by pressing Alt+M inside of VS Code.</span></span> <span data-ttu-id="d8d3f-141">Araç çubuğu varsayılan olarak gizlidir ancak gösterilebilir.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-141">The toolbar is hidden by default but can be shown.</span></span> <span data-ttu-id="d8d3f-142">Bunun için VS Code ayarlarını düzenleyin (Control+virgül) ve `"markdown.showToolbar": true` kullanıcı ayarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-142">Edit the VS Code settings (Control+comma) and adding user setting `"markdown.showToolbar": true` to show the toolbar.</span></span>

   <span data-ttu-id="d8d3f-143">Daha fazla bilgi için [Docs Yazma Paketi](how-to-write-docs-auth-pack.md) sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-143">For more information, see the [Docs Authoring Pack](how-to-write-docs-auth-pack.md) page.</span></span>


## <a name="next-steps"></a><span data-ttu-id="d8d3f-144">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="d8d3f-144">Next steps</span></span>

<span data-ttu-id="d8d3f-145">Artık [yerel Git deposunu ayarlamaya](get-started-setup-local.md) hazırsınız.</span><span class="sxs-lookup"><span data-stu-id="d8d3f-145">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
