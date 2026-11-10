# DAST

### DAST Nedir?

Dynamic Application Security Testing (DAST), çalışan bir uygulamayı dışarıdan test ederek güvenlik açıklarını tespit etmeyi amaçlayan dinamik bir güvenlik analiz yöntemidir. SAST'tan farklı olarak kaynak kodunu incelemez; uygulamaya gerçek kullanıcı veya saldırgan gibi istekler göndererek sistemin verdiği tepkileri analiz eder.

DAST araçları, uygulamanın çalışma anındaki davranışlarını değerlendirerek güvenlik açıklarını belirler. Bu sayede yalnızca kod seviyesindeki sorunlar değil, yapılandırma hataları, kimlik doğrulama problemleri ve çalışma zamanında ortaya çıkan güvenlik riskleri de tespit edilebilir.<br>

***

### DAST Nasıl Çalışır?

DAST araçları, çalışan uygulamaya HTTP/HTTPS istekleri göndererek farklı senaryoları test eder. Gönderilen istekler sonucunda uygulamanın verdiği yanıtlar analiz edilir ve güvenlik açığı oluşturabilecek durumlar raporlanır.

DAST analizlerinde yaygın olarak tespit edilen güvenlik problemleri şunlardır:

* SQL Injection
* Cross-Site Scripting (XSS)
* Komut Enjeksiyonu (Command Injection)
* Güvensiz kimlik doğrulama ve oturum yönetimi
* Hatalı yetkilendirme kontrolleri
* Güvenlik başlıklarının (Security Headers) eksik olması
* Yanlış yapılandırılmış sunucu ayarları

***

### DAST'ın Önemi

Bir uygulama geliştirme sürecinde bazı güvenlik açıkları yalnızca uygulama çalışırken ortaya çıkabilir. Bu nedenle yalnızca kaynak kodunu analiz etmek yeterli değildir. DAST, uygulamayı gerçek çalışma ortamına benzer şekilde test ederek çalışma zamanı kaynaklı güvenlik açıklarının belirlenmesine yardımcı olur.

Bu yöntem özellikle test ve canlı ortama geçmeden önce yapılan güvenlik kontrollerinde önemli bir rol oynar.<br>

***

### Avantajları ve Sınırlamaları

#### Avantajları

* Kaynak koda ihtiyaç duymadan analiz yapabilir.
* Çalışan uygulamanın gerçek davranışını test eder.
* Yapılandırma ve çalışma zamanı kaynaklı güvenlik açıklarını tespit edebilir.
* Gerçek saldırı senaryolarına benzer testler gerçekleştirir.
* Farklı teknoloji ve programlama dilleriyle geliştirilen uygulamalarda kullanılabilir.

#### Sınırlamaları

* Uygulamanın çalışır durumda olması gerekir.
* Kaynak kodunu inceleyemediği için güvenlik açığının tam olarak hangi satırdan kaynaklandığını gösteremez.
* Bazı güvenlik açıklarını tespit edemeyebilir.
* Kapsamlı analizlerde tarama süresi uzayabilir.<br>

***

### Yaygın Kullanılan DAST Araçları

DAST analizleri gerçekleştirmek için açık kaynak ve ticari birçok araç bulunmaktadır. Bu araçlar, çalışan uygulamaları gerçek kullanıcı veya saldırgan gibi test ederek güvenlik açıklarını tespit etmeyi amaçlar. Destekledikleri teknolojiler ve sundukları özellikler farklılık gösterse de temel amaçları uygulamanın çalışma zamanındaki güvenlik risklerini belirlemektir. Aşağıda yaygın olarak kullanılan DAST araçlarından bazıları açıklanmıştır.

#### Acunetix

Acunetix, en popüler ticari web uygulaması güvenlik tarayıcılarından biridir. Web uygulamalarını otomatik olarak tarayarak sayfaları, formları ve API uç noktalarını keşfeder. Ardından SQL Injection, Cross-Site Scripting (XSS), Cross-Site Request Forgery (CSRF), Server-Side Request Forgery (SSRF) ve Command Injection gibi birçok güvenlik açığını test eder. Özellikle büyük şirketler, bankalar ve penetrasyon testi ekipleri tarafından yaygın olarak kullanılmaktadır.

#### MobSF (Mobile Security Framework)

