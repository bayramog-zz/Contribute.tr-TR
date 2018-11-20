---
title: .NET belgelerine yapılan katkılara yönelik üslup ve ton yönergeleri
description: Stilimize yönelik örneklerin yönergelerimize uymayan örneklerle karşılaştırılması ile üslup ve ton yönergelerimizi öğrenin.
ms.date: 11/07/2018
ms.openlocfilehash: cf78bb5d476d35b9b168b619e90e8f372103cb93
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609705"
---
# <a name="voice-and-tone-guidelines"></a>Üslup ve ton yönergeleri

BT uzmanları ve geliştiriciler dahil olmak üzere geniş bir kitle, .NET yazılımını öğrenmek ve bunu kendi işlerinde kullanmak için belgelerinizi okumaktadır. Amacınız, kullanıcıya bu doğrultuda yardımcı olacak mükemmel belgeler oluşturmaktır. Yönergelerimiz size bu konuda yardımcı olur. Stil kılavuzumuzda aşağıdaki öneriler yer almaktadır:

Bu stil kılavuzunu okurken sunulan önerilerin her birine dair örnekler göreceksiniz. Yönergelerimizi yansıtan bu kılavuzu, .NET için belge oluştururken başvurabileceğiniz örnekler sunmak amacıyla oluşturduk. Yönergelerimizi izlemediğiniz takdirde makalelerin nasıl görüneceğini görmeniz için hatalı örnekleri de kılavuza dahil ettik.

## <a name="use-a-conversational-tone"></a>Konuşma tonu kullanma

### <a name="appropriate-style"></a>Uygun stil

Belgelerimizin konuşma tonunda olmasını istiyoruz. Öğreticilerimizden veya açıklamalarımızdan birini okurken, yazarla muhabbet ediyormuş gibi hissetmelisiniz. Sizin için bu deneyim resmi olmamalı, konuşma havasında ve bilgi verici olmalıdır. Okuyucular, makaleyi yazan kişinin kavramları açıklamasını dinliyor gibi hissetmelidir.

### <a name="inappropriate-style"></a>Uygun olmayan stil

Teknik hususların konuşma stili ile ifadesi ve akademik olarak ele alınması arasındaki fark büyüktür. Bu kaynaklar da oldukça kullanışlı olmakla birlikte bu tür makalelerin yazar tarafından ele alınış şekli, belgelerimizde olmasını istediğimiz stilden çok uzaktır. Akademik bir dergiyi okurken çok farklı bir ton ve çok farklı bir yazılış stili göze çarpar. Okuyucu, sıkıcı bir konunun sıkıcı bir açıklamasını okuyor gibi hisseder.  

Yukarıdaki ilk paragraf, önerdiğimiz konuşma stilini yansıtmaktadır. İkincisi ise akademik stile daha yakındır. Aralarındaki farkı kolaylıkla görebilirsiniz. 

## <a name="write-in-second-person"></a>İkinci şahıs kullanımı

### <a name="appropriate-style"></a>Uygun stil

Makalelerinizi, doğrudan okuyucuyla konuşuyormuş gibi yazmalısınız. Sıklıkla ikinci şahsa yönelik ifadeler kullanmalısınız (tıpkı benim bu iki cümlede yaptığım gibi). İkinci şahıs, yalnızca “siz” sözcüğünü kullanmak demek değildir. Doğrudan okuyucuya yazın. Emir cümleleri yazın. Okuyucunuza ne öğrenmesini istediğinizi anlatın.

### <a name="inappropriate-style"></a>Uygun olmayan stil

Bir yazar, üçüncü şahsı kullanarak da yazmayı seçebilir. Bu durumda yazar, kullanıcıya hitap ederken kullanacak bir zamir veya isim bulmak zorunda kalır. Okuyucular bu üçüncü şahıs stilini genellikle pek cazip ve keyifli bulmazlar.

İlk paragraf, önerdiğimiz stili yansıtmaktadır. İkincisi ise üçüncü şahıs kullanmaktadır. Lütfen ikinci şahıs kullanarak yazın. İlk paragrafı muhtemelen daha kolaylıkla okudunuz.

## <a name="use-active-voice"></a>Etken çatı kullanımı

Makalelerinizi etken çatı kullanarak yazın. Etken çatı, cümlede eylemi (fiili) gerçekleştirenin özne olması anlamına gelir. Bunun zıttı edilgen çatıdır. Bu cümleler, özneyi eylemsiz kılacak şekilde oluşturulur. Şu iki örneği karşılaştırın:

>Derleyici, kaynak kodunu yürütülebilir bir dosyaya dönüştürdü.

>Kaynak kodu, derleyici tarafından yürütülebilir bir dosyaya dönüştürüldü.

İlk cümlede etken çatı kullanılmıştır. İkinci cümle ise edilgen çatıyla yazılmıştır. (Bu iki cümle de bu çatılara birer örnektir.)

Daha kolaylıkla okunduğundan, etken çatıyı öneriyoruz. Edilgen çatıyı okumak biraz daha zor olabilir.

## <a name="target-a-fifth-grade-reading-level"></a>Beşinci derece okuma düzeyini hedefleme

Bu son yönergeyi, pek çok okuyucumuzun ana dili İngilizce olmadığı için sağlıyoruz. Makaleleriniz, uluslararası bir kitleye ulaşıyor. Bazılarının sizin sahip olduğunuz İngilizce kelime bilgisine sahip olmayabileceğini lütfen unutmayın.

Bununla birlikte, yine de teknik uzmanlara yönelik makaleler yazıyorsunuz. Okuyucularınızın programlama bilgisine ve programlamayla ilgili kelime haznesine sahip olduğunu varsayabilirsiniz. Nesneye Dayalı Programlama, Sınıf, Nesne, İşlev ve Metot gibi terimlere okuyucular aşinadır. Ancak makalelerinizi okuyan herkesin bilgisayar bilimiyle ilgili resmi bir diploması olmayabilir. “Bir kez etkili” gibi terimleri kullanırken açıklama yapmanız gerekebilir:

>`Close()` metodu bir kez etkilidir, yani metoda birden fazla çağrı yapsanız bile metot, bir kez çağrı yapmış gibi etki gösterir.

## <a name="avoid-future-tense"></a>Gelecek zaman kullanımından kaçınma

Bazı dillerde gelecek zaman kullanımı İngilizceyle aynı değildir. Gelecek zaman belgelerinizin okunmasını zorlaştırabilir. Ayrıca gelecek zaman kullanıldığında “Ne zaman?” sorusu ortaya çıkar. “PowerShell’i öğrenmek sizin için faydalı olacaktır” dediğinizde okuyucu doğal olarak bunun ne zaman faydalı olacağını merak eder. Bunun yerine sadece “PowerShell’i öğrenmek sizin için faydalıdır” deyin.

## <a name="what-is-it---so-what"></a>Bu nedir - Bu ne anlama geliyor?

Okuyucuya yeni bir kavram sunduğunuzda önce kavramı tanımlayın, bunun neden kullanışlı olduğunu ise daha sonra açıklayın. Okuyucunun bir şeyin faydalarından önce onun ne olduğunu anlaması önemlidir.
