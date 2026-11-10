# Notification

### Notification Nedir?

Notification (Bildirim), SPM platformlarında tespit edilen güvenlik olaylarının, güvenlik açıklarının ve sistem uyarılarının ilgili kişi veya ekiplere otomatik olarak iletilmesini sağlayan modüldür. Güvenlik süreçlerinde zamanında bilgilendirme yapılması, risklerin hızlı bir şekilde değerlendirilmesi ve gerekli aksiyonların alınabilmesi açısından önemli bir rol oynar.

SPM platformlarında Notification modülü; güvenlik taramaları, yeni bulunan zafiyetler, başarısız taramalar, politika ihlalleri ve diğer önemli olaylar hakkında kullanıcılara otomatik bildirim gönderebilir.<br>

***

### Notification Nasıl Çalışır?

Notification modülü, platform üzerinde gerçekleşen olayları sürekli olarak izler. Önceden tanımlanan kurallar doğrultusunda belirli bir olay gerçekleştiğinde ilgili kullanıcılara veya ekiplere bildirim gönderir.

Örneğin;

* Yeni bir kritik CVE tespit edilmesi
* SAST veya DAST analizinin başarısız olması
* Secret Scanning sonucunda hassas bilgi bulunması
* Container imajında kritik güvenlik açığı belirlenmesi
* Altyapıda yanlış yapılandırma tespit edilmesi

gibi durumlarda sistem otomatik olarak bildirim oluşturabilir.

Bildirimler e-posta, mesajlaşma platformları veya webhook entegrasyonları aracılığıyla iletilebilir.<br>

***

### Notification'ın Önemi

Güvenlik açıklarının yalnızca tespit edilmesi yeterli değildir. Bu açıkların ilgili kişilere zamanında iletilmesi ve gerekli aksiyonların hızlı şekilde alınması gerekir.

Notification modülü sayesinde güvenlik ekipleri kritik olaylardan anında haberdar olur ve güvenlik risklerine daha kısa sürede müdahale edebilir. Bu da olası güvenlik ihlallerinin etkisini azaltır.<br>

***

### Avantajları ve Sınırlamaları

#### Avantajları

* Güvenlik olaylarını anlık olarak bildirir.
* Müdahale süresini kısaltır.
* Farklı iletişim platformlarıyla entegre çalışabilir.
* Bildirim kuralları özelleştirilebilir.
* Güvenlik süreçlerinin sürekli izlenmesini destekler.

#### Sınırlamaları

* Yanlış yapılandırılan kurallar gereksiz bildirimlere neden olabilir.
* Çok fazla bildirim gönderilmesi kullanıcıların önemli uyarıları gözden kaçırmasına yol açabilir.
* Harici bildirim servislerine bağımlılık oluşabilir.
* Bildirimlerin alınması internet bağlantısı veya ilgili servislerin çalışmasına bağlıdır.<br>

***

## Yaygın Kullanılan Notification Teknolojileri

Notification modülleri farklı iletişim platformlarıyla entegre çalışarak güvenlik olaylarının ilgili kişilere iletilmesini sağlar.

#### SMTP (Simple Mail Transfer Protocol)

SMTP (Simple Mail Transfer Protocol), e-posta gönderimi için kullanılan standart iletişim protokolüdür. SPM platformları SMTP entegrasyonu sayesinde kurumların kendi e-posta sunucuları veya Gmail, Microsoft 365 gibi e-posta servisleri üzerinden otomatik bildirim gönderebilir. Güvenlik tarama sonuçları, kritik zafiyetler, politika ihlalleri ve diğer sistem uyarıları belirlenen e-posta adreslerine güvenli bir şekilde iletilir.

#### E-posta (Email Notifications)

E-posta, en yaygın kullanılan bildirim yöntemlerinden biridir. Güvenlik açıkları, analiz sonuçları ve sistem uyarıları doğrudan ilgili kullanıcıların e-posta adreslerine gönderilebilir.

#### Slack

Slack, ekip içi iletişim amacıyla kullanılan popüler bir mesajlaşma platformudur. Notification modülü Slack kanallarıyla entegre çalışarak güvenlik olaylarını ilgili ekiplere anlık olarak iletebilir.

#### Microsoft Teams

Microsoft Teams, özellikle kurumsal ortamlarda yaygın olarak kullanılan iş birliği platformudur. Güvenlik bildirimleri belirlenen Teams kanallarına gönderilerek ekiplerin hızlı şekilde bilgilendirilmesi sağlanabilir.

#### Discord

Discord, topluluklar ve geliştirme ekipleri tarafından kullanılan iletişim platformudur. Bazı SPM platformları Discord entegrasyonu sayesinde güvenlik olaylarını belirlenen sunuculara veya kanallara iletebilir.

#### Webhook

Webhook, farklı sistemler arasında gerçek zamanlı veri aktarımı sağlayan entegrasyon yöntemidir. Notification modülü, belirli olaylar gerçekleştiğinde başka uygulamalara otomatik HTTP istekleri göndererek güvenlik süreçlerinin otomatikleştirilmesini sağlar.

#### PagerDuty

PagerDuty, kritik sistem olaylarının yönetimi için geliştirilen profesyonel bir Incident Management platformudur. Özellikle yüksek öncelikli güvenlik olaylarında ilgili ekipleri anında bilgilendirerek hızlı müdahale edilmesini sağlar.

#### Opsgenie

Opsgenie, Atlassian tarafından geliştirilen olay yönetimi ve bildirim platformudur. Güvenlik ekiplerinin kritik olayları takip etmesine, görev atamalarına ve olay yönetimi süreçlerini organize etmesine yardımcı olur.<br>

***

### Notification Teknolojilerinin Karşılaştırılması

<table data-search="false"><thead><tr><th>Teknoloji</th><th>Öne Çıkan Özelliği</th></tr></thead><tbody><tr><td><strong>SMTP</strong></td><td>E-posta bildirimlerinin standart protokol üzerinden otomatik olarak gönderilmesini sağlar.</td></tr><tr><td><strong>E-posta</strong></td><td>En yaygın bildirim yöntemi</td></tr><tr><td><strong>Slack</strong></td><td>Gerçek zamanlı ekip iletişimi</td></tr><tr><td><strong>Microsoft Teams</strong></td><td>Kurumsal ekip iletişimi</td></tr><tr><td><strong>Discord</strong></td><td>Topluluk ve geliştirme ekipleri için bildirim</td></tr><tr><td><strong>Webhook</strong></td><td>Sistemler arası otomatik entegrasyon</td></tr><tr><td><strong>PagerDuty</strong></td><td>Kritik olay ve alarm yönetimi</td></tr><tr><td><strong>Opsgenie</strong></td><td>Olay yönetimi ve ekip koordinasyonu</td></tr></tbody></table>

***

### SPM ile İlişkisi

SPM platformlarında Notification modülü, güvenlik analizlerinden elde edilen bulguların ilgili kişi ve ekiplere zamanında iletilmesini sağlar. SAST, DAST, SCA, Secret Scanning, Infrastructure ve Registry analizlerinden elde edilen kritik sonuçlar merkezi olarak değerlendirilir ve önceden belirlenen kurallara göre otomatik bildirimler oluşturulur. Böylece güvenlik ekipleri risklere daha hızlı müdahale edebilir.
