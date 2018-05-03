---
title: Yerel Git deposunu ayarlama
description: Bu makale, belgelere katkıda bulunmak amacıyla çatal oluşturma ve kopyalama işlemleri dahil olmak üzere yerel Git deponuzun oluşturulmasına yönelik rehber sağlar.
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 01/18/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: d9c7211641fb05aaca8a76e10c7216ff61a5d23c
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2018
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="756e5-103">Belgeler için yerel Git deposunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="756e5-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="756e5-104">Bu makalede, Microsoft belgelerine katkıda bulunmak amacıyla yerel makinenizde bir git deposu ayarlama adımları açıklanır.</span><span class="sxs-lookup"><span data-stu-id="756e5-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="756e5-105">Katkıda bulunanlar yerel olarak kopyalanmış depoyu kullanarak yeni makaleler ekleyebilir, mevcut makalelerde büyük düzenlemeler yapabilir veya resimleri değiştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="756e5-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="756e5-106">Katkıda bulunmaya başlamak için şu bir kerelik kurulum etkinliklerini çalıştırırsınız:</span><span class="sxs-lookup"><span data-stu-id="756e5-106">You run these one-time setup activities to get started contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="756e5-107">Uygun depoyu belirleme</span><span class="sxs-lookup"><span data-stu-id="756e5-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="756e5-108">GitHub hesabınıza depo çatalı oluşturma</span><span class="sxs-lookup"><span data-stu-id="756e5-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="756e5-109">Kopyalanan dosyalar için yerel bir klasör seçme</span><span class="sxs-lookup"><span data-stu-id="756e5-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="756e5-110">Depoyu yerel makinenize kopyalama</span><span class="sxs-lookup"><span data-stu-id="756e5-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="756e5-111">Uzak yukarı akış değerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="756e5-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="756e5-112">Bir makalede yalnızca küçük değişiklikler yapıyorsanız, bu makaledeki adımları tamamlamanız *gerekmez*.</span><span class="sxs-lookup"><span data-stu-id="756e5-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="756e5-113">Doğrudan [küçük/seyrek görülen değişiklikler iş akışına](light-workflow.md) geçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="756e5-113">You can continue directly to the [minor/infrequent changes workflow](light-workflow.md).</span></span>
>

## <a name="overview"></a><span data-ttu-id="756e5-114">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="756e5-114">Overview</span></span>

<span data-ttu-id="756e5-115">Microsoft’un belge sitesine katkıda bulunmak için ilgili belge deposunu kopyalayıp Markdown dosyalarını yerel olarak oluşturabilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="756e5-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="756e5-116">Microsoft kendi github hesabınıza uygun deponun çatalını oluşturmanızı gerektirir; böylece önerdiğiniz değişiklikleri depolamak için orada okuma/yazma izinleriniz olabilir.</span><span class="sxs-lookup"><span data-stu-id="756e5-116">Microsoft requires you to fork the appropriate repository into your own github account, so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="756e5-117">Sonra, değişiklikleri paylaşılan salt okunur merkezi depoya eklemek için çekme isteklerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="756e5-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![GitHub Üçgeni](./media/git-and-github-initial-setup.png)

<span data-ttu-id="756e5-119">GitHub’da yeniyseniz çatal oluşturma ve kopyalama işlemlerine kavramsal bir genel bakış için aşağıdaki videoyu izleyin:</span><span class="sxs-lookup"><span data-stu-id="756e5-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="756e5-120">Depoyu belirleme</span><span class="sxs-lookup"><span data-stu-id="756e5-120">Determine the repository</span></span>

