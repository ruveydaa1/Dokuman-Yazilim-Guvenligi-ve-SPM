# Upload

## Upload Nedir?

Upload (Yükleme), farklı güvenlik araçlarından elde edilen analiz sonuçlarının veya raporların bir SPM platformuna manuel olarak aktarılmasını sağlayan entegrasyon yöntemidir.

Güvenlik ekipleri farklı araçlar kullanarak SAST, DAST, SCA, Vulnerability Scanning, Secret Scanning ve diğer güvenlik analizlerini gerçekleştirebilir. Bu araçlardan elde edilen sonuçlar genellikle JSON, XML, CSV veya SARIF gibi formatlarda dışarı aktarılır ve Upload yöntemiyle merkezi güvenlik platformuna yüklenebilir.

Bu sayede farklı güvenlik araçlarından gelen bulgular tek bir platform üzerinden takip edilebilir ve güvenlik riskleri merkezi olarak yönetilebilir.<br>

***

## Upload Nasıl Çalışır?

Upload sürecinde öncelikle güvenlik aracından analiz raporu alınır. Daha sonra bu rapor SPM platformuna yüklenerek sistem tarafından işlenir.

Genel süreç şu şekilde ilerler:

Güvenlik aracı tarafından tarama gerçekleştirilir.

↓

Analiz sonucu rapor dosyası oluşturulur.

↓

Rapor SPM platformuna yüklenir.

↓

Sistem rapordaki güvenlik bulgularını analiz eder.

↓

Bulgular ilgili varlıklar, risk seviyeleri ve güvenlik kategorileriyle ilişkilendirilir.

Upload işlemlerinde desteklenen yaygın rapor formatları:

* JSON
* XML
* CSV
* SARIF
* PDF

şeklindedir.<br>

***

## Upload'ın Önemi

Kurumlar genellikle tek bir güvenlik aracı yerine farklı ihtiyaçlar için farklı çözümler kullanmaktadır.

Örneğin;

* SAST için SonarQube veya Semgrep
* DAST için OWASP ZAP veya Burp Suite
* SCA için Dependency-Check veya Trivy
* Vulnerability Management için Nessus veya OpenVAS

gibi farklı araçlardan elde edilen sonuçların tek bir platformda toplanması gerekir.

Upload özelliği sayesinde farklı güvenlik araçlarının sonuçları merkezi olarak yönetilebilir ve güvenlik ekipleri tüm riskleri tek noktadan takip edebilir.<br>

***

## Avantajları ve Sınırlamaları

### Avantajları

* Farklı güvenlik araçlarından gelen raporların merkezi olarak yönetilmesini sağlar.
* Çok sayıda güvenlik aracını destekleyebilir.
* Mevcut güvenlik süreçlerine kolayca dahil edilebilir.
* Harici araçlardan elde edilen sonuçların tek platformda görüntülenmesini sağlar.
* Otomatik entegrasyon bulunmayan araçlar için alternatif çözüm sunar.

### Sınırlamaları

* Raporların manuel olarak yüklenmesi zaman alabilir.
* Gerçek zamanlı veri aktarımı sağlamayabilir.
* Desteklenmeyen dosya formatları analiz edilemeyebilir.
* Güncel sonuçlar için düzenli olarak yeni raporların yüklenmesi gerekir.<br>

***

## Yaygın Kullanılan Upload Kaynakları

Upload yöntemi, birçok güvenlik aracından elde edilen raporların SPM platformuna aktarılmasını sağlayabilir.

### SonarQube

SonarQube, kod kalitesi ve güvenlik analizleri gerçekleştiren bir platformdur.

SAST analiz sonuçları dışarı aktarılıp Upload yöntemiyle merkezi güvenlik platformlarına aktarılabilir.

### OWASP ZAP

OWASP ZAP, web uygulamalarında güvenlik testleri gerçekleştiren açık kaynaklı bir DAST aracıdır.

Tarama sonuçları XML, JSON veya HTML formatlarında dışarı aktarılabilir ve güvenlik bulgularının merkezi olarak takip edilmesi sağlanabilir.

### Nessus

Nessus, sistem ve ağ güvenlik açıklarını tespit etmek için kullanılan yaygın bir vulnerability scanner aracıdır.

Tarama sonuçları rapor formatında dışarı aktarılabilir ve güvenlik yönetim platformlarına aktarılabilir.

### OpenVAS

OpenVAS, açık kaynaklı güvenlik açığı tarama platformudur.

Ağ ve sistem taramalarından elde edilen sonuçlar farklı formatlarda dışarı aktarılarak merkezi güvenlik yönetimi süreçlerinde kullanılabilir.

### Trivy

Trivy, container image, dosya sistemi, dependency ve Kubernetes ortamlarını analiz edebilen açık kaynaklı güvenlik tarayıcısıdır.

Bulduğu güvenlik açıkları raporlanarak Upload yöntemiyle güvenlik platformlarına aktarılabilir.

### Semgrep

Semgrep, kaynak kodu üzerinde güvenlik analizi gerçekleştiren popüler bir SAST aracıdır.

Kod analiz sonuçları dışarı aktarılarak merkezi güvenlik yönetim sistemlerinde takip edilebilir.<br>

***

## Upload Kaynaklarının Karşılaştırılması

| Teknoloji | Öne Çıkan Özellik                                     |
| --------- | ----------------------------------------------------- |
| SonarQube | Kod kalitesi ve SAST analiz sonuçlarının aktarılması  |
| OWASP ZAP | Web uygulaması güvenlik test sonuçlarının aktarılması |
| Nessus    | Sistem ve ağ güvenlik açıklarının raporlanması        |
| OpenVAS   | Açık kaynak vulnerability tarama sonuçları            |
| Trivy     | Container ve dependency güvenlik analizleri           |
| Semgrep   | Kaynak kod güvenlik analiz sonuçları                  |

***

## SPM ile İlişkisi

SPM platformlarında Upload modülü, farklı güvenlik araçlarından elde edilen sonuçların merkezi olarak toplanmasını sağlar.

SAST, DAST, SCA, Secret Scanning, Infrastructure ve Vulnerability Management araçlarından gelen raporlar sisteme aktarılır ve tek bir güvenlik görünümü oluşturulur.

Bu sayede güvenlik ekipleri farklı araçlarda bulunan güvenlik bulgularını ayrı ayrı takip etmek yerine, tüm riskleri merkezi bir platform üzerinden değerlendirebilir.<br>

***

## Örnek

Bir şirket web uygulamasını güvenlik açısından test etmek için OWASP ZAP kullanmaktadır.

Tarama sonucunda ZAP tarafından oluşturulan JSON raporu SPM platformuna yüklenir.

Sistem raporu analiz ederek bulunan güvenlik açıklarını önem derecelerine göre sınıflandırır.

Örneğin;

| Açık                  | Risk Seviyesi |
| --------------------- | ------------- |
| SQL Injection         | Critical      |
| XSS                   | High          |
| Eksik Security Header | Medium        |

şeklinde sonuçlar oluşturulur.

Böylece farklı araçlardan gelen güvenlik sonuçları tek bir platform üzerinden takip edilebilir.