MobSF, mobil uygulamalar için geliştirilmiş açık kaynaklı bir güvenlik analiz platformudur. Android, iOS ve Windows Mobile uygulamalarını hem statik hem de dinamik olarak analiz edebilir. Uygulamanın izinlerini, API kullanımını, sertifika doğrulamalarını, sabit tanımlanmış gizli bilgileri (Hardcoded Secrets) ve diğer güvenlik risklerini inceleyerek ayrıntılı raporlar sunar. Mobil uygulama geliştiren ekipler tarafından yaygın olarak tercih edilmektedir.

#### Nuclei

Nuclei, ProjectDiscovery tarafından geliştirilen hızlı ve açık kaynaklı bir güvenlik tarama aracıdır. Şablon (Template) tabanlı çalışma mantığı sayesinde web uygulamaları, API'ler, sunucular, SSL servisleri, DNS yapılandırmaları ve ağ servislerini analiz edebilir. Binlerce hazır güvenlik şablonunu kullanarak bilinen güvenlik açıklarını hızlı bir şekilde tespit edebilir.

#### SQLMap

SQLMap, SQL Injection açıklarını tespit etmek ve doğrulamak amacıyla geliştirilmiş açık kaynaklı bir güvenlik aracıdır. Parametreleri otomatik olarak test ederek uygulamada SQL Injection zafiyeti bulunup bulunmadığını belirler. Güvenlik testlerinde, penetrasyon testlerinde ve güvenlik araştırmalarında yaygın olarak kullanılmaktadır.

#### OWASP ZAP (Zed Attack Proxy)

OWASP ZAP, OWASP topluluğu tarafından geliştirilen en popüler açık kaynak DAST araçlarından biridir. Tarayıcı ile web uygulaması arasında proxy olarak çalışır ve tüm HTTP isteklerini analiz eder. SQL Injection, Cross-Site Scripting (XSS), güvenlik başlıklarının eksikliği, çerez (Cookie) problemleri ve kimlik doğrulama açıkları gibi birçok güvenlik riskini otomatik olarak test edebilir. Özellikle web uygulaması güvenlik testlerinde ve eğitim amaçlı çalışmalarda yaygın olarak kullanılmaktadır.

#### Burp Suite

Burp Suite, PortSwigger tarafından geliştirilen profesyonel bir web uygulaması güvenlik test aracıdır. Proxy, Scanner, Intruder ve Repeater gibi modülleri sayesinde hem manuel hem de otomatik güvenlik testleri gerçekleştirilebilir. HTTP isteklerini yakalayıp değiştirebildiği için penetrasyon testleri yapan güvenlik uzmanları tarafından en çok tercih edilen araçlardan biridir.

#### Invicti

Invicti (eski adıyla Netsparker), web uygulamalarındaki güvenlik açıklarını otomatik olarak tespit eden ticari bir DAST çözümüdür. SQL Injection, Cross-Site Scripting (XSS) ve benzeri güvenlik açıklarını yüksek doğruluk oranıyla belirleyebilir. Yanlış pozitif sonuçları azaltan doğrulama mekanizması sayesinde kurumsal ortamlarda yaygın olarak kullanılmaktadır.

#### HCL AppScan

HCL AppScan, web uygulamaları ve API'ler üzerinde dinamik güvenlik analizleri gerçekleştiren kurumsal seviyede bir DAST platformudur. Güvenlik açıklarını ayrıntılı olarak raporlayabilir ve CI/CD süreçleriyle entegre çalışabilir. Özellikle büyük ölçekli kurumlarda güvenli yazılım geliştirme süreçlerinin önemli bir parçası olarak kullanılmaktadır.

#### Rapid7 InsightAppSec

Rapid7 InsightAppSec, bulut tabanlı çalışan modern bir DAST çözümüdür. Web uygulamalarını ve API'leri sürekli olarak tarayarak güvenlik açıklarını belirler. DevSecOps yaklaşımını destekleyen yapısı sayesinde otomatik güvenlik testlerinin CI/CD süreçlerine dahil edilmesine olanak tanır.

#### StackHawk

StackHawk, geliştiricilere yönelik tasarlanmış modern bir DAST aracıdır. Özellikle API güvenliği ve DevSecOps süreçlerine odaklanmaktadır. CI/CD sistemleriyle kolayca entegre olabilir ve her yeni sürümde otomatik güvenlik taramaları gerçekleştirerek geliştiricilere hızlı geri bildirim sağlar.<br>

