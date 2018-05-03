---
title: Büyük veya uzun ömürlü değişiklikler için GitHub katkı iş akışı
description: Bu makale, docs.microsoft.com makalelerine katkı sağlamak için “büyük” katkı iş akışını nasıl kullanacağınızı gösterir.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 08/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: a43e9a8274c430b1eeed796fc74085c2248f1c14
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>Büyük veya uzun ömürlü değişiklikler için GitHub katkı iş akışı

> [!IMPORTANT]
> Docs.microsoft.com’da yayın yapan tüm depolar [Microsoft Açık Kaynak Kullanım Şartları](https://opensource.microsoft.com/codeofconduct/)’na veya [.NET Foundation Kullanım Şartları](https://dotnetfoundation.org/code-of-conduct)'na tabidir. Daha fazla bilgi için bkz. [Kullanım Kuralları SSS](https://opensource.microsoft.com/codeofconduct/faq/). İsterseniz, soru ya da yorumlarınız için [opencode@microsoft.com](mailto:opencode@microsoft.com) veya [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) ile de iletişim kurabilirsiniz.<br>
>
> Belgelerde yapılan küçük düzeltmeler ve açıklamalar ile ortak depolardaki kod örnekleri, [docs.microsoft.com Kullanım Koşulları](https://docs.microsoft.com/legal/termsofuse)’nda anlatılmıştır. Bir Microsoft çalışanı değilseniz çekme isteğinde yeni veya önemli değişiklikler, çevrimiçi bir Katılım Lisans Sözleşmesi (CLA) göndermenizi isteyen bir yorum oluşturur. Çekme isteğiniz birleştirilmeden önce bu çevrimiçi formu doldurmanız gerekir.

## <a name="overview"></a>Genel Bakış

Bu iş akışı, büyük bir değişiklik yapması gereken veya depoya sık sık katkıda bulunacak olan kişiler için uygundur. Sık katkıda bulunanlar genellikle devam eden (uzun ömürlü) değişiklikler yapar. Bunlar, çekme isteğinin oturum kapatması ve birleştirmesinden önce birden çok derleme/doğrulama/hazırlama döngüsünden geçer veya birkaç gün sürer.

Ortak ve özel depoları kullanan projelerde çalışan Microsoft çalışanları için bu tür katkıları özel depoya yapmak da önemlidir. Özel depoda tümleşik OPS derleme, doğrulama ve hazırlama hizmetleri kullanılabilir.

Bu tür katkılar arasında şunlar vardır:

[!INCLUDE[contribute-how-to-write-workflows-major-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>Terminoloji

Başlamadan önce, bu iş akışında kullanılan bazı Git/GitHub terimleri ve bilinen adlarına göz atalım. Bunları henüz anlayamazsanız endişeye kapılmayın. Zamanla hepsini öğreneceksiniz, ayrıca bir tanımdan emin olamadığınızda her zaman bu bölüme geri dönebilirsiniz.

| Ad | Açıklama |
|-----------|-------------|
|çatal|Normalde, bir ana GitHub deposunun kopyasını ifade eden isim olarak kullanılır. Pratikte, bir çatal aslında sadece başka bir depoyu ifade eder. Ancak özelliği, GitHub’ın bu çatal ile ana/üst depo arasında bir bağlantı bulundurmasıdır. Bazen eylem içerisinde kullanılır, örneğin “Önce deponun çatalını oluşturmanız gerekir.”|
|uzak öğe|Bir uzak depoyla yapılan ve “başlangıç” veya “yukarı akış” uzak öğesi gibi bir adı olan bağlantı. Git, bunlara uzak öğeler adını verir çünkü bunlar, başka bilgisayarda barındırılan bir depoya başvururken kullanılır. Bu iş akışında uzak öğe her zaman bir GitHub deposudur.|
|başlangıç|Yerel deponuz ve bunun kopyalandığı depo arasındaki bağlantıya atanan ad. Bu iş akışında başlangıç, çatalınızla olan bağlantıyı ifade eder. Bu, bazen başlangıç deposunun bilinen adı olarak kullanılır, örneğin: “Değişikliklerinizi başlangıca göndermeyi unutmayın.”|
|yukarı akış|Başlangıç uzak öğesine benzer şekilde yukarı akış, başka bir depoyla yapılan bağlantının adıdır. Bu iş akışında yukarı akış, yerel deponuz ile çatalınızın oluşturulduğu ana depo arasındaki bağlantıyı ifade eder. Bu, bazen yukarı akış deposunun bilinen adı olarak kullanılır, örneğin: “Değişikliklerinizi yukarı akıştan almayı unutmayın.”|

## <a name="workflow"></a>İş akışı

>[!IMPORTANT]
> Daha önce tamamlamadıysanız [Kurulum](get-started-setup-github.md) bölümündeki adımları tamamlamanız gerekir. Bu bölüm GitHub hesabınızı ayarlarken, Git Bash ve bir Markdown düzenleyicisi yüklerken, çatal oluştururken ve yerel deponuzu ayarlarken size yol gösterir. Depo veya dal gibi Git ve GitHub kavramlarına aşina değilseniz lütfen önce [Git ve GitHub temel öğelerine](git-github-fundamentals.md) göz atın.

Bu iş akışında değişiklikler, tekrar eden bir döngü içerisinde akar. Siz diğer katkıda bulunanların yaptıkları değişiklikleri ekledikçe cihazınızın yerel deposundan başlayarak GitHub çatalınıza, GitHub deposuna ve tekrar yerel depoya akar.

### <a name="use-github-flow"></a>GitHub akışını kullanma

[Git ve GitHub temel öğeleri](git-github-fundamentals.md#git) bölümünden hatırlayacağınız gibi Git depoları bir ana dalın yanında bu dalla tümleştirilmemiş ek süren iş dallarını da içerir. Mantıksal olarak ilişkili bir değişiklikler kümesi eklediğinizde, iş akışında değişikliklerinizi yönetmek için bir *çalışma dalı* oluşturmak en iyi uygulamadır. Değişiklikleri tekrar ana dal ile tümleştirilebilir hale gelene kadar yineleme/geliştirmeye imkan veren bir çalışma alanı olması nedeniyle buna çalışma dalı diyoruz.

Birbiriyle alakalı değişiklikleri diğerlerinden ayırarak belirli bir dalda toplamak, bu değişiklikleri bağımsız olarak denetlemenize ve tanıtmanıza, dolayısıyla yayımlama döngüsünde hedeflediğiniz bir zamanda yayımlamanıza yardımcı olur. Yaptığınız iş türüne bağlı olarak, deponuzda birkaç çalışma dalını kolayca oluşturabilirsiniz. Her biri farklı bir projeyi temsil eden birden çok dalda aynı anda çalışmak yaygın görülen bir durumdur.

>[!TIP]
>Değişiklikleri ana dalınızda yapmak iyi bir uygulama *değildir*. Zamanlanmış özellik yayını için bir grup değişiklik yapmak üzere ana dalınızı kullandığınızı düşünün. Değişiklikleri tamamladınız ve yayımlamayı bekliyorsunuz. O sırada bir şeyi acil olarak düzeltmeniz isteniyor ve bu nedenle değişiklikleri ana daldaki bir dosyaya yapıp yayımlıyorsunuz. Bu örnekte, düzeltmeleri *ve* belirli bir tarihte yayımlanmak üzere sakladığınız değişiklikleri istemeden birlikte yayımlarsınız.

Şimdi yerel deponuzda yeni bir çalışma dalı oluşturalım ve önerdiğiniz değişiklikleri saklayalım. Her git istemcisi farklıdır, dolayısıyla tercih ettiğiniz istemcinin yardımına başvurun. GitHub Kılavuzu'nda [GitHub akışı](https://guides.github.com/introduction/flow/) işlemine genel bir bakış bulabilirsiniz.

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Sonraki adımlar
İşte bu kadar! Docs.microsoft.com içeriğine katkıda bulundunuz!

- Markdown, Markdown uzantıları söz dizimi ve daha fazlası gibi konular hakkında ayrıntılar için “Yazma temel bilgileri” bölümüne gidin.