<span data-ttu-id="756e5-121">[Docs.microsoft.com](https://docs.microsoft.com) sitesinde barındırılan belgeler [github.com](https://www.github.com)'daki birbirinden farklı çeşitli depolarda durur.</span><span class="sxs-lookup"><span data-stu-id="756e5-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="756e5-122">Hangi depoyu kullanacağınızdan emin değilseniz, web tarayıcınızı kullanarak docs.microsoft.com'daki makaleyi ziyaret edin.</span><span class="sxs-lookup"><span data-stu-id="756e5-122">If you are unsure of which repository to use, then visit the article on docs.microsoft.com using your web browser.</span></span> <span data-ttu-id="756e5-123">Makalenin sağ üst kısmındaki **Düzenle** bağlantısını (kalem simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="756e5-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![Depo ve dosya konumunu saptamak için Düzenle'ye tıklayın.](media/edit-article.png)

2. <span data-ttu-id="756e5-125">O bağlantı sizi uygun deposundaki ilgili Markdown dosyasının github.com konumuna götürür.</span><span class="sxs-lookup"><span data-stu-id="756e5-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="756e5-126">Deponun adının görüntülendiği URL'yi not alın.</span><span class="sxs-lookup"><span data-stu-id="756e5-126">Note the URL to view the repository name.</span></span>

   ![Depo konumunu saptamak için URL'ye bakın.](media/public-repo.png)

   <span data-ttu-id="756e5-128">Örneğin, şu popüler depolar genel katılımlarda kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="756e5-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="756e5-129">Azure belgeleri [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="756e5-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="756e5-130">SQL Server belgeleri [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="756e5-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="756e5-131">Visual Studio belgeleri [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="756e5-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="756e5-132">.NET Belgeleri [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="756e5-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="756e5-133">Azure .Net SDK belgeleri [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="756e5-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="756e5-134">Depo çatalı oluşturma</span><span class="sxs-lookup"><span data-stu-id="756e5-134">Fork the repository</span></span>
<span data-ttu-id="756e5-135">Uygun depoyu kullanarak, GitHub web sitesi yoluyla kendi GitHub hesabınızda depo çatalı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="756e5-135">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="756e5-136">Tüm Docs ana depoları salt okunur erişim sağladığı için depolardaki içeriklerde doğrudan değişiklik yapamazsınız, bu nedenle de kişisel bir çatal gereklidir.</span><span class="sxs-lookup"><span data-stu-id="756e5-136">A personal fork is required since all main documentation repositories provide read-only access, which means you cannot make changes directly on content in the repositories.</span></span> <span data-ttu-id="756e5-137">Değişiklik yapmak için deponuzdan ana depoya bir [çekme isteği](git-github-fundamentals.md#pull-requests) göndermeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="756e5-137">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="756e5-138">Bu işlemi kolaylaştırmak için önce deponun yazma izniniz olan bir kopyasına ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="756e5-138">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="756e5-139">GitHub *çatalı* bu amaca hizmet eder.</span><span class="sxs-lookup"><span data-stu-id="756e5-139">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="756e5-140">Ana deponun GitHub sayfasına gidin ve sağ üst köşedeki **Çatal** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="756e5-140">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![GitHub profil örneği](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="756e5-142">Sorulursa, çatalın oluşturulacağı hedef olarak GitHub hesabınızın kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="756e5-142">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="756e5-143">Bu istek, GitHub hesabınızda deponun çatal olarak bilinen bir kopyasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="756e5-143">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="756e5-144">Yerel klasör seçme</span><span class="sxs-lookup"><span data-stu-id="756e5-144">Choose a local folder</span></span>
<span data-ttu-id="756e5-145">Deponun kopyasını yerel olarak saklamak için yerel bir klasör oluşturun.</span><span class="sxs-lookup"><span data-stu-id="756e5-145">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="756e5-146">Bazı depolar büyük olabilir, örneğin 5 GB’a kadar çıkabilen azure-docs depoları.</span><span class="sxs-lookup"><span data-stu-id="756e5-146">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="756e5-147">Kullanılabilir disk alanı olan bir konum seçin.</span><span class="sxs-lookup"><span data-stu-id="756e5-147">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="756e5-148">Hatırlaması ve yazması kolay bir klasör adı seçin.</span><span class="sxs-lookup"><span data-stu-id="756e5-148">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="756e5-149">Örneğin bir kök klasör `C:\docs\` oluşturmayı düşünebilir veya kullanıcı profili dizininizde `~/Documents/docs/` bir klasör oluşturabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="756e5-149">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="756e5-150">Başka bir Git depo klasörü konumuna yerleştirilmiş bir yerel klasör yolunu seçmekten kaçının.</span><span class="sxs-lookup"><span data-stu-id="756e5-150">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="756e5-151">Kopyalanmış Git klasörlerini yan yana depolamak kabul edilebilir olsa da bu klasörleri iç içe yerleştirmek, dosya izleme açısından sorun yaratır.</span><span class="sxs-lookup"><span data-stu-id="756e5-151">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="756e5-152">Git Bash’i başlatma</span><span class="sxs-lookup"><span data-stu-id="756e5-152">Launch Git Bash</span></span>

   ![Git Bash’i başlatma](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="756e5-154">Git Bash’in genellikle başladığı konum ana dizin (~) veya Windows işletim sisteminde `/c/users/<Windows-user-account>/` olur.</span><span class="sxs-lookup"><span data-stu-id="756e5-154">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="756e5-155">Geçerli dizini belirlemek için $ isteminde `pwd` yazın.</span><span class="sxs-lookup"><span data-stu-id="756e5-155">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="756e5-156">Dizini (cd), depoyu yerel olarak depolamak için oluşturduğunuz klasör olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="756e5-156">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="756e5-157">Git Bash’in klasör yolları için ters eğik çizgi yerine eğik çizgi Linux kuralını kullandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="756e5-157">Note that Git Bash uses Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="756e5-158">Örneğin `cd /c/docs/ ` veya `cd ~/Documents/docs/`</span><span class="sxs-lookup"><span data-stu-id="756e5-158">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="756e5-159">Yerel bir kopya oluşturma</span><span class="sxs-lookup"><span data-stu-id="756e5-159">Create a local clone</span></span>

<span data-ttu-id="756e5-160">Git Bash kullanarak, **clone** komutunu çalıştırıp cihazınızda geçerli dizinde deponun bir kopyasını (çatalınızı) çekmeye hazırlanın.</span><span class="sxs-lookup"><span data-stu-id="756e5-160">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="756e5-161">Git Kimlik Bilgileri Yöneticisi kullanarak kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="756e5-161">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="756e5-162">Windows için en son Git sürümünü yüklediyseniz ve varsayılan yüklemeyi kabul ettiyseniz Git Kimlik Bilgileri Yöneticisi varsayılan olarak etkindir.</span><span class="sxs-lookup"><span data-stu-id="756e5-162">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="756e5-163">Git Kimlik Bilgileri Yöneticisi, GitHub ile daha önceden kimliği doğrulanmış bağlantılarınızı ve uzak öğelerinizi yeniden kurarken kişisel erişim belirtecinizi kullanma gereğini ortadan kaldırarak kimlik doğrulamayı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="756e5-163">Git Credential Manager makes authentication much easier, because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="756e5-164">Depo adı sağlayarak **clone** komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="756e5-164">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="756e5-165">Kopyalama, çatalı (kopyayı) yerel bilgisayarınızdaki çatallı depoya indirir.</span><span class="sxs-lookup"><span data-stu-id="756e5-165">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="756e5-166">GitHub kullanıcı arabiriminde bulunan **Kopyala veya indir** düğmesini kullanarak kopyalama komutu için çatalınızın GitHub URL’sini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="756e5-166">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > ![Kopyala veya indir](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="756e5-168">Kopyalama işlemi sırasında, çatalını oluşturduğunuz ana deponun değil, *çatalınızın* yolunu belirttiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="756e5-168">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="756e5-169">Yoksa değişikliklerinizi kaydedemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="756e5-169">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="756e5-170">Çatalınıza ise kişisel GitHub kullanıcı hesabınız üzerinden başvurulur, örneğin `github.com/<github-username>/<repo>`.</span><span class="sxs-lookup"><span data-stu-id="756e5-170">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="756e5-171">Kopyalama komutunuz şu örnektekine benzer olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="756e5-171">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="756e5-172">Sorulduğunda GitHub kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="756e5-172">When you're prompted, enter your GitHub credentials.</span></span>

    ![GitHub’da Oturum Açma](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="756e5-174">Sorulduğunda iki öğeli kimlik doğrulama kodunuzu girin.</span><span class="sxs-lookup"><span data-stu-id="756e5-174">When you're prompted, enter your two-factor authentication code.</span></span>

    ![GitHub iki öğeli kimlik doğrulama](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="756e5-176">Kimlik bilgileriniz, gelecek GitHub isteklerinde kimlik doğrulamak üzere kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="756e5-176">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="756e5-177">Bu kimlik doğrulamasını bilgisayar başına yalnızca bir kez yapmanız yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="756e5-177">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="756e5-178">Kopyala komutu, depo dosyalarının bir kopyasını çalıştırır ve çatalınızdan yerel diskteki yeni klasöre indirir.</span><span class="sxs-lookup"><span data-stu-id="756e5-178">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="756e5-179">Geçerli klasörde yeni bir klasör oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="756e5-179">A new folder is made within the current folder.</span></span> <span data-ttu-id="756e5-180">Bu, depo boyutuna bağlı olarak birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="756e5-180">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="756e5-181">İşlem tamamlandığında, yapıyı görmek adına klasörü inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="756e5-181">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="756e5-182">Uzak yukarı akışı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="756e5-182">Configure remote upstream</span></span>
<span data-ttu-id="756e5-183">Depoyu kopyaladıktan sonra ana depoya **yukarı akış** adlı bir salt okunur uzak bağlantı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="756e5-183">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="756e5-184">Yukarı akış URL’sini kullanarak yerel deponuzun başkaları tarafından yapılan değişikliklerle her zaman eşit kalmasını sağlarsınız.</span><span class="sxs-lookup"><span data-stu-id="756e5-184">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="756e5-185">**git remote** komutu, yapılandırma değerini ayarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="756e5-185">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="756e5-186">Yukarı akış deposundan dal bilgilerini yenilemek için **fetch** komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="756e5-186">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="756e5-187">**Git Kimlik Bilgileri Yöneticisi** kullanıyorsanız aşağıdaki komutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="756e5-187">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="756e5-188">\<Depo\> ve \<kuruluş\> yer tutucularını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="756e5-188">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="756e5-189">Yapılandırılmış değerleri inceleyin ve URL’lerin doğru olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="756e5-189">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="756e5-190">**Kaynak** URL’lerinin kişisel çatalınıza gittiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="756e5-190">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="756e5-191">**Yukarı akış** URL’lerinin MicrosoftDocs veya Azure gibi bir ana depoya gittiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="756e5-191">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="756e5-192">Örnek bir uzak çıkış gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="756e5-192">Example remote output is shown.</span></span> <span data-ttu-id="756e5-193">azure-docs deposuna erişmek için hayali bir MyGitAccount hesabı ve kişisel erişim belirteci yapılandırılmıştır:</span><span class="sxs-lookup"><span data-stu-id="756e5-193">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="756e5-194">Bir hata yaptıysanız, uzak değeri kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="756e5-194">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="756e5-195">Yukarı akış değerini kaldırmak için `git remote remove upstream` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="756e5-195">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="756e5-196">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="756e5-196">Next steps</span></span>
- <span data-ttu-id="756e5-197">İçerik ekleme ve güncelleştirme hakkında daha fazla bilgi edinmek için [GitHub katkı iş akışı](how-to-write-workflows-major.md) sayfasına devam edin.</span><span class="sxs-lookup"><span data-stu-id="756e5-197">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>