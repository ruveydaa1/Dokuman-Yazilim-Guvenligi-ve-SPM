# SAST

### SAST Nedir?

Static Application Security Testing (SAST), uygulamanın kaynak kodunu, derlenmeden veya çalıştırılmadan analiz ederek güvenlik açıklarını tespit etmeyi amaçlayan statik bir güvenlik test yöntemidir. SAST araçları, geliştiricilerin yazdığı kaynak kodunu inceleyerek güvenli olmayan kodlama hatalarını, güvenlik zafiyetlerini ve yazılım standartlarına aykırı durumları belirler.

Bu yöntem, yazılım geliştirme yaşam döngüsünün (SDLC) erken aşamalarında kullanılabildiği için güvenlik açıklarının henüz uygulama kullanıcılarla buluşmadan önce tespit edilmesini sağlar. Böylece güvenlik sorunlarının daha düşük maliyetle giderilmesine katkıda bulunur.<br>

***

### SAST Nasıl Çalışır?

SAST araçları, kaynak kodunu satır satır analiz ederek olası güvenlik açıklarını belirlemeye çalışır. Analiz sırasında kodun çalıştırılmasına gerek yoktur. Araçlar; veri akışı, kontrol akışı, değişken kullanımı ve güvenlik kurallarını değerlendirerek risk oluşturabilecek kod parçalarını raporlar.

SAST analizlerinde yaygın olarak tespit edilen güvenlik problemleri şunlardır:

* SQL Injection
* Cross-Site Scripting (XSS)
* Komut Enjeksiyonu (Command Injection)
* Güvensiz kimlik doğrulama işlemleri
* Hatalı giriş doğrulamaları
* Güvensiz hata yönetimi
* Kod kalitesi ve güvenli kodlama ihlalleri<br>

***

### SAST'ın Önemi

Güvenlik açıklarının yazılım geliştirme sürecinin erken aşamalarında tespit edilmesi hem maliyet hem de zaman açısından önemli avantajlar sağlar. Kod henüz geliştirme aşamasındayken bulunan güvenlik sorunları, uygulama canlı ortama alındıktan sonra tespit edilen sorunlara göre çok daha kolay giderilebilir.

Bu nedenle birçok kurum, SAST analizlerini CI/CD süreçlerine entegre ederek her kod değişikliğinde otomatik güvenlik taraması gerçekleştirmektedir.<br>

***

### Avantajları ve Sınırlamaları

#### Avantajları

* Kaynak kodunu çalıştırmadan analiz edebilir.
* Güvenlik açıklarını geliştirme aşamasında tespit eder.
* CI/CD süreçlerine kolayca entegre edilebilir.
* Güvenli kodlama standartlarının uygulanmasına katkı sağlar.
* Hataların erken giderilmesini sağlayarak maliyeti azaltır.

#### Sınırlamaları

* Çalışan uygulamanın davranışını analiz edemez.
* Yapılandırma veya çalışma zamanı kaynaklı bazı güvenlik açıklarını tespit edemeyebilir.
* Bazı durumlarda yanlış pozitif (False Positive) sonuçlar üretebilir.
* Kullanılan kuralların doğruluğu analiz kalitesini etkileyebilir.<br>

***

### Yaygın Kullanılan SAST Araçları

SAST analizleri gerçekleştirmek için açık kaynak ve ticari birçok araç bulunmaktadır. Bu araçlar; destekledikleri programlama dilleri, analiz yöntemleri ve sundukları özellikler bakımından farklılık gösterse de temel amaçları kaynak kodundaki güvenlik açıklarını erken aşamada tespit etmektir. Aşağıda yaygın olarak kullanılan SAST araçlarından bazıları açıklanmıştır.

#### Aikido Security

Aikido Security, geliştiricilere yönelik modern bir uygulama güvenliği (Application Security) platformudur. SAST özelliği sayesinde kaynak kodunu analiz ederek güvenlik açıklarını tespit eder ve geliştiricilere düzeltme önerileri sunar. GitHub başta olmak üzere farklı geliştirme araçlarıyla kolayca entegre olabilir ve kullanım kolaylığıyla öne çıkar.

