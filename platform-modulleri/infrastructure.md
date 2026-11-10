# Infrastructure

### Infrastructure Nedir?

Infrastructure (Altyapı), bir yazılım uygulamasının çalışmasını sağlayan sunucular, sanal makineler, container ortamları, bulut servisleri, ağ bileşenleri ve altyapı yapılandırmalarının tamamını ifade eder. Günümüzde uygulamalar çoğunlukla AWS, Microsoft Azure, Google Cloud veya Kubernetes gibi modern altyapılar üzerinde çalışmaktadır.

SPM platformlarında Infrastructure modülü, bu altyapıları merkezi olarak analiz ederek yanlış yapılandırmaları, güvenlik açıklarını ve uyumluluk sorunlarını tespit etmeye yardımcı olur.<br>

***

### Infrastructure Nasıl Çalışır?

Infrastructure modülü, bulut servisleri veya altyapı yönetim araçlarıyla entegre çalışır. Entegrasyon sonrasında sistemde bulunan kaynaklar analiz edilerek güvenlik riskleri belirlenir.

Analiz sırasında örneğin;

* Yanlış yapılandırılmış güvenlik grupları
* Herkese açık bırakılmış depolama alanları
* Zayıf erişim politikaları
* Yanlış IAM izinleri
* Güvensiz Kubernetes yapılandırmaları
* Güvenlik güncellemesi eksik sistemler
* Uyumluluk ihlalleri

tespit edilerek raporlanabilir.

Birçok platform bu analizleri belirli aralıklarla otomatik olarak gerçekleştirerek yeni oluşan riskleri de takip eder.<br>

***

### Infrastructure'ın Önemi

Bulut teknolojilerinin yaygınlaşmasıyla birlikte güvenlik risklerinin önemli bir bölümü altyapı yapılandırmalarından kaynaklanmaktadır. Yanlış yapılandırılmış tek bir bulut kaynağı bile veri sızıntısına veya yetkisiz erişime neden olabilir.

Infrastructure güvenliği sayesinde bu tür riskler erken aşamada tespit edilerek gerekli düzeltmeler yapılabilir ve altyapının güvenliği artırılabilir.<br>

***

### Avantajları ve Sınırlamaları

#### Avantajları

* Bulut altyapısını merkezi olarak analiz eder.
* Yanlış yapılandırmaları hızlı şekilde tespit eder.
* Uyumluluk (Compliance) kontrollerini destekler.
* Sürekli güvenlik izleme sağlar.
* Bulut ortamlarındaki güvenlik risklerini azaltır.

#### Sınırlamaları

* Desteklenmeyen altyapılar analiz edilemeyebilir.
* Yanlış yetkilendirme analiz sonuçlarını etkileyebilir.
* Çok büyük altyapılarda tarama süreleri uzayabilir.
* Bazı risklerin giderilmesi manuel müdahale gerektirebilir.<br>

***

## Yaygın Kullanılan Infrastructure Teknolojileri

Infrastructure modülleri farklı bulut sağlayıcıları, container platformları ve altyapı yönetim araçlarıyla entegre çalışabilir.

#### Amazon Web Services (AWS)

AWS, dünyanın en yaygın kullanılan bulut platformlarından biridir. EC2, S3, IAM, RDS ve Lambda gibi birçok hizmet sunmaktadır. Infrastructure modülü, AWS kaynaklarını analiz ederek yanlış yapılandırmaları ve güvenlik risklerini tespit edebilir.

#### Microsoft Azure

Microsoft Azure, Microsoft tarafından sunulan bulut platformudur. Sanal makineler, depolama hizmetleri, ağ yönetimi ve kimlik yönetimi gibi birçok servisi içerir. Güvenlik analizleri sayesinde Azure kaynaklarındaki riskler merkezi olarak izlenebilir.

#### Google Cloud Platform (GCP)

Google Cloud Platform, Google'ın bulut altyapı hizmetidir. Compute Engine, Cloud Storage, Kubernetes Engine ve diğer servisleriyle modern uygulamaların çalıştırılmasını sağlar. Infrastructure modülleri GCP kaynaklarını da analiz edebilir.

#### Kubernetes

Kubernetes, container tabanlı uygulamaların dağıtılması ve yönetilmesi için kullanılan açık kaynaklı bir container orkestrasyon platformudur. Güvenlik analizleri sırasında pod güvenliği, RBAC ayarları, ağ politikaları ve yanlış yapılandırmalar kontrol edilebilir.

#### Docker

Docker, uygulamaların container teknolojisi kullanılarak çalıştırılmasını sağlayan platformdur. Infrastructure modülleri Docker ortamlarını analiz ederek güvenlik riskleri ve yanlış yapılandırmaları belirleyebilir.

#### Terraform

Terraform, Infrastructure as Code (IaC) yaklaşımıyla altyapının kod olarak yönetilmesini sağlayan açık kaynaklı bir araçtır. Infrastructure modülleri Terraform dosyalarını analiz ederek güvenlik açısından risk oluşturabilecek yapılandırmaları tespit edebilir.

#### Ansible

Ansible, sunucu yapılandırması ve otomasyon süreçlerinde kullanılan açık kaynaklı bir yapılandırma yönetim aracıdır. Güvenlik ekipleri yanlış yapılandırmaları tespit etmek ve altyapı standartlarını korumak amacıyla Ansible yapılandırmalarını analiz edebilir.

#### OpenShift

OpenShift, Kubernetes tabanlı kurumsal container platformudur. Container yönetimi, güvenlik politikaları ve uygulama dağıtım süreçlerini merkezi olarak yönetmeye olanak sağlar.

#### **CrowdStrike Falcon**

