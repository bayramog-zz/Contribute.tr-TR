---
title: Yerel Git deposunu ayarlama
description: Bu makale, belgelere katkıda bulunmak amacıyla çatal oluşturma ve kopyalama işlemleri dahil olmak üzere yerel Git deponuzun oluşturulmasına yönelik rehber sağlar.
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: 5373bf34399105c15caabe0abdc1ea0692c46a4a
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609511"
---
# <a name="set-up-git-repository-locally-for-documentation"></a>Belgeler için yerel Git deposunu ayarlama

Bu makalede, Microsoft belgelerine katkıda bulunmak amacıyla yerel makinenizde bir git deposu ayarlama adımları açıklanır. Katkıda bulunanlar yerel olarak kopyalanmış depoyu kullanarak yeni makaleler ekleyebilir, mevcut makalelerde büyük düzenlemeler yapabilir veya resimleri değiştirebilirler.

Katkıda bulunmaya başlamak için şu bir kerelik kurulum etkinliklerini çalıştırırsınız:
> [!div class="checklist"]
> * Uygun depoyu belirleme
> * GitHub hesabınıza depo çatalı oluşturma
> * Kopyalanan dosyalar için yerel bir klasör seçme
> * Depoyu yerel makinenize kopyalama
> * Uzak yukarı akış değerini yapılandırma

