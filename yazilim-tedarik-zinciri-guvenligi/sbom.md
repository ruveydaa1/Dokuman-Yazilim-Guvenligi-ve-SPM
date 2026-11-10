# SBOM

### SBOM Nedir?

SBOM (Software Bill of Materials), bir yazılımın içerisinde bulunan tüm bileşenleri, kütüphaneleri, bağımlılıkları ve bunların sürüm bilgilerini listeleyen standart bir envanterdir. Bir yazılımın hangi açık kaynak veya üçüncü taraf bileşenleri kullandığını göstererek yazılımın içeriğini görünür hale getirir.

Yazılım geliştirme süreçlerinde uygulamalar yalnızca geliştiricilerin yazdığı kodlardan oluşmaz. Çoğu uygulama; açık kaynak kütüphaneler, paket yöneticileri ve üçüncü taraf bileşenler kullanılarak geliştirilir. Bu nedenle kullanılan tüm bileşenlerin bilinmesi, güvenlik ve bakım süreçleri açısından büyük önem taşır.<br>

***

### SBOM Nasıl Çalışır?

SBOM, uygulama geliştirme sürecinde kullanılan bağımlılıkları analiz ederek bunların bir listesini oluşturur. Bu listede her bileşen için genellikle aşağıdaki bilgiler yer alır:

* Bileşen adı
* Sürüm bilgisi
* Üretici veya sağlayıcı bilgisi
* Lisans bilgisi
* Bileşenler arasındaki bağımlılık ilişkileri

Bu bilgiler sayesinde uygulamanın hangi yazılım bileşenlerinden oluştuğu ayrıntılı olarak görülebilir.<br>

***

### SBOM'un Önemi

Bir güvenlik açığı duyurulduğunda kurumların ilk olarak etkilenen yazılım bileşenlerini belirlemesi gerekir. Eğer uygulamanın kullandığı bileşenler bilinmiyorsa hangi sistemlerin risk altında olduğu da kolayca tespit edilemez.

SBOM sayesinde kurumlar, uygulamalarında kullanılan tüm bileşenleri merkezi olarak görüntüleyebilir ve güvenlik açıklarından etkilenen bileşenleri hızlı bir şekilde belirleyebilir. Ayrıca lisans yönetimi, güncelleme planlaması ve uyumluluk süreçlerinde de önemli kolaylıklar sağlar.<br>

***

### SPM ile İlişkisi

SPM platformları, uygulamalara ait SBOM bilgilerini kullanarak hangi bileşenlerin bulunduğunu analiz eder. Daha sonra bu bilgiler güvenlik açıkları, risk puanları ve diğer güvenlik verileriyle ilişkilendirilerek kapsamlı bir güvenlik görünümü oluşturulur.

SBOM, SPM platformlarının yazılım tedarik zincirini izleyebilmesi için temel veri kaynaklarından biridir.<br>

***

### Örnek

Node.js ile geliştirilen bir projede bulunan **package.json** dosyasında Express, jsonwebtoken, multer ve pg gibi bağımlılıklar yer alabilir. SBOM oluşturulduğunda bu bağımlılıkların isimleri, sürümleri ve diğer ilgili bilgiler tek bir envanter halinde listelenir.

Bu envanter sayesinde herhangi bir bağımlılıkta güvenlik açığı tespit edildiğinde hangi uygulamaların etkilendiği kolayca belirlenebilir.
