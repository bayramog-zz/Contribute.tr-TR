---
title: .NET belge çekme isteği gözden geçirme süreci
description: .NET belgelerinde PR birleştirme web kancaları etkin değildir. Bu makale, bu depolar için PR sürecini açıklar
ms.date: 01/04/2019
ms.openlocfilehash: f710e330e31e56887d43030290d5aa6a5c62961b
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653609"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a>.NET belge depoları için çekme isteği gözden geçirme süreci

Birçok depoda, önemsiz PR’leri otomatik olarak birleştiren PR Birleştirme web kancaları etkin değildir. Bu makale, bu depolar için PR gözden geçirme sürecini açıklar. PR gözden geçirme süreci, şu amaçlarla tasarlanmıştır:

1. Ekibimizin, ürün ekibi üyelerinin ve topluluk üyelerinin yüksek kaliteli içeriklerini yayımlayın.
1. Yazarlara her zaman zamanında ve eyleme dönüştürülebilir geri bildirim sağlamak.
1. Yazarlar ve gözden geçirenler arasındaki tartışmaları kolaylaştırmak.

Ekipler yeni fikirler ürettikçe ve platform geliştikçe bu süreçler de iyileşmeye devam etmektedir.

## <a name="reviewers"></a>Gözden Geçirenler

İçerik ekibi üyelerinden biri, tüm PR’leri inceler. İçerik ekibi üyeleri, teknik tutarlılığı doğrulamak adına belirli ürün ekibi üyelerinden gözden geçirme isteğinde bulunabilir. İçerik ekibi, GitHub’ın Kod Sahipliği özelliğini kullanarak içerik ekibi üyelerinden otomatik olarak gözden geçirme talep edebilir. Bu işlemin bir parçası olarak bir gözden geçiren, dahili PR’leri incelemeleri için diğer ekip üyelerini etiketleyebilir. Ekip üyeleri, ekiplerindeki üyelerden ve topluluk üyelerinden gelen gözden geçirme isteklerini aynı sırada görür.

Topluluk üyeleri de PR’leri gözden geçirip geri bildirim sağlayabilirler. Ancak bir PR birleştirilmeden önce, en az bir çekirdek içerik ekibi üyesi bu PR’yi onaylamalıdır.

## <a name="review-process"></a>Gözden geçirme süreci

Gözden geçirme süreci, PR’ye bağlı olarak şu üç yoldan birini izler:

- **Küçük PR’ler** - Küçük PR’ler tekli hata düzeltmeleri içerir: yazım hataları, bozuk bağlantılar, küçük kod değişiklikleri vb. değişiklikler.
- **Büyük katkılar** - Büyük katkılar; mevcut bir makalede yapılan büyük düzenlemeler, yeni makaleler veya birkaç makalede yapılan düzenlemelerdir.
- **Süren iş** - Yazarlar, başlıkta “[WIP]” etiketi kullanarak süreç devam ederken bir gözden geçirme isteyebilirler. “WIP” etiketi, “Work in Progress” yani “Süren İş” anlamına gelir. 

Katılımcı Lisans Sözleşmesi (CLA) botu tarafından kullanılan işleme, “küçük” ve “büyük” katkıları birbirinden ayırmak için güzel bir yönerge sağlar. CLA’nın imzalanmasını gerektirmeyen PR’ler büyük olasılıkla “küçük”tür. CLA gerektirenler ise büyük olasılıkla “büyük”tür.

### <a name="small-prs"></a>Küçük PR’ler

Küçük PR’lerdeki değişikliklerde doğruluk gözden geçirilir ve gözden geçirme sitesindeki derleme kullanılarak denetleme yapılır. Küçük oldukları için bu PR’ler, bütün makalenin gözden geçirilmesini tetiklemez. 

