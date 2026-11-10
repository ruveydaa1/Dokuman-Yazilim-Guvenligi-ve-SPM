# Manual

## Manual Nedir?

Manual (Manuel Güvenlik Testi), güvenlik açıklarının otomatik araçlar yerine güvenlik uzmanları tarafından manuel olarak incelenmesini ve doğrulanmasını ifade eder.

Otomatik güvenlik tarama araçları birçok güvenlik açığını hızlı şekilde tespit edebilse de bazı karmaşık güvenlik problemlerini anlamak ve doğrulamak için uzman analizi gereklidir.

SPM platformlarında Manual modülü, otomatik taramalar sonucunda elde edilen bulguların manuel olarak incelenmesini, doğrulanmasını ve takip edilmesini sağlar.

Özellikle penetrasyon testleri, güvenlik değerlendirmeleri ve özel test senaryolarında manuel analizler önemli bir rol oynar.<br>

***

## Manual Nasıl Çalışır?

Manuel güvenlik testlerinde uzmanlar, uygulamaları ve sistemleri gerçek bir saldırganın davranışlarını taklit ederek inceler.

Test süreçlerinde genellikle;

* Uygulama davranışlarının incelenmesi
* Kullanıcı yetkilendirme kontrollerinin test edilmesi
* API güvenlik kontrollerinin yapılması
* İş mantığı açıklarının araştırılması
* Oturum yönetimi kontrollerinin gerçekleştirilmesi
* Otomatik araçların bulamadığı güvenlik problemlerinin aranması

gibi işlemler gerçekleştirilir.

Manuel test sonucunda bulunan güvenlik açıkları raporlanarak ilgili ekiplerin düzeltme yapması sağlanır.<br>

***

## Manual'ın Önemi

Otomatik güvenlik araçları hızlı analiz yapabilse de her güvenlik açığını tespit edemez. Özellikle uygulamanın iş mantığıyla ilgili problemler veya karmaşık saldırı senaryoları uzman değerlendirmesi gerektirir.

Manuel güvenlik testleri sayesinde;

* Daha kapsamlı güvenlik değerlendirmesi yapılır.
* Otomatik araçların kaçırdığı açıklar bulunabilir.
* Gerçek saldırı senaryolarına daha yakın testler gerçekleştirilir.
* Güvenlik açıklarının etkisi daha doğru şekilde değerlendirilir.

Bu nedenle birçok kurum otomatik güvenlik taramalarını manuel güvenlik testleriyle desteklemektedir.<br>

***

## Avantajları ve Sınırlamaları

### Avantajları

* Karmaşık güvenlik açıklarını tespit edebilir.
* İş mantığı kaynaklı problemleri ortaya çıkarabilir.
* Gerçek saldırı senaryolarına daha yakın analiz yapar.
* Otomatik araçların sonuçlarını doğrulamaya yardımcı olur.
* Uzman değerlendirmesi sayesinde daha doğru risk analizi sağlar.

### Sınırlamaları

* Uzman bilgisi ve deneyimi gerektirir.
* Otomatik testlere göre daha uzun sürebilir.
* İnsan hatasına bağlı sonuç farklılıkları oluşabilir.
* Büyük sistemlerde kapsamlı test yapmak zaman alabilir.<br>

***

## Yaygın Kullanılan Manual Teknolojileri

Manuel güvenlik testlerinde uzmanlar, sistemleri analiz etmek ve güvenlik açıklarını doğrulamak için çeşitli araçlardan yararlanır.

### Burp Suite

Burp Suite, web uygulamalarının güvenlik testlerinde en yaygın kullanılan araçlardan biridir.

Bir proxy görevi görerek tarayıcı ile web uygulaması arasındaki HTTP/HTTPS trafiğini analiz etmeyi sağlar.

Kullanıcı isteklerini değiştirme, güvenlik açıklarını doğrulama ve web uygulaması davranışlarını inceleme amacıyla kullanılır.

Özellikle;

* SQL Injection
* XSS
* Authentication açıkları
* Session problemleri
* API güvenlik testleri

gibi kontrollerde yaygın olarak tercih edilir.

### OWASP ZAP

OWASP ZAP (Zed Attack Proxy), OWASP tarafından geliştirilen açık kaynaklı bir web güvenlik test aracıdır.

Proxy olarak çalışarak uygulama trafiğini analiz eder ve güvenlik testlerinde kullanılır.

Manuel test süreçlerinde istekleri inceleme, değiştirme ve güvenlik açıklarını doğrulama amacıyla kullanılabilir.

### Metasploit Framework

Metasploit Framework, güvenlik uzmanları tarafından penetrasyon testlerinde kullanılan popüler bir platformdur.

Bilinen güvenlik açıklarını test etmek, saldırı senaryolarını simüle etmek ve güvenlik kontrollerini doğrulamak amacıyla kullanılır.

### Nmap

Nmap (Network Mapper), ağ keşfi ve güvenlik değerlendirmelerinde kullanılan açık kaynaklı bir araçtır.

Ağ üzerindeki cihazları, açık portları ve çalışan servisleri belirlemek için kullanılır.

Güvenlik testlerinde hedef sistem hakkında bilgi toplamak amacıyla yaygın olarak tercih edilir.

### Wireshark

Wireshark, ağ trafiğini analiz etmek için kullanılan güçlü bir paket analiz aracıdır.

Ağ üzerinden geçen veri paketlerini inceleyerek iletişim problemlerinin ve güvenlik risklerinin analiz edilmesini sağlar.

### Kali Linux

Kali Linux, penetrasyon testi ve güvenlik araştırmaları için hazırlanmış Linux dağıtımıdır.

İçerisinde Nmap, Metasploit, Burp Suite ve birçok güvenlik test aracını barındırır.

Güvenlik uzmanları tarafından test ortamlarında yaygın olarak kullanılmaktadır.<br>

***

## Manual Güvenlik Araçlarının Karşılaştırılması

| Teknoloji            | Öne Çıkan Özellik                                                 |
| -------------------- | ----------------------------------------------------------------- |
| Burp Suite           | Web uygulamalarında manuel güvenlik testi ve HTTP trafiği analizi |
| OWASP ZAP            | Açık kaynak web güvenlik testi ve proxy analizi                   |
| Metasploit Framework | Penetrasyon testi ve güvenlik açığı doğrulama                     |
| Nmap                 | Ağ keşfi ve servis taraması                                       |
| Wireshark            | Ağ paket analizi ve trafik inceleme                               |
| Kali Linux           | Güvenlik test araçlarını bir arada sunan işletim sistemi          |

***

## SPM ile İlişkisi

SPM platformlarında Manual modülü, otomatik güvenlik analizlerinden elde edilen sonuçların uzmanlar tarafından incelenmesini ve yönetilmesini sağlar.

SAST, DAST, SCA, Secret Scanning, Infrastructure ve Registry gibi modüllerden gelen bulgular manuel olarak doğrulanabilir, önceliklendirilebilir ve ilgili ekiplerle paylaşılabilir.

Bu yaklaşım sayesinde otomatik analizlerin sağladığı hız ile uzman değerlendirmesinin sağladığı doğruluk birleştirilerek daha kapsamlı bir güvenlik yönetimi oluşturulur.
