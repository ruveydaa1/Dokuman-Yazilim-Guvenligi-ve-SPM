# Task Management

## Task Management Nedir?

Task Management (Görev Yönetimi), yazılım geliştirme ve güvenlik süreçlerinde ortaya çıkan görevlerin oluşturulmasını, atanmasını, takip edilmesini ve sonuçlandırılmasını sağlayan yönetim sürecidir.

SPM platformlarında Task Management modülü, güvenlik analizleri sonucunda tespit edilen güvenlik açıklarının ilgili ekip veya kişilere görev olarak aktarılmasını sağlar. Böylece güvenlik bulguları yalnızca raporlanmakla kalmaz, çözüm sürecinin tamamı merkezi olarak takip edilebilir.

SAST, DAST, SCA, Secret Scanning, Infrastructure ve Registry gibi güvenlik analizlerinden elde edilen sonuçlar otomatik olarak görevlere dönüştürülebilir ve ilgili ekiplerin aksiyon alması sağlanabilir.<br>

***

## Task Management Nasıl Çalışır?

Task Management modülü, güvenlik analizlerinden elde edilen bulguları takip edilebilir görevlere dönüştürür.

Örneğin;

* Kritik seviyede bir SQL Injection açığı tespit edilmesi
* Eski ve güvenlik açığı bulunan bir bağımlılığın belirlenmesi
* Kaynak kodunda gizli anahtar bulunması
* Cloud ortamında yanlış yapılandırma tespit edilmesi

gibi durumlarda otomatik olarak bir görev oluşturulabilir.

Oluşturulan görevlerde genellikle;

* Güvenlik açığının açıklaması
* Risk seviyesi
* CVSS puanı
* İlgili varlık
* Sorumlu kişi veya ekip
* Son teslim tarihi
* Görev durumu

gibi bilgiler yer alır.

Bu sayede güvenlik açıklarının çözüm süreci baştan sona takip edilebilir.<br>

***

## Task Management'ın Önemi

Güvenlik ekipleri tarafından tespit edilen açıkların yalnızca raporlanması yeterli değildir. Bu açıkların doğru kişilere aktarılması ve belirlenen süre içerisinde giderilmesi gerekir.

Task Management sayesinde;

* Güvenlik açıklarının unutulmasının önüne geçilir.
* Geliştirici ve güvenlik ekipleri arasındaki iletişim kolaylaşır.
* Açıkların çözüm süreci takip edilir.
* Önceliklendirme yapılabilir.
* Güvenlik süreçleri daha düzenli hale gelir.

Bu nedenle birçok kurum Task Management sistemlerini geliştirme ve güvenlik süreçlerinin bir parçası olarak kullanmaktadır.<br>

***

## Avantajları ve Sınırlamaları

### Avantajları

* Güvenlik bulgularını takip edilebilir görevlere dönüştürür.
* Görevlerin sorumlu kişilere atanmasını sağlar.
* Çözüm süreçlerinin merkezi olarak izlenmesine yardımcı olur.
* Geliştirme ve güvenlik ekipleri arasındaki koordinasyonu artırır.
* CI/CD ve güvenlik araçlarıyla entegre çalışabilir.

### Sınırlamaları

* Yanlış yapılandırılan görev kuralları gereksiz görev oluşmasına neden olabilir.
* Çok fazla güvenlik bulgusu yönetim zorluğu oluşturabilir.
* Görevlerin kapatılması için ekiplerin manuel aksiyon alması gerekir.
* Harici görev yönetim sistemlerine bağımlılık oluşturabilir.<br>

***

## Yaygın Kullanılan Task Management Teknolojileri

Task Management sistemleri, güvenlik ekipleri ve yazılım geliştirme ekiplerinin görevleri oluşturması, takip etmesi ve yönetmesi amacıyla kullanılır.

### Jira Cloud

Jira Cloud, Atlassian tarafından geliştirilen popüler bir proje ve görev yönetim platformudur.

SPM platformlarıyla entegre edilerek güvenlik bulgularının otomatik olarak Jira görevlerine dönüştürülmesini sağlar. Ekipler oluşturulan görevleri atayabilir, durumlarını takip edebilir ve çözüm süreçlerini yönetebilir.

### Jira On-Premise

Jira On-Premise, Jira platformunun kurumların kendi sunucuları üzerinde çalıştırdığı sürümüdür.

Özellikle güvenlik politikaları nedeniyle verilerini kendi altyapısında tutmak isteyen kurumlar tarafından tercih edilir. SPM entegrasyonu sayesinde güvenlik bulguları kurum içindeki Jira sistemine aktarılabilir.

### GitHub Issues

GitHub Issues, yazılım projelerinde hata, geliştirme görevi ve güvenlik problemlerinin takip edilmesini sağlayan GitHub özelliğidir.

Kod depolarıyla doğrudan ilişkili çalıştığı için geliştirici ekipler tarafından yaygın olarak kullanılmaktadır.

### GitLab Issues

GitLab Issues, GitLab platformu içerisinde görev ve hata takibi yapılmasını sağlayan bir yönetim aracıdır.

CI/CD süreçleriyle entegre çalışarak geliştirme ve güvenlik süreçlerinin birlikte yönetilmesine yardımcı olur.

### Azure DevOps Boards

Azure DevOps Boards, Microsoft tarafından geliştirilen proje ve görev yönetimi çözümüdür.

Yazılım geliştirme ekiplerinin görevleri planlamasına, takip etmesine ve geliştirme süreçlerini yönetmesine olanak sağlar.

### ServiceNow

ServiceNow, özellikle büyük kurumlarda kullanılan kurumsal seviyede IT Service Management (ITSM) platformudur.

Güvenlik olayları, talepler ve görevlerin merkezi olarak yönetilmesini sağlar.<br>

***

## Task Management Teknolojilerinin Karşılaştırılması

<table data-search="false"><thead><tr><th>Teknoloji</th><th>Öne Çıkan Özellik</th></tr></thead><tbody><tr><td>Jira Cloud</td><td>Bulut tabanlı görev yönetimi ve güvenlik bulgularının otomatik oluşturulması</td></tr><tr><td>Jira On-Premise</td><td>Kurum içi sunucularda çalışan Jira çözümü</td></tr><tr><td>GitHub Issues</td><td>Kod depolarıyla entegre görev takibi</td></tr><tr><td>GitLab Issues</td><td>CI/CD süreçleriyle entegre proje yönetimi</td></tr><tr><td>Azure DevOps Boards</td><td>Microsoft ekosisteminde geliştirme ve görev yönetimi</td></tr><tr><td>ServiceNow</td><td>Kurumsal ITSM ve olay yönetimi</td></tr></tbody></table>

***

## SPM ile İlişkisi

SPM platformlarında Task Management modülü, güvenlik analizlerinden elde edilen bulguların aksiyona dönüştürülmesini sağlar.

SAST, DAST, SCA, Secret Scanning, Infrastructure ve Registry sonuçları merkezi olarak değerlendirilerek ilgili ekip veya kişilere görev olarak atanabilir.

Böylece güvenlik ekipleri yalnızca açıkları tespit etmekle kalmaz, bu açıkların giderilme sürecini de takip ederek güvenlik yönetimini daha etkin hale getirir.
