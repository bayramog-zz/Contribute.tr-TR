---
title: Küçük veya seyrek görülen değişiklikler için GitHub katkı iş akışı
description: Bu makale, docs.microsoft.com makalelerine katkı sağlamak için “küçük” katkı iş akışını nasıl kullanacağınızı gösterir.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a>Küçük veya seyrek görülen değişiklikler için GitHub katkı iş akışı

> [!IMPORTANT]
> Docs.microsoft.com’da yayın yapan tüm depolar [Microsoft Açık Kaynak Kullanım Şartları](https://opensource.microsoft.com/codeofconduct/)’na veya [.NET Foundation Kullanım Şartları](https://dotnetfoundation.org/code-of-conduct)'na tabidir. Daha fazla bilgi için bkz. [Kullanım Kuralları SSS](https://opensource.microsoft.com/codeofconduct/faq/). İsterseniz, soru ya da yorumlarınız için [opencode@microsoft.com](mailto:opencode@microsoft.com) veya [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) ile de iletişim kurabilirsiniz.<br>
>
> Belgelerde yapılan küçük düzeltmeler ve açıklamalar ile ortak depolardaki kod örnekleri, [docs.microsoft.com Kullanım Koşulları](https://docs.microsoft.com/legal/termsofuse)’nda anlatılmıştır. Bir Microsoft çalışanı değilseniz çekme isteğinde yeni veya önemli değişiklikler, çevrimiçi bir Katılım Lisans Sözleşmesi (CLA) göndermenizi isteyen bir yorum oluşturur. Çekme isteğiniz kabul edilmeden önce bu çevrimiçi formu doldurmanız gerekir.

## <a name="overview"></a>Genel Bakış

Bu iş akışı, GitHub’ın web tabanlı markdown düzenleyicisini kullanarak küçük veya seyrek görülen değişiklikler yapmak için uygundur. Yapabilecekleriniz açısından GitHub düzenleyicisi sınırlıdır, çünkü bu düzenleyicinin kullanıcı arabirimi tüm Git işlemlerini ve yazma senaryolarınızı desteklemez. Büyük katkılar yapmanız gerekiyorsa veya gelişmiş Git özellikleri (dallara ayırma yönetimi veya gelişmiş birleştirme çakışmasını çözümleme gibi) konusunda desteğe ihtiyacınız varsa [büyük veya uzun ömürlü değişiklikler iş akışına](full-workflow.md) başvurun.

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a>Değişikliklerinizi sunmak için GitHub düzenleyicisini kullanma yordamı

1. Makalenin ilgili GitHub deposu ve Markdown dosyasına göz atın. Aşağıdaki yöntemlerden birini kullanabilirsiniz:

   - İlgili GitHub deposundaki Markdown dosyalarına göz atarak makaleyi bulun.
   - [docs.microsoft.com](https://docs.microsoft.com/) adresindeki makaleye gidin ve sayfanın sağ üst köşesindeki **Düzenle** bağlantısını seçin.

     ![Düzenle bağlantısının konumu](./media/light-workflow/contributetogit.png)

2. Kalem şeklindeki **Bu dosyayı düzenle** simgesini seçerek düzenleme moduna geçin:

    ![Kalem simgesinin konumu](./media/light-workflow/editicon.png)

3. Markdown kullanarak **Dosya düzenle** sekmesinde değişiklikler yapın ve **Değişiklik önizlemesi** sekmesinde bunların önizlemesini görün. Düzenleyiciyi kullanmak zor değildir ancak yine de yardıma ihtiyacınız olursa şu kılavuzlara bakın:

   - [Markdown’ı Kullanma](how-to-write-use-markdown.md)
   - [GitHub’da dosya oluşturma](https://github.com/blog/1327-creating-files-on-github)
   - [Depolarınıza dosya yükleme](https://github.com/blog/2105-upload-files-to-your-repositories)

4. Sayfanın sonuna kadar kaydırdığınızda aşağıdakilerden birini görürsünüz:

   - **Dosya değişikliği öner**: [Başka bir kullanıcının deposunda dosya düzenleme](https://help.github.com/articles/editing-files-in-another-user-s-repository/) işleminde olduğu gibi depoda salt okunur izinleriniz olduğunda görüntülenir. Bu durumda GitHub, depo çatalınızda bir “düzeltme” dalı oluşturur (çatal yoksa otomatik olarak bir çatal oluşturur). **Dosya değişikliği öner**’i seçtikten sonra değişikliklerinizi doğrulayabilmeniz için **Değişiklikleri karşılaştırma** sayfası görüntülenir. Daha sonra değişikliklerinizi çekme isteği sırasına göndermek için **Çekme isteği oluştur** düğmesini seçip [sonraki bölüme](#pull-request-processing) ilerleyin.

   - **Değişiklikleri işle**: [Kendi deponuzda dosya düzenleme](https://help.github.com/articles/editing-files-in-your-repository/) işleminde olduğu gibi depoda yazma izinleriniz olduğunda görüntülenir. Bu durumda, değişikliklerinizi kaydetmeniz için GitHub size iki seçenek sunar:

     - **Doğrudan `<branch-name>` dalına işleme**, burada `<branch-name>`, **Düzenle** düğmesini seçtiğinizde çalışıyor olduğunuz dalın adıdır. Bu, çekme isteği kullanmak yerine değişikliklerinizi doğrudan dala uygular. Bu noktada işiniz bitmiştir!

     - **Bu işleme için yeni bir dal oluştur ve çekme isteği başlat**: Yeni bir dal oluşturmak için varsayılan bir adla istem yapar. **Dosya değişikliği öner**’i seçtikten sonra değişikliklerinizi doğrulayabilmeniz için **Değişiklikleri karşılaştırma** sayfası görüntülenir. Daha sonra değişikliklerinizi çekme isteği sırasına göndermek için **Çekme isteği oluştur** düğmesini seçip [sonraki bölüme](#pull-request-processing) ilerleyin.

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Sonraki adımlar

- Markdown, Markdown uzantıları söz dizimi ve daha fazlası hakkında bilgi almak için “Yazma temel bilgileri” makalesine gidin.
