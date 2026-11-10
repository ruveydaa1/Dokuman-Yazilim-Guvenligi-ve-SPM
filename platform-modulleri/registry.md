# Registry

### Registry Nedir?

Registry, yazılım geliştirme süreçlerinde kullanılan container imajlarının (Container Images), paketlerin veya yazılım bileşenlerinin merkezi olarak saklandığı, yönetildiği ve dağıtıldığı depolama alanıdır. Özellikle Docker ve Kubernetes tabanlı uygulamalarda container imajlarının güvenli bir şekilde saklanması ve dağıtılması için kullanılır.

SPM platformlarında Registry modülü, registry sistemleriyle entegre olarak container imajlarını analiz eder, güvenlik açıklarını tespit eder ve kullanılan imajların güvenlik durumunu merkezi olarak takip etmeyi sağlar.<br>

***

### Registry Nasıl Çalışır?

Yazılım geliştirme sürecinde oluşturulan container imajları bir registry sistemine yüklenir. Registry modülü bu imajları düzenli olarak tarayarak kullanılan işletim sistemi paketlerini, açık kaynak bağımlılıklarını ve yazılım bileşenlerini analiz eder.

Analiz sonucunda;

* Bilinen CVE kayıtları
* CVSS risk puanları
* Güncel olmayan paketler
* Güvenlik açığı bulunan bileşenler
* Yanlış yapılandırmalar

tespit edilerek raporlanır.

Birçok platform yeni bir imaj registry'e yüklendiğinde otomatik tarama başlatabilir veya belirli aralıklarla mevcut imajları yeniden analiz edebilir.<br>

***

### Registry'nin Önemi

Container teknolojilerinin yaygınlaşmasıyla birlikte uygulamaların büyük bölümü Docker imajları üzerinde çalışmaktadır. Güvenlik açığı bulunan tek bir container imajı, aynı imajı kullanan onlarca uygulamayı etkileyebilir.

Registry güvenliği sayesinde güvenlik açığı içeren imajlar henüz üretim ortamına alınmadan tespit edilebilir ve güvenli sürümler kullanılabilir.<br>

***

### Avantajları ve Sınırlamaları

#### Avantajları

* Container imajlarının merkezi olarak yönetilmesini sağlar.
* Güvenlik açıklarını otomatik olarak tespit edebilir.
* Yeni yayınlanan CVE'lere karşı mevcut imajları tekrar analiz edebilir.
* CI/CD süreçleriyle entegre çalışabilir.
* Güvenli container kullanımını destekler.

#### Sınırlamaları

* Yalnızca registry'de bulunan imajları analiz edebilir.
* Yanlış yapılandırılmış registry sistemleri güvenlik riski oluşturabilir.
* Bazı özel veya kapalı bileşenleri analiz edemeyebilir.
* Büyük registry ortamlarında analiz süresi uzayabilir.<br>

***

## Yaygın Kullanılan Registry Platformları

Registry hizmeti sunan birçok platform bulunmaktadır. Bu platformlar container imajlarının güvenli şekilde saklanmasını, dağıtılmasını ve güvenlik analizlerinin yapılmasını sağlar.

#### Docker Hub

Docker Hub, dünyanın en yaygın kullanılan public container registry platformudur. Docker imajlarının paylaşılması, sürümlenmesi ve dağıtılması için kullanılır. Açık kaynak projelerin büyük bölümü Docker Hub üzerinden dağıtılmaktadır.

#### Harbor

Harbor, açık kaynaklı kurumsal container registry platformudur. Kullanıcı yönetimi, rol tabanlı yetkilendirme, imaj imzalama (Image Signing), güvenlik taraması ve replikasyon gibi gelişmiş özellikler sunar. Kurumsal ortamlarda oldukça yaygın kullanılmaktadır.

#### GitHub Container Registry (GHCR)

GitHub Container Registry, GitHub tarafından sunulan container registry hizmetidir. GitHub Actions ile doğrudan entegre çalışabilir ve container imajlarının GitHub üzerinden güvenli şekilde yönetilmesini sağlar.

#### GitLab Container Registry

GitLab Container Registry, GitLab platformuna entegre çalışan registry hizmetidir. CI/CD süreçleriyle birlikte kullanılabilir ve oluşturulan container imajlarının otomatik olarak saklanmasını sağlar.

#### Azure Container Registry (ACR)

Azure Container Registry, Microsoft Azure tarafından sunulan yönetilen container registry hizmetidir. Azure Kubernetes Service (AKS) başta olmak üzere Azure servisleriyle tam entegre çalışır.

#### Amazon Elastic Container Registry (Amazon ECR)

Amazon ECR, AWS tarafından sunulan yönetilen container registry hizmetidir. Amazon ECS ve Amazon EKS ile entegre çalışarak container tabanlı uygulamaların güvenli şekilde dağıtılmasını sağlar.

#### Google Artifact Registry

Google Artifact Registry, Google Cloud Platform üzerinde çalışan container ve paket yönetim platformudur. Docker imajlarının yanı sıra Maven, npm ve Python paketlerini de yönetebilir.

#### JFrog Artifactory

JFrog Artifactory, yalnızca container registry değil, aynı zamanda farklı paket türlerini de yönetebilen kurumsal artifact yönetim platformudur. Docker, Maven, npm, NuGet ve birçok paket yöneticisini destekler.<br>

***

### Registry Platformlarının Karşılaştırılması

<table data-search="false"><thead><tr><th>Platform</th><th>Öne Çıkan Özelliği</th></tr></thead><tbody><tr><td><strong>Docker Hub</strong></td><td>En yaygın kullanılan public container registry</td></tr><tr><td><strong>Harbor</strong></td><td>Açık kaynak kurumsal registry ve güvenlik taraması</td></tr><tr><td><strong>GitHub Container Registry</strong></td><td>GitHub ile tam entegrasyon</td></tr><tr><td><strong>GitLab Container Registry</strong></td><td>GitLab CI/CD entegrasyonu</td></tr><tr><td><strong>Azure Container Registry</strong></td><td>Azure servisleriyle tam uyum</td></tr><tr><td><strong>Amazon ECR</strong></td><td>AWS container servisleriyle entegrasyon</td></tr><tr><td><strong>Google Artifact Registry</strong></td><td>Container ve paket yönetimi</td></tr><tr><td><strong>JFrog Artifactory</strong></td><td>Kurumsal artifact ve registry yönetimi</td></tr></tbody></table>

***

### SPM ile İlişkisi

SPM platformları Registry modülü sayesinde container registry sistemlerine bağlanarak kullanılan imajları sürekli analiz eder. Tespit edilen güvenlik açıkları CVE, CVSS ve diğer güvenlik bulgularıyla ilişkilendirilerek merkezi bir panel üzerinden görüntülenir. Böylece güvenlik ekipleri hangi container imajlarının risk taşıdığını kolayca takip edebilir ve gerekli güncellemeleri planlayabilir.<br>

***

### Örnek

Bir yazılım ekibi Docker imajlarını Harbor registry üzerinde saklamaktadır. Yeni oluşturulan bir imaj registry'e yüklendiğinde SPM platformu otomatik olarak tarama başlatır. Analiz sonucunda kullanılan Linux paketlerinden birinde kritik seviyede bir CVE bulunduğu tespit edilir. Sistem güvenlik ekibine bildirim gönderir ve ilgili imajın güncellenmesi önerilir.
