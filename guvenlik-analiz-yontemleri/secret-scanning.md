# Secret Scanning

### Secret Scanning Nedir?

Secret Scanning, kaynak kodu, yapılandırma dosyaları ve Git depoları içerisinde yanlışlıkla paylaşılmış hassas bilgileri tespit etmeyi amaçlayan bir güvenlik analiz yöntemidir. Bu yöntem; API anahtarları, erişim belirteçleri (Access Token), şifreler, SSH anahtarları, veritabanı bağlantı bilgileri ve diğer gizli bilgilerin istemeden depoya eklenmesini önlemeye yardımcı olur.

Geliştiriciler zaman zaman test amacıyla kullandıkları gizli bilgileri doğrudan kaynak koduna yazabilir veya yanlışlıkla Git deposuna gönderebilir. Bu durum, özellikle herkese açık depolarda ciddi güvenlik riskleri oluşturabilir. Secret Scanning araçları bu tür bilgileri otomatik olarak tespit ederek geliştiricileri uyarır.<br>

***

### Secret Scanning Nasıl Çalışır?

Secret Scanning araçları, kaynak kodunu ve ilgili dosyaları belirli kurallar ve desenler doğrultusunda analiz eder. Analiz sırasında API anahtarları, erişim belirteçleri, sertifikalar, özel anahtarlar ve benzeri hassas bilgiler aranır.

Birçok araç, yalnızca belirli anahtarları değil, AWS, Azure, Google Cloud, GitHub ve diğer popüler servis sağlayıcılarına ait kimlik bilgilerini de tanıyabilecek şekilde geliştirilmiştir. Böylece yanlışlıkla paylaşılan bilgiler hızlı bir şekilde tespit edilerek güvenlik ekiplerine bildirilebilir.<br>

***

### Secret Scanning'in Önemi

Gizli bilgilerin kaynak kodunda bulunması, saldırganların sistemlere yetkisiz erişim sağlamasına neden olabilir. Ele geçirilen bir API anahtarı veya erişim belirteci; veritabanlarına erişim, bulut servislerinin kötüye kullanılması veya hassas verilere ulaşılması gibi ciddi sonuçlar doğurabilir.

Secret Scanning, bu tür riskleri erken aşamada tespit ederek geliştiricilerin gerekli düzeltmeleri yapmasına olanak sağlar. Böylece güvenlik ihlallerinin önüne geçilmesine katkıda bulunur.<br>

***

### Avantajları ve Sınırlamaları

#### Avantajları

* Kaynak kodunda bulunan hassas bilgileri hızlı bir şekilde tespit eder.
* Güvenlik ihlallerinin önlenmesine katkı sağlar.
* Git depoları ve CI/CD süreçleriyle entegre çalışabilir.
* Yanlışlıkla paylaşılan erişim bilgilerinin erken tespit edilmesini sağlar.
* Geliştiricilerin güvenli yazılım geliştirme süreçlerini destekler.

#### Sınırlamaları

* Bilinmeyen veya özel formatta oluşturulmuş gizli bilgileri her zaman tespit edemeyebilir.
* Bazı durumlarda yanlış pozitif sonuçlar üretebilir.
* Tespit edilen gizli bilginin otomatik olarak geçersiz hale getirilmesini sağlamaz; gerekli işlemlerin kullanıcı tarafından yapılması gerekir.<br>

***

### Yaygın Kullanılan Secret Scanning Araçları

Secret Scanning işlemleri için açık kaynak ve ticari birçok araç bulunmaktadır. Bu araçlar, kaynak kodunu, Git depolarını ve commit geçmişini analiz ederek yanlışlıkla paylaşılmış API anahtarları, erişim belirteçleri (Access Token), parolalar, SSH anahtarları ve diğer hassas bilgileri tespit etmeyi amaçlar. Aşağıda yaygın olarak kullanılan Secret Scanning araçlarından bazıları açıklanmıştır.

#### GitHub Secret Scanning

GitHub Secret Scanning, GitHub tarafından sunulan yerleşik bir güvenlik özelliğidir. Depoları sürekli olarak tarayarak AWS, Azure, Google Cloud, GitHub ve diğer birçok popüler servise ait erişim anahtarlarını tespit edebilir. Desteklenen bir gizli bilgi bulunduğunda geliştiricilere uyarı gönderir ve ilgili anahtarın iptal edilmesini önerir.

#### Gitleaks

