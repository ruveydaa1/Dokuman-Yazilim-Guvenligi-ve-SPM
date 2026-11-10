# SBOM Management

### SBOM Management Nedir?

SBOM Management, yazılımlara ait Software Bill of Materials (SBOM) kayıtlarının oluşturulması, saklanması, güncellenmesi ve yönetilmesini sağlayan süreçlerin bütünüdür. Amaç, uygulamalarda kullanılan tüm yazılım bileşenlerini yaşam döngüsü boyunca takip etmek ve bu bileşenlerle ilgili güvenlik, lisans ve uyumluluk süreçlerini etkin bir şekilde yönetmektir.

Yazılım projeleri zaman içerisinde sürekli olarak güncellenir. Yeni bağımlılıklar eklenebilir, mevcut paketler güncellenebilir veya bazı bileşenler kaldırılabilir. Bu nedenle oluşturulan SBOM kayıtlarının da güncel tutulması gerekir. SBOM Management, bu değişikliklerin takip edilmesini ve yazılım bileşenlerinin sürekli izlenmesini sağlar.<br>

***

### SBOM Management Nasıl Çalışır?

SBOM Management çözümleri, uygulamalardan elde edilen SBOM verilerini merkezi bir ortamda toplar ve yönetir. Bu süreçte gerçekleştirilen temel işlemler şunlardır:

* SBOM dosyalarının oluşturulması ve saklanması
* Yazılım bileşenlerindeki değişikliklerin takip edilmesi
* Güncel olmayan veya riskli bileşenlerin belirlenmesi
* Güvenlik açıklarının ilgili bileşenlerle eşleştirilmesi
* Lisans ve uyumluluk kontrollerinin gerçekleştirilmesi
* Raporlama ve izleme süreçlerinin yönetilmesi

Bu sayede kurumlar, yazılım portföylerinde bulunan tüm bileşenleri tek bir platform üzerinden takip edebilir.<br>

***

### SBOM Management'ın Önemi

Bir kurumda yüzlerce uygulama ve binlerce yazılım bileşeni bulunabilir. Bu bileşenlerin manuel olarak takip edilmesi oldukça zor ve hata yapmaya açıktır.

SBOM Management sayesinde kurumlar, hangi uygulamada hangi bileşenin kullanıldığını, hangi sürümün yüklü olduğunu ve bu bileşenlerde bilinen güvenlik açıklarının bulunup bulunmadığını kolayca görebilir. Böylece güvenlik ekipleri riskleri daha hızlı değerlendirebilir ve gerekli güncellemeleri planlayabilir.<br>

***

### SPM ile İlişkisi

SPM platformları, SBOM Management yeteneklerini kullanarak yazılım bileşenlerini sürekli olarak izler ve bu bileşenleri güvenlik açıkları, CVE kayıtları ve CVSS risk puanlarıyla ilişkilendirir.

Bu sayede yalnızca bir bileşenin varlığı değil, o bileşenin oluşturabileceği güvenlik riski de merkezi olarak takip edilebilir. Ayrıca güvenlik ekipleri, kritik seviyedeki bileşenleri önceliklendirerek daha etkili bir risk yönetimi gerçekleştirebilir.<br>

***

### Örnek

Bir kurumun geliştirdiği web uygulamasında **Express 4.17.1** sürümü kullanılmaktadır. Daha sonra bu sürüm için kritik bir güvenlik açığı yayımlanmıştır.

SBOM Management sistemi, uygulamanın SBOM kaydını inceleyerek bu sürümün kullanıldığını tespit eder ve ilgili güvenlik açığını uygulamayla ilişkilendirir. Böylece güvenlik ekibi hangi uygulamanın etkilendiğini hızlı bir şekilde belirleyebilir ve gerekli güncelleme işlemlerini planlayabilir.
