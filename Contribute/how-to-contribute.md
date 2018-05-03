---
title: docs.microsoft.com’a katkıda bulunma
description: Bu makale, docs.microsoft.com’a içerik ekleyebilmenin farklı yollarını açıklar.
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 01/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: bc6f9c314eda5f0d950da049374a7a157f16782a
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2018
---
# <a name="how-to-contribute-to-docsmicrosoftcom"></a>docs.microsoft.com’a katkıda bulunma

[docs.microsoft.com](https://docs.microsoft.com)’u oluşturan içeriği iyileştirmeye katkıda bulunmanın birkaç yolu vardır:

- Yeni makaleler oluşturmak için [sorun konu başlıkları oluşturabilirsiniz](#create-issues) veya mevcut makaleleri iyileştirebilirsiniz.
- GitHub çevrimiçi düzenleyicisinde küçük değişiklikler yapmak için makaleleri [hızlı bir şekilde düzenleyebilirsiniz](#quick-edits).
- Kalite ve teknik doğruluktan emin olmak için [yeni makalelerin taslaklarını inceleyebilirsiniz](#review-new-articles).
- İçerik hikayesini öne çıkarmak istediğiniz konu başlıkları için [yeni makaleler oluşturabilirsiniz](#create-new-articles).
- Önemli kavramları güçlendiren kod örneklerini geliştirmek için örnekleri [güncelleştirebilir](#update-samples) veya [oluşturabilirsiniz](#create-samples).

Bu makalede; katkıda bulunmanın farklı yollarını öğrenecek, bu görevlerin her birini nasıl yerine getireceğinizi görecek ve bu görevler hakkında daha fazla bilgi için nereye bakmanız gerektiğini bulacaksınız.

Ortak depolarımız [GitHub](https://wwww.GitHub.com)’da barındırılır.  Belge depolarımıza katılmak için GitHub’da bir hesap oluşturmanız gerekecektir.

Belgeleri güncelleştirmek için bir metin düzenleyicisi de gerekecektir. [Visual Studio Code](https://www.visualstudio.com/code)’u öneririz. [Markdown](https://daringfireball.net/projects/markdown/syntax) söz dizimine dair temel bir anlayışınızın olması gerekir.

Örnek ekliyor veya değiştiriyorsanız bir geliştirme ortamına gereksinim duyacaksınız. Tüm platformlar için [Visual Studio Code](https://www.visualstudio.com/code)’u öneririz ancak bilgisayar ve Mac’te [Visual Studio](https://www.visualstudio.com)’yu da kullanabilirsiniz.

## <a name="create-issues"></a>Sorun konu başlığı oluşturma

Bir makalede eksik veya yanlışlıkları fark ederseniz, bu makale için bir sorun konu başlığı oluşturun. Doğru konumu bulmanın en kolay yolu tarayıcınızdaki “Düzenle” düğmesine tıklamaktır, böylece doğru ortak GitHub deposundaki makale kaynağına yönlendirilirsiniz. Burada, adres çubuğunuzdan makale kaynağının URL’sini alabilirsiniz. Makale hakkında yeni bir sorun konu başlığı oluşturmak için “Sorun Oluştur”a tıklayın.

> [!NOTE]
> Harf hataları veya gramer sorunları gibi küçük düzenlemelerle çözebileceğiniz sorunlar bulursanız, hem kendinizin hem de bizim vaktimizi almamak adına kaynağı düzenlemek için tarayıcıyı kullanarak [çözümü gönderebilirsiniz](#quick-edits).

Çoğu ortak depomuz, sorunu çözmek için gereken bilgileri sağlamanıza yardımcı olacak yeni sorun konu başlığı şablonları barındırır.

İhtiyacınız olan bilgileri bulamazsanız yeni sorun konu başlıkları da ekleyebilirsiniz. Süreç aynıdır: ortak belge depolarından birinde yeni bir sorun konu başlığı oluşturun. Neyi aradığınızı, ne yapmak istediğinizi ve bulduğunuz makalelerin size neden istediğiniz gibi yardımcı olamadığını bize anlatın.

## <a name="review-new-articles"></a>Yeni makaleleri gözden geçirme

Yeni, belki CTP veya beta yazılımlar üzerinde çalışıyorsanız, siz bu teknoloji keşfederken biz büyük ihtimalle belgeleri derliyor oluruz. Üzerinde çalışılan belgeleri ortak depolarımızda bulabilirsiniz. Belgeleri yayınlanmadan önce iyileştirmek için yorumlarınız varsa bunları paylaşabilirsiniz.

Yeni makaleler, [GitHub akış](https://guides.github.com/introduction/flow/) işlemi ile herkes tarafından gözden geçirilebilir. Herhangi bir belge depomuza bakın ve açık çekme isteklerini (PR’ler) kontrol edin. Tüm açık çekme istekleri yorum ve görüşlerinize açıktır. Bu yolla, daha sonra gelecek geri bildirimleri beklemek yerine ilk yayımda daha iyi içerikler paylaşabiliyoruz.

Teknik doğruluğu, açıklamaların netliğini ve doğru gramer kullanımını artırmanın yollarını arıyoruz.

## <a name="quick-edits"></a>Hızlı düzenlemeler

Hızlı düzenlemeler, tarayıcı tabanlı düzenleyici kullanarak küçük düzeltmeler yapmanın bir yoludur. Ufak tefek harf veya gramer hataları ya da yanlış adlandırılmış API’ler görürseniz, bir sorun başlığı açmak yerine düzenlemeyi yapıp bir PR gönderebilirsiniz.

Makalelerde “Düzenle” düğmesine (genellikle sayfanın sağ üst taraflarında bulunur) tıklayın, düzenlemelerinizi yapın ve sayfanın sonundaki “PR Yolla” düğmesine tıklayın. Günlük PR incelememizi yaparken bu PR’yi de inceleyip birleştireceğiz.

## <a name="create-new-articles"></a>Yeni makale oluşturma

İlgilendiğiniz kavramlar varsa ve bunları başkalarına açıklamak isterseniz, bu konularda makaleler oluşturup PR yollayabilirsiniz.

Yeni makaleler oluşturmak çok zaman alan bir süreçtir ve bizler sizin zamanınıza ve katkılarınıza önem veriyoruz. Sürecin başından itibaren buna dahil olarak kılavuz ilkelerimizi ve stilimizi takip ettiğinizden emin olmak istiyoruz. Aşağıdaki adımları öneriyoruz:

1. Neyin eksik olduğunu ve bunu nasıl çözeceğinizi açıklayan [bir sorun konu başlığı oluşturun](#create-issues).
1. Sorun hakkındaki yorumlarınızı yazın ve bize makale için bir taslak ve özet sağlayarak bu konuda çalışmak istediğinizi belirtin.
1. Size önerilerimizi içeren bir yanıt vereceğiz. Bu öneriler ilgili makale bağlantıları, örnek için öneriler veya makalenin nasıl düzenleneceği ile ilgili olabilir.
1. Taslak üzerinde anlaştıktan sonra deponun çatalını oluşturun ve çalışmaya başlayın.
1. Sürecin erken aşamalarındayken bir PR açın ve başlığının önüne “[WIP]” ekleyin.
1. Çekirdek katkıda bulunanlardan biri size ilk geri bildirimi sağlayacaktır.
1. Yazmaya devam edin ve tekrar geri bildirime ihtiyaç duyduğunuzda ilk taslağı gözden geçiren kişiye @-mention yapın.
1. Son gözden geçirme için hazır olduğunuzda “[WIP]” ibaresini kaldırın.
1. Geri bildirime yanıt
1. Çekirdek katkıda bulunanlar, PR’nizi birleştirecektir.

Bu listede ayrıntısına girmeye değer birkaç nokta var. Genellikle [GitHub akış](https://guides.github.com/introduction/flow/) işlemini kullanarak içerikleri olabildiğince erken gözden geçirmeye çalışıyoruz. Böylelikle bir makalenin içerik tablosunda nerede bulunacağına, yeni makaleden okuyucuların ne kazanacağına ve oluşturacağınız örneklerin kapsamına karar veriyoruz. Gerekli düzeltmeleri erkenden, siz makaleyi yazmaya uzun süreler harcamadan önce yapabiliyoruz.

## <a name="update-samples"></a>Örnek güncelleştirme

Bazı örnekler birkaç yayın önce yazılmış ve artık önerilmeyen uygulamaları içeriyor olabilir. Bu örnekleri güncelleştirmemize yardım etmek isteyebilirsiniz. Öte yandan değişken adında yapılan basit bir değişiklikle açıklamanın daha netleştirilebileceğini de fark edebilirsiniz.

Tüm makalelerde görüntülenen örnek kodlar, CI sistemimiz ile derlenmiş ve genellikle yine bununla test edilmiş programların bir parçasıdır.

Küçük güncelleştirmeler yapmak için uygun depoda kaynağı bulup tarayıcıda kod değişikliği yapmanız ve bir PR göndermeniz gerekir. CI sistemimiz değişiklikleri derler ve bu işlem bittiğinde PR’yi birleştiririz.

Daha büyük ölçekli değişiklikler için deponun çatalını oluşturun ve dilediğiniz geliştirme ortamında değişikliklerinizi uygulayın. Bu değişikliklerin sizin istediğiniz şekilde uygulandığından emin olmak için birkaç test eklemeyi unutmayın. Bir PR gönderin, biz de bunu inceleyelim.

Tüm kod değişikliklerinde, değiştirdiğiniz koddaki mevcut kod kurallarını izleyin. Örnek depolarında kod standartlarımız, ilgili ürün ekiplerimizin standartlarını yansıtır. Depoya özel kılavuz için her bir depoyu kontrol edin.

> [!NOTE]
> Biz de bu kılavuzu uygulama konusunda çalışıyoruz. Örneklerden bazıları mevcut standartlarımızdan daha eski ve hala güncelleştirilmemiş. Tüm çalışan örnek kodların, çalışan ve test edilmiş örneklerden görüntülenmesine yönelik bir amacımız var.

## <a name="create-samples"></a>Örnek oluşturma

Kavram veya senaryoları gösteren yeni örnekler de oluşturabilirsiniz. Tüm örneklerin yanında, örnekteki anahtar bilgileri açıklayan bir makale bulunmalıdır.

Örneğiniz mevcut bir makaleyi tamamlayıcı nitelikteyse, bu makalede bu örnek için bir başvuru ekleyin. Değilse de bu örneğe eşlik edecek [makaleyi yazmak](#create-new-articles) üzere bizimle birlikte çalışın.

Örnek kodumuz her zaman ilgili ürün ekipleri tarafından kullanılan kodlama kurallarını izler. Fakat bunun bir istisnası vardır: Makalenin içinde örtük olarak belirtilen değişkenler (`var` ile belirtilir) varsa, genellikle bunlar yerine açık olarak belirtilen değişkenleri tercih ediyoruz.

Yukarıdaki [yeni makaleler](#create-new-articles) kısmında anlatılan örnek sürecini izleyin, böylece geliştirme sürecinin başlarındayken kodu gözden geçirebiliriz.