#### Bandit

Bandit, yalnızca Python projeleri için geliştirilmiş açık kaynaklı bir SAST aracıdır. Python kodlarını analiz ederek **eval()** kullanımı, güvensiz **subprocess** çağrıları, sabit olarak tanımlanmış parolalar (Hardcoded Password) ve zayıf kriptografi kullanımı gibi güvenlik problemlerini tespit edebilir. Python tabanlı projelerde yaygın olarak tercih edilmektedir.

#### Checkmarx

Checkmarx, kurumsal ölçekte en yaygın kullanılan ticari SAST çözümlerinden biridir. Çok sayıda programlama dilini destekler, büyük projeleri analiz edebilir ve ayrıntılı güvenlik raporları oluşturabilir. Ayrıca CI/CD süreçleriyle entegre çalışarak güvenlik kontrollerinin otomatik olarak gerçekleştirilmesini sağlar.

#### Checkov

Checkov, klasik anlamda uygulama kaynak kodunu analiz etmek yerine **Infrastructure as Code (IaC)** dosyalarının güvenliğini değerlendiren bir analiz aracıdır. Terraform, Kubernetes YAML, Docker Compose ve CloudFormation gibi yapılandırma dosyalarını inceleyerek yanlış yapılandırmaları tespit eder. Örneğin herkese açık bırakılmış bir S3 Bucket veya gereğinden fazla yetkiye sahip bir Kubernetes pod'u gibi güvenlik risklerini belirleyebilir.

#### Fortify Static Code Analyzer

Fortify Static Code Analyzer (Fortify SCA), OpenText tarafından geliştirilen kurumsal seviyede bir SAST aracıdır. Çok sayıda programlama dilini destekler ve kaynak kodunu ayrıntılı olarak analiz ederek güvenlik açıklarını raporlar. Özellikle büyük ölçekli kurumlarda ve güvenli yazılım geliştirme süreçlerinde yaygın olarak kullanılmaktadır.

#### Gosec

Gosec, yalnızca Go (Golang) dili için geliştirilmiş açık kaynaklı bir güvenlik analiz aracıdır. Go projelerinde sabit tanımlanmış kimlik bilgileri (Hardcoded Credentials), güvensiz rastgele sayı üretimi, hatalı dosya izinleri ve SQL Injection gibi güvenlik risklerini tespit edebilir.

#### Semgrep

Semgrep, en popüler açık kaynak SAST araçlarından biridir. JavaScript, TypeScript, Python, Java, Go, C#, PHP ve Ruby gibi birçok programlama dilini destekler. Hızlı analiz yapabilmesi, özelleştirilebilir kurallara sahip olması ve CI/CD süreçlerine kolayca entegre edilebilmesi nedeniyle geliştiriciler tarafından yaygın olarak kullanılmaktadır.

#### Shannon

Shannon, kaynak kodunu analiz ederek güvenlik açıklarını ve kod kalitesi problemlerini tespit eden bir SAST aracıdır. Kaynak kodunu güvenlik kuralları doğrultusunda inceleyerek potansiyel riskleri raporlar ve geliştiricilerin güvenli kod yazmasına katkı sağlar.

#### Snyk Code

Snyk Code, Snyk platformunun statik kod analiz çözümüdür. IDE içerisinde çalışabilir, geliştiricilere kod yazımı sırasında anlık uyarılar gösterebilir ve GitHub gibi sürüm kontrol sistemleriyle entegre olabilir. Güvenlik açıklarını tespit etmenin yanı sıra düzeltme önerileri de sunarak geliştirici odaklı bir yaklaşım benimser.

#### SonarQube

