# Version Control

### Version Control Nedir?

Version Control (Sürüm Kontrolü), yazılım projelerinde kaynak kodunun, yapılandırma dosyalarının ve diğer proje dosyalarının zaman içerisindeki değişikliklerini takip etmeyi sağlayan sistemdir. Geliştiricilerin aynı proje üzerinde birlikte çalışmasına, yapılan değişikliklerin kayıt altına alınmasına ve gerektiğinde önceki sürümlere geri dönülmesine olanak tanır.

SPM platformlarında Version Control modülü; Git tabanlı sürüm kontrol sistemleriyle entegre çalışarak kaynak kodunu, commit geçmişini ve pull request süreçlerini analiz eder. Böylece güvenlik açıkları, yanlışlıkla paylaşılan hassas bilgiler ve riskli kod değişiklikleri merkezi olarak takip edilebilir.<br>

***

### Version Control Nasıl Çalışır?

Geliştiriciler yaptıkları değişiklikleri commit ederek sürüm kontrol sistemine gönderir. Daha sonra bu değişiklikler GitHub, GitLab veya Bitbucket gibi platformlara push edilir.

SPM platformu, sürüm kontrol sistemiyle entegre olarak;

* Kaynak kodunu analiz eder.
* Yeni commit'leri takip eder.
* Pull Request (PR) süreçlerini inceleyebilir.
* Secret Scanning sonuçlarını görüntüleyebilir.
* SAST ve SCA analizlerini tetikleyebilir.
* Güvenlik açıklarını ilgili commit veya geliştiriciyle ilişkilendirebilir.

Bu sayede güvenlik sorunları daha kod geliştirme aşamasındayken tespit edilebilir.<br>

***

### Version Control'ün Önemi

Modern yazılım geliştirme süreçlerinde tüm kod değişiklikleri sürüm kontrol sistemleri üzerinden gerçekleştirilmektedir. Güvenlik kontrollerinin de bu sürece dahil edilmesi, güvenlik açıklarının erken aşamada tespit edilmesini sağlar.

Version Control entegrasyonu sayesinde güvenlik ekipleri yalnızca mevcut kaynak kodunu değil, geçmiş değişiklikleri de inceleyebilir. Böylece güvenlik açıklarının hangi commit ile eklendiği veya hangi geliştirici tarafından yapıldığı kolayca takip edilebilir.<br>

***

### Avantajları ve Sınırlamaları

#### Avantajları

* Kaynak kodundaki değişiklikleri takip eder.
* Ekip çalışmasını kolaylaştırır.
* Güvenlik analizlerinin otomatik olarak çalıştırılmasını sağlar.
* Commit geçmişini inceleyebilir.
* CI/CD süreçleriyle entegre çalışabilir.

#### Sınırlamaları

* Yanlış yapılandırılmış erişim izinleri güvenlik riski oluşturabilir.
* Hassas bilgiler yanlışlıkla commit edilebilir.
* Büyük projelerde geçmiş analizleri zaman alabilir.
* Eski commit'lerde bulunan güvenlik riskleri manuel müdahale gerektirebilir.<br>

***

### Yaygın Kullanılan Version Control Platformları

Version Control sistemleri için farklı platformlar kullanılmaktadır. Bu platformlar yalnızca kod saklamakla kalmaz; kod inceleme, CI/CD, güvenlik analizi ve ekip yönetimi gibi birçok özelliği de destekler.

#### Git

Git, en yaygın kullanılan dağıtık sürüm kontrol sistemidir. Kaynak kodundaki tüm değişiklikleri takip eder, geliştiricilerin aynı proje üzerinde eş zamanlı çalışmasını sağlar ve sürüm geçmişini korur. Günümüzde neredeyse tüm modern yazılım projeleri Git kullanmaktadır.

#### GitHub

GitHub, Git tabanlı en popüler sürüm kontrol platformudur. Kod depolamanın yanı sıra Pull Request, GitHub Actions, Secret Scanning, CodeQL ve Dependabot gibi güvenlik ve otomasyon özellikleri sunar.

#### GitLab

GitLab, Git tabanlı kapsamlı bir DevOps platformudur. Kaynak kodu yönetiminin yanında CI/CD, güvenlik testleri, container registry ve proje yönetimi gibi birçok özelliği tek platformda sunar.

#### Bitbucket

Bitbucket, Atlassian tarafından geliştirilen Git tabanlı sürüm kontrol platformudur. Özellikle Jira ve Confluence ile güçlü entegrasyonu sayesinde kurumsal yazılım ekipleri tarafından yaygın olarak kullanılmaktadır.

#### Azure DevOps Repos

Azure DevOps Repos, Microsoft Azure DevOps platformunun Git tabanlı sürüm kontrol hizmetidir. Azure Pipelines, Boards ve diğer Azure DevOps servisleriyle entegre çalışarak kurumsal yazılım geliştirme süreçlerini destekler.<br>

***

### Version Control Platformlarının Karşılaştırılması

| Platform               | Öne Çıkan Özelliği                                |
| ---------------------- | ------------------------------------------------- |
| **Git**                | En yaygın dağıtık sürüm kontrol sistemi           |
| **GitHub**             | Kod yönetimi, güvenlik araçları ve GitHub Actions |
| **GitLab**             | DevOps ve CI/CD entegrasyonu                      |
| **Bitbucket**          | Jira ve Atlassian ürünleriyle entegrasyon         |
| **Azure DevOps Repos** | Microsoft ekosistemiyle tam uyum                  |

***

### SPM ile İlişkisi

SPM platformları Version Control modülü sayesinde Git tabanlı depolara bağlanarak kaynak kodunu ve değişiklik geçmişini analiz eder. SAST, Secret Scanning ve SCA gibi güvenlik analizlerinden elde edilen sonuçlar ilgili commit'ler ve geliştiricilerle ilişkilendirilir. Böylece güvenlik ekipleri riskleri tek bir platform üzerinden takip edebilir ve güvenlik açıklarının kaynağını daha hızlı belirleyebilir.<br>

***

### Örnek

Bir geliştirici GitHub üzerinde bulunan projeye yeni bir commit gönderir. Commit içerisinde yanlışlıkla bir API anahtarı bulunduğunu düşünelim. Version Control modülü bu değişikliği algılar ve Secret Scanning analizini tetikler. Analiz sonucunda hassas bilgi tespit edilirse geliştirici ve güvenlik ekibi bilgilendirilir. Aynı zamanda ilgili commit, SPM platformunda riskli değişiklik olarak işaretlenebilir.