Gitleaks, en popüler açık kaynak Secret Scanning araçlarından biridir. Git depolarını, commit geçmişini, branch'leri ve dosyaları tarayarak yanlışlıkla paylaşılmış hassas bilgileri tespit eder. Belirli anahtar formatlarını ve desenlerini (Pattern) kullanarak analiz gerçekleştirir. Eski commit'lerde bulunmaya devam eden gizli bilgileri de tespit edebilmesi önemli avantajlarından biridir.

#### TruffleHog

TruffleHog, açık kaynaklı ve yaygın olarak kullanılan bir Secret Scanning aracıdır. Desen tabanlı taramanın yanı sıra bulduğu gizli bilgilerin gerçekten geçerli olup olmadığını doğrulamaya çalışabilir. Örneğin tespit edilen bir AWS erişim anahtarının hâlâ kullanılabilir olup olmadığını kontrol ederek risk seviyesini daha doğru belirleyebilir.

#### GitLab Secret Detection

GitLab Secret Detection, GitLab CI/CD süreçlerine entegre çalışan bir Secret Scanning çözümüdür. Kod depolarını ve merge request'leri tarayarak API anahtarları, erişim belirteçleri ve diğer hassas bilgileri tespit eder. Güvenlik kontrollerinin yazılım geliştirme sürecine otomatik olarak dahil edilmesini sağlar.

#### GitGuardian

GitGuardian, kurumsal ortamlarda yaygın olarak kullanılan bulut tabanlı bir Secret Scanning platformudur. GitHub, GitLab, Bitbucket ve diğer sürüm kontrol sistemleriyle entegre çalışabilir. Sürekli izleme yaparak yanlışlıkla paylaşılan gizli bilgileri hızlı bir şekilde tespit eder ve ayrıntılı güvenlik raporları sunar.

#### Detect Secrets

Detect Secrets, Yelp tarafından geliştirilen açık kaynaklı bir Secret Scanning aracıdır. Özellikle Git commit işlemleri sırasında çalıştırılarak hassas bilgilerin depoya gönderilmesini önlemeye yardımcı olur. Özelleştirilebilir kuralları sayesinde farklı projelerde güvenli yazılım geliştirme süreçlerini desteklemektedir.<br>

***

### Secret Scanning Araçlarının Karşılaştırılması

Yukarıda açıklanan araçlar farklı çalışma yöntemlerine sahip olsa da temel amaçları kaynak kodunda ve Git depolarında bulunan hassas bilgileri tespit etmektir. Aşağıdaki tabloda araçların öne çıkan özellikleri özetlenmiştir.

| Araç                        | Öne Çıkan Özelliği                                      |
| --------------------------- | ------------------------------------------------------- |
| **GitHub Secret Scanning**  | GitHub depolarında yerleşik gizli bilgi taraması        |
| **Gitleaks**                | Git geçmişi ve commit'leri tarayan açık kaynak araç     |
| **TruffleHog**              | Bulduğu gizli bilgilerin geçerliliğini doğrulayabilmesi |
| **GitLab Secret Detection** | GitLab CI/CD süreçleriyle entegre secret taraması       |
| **GitGuardian**             | Kurumsal ortamlarda sürekli secret izleme ve raporlama  |
| **Detect Secrets**          | Commit öncesinde hassas bilgilerin tespit edilmesi      |

***

### SPM ile İlişkisi

SPM platformları, Secret Scanning araçlarından elde edilen bulguları diğer güvenlik analiz sonuçlarıyla birlikte merkezi olarak yönetir. Böylece geliştiriciler ve güvenlik ekipleri yalnızca güvenlik açıklarını değil, yanlışlıkla paylaşılmış hassas bilgileri de tek bir platform üzerinden takip edebilir.

Bu yaklaşım, uygulama güvenliğinin daha kapsamlı bir şekilde değerlendirilmesine ve güvenlik risklerinin azaltılmasına katkı sağlar.<br>

***

### Örnek

Bir geliştiricinin test amacıyla kullandığı AWS Access Key'i doğrudan kaynak koduna eklediğini düşünelim. Kod Git deposuna gönderildiğinde Secret Scanning aracı bu anahtarı tespit eder ve güvenlik ekibini uyarır.

Bunun sonucunda ilgili erişim anahtarı iptal edilerek yeni bir anahtar oluşturulabilir. Böylece hassas bilgilerin kötü niyetli kişiler tarafından kullanılmasının önüne geçilmiş olur.