***

### DAST Araçlarının Karşılaştırılması

Yukarıda açıklanan araçlar farklı ihtiyaçlara yönelik geliştirilmiş olsa da temel amaçları çalışan uygulamalardaki güvenlik açıklarını tespit etmektir. Aşağıdaki tabloda araçların öne çıkan kullanım alanları özetlenmiştir.

<table data-search="false"><thead><tr><th>Araç</th><th>En Çok Kullanıldığı Alan</th></tr></thead><tbody><tr><td><strong>Acunetix</strong></td><td>Web uygulamalarının kapsamlı güvenlik taraması</td></tr><tr><td><strong>MobSF</strong></td><td>Android ve iOS mobil uygulama güvenliği</td></tr><tr><td><strong>Nuclei</strong></td><td>Template tabanlı web, ağ ve servis taramaları</td></tr><tr><td><strong>SQLMap</strong></td><td>SQL Injection tespiti ve doğrulaması</td></tr><tr><td><strong>OWASP ZAP</strong></td><td>Açık kaynak web uygulaması güvenlik testleri</td></tr><tr><td><strong>Burp Suite</strong></td><td>Manuel ve otomatik penetrasyon testleri</td></tr><tr><td><strong>Invicti</strong></td><td>Kurumsal web uygulaması güvenlik taramaları</td></tr><tr><td><strong>HCL AppScan</strong></td><td>Kurumsal DAST ve API güvenliği</td></tr><tr><td><strong>Rapid7 InsightAppSec</strong></td><td>Bulut tabanlı DevSecOps güvenlik taramaları</td></tr><tr><td><strong>StackHawk</strong></td><td>API güvenliği ve CI/CD entegrasyonu</td></tr></tbody></table>

***

### SPM ile İlişkisi

SPM platformları, DAST araçlarından elde edilen güvenlik bulgularını diğer güvenlik verileriyle birlikte merkezi olarak yönetir. Böylece çalışma zamanında tespit edilen güvenlik açıkları ilgili varlıklar, CVE kayıtları ve risk puanlarıyla ilişkilendirilerek tek bir platform üzerinden takip edilebilir.

Bu yaklaşım, güvenlik ekiplerinin yalnızca kod seviyesindeki değil, çalışan sistemlerde bulunan güvenlik risklerini de bütüncül olarak değerlendirmesine olanak sağlar.<br>

***

### Örnek

Bir e-ticaret uygulamasının giriş ekranı DAST aracı tarafından test edilmektedir. Araç, farklı giriş denemeleri gerçekleştirerek uygulamanın hata mesajlarını, oturum yönetimini ve kullanıcı giriş sürecini analiz eder.

Eğer uygulama hatalı yapılandırılmış bir yetkilendirme mekanizmasına sahipse veya SQL Injection gibi bir güvenlik açığı barındırıyorsa, DAST aracı bu durumu raporlayarak güvenlik ekibini bilgilendirir.<br>

***

**SAST ve DAST benzer amaçlara hizmet etse de analiz yöntemleri ve kullanım alanları bakımından birbirinden farklıdır. Aşağıdaki tabloda iki yöntem arasındaki temel farklar özetlenmiştir.**

| Özellik                           | SAST               | DAST                         |
| --------------------------------- | ------------------ | ---------------------------- |
| Analiz Türü                       | Statik             | Dinamik                      |
| Kaynak Kod Gereksinimi            | Evet               | Hayır                        |
| Uygulamanın Çalışması Gerekir mi? | Hayır              | Evet                         |
| Analiz Zamanı                     | Geliştirme aşaması | Test veya canlı ortam öncesi |
| İncelediği Alan                   | Kaynak kodu        | Çalışan uygulama             |

SAST ve DAST birbirinin alternatifi değil, tamamlayıcısıdır. SAST geliştirme aşamasında kaynak kodunu analiz ederken, DAST çalışan uygulamayı test ederek çalışma zamanında ortaya çıkabilecek güvenlik açıklarını tespit eder. Bu nedenle güvenli yazılım geliştirme süreçlerinde her iki yöntemin birlikte kullanılması önerilmektedir.

