---
title: Microsoft Docs katkıda bulunan kılavuzuna genel bakış
description: Bu kılavuz, Microsoft belge sitesi olan docs.microsoft.com’a nasıl katkıda bulunabileceğinizi açıklar.
author: billwagner
ms.author: wiwagn
ms.date: 02/19/2019
ms.openlocfilehash: 9b091f864f5191c9f7a00900ec11a4a1cffdb698
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653517"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Microsoft Docs katkıda bulunan kılavuzuna genel bakış

[docs.microsoft.com ](https://docs.microsoft.com) (Docs) Stil Kılavuzu’na hoş geldiniz!

Microsoft belgelerinin birkaçı açık kaynaktır ve GitHub’da barındırılır. Tüm belge kümeleri tamamen açık kaynak değildir, ancak birçoğunda çekme istekleri aracılığıyla önerilen değişiklikler yapabileceğiniz genel kullanıma yönelik depolar vardır. Bu açık kaynak yaklaşımı ürün mühendisleri, içerik ekipleri ve müşteriler arasındaki iletişimi kolaylaştırır ve diğer avantajlar sunar:

- Açık kaynak depolar, hangi belgelere en çok ihtiyaç olduğuna dair geri bildirim almak için _açık olarak planlanır_.
- Açık kaynak depolar, ilk sürümde en faydalı içeriği yayımlamak için _açık olarak gözden geçirilir_.
- Açık kaynak depolar, içeriği devamlı olarak geliştirmeyi kolaylaştırmak için _açık olarak güncelleştirilir_.

[docs.microsoft.com](https://docs.microsoft.com) kullanıcı deneyimi, [GitHub](https://github.com) iş akışlarını doğrudan tümleştirerek daha da kolaylaştırır. [Görüntülediğiniz belgeyi düzenleyerek](#quick-edits-to-existing-documents) başlayın. Veya [yeni konuları inceleyerek](#review-open-prs) ya da [kalite sorunları oluşturarak](#create-quality-issues) yardımcı olun.

> [!IMPORTANT]
> Docs.microsoft.com’da yayın yapan tüm depolar [Microsoft Açık Kaynak Kullanım Şartları](https://opensource.microsoft.com/codeofconduct/) veya [.NET Foundation Kullanım Şartları](https://dotnetfoundation.org/code-of-conduct)’na tabidir. Daha fazla bilgi için bkz. [Kullanım Kuralları SSS](https://opensource.microsoft.com/codeofconduct/faq/). İsterseniz, soru ya da yorumlarınız için [opencode@microsoft.com](mailto:opencode@microsoft.com) veya [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) ile de iletişim kurabilirsiniz.<br>
>
> Belgelerde yapılan küçük düzeltmeler ve açıklamalar ile ortak depolardaki kod örnekleri, [docs.microsoft.com Kullanım Koşulları](https://docs.microsoft.com/legal/termsofuse)’nda anlatılmıştır. Bir Microsoft çalışanı değilseniz çekme isteğinde yeni veya önemli değişiklikler, çevrimiçi bir Katılım Lisans Sözleşmesi (CLA) göndermenizi isteyen bir yorum oluşturur. Çekme isteğiniz gözden geçirilmeden veya kabul edilmeden önce bu çevrimiçi formu doldurmanız gerekir.

## <a name="quick-edits-to-existing-documents"></a>Mevcut belgelerde hızlı düzeltmeler

Hızlı düzeltmeler, belgelerdeki küçük hataları ve eksikleri rapor etme ve düzeltme sürecini kolaylaştırır. Tüm çabalara rağmen yayımlanmış belgelerimizde ufak dil bilgisi ve yazım hataları _oluyor_. Bir hatayı rapor etmek için sorun da oluşturabilirsiniz ancak mümkün olduğunda bunun için çekme isteği (PR) oluşturmak, daha hızlı ve kolaydır.

1. Bazı belge sayfalarında doğrudan tarayıcıda düzenleme yapabilirsiniz. Böyle durumlarda aşağıdaki gibi bir **Düzenle** düğmesi görürsünüz. **Edit** (veya eşdeğer çevirisi olan Düzenle) düğmesine tıklayarak GitHub’daki kaynak dosyaya gidebilirsiniz. **Düzenle** düğmesi (metin içermeyen kalem simgesi) olmadığında belge sayfası değiştirilemez.

   ![Düzenle bağlantısının konumu](./media/index/edit-article.png)

2. Sonra, gösterildiği biçimde makaleyi düzenlemek için kalem simgesine tıklayın. Kalem simgesi griyse GitHub hesabınızla oturum açmanız veya yeni bir hesap oluşturmanız gerekir. 

   ![Kalem simgesinin konumu](./media/index/edit-icon.png)


3. Web düzenleyicisinde değişiklik yapın. Değişikliklerinizin biçimlendirmesini denetlemek için **Değişiklik önizlemesi** sekmesine tıklayın.

4. Değişikliklerinizi tamamladıktan sonra sayfanın sonuna kaydırın. Değişiklikleriniz için bir ad ve açıklama girdikten sonra, aşağıdaki şekilde gösterildiği gibi **Dosya değişikliği öner**’e tıklayın:

   ![Dosya değişikliği önerme](./media/index/submit-pull-request.png)

5. Değişikliğinizi önerdiğinizde göre deponun sahiplerinden yaptığınız değişiklikleri depolarına "çekmelerini" istemeniz gerekir. Bunun için "çekme isteği" adı verilen bir işlem kullanılır. Yukarıdaki şekilde **Dosya değişikliği öner**'e tıkladığınızda aşağıdakine benzer bir sayfanın açılması gerekir:

   ![Çekme isteği oluşturma](media/index/create-pull-request.png)

   **Çekme isteği oluştur**'a tıklayın, çekme isteği için bir ad (ve isteğe bağlı olarak bir açıklama) girin ve yeniden **Çekme isteği oluştur**'a tıklayın. (GitHub’da yeniyseniz daha fazla bilgi için bkz. [Çekme İstekleri Hakkında](https://help.github.com/en/articles/about-pull-requests).)

6. İşte bu kadar! İçerik ekibi üyeleri, PR’nizi gözden geçirip birleştirecekler. Büyük değişiklikler yaptıysanız, değişiklik talep eden geri bildirimler alabilirsiniz.

GitHub düzenleme UI’si depodaki izinlerinizi yanıtlar. Önceki görüntüler, hedef depoda yazma izinleri olmayan katkıda bulunanlar için geçerlidir. GitHub, hesabınızda otomatik olarak hedef depo çatalı oluşturur. Hedef depoda yazma erişiminiz varsa GitHub, hedef depoda yeni bir dal oluşturur. Bu dalın adı **\<GitHubKimliği\>-düzeltmeeki-n** biçimindedir. GitHub kimliğiniz ve düzeltme eki dalı için bir sayısal tanımlayıcı kullanılır.

Yazma erişimi olan katkıda bulunanlar dahil olmak üzere hepimiz değişiklikler için çekme isteklerini kullanıyoruz. Çoğu depoda, güncelleştirmelerin çekme isteği olarak gönderilmesi için `master` dal korumalıdır.

Tarayıcıda düzenleme deneyimi, ufak veya sık görülmeyen değişiklikler için idealdir. Büyük katkılar yapıyor veya gelişmiş Git özellikleri (dallara ayırma yönetimi veya gelişmiş birleştirme çakışmasını çözümleme gibi) kullanıyorsanız [deponun çatalını oluşturup yerel olarak çalışmanız](how-to-write-workflows-major.md) gerekir.

> [!NOTE]
> Bu özellik etkinleştirilmişse makaleyi **istediğiniz dilde** düzenleyebilirsiniz ve düzenleme türüne göre aşağıdaki işlemler gerçekleştirilir:
> 1. onaylanan dilbilimsel değişiklikler, Makine Çevirisi altyapımızın geliştirilmesine de yardımcı olur
> 2. Makalenin içeriğini önemli ölçüde değiştiren düzenlemeler şirket içinde değerlendirilerek İngilizce makale için değişiklik önerisi oluşturulur ve onaylanması durumunda bu değişikliğin tüm dillere yansıtılması sağlanır.
> Geliştirme önerileriniz yalnızca kendi dilinizdeki makaleleri olumlu yönde değiştirmekle kalmaz, diğer tüm dillerdeki içeriğe de katkıda bulunur.

## <a name="review-open-prs"></a>Açık PR’leri gözden geçirme

Açık PR’lere bakarsanız, yeni konuları yayımlanmadan önce okuyabilirsiniz. Gözden geçirmeler, [GitHub akış](https://guides.github.com/introduction/flow/) sürecini takip eder. Önerilen güncelleştirmeleri ve yeni makaleleri ortak depolarda görebilirsiniz. Bunları gözden geçirip yorumlarınızı ekleyin. Herhangi bir belge depomuza bakın ve ilginizi çeken alanlarda açık çekme isteklerini (PR’ler) kontrol edin. Önerilen güncelleştirmelerde topluluk geri bildirimi, tüm topluluğa yardımcı olur.

## <a name="create-quality-issues"></a>Kalite sorunları oluşturma

Belgelerimiz, devamlı olarak süren işlerdir. İyi sorunlar, topluluk için en önemli olan yerlere odaklanmamıza yardımcı olur. Ne kadar çok ayrıntı sağlayabilirseniz, sorun da o kadar yararlı olur. Hangi bilgileri aradığınızı bizimle paylaşın. Kullandığınız arama terimlerini de. Nereden başlayacağınızı bilmiyorsanız, bilmediğiniz bir teknolojiyi nasıl keşfetmek istediğinizi bizimle paylaşın.

Microsoft’un belge sayfalarının birçoğunda, sayfanın alt kısmında bir **Geri bildirim** bölümü bulunur. Söz konusu makaleye özel sorunları izlemek için buraya tıklayarak **Ürün geri bildirimi** veya **İçerik geri bildirimi** bırakabilirsiniz.

Sorunlar, gerekli şeyler konusunda konuşma başlatır. İçerik ekibi, ekleyebileceğimiz şeylerle ilgili fikirlerini verir ve sizden de düşüncelerinizi ister. Bir taslak oluşturduğumuzda, [PR’yi incelemenizi](#review-open-prs) isteyeceğiz.

## <a name="get-more-involved"></a>Daha fazla katılım gösterin

Diğer konular, Microsoft Docs’a daha fazla katkıda bulunmaya başlamanıza yardımcı olacaktır. GitHub depoları, Markdown araçları ve Microsoft Docs platformunda kullanılan uzantılar; diğer konularda açıklanır.