Gözden geçirenler, bir makaleyi iyileştirecek başka küçük değişiklikler fark edebilirler. Bu değişiklikler de küçükse, bunları gözden geçirme yorumları olarak önerebilirsiniz. Ancak değişiklikler daha büyük bir gözden geçirmeyi tetikleyecekse, bir sorun açın ve bunlarla daha sonra ilgilenin. 

### <a name="larger-changes"></a>Daha büyük değişiklikler

Daha büyük PR’ler, daha kapsamlı bir gözden geçirme sürecinden geçer. Aşağıdakilerin tümü denetlenir:

- Örnek kod PR’de, kaynakta ve indirilebilir bir zip dosyası olarak bulunmalıdır.
- Örnek kod hatasız bir şekilde sıkışmalı ve çalışmalıdır.
- Makale okuyucuya amaçlarını açık bir şekilde anlatmalı ve bu amaçlara ulaşmalıdır.
- Makale [stil ve dilbilgisi ilkelerini](dotnet-style-guide.md) yerine getirmekte ve [ifade ve üslup prensiplerimizi](dotnet-voice-tone.md) takip etmektedir.
- Tüm bağlantılar hatasız bir şekilde açılmalıdır.

İçerik ekibi PR’yi gözden geçirecek ve yorumlarla birlikte sonuçları gönderecektir. Yalnızca ufak değişiklikler istenmişse ekip üyeleri PR’yi geri bildirimle birlikte “onay”layabilir. Yazar daha sonra geri bildirimi inceleyip PR’yi birleştirebilir. Çoğu gözden geçirme, değişiklik isteğiyle sonuçlanır ve bu değişiklikler tamamlandığında gözden geçiren bir kez daha makaleyi gözden geçirir.

Düzenlemeler bir teknik gözden geçirme gerektiriyorsa, içerik ekibi gözden geçireni uygun ürün ekibi üyesinden bir gözden geçirme ister.

### <a name="review-wip-pull-requests"></a>Süren iş çekme isteklerini gözden geçirme

Yeni yazarlar, sürecin erken safhalarında geri bildirim isteyebilirler. Bunun için başlığa “[WIP]” etiketi ekleyerek bir PR açabilirler. Bir yorum ile erken gözden geçirme isteyebilirler.

Bu erken gözden geçirmeler, tam PR gözden geçirmesi kadar kapsamlı değildir. İçerik ekibi yorum yazar ancak GitHub’ın gözden geçirme özelliği ile “onay”lamaz veya “değişiklik iste”mez. Bu erken gözden geçirmeler, makalenin yapısına odaklanır: ana hat, genel içerik ve örnekler. Bu gözden geçirmede gramer ve bağlantılar ayrıntılı incelenmez.

## <a name="respond-to-reviews"></a>Gözden geçirmelere yanıt

Yazar, incelediği tüm yorumlara “+1” tepkisi ile yanıt vererek bunları incelediğini belirtir ve PR’yi böylece güncelleştirir. Yazar, yoruma katılmıyorsa veya yorumu farklı bir şekilde ele alıyorsa; yaptığı değişikliği açıklayan bir yorum ekler.

Yazar @-mentions, bir yorum ile asıl gözden geçiren kişiden yeni bir gözden geçirme ister. 

## <a name="response-time-expectations"></a>Tahmini yanıt süresi

İçerik ekibi üyeleri yeni PR’leri genellikle iki iş günü içerisinde gözden geçirir. Gözden geçirme daha uzun sürecekse ekip üyelerinden biri PR’yi gözden geçirdiklerini ve tahmini yanıt süresini belirtmek için bir yorum ekler.

Bir gözden geçirme gönderildikten sonra yazarlar, yorumlara en fazla bir hafta içerisinde yanıt vermelidir. Gönüllüler başka işleri olduğundan dolayı her zaman bu beklentileri karşılayamayabilirler. Böyle bir durumda ekip üyeleri, topluluk yazarına PR’yi güncelleştirip güncelleştiremeyeceğini sorar. Yazar olumsuz dönüş yaparsa ekip üyesi PR’yi onun için güncelleştirir ve birleştirir.
