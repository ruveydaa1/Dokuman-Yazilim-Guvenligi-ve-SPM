# SCA

### SCA Nedir?

Software Composition Analysis (SCA), yazılım projelerinde kullanılan açık kaynak kütüphaneleri, üçüncü taraf bağımlılıkları ve diğer yazılım bileşenlerini analiz ederek güvenlik açıklarını, lisans risklerini ve güncellik durumlarını tespit eden bir güvenlik analiz yöntemidir.

Modern yazılım projelerinin büyük bir bölümü açık kaynak bileşenlerden oluşmaktadır. Bu bileşenler geliştirme sürecini hızlandırsa da zaman zaman güvenlik açıkları içerebilir. SCA araçları, kullanılan bağımlılıkları analiz ederek bu bileşenlerde bilinen güvenlik açıklarının bulunup bulunmadığını belirler ve geliştiricilere rapor sunar.<br>

***

### SCA Nasıl Çalışır?

SCA araçları, uygulamanın kullandığı bağımlılıkları belirleyerek bunları güvenlik veritabanlarıyla karşılaştırır. Analiz sırasında bileşenlerin sürümleri incelenir ve bilinen güvenlik açıkları, lisans sorunları veya güncel olmayan paketler tespit edilir.

Bu süreçte genellikle aşağıdaki bilgiler değerlendirilir:

* Kullanılan açık kaynak kütüphaneleri
* Bağımlılıkların sürüm bilgileri
* Bilinen CVE kayıtları
* CVSS risk puanları
* Lisans türleri
* Güncel sürüm bilgileri

Analiz sonucunda riskli bileşenler raporlanır ve gerekli güncelleme veya düzeltme önerileri sunulur.<br>

***

### SCA'nın Önemi

Günümüzde birçok güvenlik ihlali, kurumların geliştirdiği koddan değil; kullandıkları açık kaynak bileşenlerde bulunan güvenlik açıklarından kaynaklanmaktadır. Bu nedenle yalnızca uygulamanın kendi kodunu analiz etmek yeterli değildir.

SCA, güvenlik açığı bulunan bağımlılıkların erken aşamada tespit edilmesini sağlayarak olası saldırıların önlenmesine katkı sağlar. Ayrıca lisans uyumluluğunun kontrol edilmesi ve güncel olmayan paketlerin belirlenmesi açısından da önemli bir rol oynar.<br>

***

### Yaygın Kullanılan SCA Araçları

SCA analizleri gerçekleştirmek için açık kaynak ve ticari birçok araç bulunmaktadır. Bu araçlar, projelerde kullanılan açık kaynak kütüphaneleri, üçüncü taraf bağımlılıkları ve yazılım bileşenlerini analiz ederek güvenlik açıklarını, lisans risklerini ve güncellik durumlarını tespit eder. Aşağıda yaygın olarak kullanılan SCA araçlarından bazıları açıklanmıştır.

#### OWASP Dependency-Check

OWASP Dependency-Check, en yaygın açık kaynak SCA araçlarından biridir. Projede kullanılan bağımlılıkları analiz ederek bunları CVE veritabanıyla karşılaştırır. Güvenlik açığı bulunan paketleri tespit eder ve geliştiricilere ayrıntılı raporlar sunar. Özellikle Java projelerinde yaygın olarak kullanılmasına rağmen farklı platformları da desteklemektedir.

#### Dependency-Track

Dependency-Track, SBOM (Software Bill of Materials) yönetimi üzerine odaklanan açık kaynaklı bir platformdur. Projelerde kullanılan yazılım bileşenlerini sürekli takip eder ve bu bileşenlerde yeni bir güvenlik açığı yayımlandığında kullanıcıları bilgilendirir. Böylece güvenlik riskleri sürekli olarak izlenebilir.

#### GitHub Dependabot

GitHub Dependabot, GitHub tarafından sunulan yerleşik bağımlılık yönetim sistemidir. Depodaki bağımlılıkları düzenli olarak analiz ederek güvenlik açığı bulunan veya eski sürümde kalan paketleri tespit eder. Gerekli durumlarda otomatik Pull Request oluşturarak güvenli sürüme güncellenmesini önerir.

#### Trivy

Trivy, en popüler açık kaynak güvenlik tarama araçlarından biridir. Container imajlarını, bağımlılıkları, dosya sistemlerini, Kubernetes yapılandırmalarını ve Infrastructure as Code (IaC) dosyalarını analiz edebilir. Çok yönlü yapısı sayesinde DevSecOps süreçlerinde yaygın olarak kullanılmaktadır.

#### Grype

Grype, container imajlarını ve dosya sistemlerini analiz ederek içerdikleri paketlerde bulunan bilinen CVE kayıtlarını tespit eden açık kaynaklı bir SCA aracıdır. Özellikle container tabanlı uygulamalarda bağımlılık güvenliğinin sağlanması amacıyla kullanılmaktadır.

#### JFrog Xray

JFrog Xray, kurumsal seviyede kullanılan kapsamlı bir yazılım bileşeni analiz platformudur. Artifact'leri ve bağımlılıkları analiz ederek güvenlik açıklarını, lisans uyumluluğunu ve riskli paketleri belirler. Büyük ölçekli yazılım geliştirme süreçlerinde yaygın olarak tercih edilmektedir.