SonarQube, temel olarak bir kod kalite platformu olmasına rağmen güvenlik analizleri de gerçekleştirebilir. Güvenlik açıklarının yanı sıra hataları (Bug), kod tekrarlarını, performans problemlerini ve kod kokularını (Code Smells) tespit eder. Bu nedenle birçok yazılım ekibi tarafından hem kod kalitesini artırmak hem de temel güvenlik kontrollerini gerçekleştirmek amacıyla kullanılmaktadır.

#### CodeQL

CodeQL, GitHub tarafından geliştirilen gelişmiş bir statik kod analiz teknolojisidir. Kaynak kodunu sorgulanabilir bir veritabanına dönüştürerek güvenlik açıklarının özel sorgular aracılığıyla tespit edilmesini sağlar. Özellikle **GitHub Advanced Security** kapsamında yaygın olarak kullanılmakta olup birçok programlama dilini desteklemektedir.

#### Veracode Static Analysis

Veracode Static Analysis, bulut tabanlı çalışan kurumsal bir SAST çözümüdür. Kaynak kodunu analiz ederek güvenlik açıklarını belirler ve sonuçları merkezi bir platform üzerinden raporlar. DevSecOps ve CI/CD süreçleriyle kolayca entegre olabildiği için özellikle büyük ölçekli kurumlarda yaygın olarak tercih edilmektedir.<br>

***

### SAST Araçlarının Karşılaştırılması

<table data-search="false"><thead><tr><th>Araç</th><th>Öne Çıkan Özelliği</th></tr></thead><tbody><tr><td><strong>Aikido Security</strong></td><td>Geliştirici odaklı modern uygulama güvenliği platformu</td></tr><tr><td><strong>Bandit</strong></td><td>Python projeleri için güvenlik analizi</td></tr><tr><td><strong>Checkmarx</strong></td><td>Kurumsal ölçekte kapsamlı SAST çözümü</td></tr><tr><td><strong>Checkov</strong></td><td>Infrastructure as Code (IaC) güvenliği</td></tr><tr><td><strong>Fortify Static Code Analyzer</strong></td><td>Büyük ölçekli kurumsal güvenlik analizleri</td></tr><tr><td><strong>Gosec</strong></td><td>Go (Golang) projeleri için güvenlik analizi</td></tr><tr><td><strong>Semgrep</strong></td><td>Hızlı, çok dilli ve özelleştirilebilir analiz</td></tr><tr><td><strong>Shannon</strong></td><td>Kaynak kodu güvenliği ve kod kalite analizi</td></tr><tr><td><strong>Snyk Code</strong></td><td>Gerçek zamanlı geliştirici odaklı SAST</td></tr><tr><td><strong>SonarQube</strong></td><td>Kod kalitesi ve temel güvenlik analizleri</td></tr><tr><td><strong>CodeQL</strong></td><td>GitHub tabanlı gelişmiş statik kod analizi</td></tr><tr><td><strong>Veracode Static Analysis</strong></td><td>Bulut tabanlı kurumsal SAST çözümü</td></tr></tbody></table>

***

### SPM ile İlişkisi

SPM platformları, SAST araçlarından elde edilen güvenlik bulgularını merkezi olarak toplar ve diğer güvenlik verileriyle ilişkilendirir. Böylece güvenlik ekipleri, tespit edilen kod seviyesindeki güvenlik açıklarını ilgili varlıklar, CVE kayıtları ve risk puanlarıyla birlikte değerlendirebilir.

Ayrıca SAST sonuçları, güvenlik ekiplerinin geliştiricilerle iş birliği içerisinde güvenlik açıklarını daha hızlı gidermesine yardımcı olur.<br>

***

### Örnek

Bir geliştiricinin kullanıcıdan aldığı veriyi doğrulamadan doğrudan SQL sorgusunda kullandığını düşünelim. SAST aracı kaynak kodunu analiz ederken bu durumu tespit ederek olası bir **SQL Injection** zafiyeti konusunda uyarı verir.

Bu sayede uygulama henüz test veya canlı ortama alınmadan önce ilgili kod düzeltilerek güvenlik riski ortadan kaldırılabilir.