CrowdStrike Falcon, uç nokta güvenliği (Endpoint Detection and Response - EDR) sağlayan kurumsal bir güvenlik platformudur. Sunucuların ve istemci bilgisayarların davranışlarını sürekli izleyerek kötü amaçlı yazılımları, fidye yazılımlarını ve diğer tehditleri tespit eder. Gerçek zamanlı koruma sağlaması nedeniyle özellikle büyük ölçekli kurumlarda yaygın olarak kullanılmaktadır.

#### Nessus

Nessus, dünyanın en yaygın kullanılan güvenlik açığı tarama araçlarından biridir. Sunucuları, ağ cihazlarını, işletim sistemlerini ve çeşitli servisleri analiz ederek yanlış yapılandırmaları, eksik güvenlik güncellemelerini, açık portları ve bilinen CVE kayıtlarını tespit eder.

#### OpenVAS

OpenVAS (Greenbone Vulnerability Management), açık kaynaklı bir güvenlik açığı tarama platformudur. Ağ üzerindeki cihazları ve sunucuları analiz ederek güvenlik açıklarını belirler. Nessus'a açık kaynaklı bir alternatif olarak değerlendirilmektedir.

#### Prowler

Prowler, AWS ortamlarının güvenlik ve uyumluluk analizini gerçekleştiren açık kaynaklı bir araçtır. AWS hesaplarını tarayarak IAM izinleri, S3 Bucket yapılandırmaları, MFA kullanımı, CloudTrail ayarları ve diğer güvenlik kontrollerini değerlendirir.

#### Red Hat Advanced Cluster Security (RHACS)

RHACS, Kubernetes ve OpenShift ortamlarının güvenliğini sağlamak amacıyla geliştirilmiş kurumsal bir platformdur. Container imajlarını, pod'ları, RBAC yapılandırmalarını, ağ politikalarını ve cluster güvenliğini analiz ederek riskleri belirler.

#### roxctl

roxctl, RHACS platformunun komut satırı (CLI) aracıdır. Güvenlik taramalarını başlatmak, politika kontrollerini gerçekleştirmek ve Kubernetes kümelerini terminal üzerinden yönetmek amacıyla kullanılır.

#### Tenable

Tenable, kurumsal seviyede güvenlik açığı ve maruz kalma yönetimi (Exposure Management) sağlayan kapsamlı bir güvenlik platformudur. Varlık yönetimi, bulut güvenliği, container güvenliği ve güvenlik açığı yönetimi gibi birçok özelliği tek platform üzerinden sunmaktadır. Nessus da Tenable tarafından geliştirilen ürünlerden biridir.<br>

***

### Infrastructure Teknolojilerinin Karşılaştırılması

<table data-search="false"><thead><tr><th>Teknoloji</th><th>Öne Çıkan Özelliği</th></tr></thead><tbody><tr><td><strong>AWS</strong></td><td>En yaygın bulut platformu</td></tr><tr><td><strong>CrowdStrike Falcon</strong></td><td>Endpoint Detection &#x26; Response (EDR) ve gerçek zamanlı tehdit tespiti</td></tr><tr><td><strong>Microsoft Azure</strong></td><td>Microsoft ekosistemiyle tam uyum</td></tr><tr><td><strong>Google Cloud Platform</strong></td><td>Google bulut hizmetleri</td></tr><tr><td><strong>Kubernetes</strong></td><td>Container orkestrasyonu</td></tr><tr><td><strong>Docker</strong></td><td>Container oluşturma ve çalıştırma</td></tr><tr><td><strong>Terraform</strong></td><td>Infrastructure as Code (IaC)</td></tr><tr><td><strong>Ansible</strong></td><td>Yapılandırma yönetimi ve otomasyon</td></tr><tr><td><strong>OpenShift</strong></td><td>Kurumsal Kubernetes platformu</td></tr><tr><td><strong>Nessus</strong></td><td>Sunucu, ağ ve sistemlerde kapsamlı güvenlik açığı taraması</td></tr><tr><td><strong>OpenVAS</strong></td><td>Açık kaynaklı güvenlik açığı tarama platformu</td></tr><tr><td><strong>Prowler</strong></td><td>AWS güvenlik yapılandırmaları ve uyumluluk kontrolleri</td></tr><tr><td><strong>RHACS</strong></td><td>Kubernetes ve OpenShift güvenliği</td></tr><tr><td><strong>roxctl</strong></td><td>RHACS platformunun komut satırı yönetim aracı</td></tr><tr><td><strong>Tenable</strong></td><td>Kurumsal düzeyde vulnerability ve exposure management platformu</td></tr></tbody></table>

***

### SPM ile İlişkisi

SPM platformları Infrastructure modülü sayesinde bulut servislerine, Kubernetes kümelerine ve altyapı yönetim araçlarına bağlanarak güvenlik analizleri gerçekleştirir. Tespit edilen yanlış yapılandırmalar, güvenlik açıkları ve uyumluluk ihlalleri merkezi bir panel üzerinden görüntülenir. Böylece güvenlik ekipleri altyapıdaki riskleri tek noktadan takip edebilir ve gerekli iyileştirmeleri planlayabilir.<br>

***

### Örnek

Bir şirket uygulamalarını AWS üzerinde çalıştırmaktadır. Infrastructure modülü düzenli olarak AWS kaynaklarını analiz eder ve herkese açık erişime izin verilmiş bir S3 Bucket tespit eder. Sistem bu durumu yüksek risk olarak raporlar ve güvenlik ekibine bildirim gönderir. Yapılan düzeltmeyle birlikte erişim yalnızca yetkili kullanıcılarla sınırlandırılarak olası veri sızıntısının önüne geçilir.
