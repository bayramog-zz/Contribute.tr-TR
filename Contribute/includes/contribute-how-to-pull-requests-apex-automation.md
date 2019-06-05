---
ms.openlocfilehash: b64e8dd4c62ca05b6e04ef404ebf98a618d0171e
ms.sourcegitcommit: 2563918217ba0760a4f3877af2272a0a4b2c3052
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66391283"
---
Yorum otomasyonu, okuma düzeyindeki kullanıcıların (bir depo içinde yazma izinlerine sahip olmayan kullanıcılar) bir çekme isteğine uygun etiketi atayarak yazma düzeyinde eylem gerçekleştirmesine olanak tanır. Yorum otomasyonunun uygulandığı bir depoda çalışıyorsanız etiket atamak, etiketleri değiştirmek veya bir çekme isteğini kapatmak için aşağıdaki tabloda listelenen diyez etiketi yorumlarını kullanın. Yazarı olduğunuz makaleler için değişiklikler önerildiğinde, ortak depo PR’lerinin gözden geçirilmesi ve onaylanması için Microsoft çalışanlarına da e-posta ile bildirim gönderilir.

| Diyez etiketi açıklaması | Ne yapar | Depo kullanılabilirliği |
| --- | --- | --- |
| `#sign-off` |Bir makalenin yazarı yorum akışına `#sign-off` yorumunu yazdığında, **ready-to-merge** etiketi atanır. Bu etiket, depodaki gözden geçirenlerin, bir çekme isteğinin gözden geçirilmeye/birleştirilmeye ne zaman hazır olduğunu bilmesini sağlar. <br/><br/> Listelenen yazar *olmayan* bir katkıda bulunan `#sign-off` yorumunu kullanarak bir genel depo çekme isteğini onaylamaya çalışırsa, çekme isteğine yalnızca yazarın etiketi atayabileceğini belirten bir ileti yazılır. |Genel ve özel |
| `#hold-off` |Yazarlar fikirlerini değiştirmeleri veya hata yapmaları durumunda **ready-to-merge** etiketini kaldırmak için PR yorumuna `#hold-off` yazabilir. Özel bir depoda bu yorum **do-not-merge** etiketini atar. |Genel ve özel |
| `#please-close` |Yazarlar değişikliklerin birleştirilmemesine karar verirse çekme isteğini kapatmak için yorum akışına `#please-close` yazabilir. |Genel |
