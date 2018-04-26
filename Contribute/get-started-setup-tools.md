---
title: İçerik yazma araçlarını yükleme
description: Bu makale, Git ve markdown dosyalarını düzenlemek için ihtiyacınız olacak istemci araçları indirip yüklemenize yardımcı olur.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 62c4b234f23b470ffea33cacdfc469fbd7e526bd
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="05029-103">İçerik yazma araçlarını yükleme</span><span class="sxs-lookup"><span data-stu-id="05029-103">Install content authoring tools</span></span>

<span data-ttu-id="05029-104">Bu makalede Git istemci araçlarını ve Visual Studio Code'u etkileşimli olarak yükleme adımları açıklanır.</span><span class="sxs-lookup"><span data-stu-id="05029-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="05029-105">[Windows için Git](https://git-scm.com/download/win)'i yükleme</span><span class="sxs-lookup"><span data-stu-id="05029-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="05029-106">[Visual Studio Code](https://code.visualstudio.com/)'u yükleme</span><span class="sxs-lookup"><span data-stu-id="05029-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="05029-107">Bir makalede yalnızca küçük değişiklikler yapıyorsanız bu makaledeki adımları tamamlamanız gerekli *değildir* ve doğrudan [küçük/seyrek görülen değişiklikler iş akışı](light-workflow.md) kısmına gidebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05029-107">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [minor/infrequent changes workflow](light-workflow.md).</span></span>
>
> <span data-ttu-id="05029-108">Büyük katkılarda bulunanların bu adımı tamamlaması önerilir, bu adımdan sonra [büyük/uzun ömürlü değişiklikler iş akışı](full-workflow.md) kısmına geçebilirler.</span><span class="sxs-lookup"><span data-stu-id="05029-108">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](full-workflow.md).</span></span> <span data-ttu-id="05029-109">Ana depoda yazma izinleriniz olsa bile, önerdiğiniz değişiklikleri çatalınızda depolamak üzere okuma/yazma izinlerinizin olacağı *depo çatalını oluşturmanız ve kopyalamanız kesinlikle önerilir (ve bu makalede öyle yaptığınız varsayılır)*.</span><span class="sxs-lookup"><span data-stu-id="05029-109">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="05029-110">Windows'da Git istemci araçlarını yükleme</span><span class="sxs-lookup"><span data-stu-id="05029-110">Install Git client tools on Windows</span></span>

 <span data-ttu-id="05029-111">[Software Freedom Conservancy’nin Git istemci araçlarının](https://git-scm.com/download/) son sürümünü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="05029-111">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="05029-112">Yükleme, Git sürüm denetim sistemini ve yerel Git deponuzla etkileşim için kullandığınız komut satırı uygulaması olan Git Bash'i içerir.</span><span class="sxs-lookup"><span data-stu-id="05029-112">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="05029-113">Komut satırı arabirimi (CLI) yerine bir grafik kullanıcı arabirimi (GUI) tercih ederseniz popüler seçenekler için [Software Freedom Conservancy’nin uygun GUI İstemcileri sayfası](https://git-scm.com/downloads/guis), [GitHub’ın GitHub Masaüstü](https://desktop.github.com/) veya [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)’a bakın.</span><span class="sxs-lookup"><span data-stu-id="05029-113">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="05029-114">Yükleme ve yapılandırma için seçtiğiniz istemcinin yönergelerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="05029-114">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="05029-115">Sonraki makalede, [yerel Git deponuzu ayarlayacaksınız](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="05029-115">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="05029-116">Ek Git kaynaklarını burada bulabilirsiniz: [Git terminolojisi](https://help.github.com/articles/github-glossary) | [Git temel bilgileri](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Git ve GitHub'ı öğrenme](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span><span class="sxs-lookup"><span data-stu-id="05029-116">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="05029-117">Markdown düzenleyicilerini anlama</span><span class="sxs-lookup"><span data-stu-id="05029-117">Understand Markdown editors</span></span>

<span data-ttu-id="05029-118">Markdown, okuması ve öğrenmesi kolay bir biçimlendirme dilidir.</span><span class="sxs-lookup"><span data-stu-id="05029-118">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="05029-119">Bu nedenle, bu dil kısa sürede endüstri standardı haline gelmiştir.</span><span class="sxs-lookup"><span data-stu-id="05029-119">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="05029-120">Markdown’da makale yazmak için önce bir Markdown düzenleyicisi indirip yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="05029-120">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="05029-121">[Visual Studio Code](https://code.visualstudio.com/), Microsoft'ta Markdown'ı düzenlemek için tercih edilen dildir.</span><span class="sxs-lookup"><span data-stu-id="05029-121">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="05029-122">Markdown'ı düzenlemeye yönelik bir diğer popüler araç da [Atom](https://atom.io)'dur.</span><span class="sxs-lookup"><span data-stu-id="05029-122">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="05029-123">Markdown metinleri, .md uzantılı dosyalara kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="05029-123">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="05029-124">Markdown temel bilgileri ve OPS özel Markdown uzantıları tarafından desteklenen özellikler dahil olmak üzere Markdown ile makale yazmaya yönelik ilave ayrıntılar daha sonra [Markdown kullanımı](how-to-write-use-markdown.md) makalesinde ele alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="05029-124">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="05029-125">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="05029-125">Visual Studio Code</span></span>

<span data-ttu-id="05029-126">VS Code olarak da bilinen [Visual Studio Code](https://code.visualstudio.com/), Windows, Linux ve Mac üzerinde çalışan basit bir düzenleyicidir.</span><span class="sxs-lookup"><span data-stu-id="05029-126">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="05029-127">Git tümleştirmesi ve uzantılar için destek içerir.</span><span class="sxs-lookup"><span data-stu-id="05029-127">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="05029-128">[VS Code](https://code.visualstudio.com/)'u indirin ve yükleyin.</span><span class="sxs-lookup"><span data-stu-id="05029-128">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="05029-129">VS Code giriş sayfasında işletim sisteminiz doğru algılanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="05029-129">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="05029-130">Windows</span><span class="sxs-lookup"><span data-stu-id="05029-130">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="05029-131">Mac</span><span class="sxs-lookup"><span data-stu-id="05029-131">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="05029-132">Linux</span><span class="sxs-lookup"><span data-stu-id="05029-132">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="05029-133">VS Code'u başlatmak ve geçerli klasörü açmak için, komut satırında veya bash kabuğunda `code .` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="05029-133">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="05029-134">Geçerli klasör yerel git deposunun bir parçasıysa, github tümleştirmesi Visual Studio Code'da otomatik olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="05029-134">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="05029-135">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="05029-135">Next steps</span></span>

<span data-ttu-id="05029-136">Artık [yerel Git deposunu ayarlamaya](get-started-setup-local.md) hazırsınız.</span><span class="sxs-lookup"><span data-stu-id="05029-136">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
