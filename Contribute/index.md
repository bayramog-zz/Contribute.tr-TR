---
title: Microsoft Docs katkıda bulunan kılavuzuna genel bakış
description: Bu kılavuz, Microsoft belge sitesi olan docs.microsoft.com’a nasıl katkıda bulunabileceğinizi açıklar.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 04/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1cda40c890e5b30e6e1e10f3bcee0278f8004653
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2018
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Microsoft Docs katkıda bulunan kılavuzuna genel bakış

[docs.microsoft.com ](https://docs.microsoft.com) (Docs) Stil Kılavuzu’na hoş geldiniz!

Belge kümelerimizden birkaçı açık kaynaktır ve GitHub’da barınır. Daha fazla ekip bu modeli benimsemektedir. Tamamen açık kaynak olmayan belge kümelerinde bile çekme istekleri yapabileceğiniz genel kullanıma yönelik depolar vardır. Böylece mühendisler, içerik ekipleri ve müşterilerimiz arasındaki iletişim kolaylaşır ve iyileşir. Açık çalışmanın bazı avantajları vardır:

- Açık kaynak depolar, hangi belgelere en çok ihtiyaç olduğuna dair geri bildirim almak için açık olarak planlanır.
- Açık kaynak depolar, ilk sürümde en faydalı içeriği yayımlamak için açık olarak gözden geçirilir.
- Açık kaynak depolar, içeriği devamlı olarak geliştirmeyi kolaylaştırmak için açık olarak güncelleştirilir.

[docs.microsoft.com](https://docs.microsoft.com) kullanıcı deneyimi, [GitHub](https://github.com) iş akışlarını doğrudan tümleştirerek daha da kolaylaştırır. [Görüntülediğiniz belgeyi düzenleyerek](#quick-edits-to-existing-documents) başlayın. Veya [yeni konuları inceleyerek](#review-open-prs) ya da [kalite sorunları oluşturarak](#create-quality-issues) yardımcı olun.

> [!IMPORTANT]
> Docs.microsoft.com’da yayın yapan tüm depolar [Microsoft Açık Kaynak Kullanım Şartları](https://opensource.microsoft.com/codeofconduct/) veya [.NET Foundation Kullanım Şartları](https://dotnetfoundation.org/code-of-conduct)’na tabidir. Daha fazla bilgi için bkz. [Kullanım Kuralları SSS](https://opensource.microsoft.com/codeofconduct/faq/). İsterseniz, soru ya da yorumlarınız için [opencode@microsoft.com](mailto:opencode@microsoft.com) veya [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) ile de iletişim kurabilirsiniz.<br>
>
> Belgelerde yapılan küçük düzeltmeler ve açıklamalar ile ortak depolardaki kod örnekleri, [docs.microsoft.com Kullanım Koşulları](https://docs.microsoft.com/legal/termsofuse)’nda anlatılmıştır. Bir Microsoft çalışanı değilseniz çekme isteğinde yeni veya önemli değişiklikler, çevrimiçi bir Katılım Lisans Sözleşmesi (CLA) göndermenizi isteyen bir yorum oluşturur. Çekme isteğiniz gözden geçirilmeden veya kabul edilmeden önce bu çevrimiçi formu doldurmanız gerekir.

## <a name="quick-edits-to-existing-documents"></a>Mevcut belgelerde hızlı düzeltmeler

Hızlı düzeltmeler, belgelerdeki küçük hataları ve eksikleri rapor etme ve düzeltme sürecini kolaylaştırır. Tüm çabalara rağmen yayımlanmış belgelerimizde ufak gramer ve yazım hataları oluyor. Bir hatayı rapor etmek için sorun da oluşturabilirsiniz ancak bunun için çekme isteği (PR) oluşturmak, daha hızlı ve kolaydır. Neredeyse tüm makalelerde, aşağıdaki şekilde gösterildiği gibi bir düzenleme düğmesi vardır. **Düzenle** düğmesine tıklayarak GitHub’daki kaynak dosyaya gidersiniz.

![Düzenle bağlantısının konumu](./media/index/edit-article.png)

Daha sonra, aşağıdaki şekilde gösterilen kalem simgesine tıklayarak makaleyi düzenleyin.

> [!NOTE]
> Kalem simgesi griyse GitHub hesabınızla oturum açmanız veya yeni bir hesap oluşturmanız gerekir. Web düzenleyicisinde değişiklik yapın. **Değişiklik önizlemesi** sekmesine tıklayarak değişikliklerinizin biçimini görebilirsiniz.

![Kalem simgesinin konumu](./media/index/editicon.png)

Değişikliklerinizi tamamladıktan sonra sayfanın sonuna kaydırın. PR’niz için bir ad ve açıklama girdikten sonra, aşağıdaki şekilde gösterildiği gibi **Dosya değişikliği öner**’e tıklayın:

![değişikliğinizi önerme](./media/index/submit-pull-request.png)

İşte bu kadar! İçerik ekibi üyeleri, PR’nizi gözden geçirip birleştirecekler. Büyük değişiklikler yaptıysanız, değişiklik talep eden geri bildirimler alabilirsiniz.

GitHub düzenleme UI’si depodaki izinlerinizi yanıtlar. Önceki görüntüler, hedef depoda yazma izinleri olmayan katkıda bulunanlar için geçerlidir. GitHub, hesabınızda otomatik olarak hedef depo çatalı oluşturur. Hedef depoda yazma erişiminiz varsa, GitHub hedef depoda yeni bir dal oluşturur. Bu dalın adı **\<GitHubKimliği\>-düzeltmeeki-n** biçimindedir. GitHub kimliğiniz ve düzeltme eki dalı için bir sayısal tanımlayıcı kullanılır.

Hepimiz değişiklikler için PR’leri kullanıyoruz, yazma erişimi olan katkıda bulunanlar bile. Çoğu depoda, güncelleştirmelerin PR olarak gönderilmesi için `master` dal korumalıdır.

Tarayıcıda düzenleme deneyimi, ufak veya sık görülmeyen değişiklikler için idealdir. BBüyük katkılar yapıyor veya gelişmiş Git özellikleri (dallara ayırma yönetimi veya gelişmiş birleştirme çakışmasını çözümleme gibi) kullanıyorsanız [deponun çatalını oluşturup yerel olarak çalışmanız](how-to-write-workflows-major.md) gerekir.

## <a name="review-open-prs"></a>Açık PR’leri gözden geçirme

Açık PR’lere bakarsanız, yeni konuları yayımlanmadan önce okuyabilirsiniz. Gözden geçirmeler, [GitHub akış](https://guides.github.com/introduction/flow/) sürecini takip eder. Önerilen güncelleştirmeleri ve yeni makaleleri ortak depolarda görebilirsiniz. Bunları gözden geçirip yorumlarınızı ekleyin. Herhangi bir belge depomuza bakın ve ilginizi çeken alanlarda açık çekme isteklerini (PR’ler) kontrol edin. Önerilen güncelleştirmelerde topluluk geri bildirimi, tüm topluluğa yardımcı olur.

## <a name="create-quality-issues"></a>Kalite sorunları oluşturma

Belgelerimiz, devamlı olarak süren işlerdir. İyi sorunlar, topluluk için en önemli olan yerlere odaklanmamıza yardımcı olur. Ne kadar çok ayrıntı sağlayabilirseniz, sorun da o kadar yararlı olur. Hangi bilgileri aradığınızı bizimle paylaşın. Kullandığınız arama terimlerini de. Nereden başlayacağınızı bilmiyorsanız, bilmediğiniz bir teknolojiyi nasıl keşfetmek istediğinizi bizimle paylaşın.

Sorunlar, gerekli şeyler konusunda konuşma başlatır. İçerik ekibi, ekleyebileceğimiz şeylerle ilgili fikirlerini verir ve sizden de düşüncelerinizi ister. Bir taslak oluşturduğumuzda, [PR’yi incelemenizi](#review-open-prs) isteyeceğiz.

## <a name="get-more-involved"></a>Daha fazla katılım gösterin

Diğer konular, Microsoft Docs’a daha fazla katkıda bulunmaya başlamanıza yardımcı olacaktır. GitHub depoları, Markdown araçları ve Microsoft Docs platformunda kullanılan uzantılar; diğer konularda açıklanır.