> [!IMPORTANT]
> Bir makalede yalnızca küçük değişiklikler yapıyorsanız, bu makaledeki adımları tamamlamanız *gerekmez*. Doğrudan [hızlı değişiklikler iş akışına](index.md#quick-edits-to-existing-documents) geçebilirsiniz.
>

## <a name="overview"></a>Genel Bakış

Microsoft’un belge sitesine katkıda bulunmak için ilgili belge deposunu kopyalayıp Markdown dosyalarını yerel olarak oluşturabilir ve düzenleyebilirsiniz. Microsoft kendi GitHub hesabınıza uygun deponun çatalını oluşturmanızı gerektirir; böylece önerdiğiniz değişiklikleri depolamak için orada okuma/yazma izinleriniz olabilir. Sonra, değişiklikleri paylaşılan salt okunur merkezi depoya eklemek için çekme isteklerini kullanırsınız.

![GitHub Üçgeni](./media/git-and-github-initial-setup.png)

GitHub’da yeniyseniz çatal oluşturma ve kopyalama işlemlerine kavramsal bir genel bakış için aşağıdaki videoyu izleyin:

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a>Depoyu belirleme

[Docs.microsoft.com](https://docs.microsoft.com) sitesinde barındırılan belgeler [github.com](https://www.github.com)'daki birbirinden farklı çeşitli depolarda durur.

1. Hangi depoyu kullanacağınızdan emin değilseniz Web tarayıcınızı kullanarak [docs.microsoft.com](https://docs.microsoft.com) adresindeki makaleyi ziyaret edin. Makalenin sağ üst kısmındaki **Düzenle** bağlantısını (kalem simgesi) seçin.

   ![Depo ve dosya konumunu saptamak için Düzenle'ye tıklayın.](media/index/edit-article.png)

2. O bağlantı sizi uygun deposundaki ilgili Markdown dosyasının github.com konumuna götürür. Deponun adının görüntülendiği URL'yi not alın.

   ![Depo konumunu saptamak için URL'ye bakın.](media/public-repo.png)

   Örneğin, şu popüler depolar genel katılımlarda kullanılabilir:
   - Azure belgeleri [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)
   - SQL Server belgeleri [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)
   - Visual Studio belgeleri [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)
   - .NET Belgeleri [https://github.com/dotnet/docs](https://github.com/dotnet/docs)
   - Azure .Net SDK belgeleri [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)

## <a name="fork-the-repository"></a>Depo çatalı oluşturma
Uygun depoyu kullanarak, GitHub web sitesi yoluyla kendi GitHub hesabınızda depo çatalı oluşturun.

Tüm ana belge depoları salt okunur erişim sağladığı için kişisel bir çatal gereklidir. Değişiklik yapmak için deponuzdan ana depoya bir [çekme isteği](git-github-fundamentals.md#pull-requests) göndermeniz gerekir. Bu işlemi kolaylaştırmak için önce deponun yazma izniniz olan bir kopyasına ihtiyacınız vardır. GitHub *çatalı* bu amaca hizmet eder.

1. Ana deponun GitHub sayfasına gidin ve sağ üst köşedeki **Çatal** düğmesine tıklayın.

   ![GitHub profil örneği](./media/contribute-get-started-setup-local/fork.png)

2. Sorulursa, çatalın oluşturulacağı hedef olarak GitHub hesabınızın kutucuğunu seçin. Bu istek, GitHub hesabınızda deponun çatal olarak bilinen bir kopyasını oluşturur.

## <a name="choose-a-local-folder"></a>Yerel klasör seçme
Deponun kopyasını yerel olarak saklamak için yerel bir klasör oluşturun. Bazı depolar büyük olabilir, örneğin 5 GB’a kadar çıkabilen azure-docs depoları. Kullanılabilir disk alanı olan bir konum seçin.

1. Hatırlaması ve yazması kolay bir klasör adı seçin. Örneğin bir kök klasör `C:\docs\` oluşturmayı düşünebilir veya kullanıcı profili dizininizde `~/Documents/docs/` bir klasör oluşturabilirsiniz

   > [!IMPORTANT]
   > Başka bir Git depo klasörü konumuna yerleştirilmiş bir yerel klasör yolunu seçmekten kaçının. Kopyalanmış Git klasörlerini yan yana depolamak kabul edilebilir olsa da bu klasörleri iç içe yerleştirmek, dosya izleme açısından sorun yaratır.

2. Git Bash’i başlatma

   ![Git Bash’i başlatma](./media/contribute-get-started-setup-local/gitbash-start.png)

   Git Bash’in genellikle başladığı konum ana dizin (~) veya Windows işletim sisteminde `/c/users/<Windows-user-account>/` olur.

   Geçerli dizini belirlemek için $ isteminde `pwd` yazın. 

3. Dizini (cd), depoyu yerel olarak depolamak için oluşturduğunuz klasör olarak değiştirin. Git Bash’in klasör yolları için ters eğik çizgi yerine eğik çizgi Linux kuralını kullandığını unutmayın.

   Örneğin `cd /c/docs/ ` veya `cd ~/Documents/docs/`

## <a name="create-a-local-clone"></a>Yerel bir kopya oluşturma

Git Bash kullanarak, **clone** komutunu çalıştırıp cihazınızda geçerli dizinde deponun bir kopyasını (çatalınızı) çekmeye hazırlanın. 

### <a name="authenticate-by-using-git-credential-manager"></a>Git Kimlik Bilgileri Yöneticisi kullanarak kimlik doğrulama
Windows için en son Git sürümünü yüklediyseniz ve varsayılan yüklemeyi kabul ettiyseniz Git Kimlik Bilgileri Yöneticisi varsayılan olarak etkindir. Git Kimlik Bilgileri Yöneticisi, GitHub ile daha önceden kimliği doğrulanmış bağlantılarınızı ve uzak öğelerinizi yeniden kurarken kişisel erişim belirtecinizi kullanma gereğini ortadan kaldırarak kimlik doğrulamasını kolaylaştırır.

1. Depo adı sağlayarak **clone** komutunu çalıştırın. Kopyalama, çatalı (kopyayı) yerel bilgisayarınızdaki çatallı depoya indirir. 

    > [!Tip]
    > GitHub kullanıcı arabiriminde bulunan **Kopyala veya indir** düğmesini kullanarak kopyalama komutu için çatalınızın GitHub URL’sini alabilirsiniz:
    >
    > ![Kopyala veya indir](./media/contribute-get-started-setup-local/clone-or-download.png)

    Kopyalama işlemi sırasında, çatalını oluşturduğunuz ana deponun değil, *çatalınızın* yolunu belirttiğinizden emin olun. Yoksa değişikliklerinizi kaydedemezsiniz. Çatalınıza ise kişisel GitHub kullanıcı hesabınız üzerinden başvurulur, örneğin `github.com/<github-username>/<repo>`.

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    Kopyalama komutunuz şu örnektekine benzer olmalıdır:

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. Sorulduğunda GitHub kimlik bilgilerinizi girin.

    ![GitHub’da Oturum Açma](./media/contribute-get-started-setup-local/github-login.png)

3. Sorulduğunda iki öğeli kimlik doğrulama kodunuzu girin.

    ![GitHub iki öğeli kimlik doğrulama](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > Kimlik bilgileriniz, gelecek GitHub isteklerinde kimlik doğrulamak üzere kaydedilir. Bu kimlik doğrulamasını bilgisayar başına yalnızca bir kez yapmanız yeterlidir. 

4. Kopyala komutu, depo dosyalarının bir kopyasını çalıştırır ve çatalınızdan yerel diskteki yeni klasöre indirir. Geçerli klasörde yeni bir klasör oluşturulur. Bu, depo boyutuna bağlı olarak birkaç dakika sürebilir. İşlem tamamlandığında, yapıyı görmek adına klasörü inceleyebilirsiniz.

## <a name="configure-remote-upstream"></a>Uzak yukarı akışı yapılandırma
Depoyu kopyaladıktan sonra ana depoya **yukarı akış** adlı bir salt okunur uzak bağlantı ayarlayın. Yukarı akış URL’sini kullanarak yerel deponuzun başkaları tarafından yapılan değişikliklerle her zaman eşit kalmasını sağlarsınız. **git remote** komutu, yapılandırma değerini ayarlamak için kullanılır. Yukarı akış deposundan dal bilgilerini yenilemek için **fetch** komutunu kullanın.

1. **Git Kimlik Bilgileri Yöneticisi** kullanıyorsanız aşağıdaki komutları kullanın. \<Depo\> ve \<kuruluş\> yer tutucularını değiştirin.
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. Yapılandırılmış değerleri inceleyin ve URL’lerin doğru olduğunu onaylayın. **Kaynak** URL’lerinin kişisel çatalınıza gittiğinden emin olun. **Yukarı akış** URL’lerinin MicrosoftDocs veya Azure gibi bir ana depoya gittiğinden emin olun. 
   ```bash
   git remote -v 
   ```

   Örnek bir uzak çıkış gösterilmiştir. azure-docs deposuna erişmek için hayali bir MyGitAccount hesabı ve kişisel erişim belirteci yapılandırılmıştır:
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. Bir hata yaptıysanız, uzak değeri kaldırabilirsiniz. Yukarı akış değerini kaldırmak için `git remote remove upstream` komutunu çalıştırın.

## <a name="next-steps"></a>Sonraki adımlar
- İçerik ekleme ve güncelleştirme hakkında daha fazla bilgi edinmek için [GitHub katkı iş akışı](how-to-write-workflows-major.md) sayfasına devam edin.