#### Prisma Cloud

Prisma Cloud, bulut tabanlı uygulamalar için geliştirilmiş kapsamlı bir güvenlik platformudur. Container güvenliği, Kubernetes güvenliği ve yazılım bağımlılıklarının analizini tek platform üzerinden gerçekleştirebilir. Cloud-native uygulamalarda yaygın olarak kullanılmaktadır.

#### SBOM Generator

SBOM Generator araçları, projede kullanılan tüm yazılım bileşenlerini listeleyerek Software Bill of Materials (SBOM) oluşturur. Oluşturulan SBOM dosyaları daha sonra SCA araçları tarafından analiz edilerek güvenlik açıklarının ve bağımlılık risklerinin takip edilmesini sağlar.

#### Sysdig Secure

Sysdig Secure, container güvenliği, çalışma zamanı güvenliği ve yazılım bileşenlerinin analizini birlikte gerçekleştiren kurumsal bir güvenlik platformudur. Özellikle Kubernetes ortamlarında güvenlik ve uyumluluk kontrolleri için tercih edilmektedir.

#### Xeol

Xeol, kullanılan yazılım bileşenlerinin End of Life (EOL) yani destek süresi durumunu analiz eden bir araçtır. Destek süresi sona ermiş veya güncelliğini kaybetmiş yazılım bileşenlerini belirleyerek geliştiricilere güncelleme önerilerinde bulunur.

#### Snyk Open Source

Snyk Open Source, Snyk platformunun açık kaynak bağımlılık analizi çözümüdür. Projedeki bağımlılıkları sürekli olarak izleyerek güvenlik açıklarını tespit eder, lisans kontrolleri gerçekleştirir ve güvenli sürümlere yükseltme önerileri sunar. GitHub, GitLab ve CI/CD süreçleriyle kolayca entegre çalışabilmesi nedeniyle günümüzde en yaygın kullanılan SCA araçlarından biridir.<br>

***

### SCA Araçlarının Karşılaştırılması

Yukarıda açıklanan araçlar farklı özelliklere sahip olsa da temel amaçları projelerde kullanılan yazılım bileşenlerinin güvenliğini sağlamaktır. Aşağıdaki tabloda araçların öne çıkan kullanım alanları özetlenmiştir.

<table data-search="false"><thead><tr><th>Araç</th><th>Öne Çıkan Özelliği</th></tr></thead><tbody><tr><td><strong>OWASP Dependency-Check</strong></td><td>Bağımlılıkları CVE veritabanıyla karşılaştırır</td></tr><tr><td><strong>Dependency-Track</strong></td><td>SBOM yönetimi ve sürekli güvenlik takibi</td></tr><tr><td><strong>GitHub Dependabot</strong></td><td>Otomatik bağımlılık güncelleme önerileri</td></tr><tr><td><strong>Trivy</strong></td><td>Container, dependency, Kubernetes ve IaC taraması</td></tr><tr><td><strong>Grype</strong></td><td>Container imajları ve dosya sistemlerinde CVE analizi</td></tr><tr><td><strong>JFrog Xray</strong></td><td>Kurumsal güvenlik ve lisans uyumluluğu</td></tr><tr><td><strong>Prisma Cloud</strong></td><td>Cloud-native uygulama ve container güvenliği</td></tr><tr><td><strong>SBOM Generator</strong></td><td>Yazılım bileşenlerinin SBOM'unu oluşturur</td></tr><tr><td><strong>Sysdig Secure</strong></td><td>Container ve çalışma zamanı güvenliği</td></tr><tr><td><strong>Xeol</strong></td><td>End of Life (EOL) durumunu analiz eder</td></tr><tr><td><strong>Snyk Open Source</strong></td><td>Açık kaynak bağımlılıklarını sürekli izler ve güncelleme önerir</td></tr></tbody></table>



***

### SPM ile İlişkisi

SPM platformları, SCA araçlarından elde edilen analiz sonuçlarını merkezi bir panelde görüntüler. Tespit edilen güvenlik açıkları ilgili varlıklar, CVE kayıtları ve CVSS risk puanlarıyla ilişkilendirilerek güvenlik ekiplerine kapsamlı bir risk görünümü sunulur.

Böylece kurumlar yalnızca hangi bağımlılıkların kullanıldığını değil, bu bağımlılıkların oluşturabileceği güvenlik risklerini de tek bir platform üzerinden takip edebilir.<br>

***

### Örnek

Node.js ile geliştirilen bir projede **Express**, **jsonwebtoken** ve **multer** gibi açık kaynak kütüphaneler kullanılmaktadır. SCA aracı bu bağımlılıkları analiz ederek kullanılan sürümlerde bilinen bir güvenlik açığı olup olmadığını kontrol eder.

Örneğin kullanılan bir kütüphanede kritik seviyede bir CVE kaydı bulunduğu tespit edilirse, SCA aracı bu durumu raporlar ve güvenli sürüme yükseltilmesini önerir. Böylece güvenlik riski oluşmadan önce gerekli güncelleme planlanabilir.
