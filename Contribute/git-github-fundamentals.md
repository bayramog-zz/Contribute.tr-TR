---
title: Belgeler için Git ve GitHub temel özellikleri
description: Bu makale, Git ve GitHub deposuna genel bir bakış sağlar, içeriğin nasıl organize edildiğini ve docs.microsoft.com adlandırma kurallarını açıklar.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 5ad2ca323b680078c2bfd2fc4cac6fb1883c411f
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2018
---
# <a name="git-and-github-essentials-for-docs"></a>Docs belgeleri için Git ve GitHub temel özellikleri

## <a name="overview"></a>Genel Bakış

Docs içeriğine katkıda bulunan bir kullanıcı olarak birden fazla araç ve işlem ile etkileşimde bulunursunuz. Aynı projede diğer katkıda bulunanlarla paralel olarak, muhtemelen tam olarak aynı içerik üzerinde ve hatta aynı zamanda çalışırsınız. Tüm bunlar, Git ve GitHub yazılımları ile sağlanır.

Git, açık kaynaklı bir sürüm denetim sistemidir. *Depolarda* bulunan dosyaların *dağıtılmış sürüm denetimi* yoluyla bu tip toplu proje işbirliğini kolaylaştırır. Temel olarak Git, herhangi bir depoda birden çok katkıda bulunan tarafından yapılan iş akışlarını tümleştirmeyi mümkün kılar.

