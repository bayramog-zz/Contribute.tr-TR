## <a name="pull-request-processing"></a>Çekme isteği işleme

Önceki bölümdeki adım adım kılavuzda, önerilen değişiklikleri, hedef deponun çekme isteği kuyruğuna eklenen yeni bir çekme isteği halinde paketleyerek gönderme işleminin adımlarını uyguladınız. Çekme isteği, çalışma dalınızdaki değişikliklerin çekilmesini ve başka bir dalla birleştirilmesini isteyerek GitHub'ın işbirliği modelini uygular. Çoğu durumda diğer dal, ana depodaki varsayılan/ana daldır.

### <a name="validation"></a>Doğrulama

Çekme isteğinizin hedef dalıyla birleştirilebilmesi için, öncelikle bir veya daha fazla çekme isteği doğrulama işleminden geçmesi gerekebilir. Doğrulama işlemleri, önerilen değişikliklerin kapsamına ve hedef deponun kurallarına göre değişiklik gösterebilir. Çekme isteğiniz gönderildikten sonra, aşağıdakilerin biri veya daha fazlası gerçekleşebilir:

- **Birleştirilebilirlik**: Öncelikle dalınızdaki önerilen değişikliklerin hedef dalla çakışmadığını doğrulamak için temel bir GitHub birleştirilebilirlik testi gerçekleştirilir. Çekme isteği bu testin başarısız olduğunu belirtirse, işlemin devam edebilmesi için birleştirme çakışmasına neden olan içerikleri mutabık kılmanız gerekir.
- **CLA**: Ortak bir depoya katkıda bulunuyorsanız ve Microsoft çalışanı değilseniz önerilen değişikliklerin ölçeğine bağlı olarak, ilgili depoya ilk kez çekme isteği gönderdiğinizde kısa bir Katılım Lisans Sözleşmesi (CLA) formu doldurmanız istenebilir. CLA adımı tamamlandıktan sonra çekme isteğiniz işlenir.
- **Etiketleme**: Doğrulama iş akışı boyunca çekme isteğinizin ilerleme durumunun belirtilmesi için çekme isteğinize otomatik etiketler uygulanır. Örneğin, çekme isteğinin doğrulama, gözden geçirme ve kabul aşamalarını henüz tamamlamadığını belirten "do-not-merge" (birleştirmeyin) etiketi, yeni çekme isteklerine otomatik olarak uygulanabilir.
- **Doğrulama ve derleme**: Otomatik denetimler, değişikliklerinizin doğrulama testlerini geçtiğini doğrular. Doğrulama testleri uyarılar veya hatalar vererek, çekme isteğinizin gönderilebilmesi için bir veya daha fazla değişiklik yapmanızı isteyebilir. Doğrulama testinin sonuçları, gözden geçirmeniz için çekme isteğinize yorum olarak eklenir ve e-postayla da gönderilebilir.
- **Hazırlama**: Değişikliklerinizden etkilenen makale sayfaları, doğrulama ve derleme aşamasını başarıyla geçtikten sonra gözden geçirilmek üzere otomatik olarak bir hazırlama ortamına dağıtılır. Çekme isteği yorumlarında önizleme URL’leri görüntülenir.
- **Otomatik birleştirme**: Doğrulama testini geçen ve belirli ölçütleri karşılayan çekme istekleri otomatik olarak birleştirilebilir. Bu durumda başka işlem gerçekleştirmeniz gerekmez.

### <a name="review-and-sign-off"></a>Gözden geçirme ve kabul

Çekme isteğiyle ilgili tüm işlemler tamamlandığında, sonuçları (çekme isteği yorumları, önizleme URL'leri vb.) gözden geçirmeniz ve birleştirme için kapatmadan önce dosyalarda yapılması gereken ek değişiklikler olup olmadığına karar vermeniz gerekir. Çekme isteğinizi gözden geçiren bir çekme isteği gözden geçireni varsa, bu kişi birleştirme işleminden önce ilgilenilmesi gereken sorunlar/sorular hakkındaki geri bildirimlerini yorumlar aracılığıyla belirtebilir.

[!INCLUDE[contribute-how-to-pull-requests-apex-automation.md](contribute-how-to-pull-requests-apex-automation.md)]

Çekme isteği tüm sorunlardan arındırıldıktan ve kabul edildikten sonra, yaptığınız değişiklikler ana dalla birleştirilir ve çekme isteği kapatılır.

### <a name="publishing"></a>Yayımlama

Değişikliklerin bir sonraki zamanlanmış yayımlama çalıştırmasına dahil edilebilmesi için, çekme isteğinizin bir çekme isteği gözden geçireni tarafından birleştirilmesi gerektiğini unutmayın. Çekme istekleri normalde gönderim sırasına göre gözden geçirilir/birleştirilir. Çekme isteğinizin belirli bir yayımlama çalıştırmasında birleştirilmesi gerekiyorsa, çekme isteğinizi gözden geçireni önceden bilgilendirerek birleştirme işleminin yayımlama öncesinde gerçekleştirilmesini sağlamanız gerekir.

Katkılarınız, onaylanıp birleştirildikten sonra docs.microsoft.com yayımlama işlemi tarafından toplanır. Yayımlama süreleri, katkıda bulunduğunuz depoyu yöneten ekibe bağlı olarak değişiklik gösterebilir. Aşağıdaki yollarda yayımlanan makaleler normalde Pazartesi-Cuma günleri ve 10:30-15:30 PST saatleri arasında dağıtılır:

- https://docs.microsoft.com/azure/
- https://docs.microsoft.com/aspnet/
- https://docs.microsoft.com/dotnet/
- https://docs.microsoft.com/enterprise-mobility-security

Makalelerin yayımlandıktan sonra çevrimiçi ortamda görünmesi 45 dakikaya kadar sürebilir. Makaleniz yayımlandıktan sonra değişikliklerinizi ilgili URL'den doğrulayabilirsiniz: `https://docs.microsoft.com/<path-to-your-article-without-the-md-extension>`.