GitHub, [docs.microsoft.com](https://docs.microsoft.com) içeriklerini saklamak için kullanılan depolar gibi Git depoları için web tabanlı bir barındırma hizmetidir. Herhangi bir proje için GitHub, ana depoyu barındırır ve katkıda bulunanlar, bu depodan kendi işlerinin kopyasını alabilirler.

## <a name="git"></a>Git

Merkezileştirilmiş sürüm denetim sistemlerine (Team Foundation Server, SharePoint veya Visual SourceSafe gibi) yabancı değilseniz kendi dağıtılmış modelini desteklemek için Git’in benzersiz bir katkı iş akışı ve terminolojisi olduğunu fark edebilirsiniz. Örneğin, normalde giriş/çıkış işlemleriyle birlikte gelen dosya kilitleme işlemi burada yoktur. Git, değişiklikleri daha ayrıntılı bir düzeyde ele alır ve dosyaları bayt düzeyinde karşılaştırır.

Git ayrıca, bir projenin içeriğini yönetmek için katmanlı bir yapı kullanır:

- *Depo* - Aynı zamanda *repo* olarak bilinir, en üst düzey depolama birimidir. Bir depo bir veya daha fazla dal içerir.
- *Dal*: Bir projenin içerik kümesini oluşturan dosya ve klasörleri içeren depolama birimi. Dallar, iş akışlarını (genellikle sürümler olarak adlandırılır) birbirinden ayırır. Katkılar her zaman belirli bir dal kapsamında yapılır. Tüm depoların bir varsayılan dalı (genellikle “ana” olarak adlandırılır) ve tekrar bu ana dalla birleştirilmek üzere bir veya daha fazla dalı bulunur. Ana dal, projenin geçerli sürümü ve "tek gerçeklik kaynağı" olarak görev yapar. Depodaki diğer tüm dallar bu üst öğeden oluşturulur.

Katkıda bulunanlar, yerel ve GitHub seviyelerinde depoları güncelleştirmek ve yönlendirmek için Git’i kullanır:

- Yerel depoları yönetmek ve GitHub depoları ile iletişime geçmek için Git komutlarını destekleyen Git Bash konsolu gibi araçlarla yerel olarak
- Ana depoya geri akan katkıların birleşimini yönetmek için Git’i tümleştiren [www.github.com](https://www.github.com) aracılığıyla

## <a name="github"></a>GitHub

> [!NOTE]
> Docs kılavuzu, GitHub kullanımı tabanında oluşturulmuş olsa da, bazı takımlar Git depolarını barındırmak için Visual Studio Team Services kullanır. Visual Studio Takım Gezgini istemcisi, Visual Studio Team Services depoları ile etkileşime geçmek için bir GUI sağlar. Bu, bir komut satırından Git komutları kullanmaya alternatiftir.
> </br>
> Ayrıca aşağıdaki bilgilerin pek çoğu, GitHub’da Azure hizmet içeriklerinin barındırılmasıyla yıllar içinde elde edilen deneyimlere dayanan en iyi uygulamalardır. Bu uygulamalar bazı Docs depolarında gerekli olabilir.

Tüm iş akışları, herhangi bir Docs projesinin ana deposunun saklandığı GitHub seviyesinde başlayıp biter. Katkıda bulunanların kendi kullanımları için oluşturduğu kopyalar birden fazla bilgisayara dağıtılır. Bu kopyalar sonunda projenin ana GitHub deposuyla uzlaştırılır.

### <a name="directory-organization"></a>Dizin düzeni

Daha önce bahsedildiği gibi bir projenin varsayılan/ana dalı, projenin geçerli içerik sürümü olarak hizmet verir. Ana daldaki (ve bundan oluşturulan dallardaki) içerikler, karşılık gelen Docs sayfalarındaki makalelerin düzeniyle biraz benzerdir. Alt dizinler; benzer içerikler (hizmetler gibi), medya içerikleri (görüntü dosyaları gibi) ve içeriğin tekrar kullanımını sağlayan “ekleme” dosyalarının ayrılması için kullanılır.

Bir ana `articles` dizinini genellikle deponun kökünde bulabilirsiniz. Makale dizini bir alt dizin kümesini içerir. Alt dizinlerdeki makaleler, *.md* uzantısı kullanan Markdown dosyaları olarak biçimlendirilir. Birden fazla hizmeti destekleyen bazı depolar, genel bir `/articles` alt dizini kullanır, örneğin [https://github.com/microsoft/Azure-Docs](https://github.com/microsoft/Azure-Docs) deposu gibi. Diğerleri ise hizmete özgü bir ad kullanabilir, örneğin `/IntuneDocs` kullanan[https://github.com/microsoft/IntuneDocs](https://github.com/microsoft/IntuneDocs) deposu.

Bu dizinin kökünde, hizmet veya ürünün geneliyle alakalı makaleler bulabilirsiniz. Genelde özellikler/hizmetler veya yaygın senaryolarla eşleşen başka bir alt dizinler serisi bulabilirsiniz. Örneğin Azure “sanal makine” makaleleri `/virtual-machines` alt dizininde, “anlama ve keşfetme” makaleleri ise `/understand-explore` alt dizininde yer alır.

### <a name="media-subdirectory"></a>Medya alt dizini

Her makale dizini, karşılık gelen medya dosyaları için bir `/media` alt dizini içerir. Medya dosyaları, görüntü başvuruları bulunan makaleler tarafından kullanılan görüntüler içerir.

### <a name="includes-subdirectory"></a>Eklemeler alt dizini

İki ya da daha fazla makale tarafından paylaşılan yeniden kullanılabilir içerik olduğunda, bu içerikler ana `/includes` dizininden alınan bir `articles` alt dizinine yerleştirilir. Ekleme dosyasını kullanan Markdown dosyasında, ekleme dosyasına başvurulması gereken konuma karşılık gelen bir “ekleme” Markdown uzantısı yerleştirilir.

Daha fazla bilgi için [Markdown’ı kullanma - Eklemeler](how-to-write-use-markdown.md#includes) bölümüne bakın.

### <a name="markdown-file-template"></a>Markdown dosya şablonu

Kolaylık sağlamak için her deponun kök dizini genellikle `template.md` adlı bir Markdown şablon dosyası içerir. Depoya göndermek üzere yeni bir makale oluşturmanız gerekirse "başlangıç dosyası" olarak bu şablonu kullanabilirsiniz. Bu dosya şunları içerir:

- Dosyanın üst kısmında iki adet 3 kısa çizgi ile gösterilen bir **meta veri üst bilgisi**. Makaleyle ilgili izleme bilgileri için kullanılan çeşitli etiketleri içerir. Makale meta verileri yazar alıntısı, katılımcı alıntısı, içerik haritaları ve makale açıklamaları gibi belirli işlevleri etkinleştirir. Ayrıca, SEO iyileştirmeleri ve Microsoft’un içerik performansını değerlendirmek için kullandığı raporlama işlemlerini içerir. Bu nedenle meta veriler önemlidir!
- Çeşitli meta veri etiketleri ve değerlerinin açıklandığı **meta veriler bölümü**. Meta veri bölümü için kullanılacak değerlerden emin değilseniz bölümü boş bırakabilirsiniz veya başına (#) diyez etiketi koyarak yorumlayabilirsiniz, bunlar daha sonra depo için çekme isteğini gözden geçiren tarafından incelenir/tamamlanır.
- Bir makalenin öğelerini biçimlendirmeye yönelik çeşitli **Markdown kullanım örnekleri**.
- Çeşitli uyarı türleri için kullanabileceğiniz, **Markdown uzantılarının kullanılması ile ilgili genel talimatlar**.
- iframe kullanarak **video ekleme** örnekleri.
- Düğme ve seçici gibi özel denetimler için kullanabileceğiniz, **docs.microsoft.com uzantılarının kullanılması ile ilgili genel yönergeler**.

## <a name="pull-requests"></a>Çekme istekleri

Bir *çekme isteği*, katkıda bulunan kişinin varsayılan dala uygulanacak bir grup değişikliği sunması için kolay bir yol sağlar. Bu değişiklikler (*işlemeler* olarak da bilinir), katkıda bulunan kişinin dalında depolanır ve GitHub varsayılan dalda *birleştirme* etkisinin modelini oluşturabilir. Çekme isteği ayrıca katkıda bulunan kişiye, çekme isteğini gözden geçiren kişi tarafından yapılan derleme/doğrulama işleminden sonra geri bildirim yollamaya yarar. Böylece katkıda bulunan, değişiklikler varsayılan dalla birleştirilmeden önce olası sorunlar veya soruları çözebilir.

Önermek istediğiniz değişikliklerin boyutuna bağlı olarak çekme isteği ile katkıda bulunmanın iki yolu vardır. Bunu daha sonra, bu kılavuzun [GitHub iş akışı](light-workflow.md) bölümünde ayrıntılı şekilde açıklayacağız.

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
