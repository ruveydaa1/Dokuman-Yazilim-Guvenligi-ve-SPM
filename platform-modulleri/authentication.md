# Authentication

### Authentication Nedir?

Authentication (Kimlik Doğrulama), kullanıcıların veya sistemlerin gerçekten iddia ettikleri kişi ya da servis olduklarını doğrulama işlemidir. Yazılım güvenliğinin en temel bileşenlerinden biri olan kimlik doğrulama sayesinde yalnızca yetkili kullanıcıların uygulamalara, sistemlere ve verilere erişmesi sağlanır.

SPM platformlarında Authentication modülü; kullanıcı hesaplarının yönetilmesi, kurumsal dizin servisleriyle entegrasyon sağlanması, Tek Oturum Açma (Single Sign-On - SSO) desteği sunulması ve çok faktörlü kimlik doğrulama (MFA) gibi güvenlik mekanizmalarının merkezi olarak yönetilmesini sağlar.<br>

***

### Authentication Nasıl Çalışır?

Authentication modülü, kullanıcının sisteme giriş yapmak için sunduğu bilgileri (kullanıcı adı, parola, erişim anahtarı veya güvenlik belirteci gibi) doğrular. Kimlik doğrulama başarılı olursa kullanıcıya sisteme erişim izni verilir.

Modern platformlarda bu süreç yalnızca kullanıcı adı ve parola ile sınırlı değildir. LDAP, Active Directory, OAuth 2.0, OpenID Connect (OIDC) ve SAML gibi standartlar kullanılarak kurumsal kimlik sistemleriyle güvenli entegrasyon sağlanabilir. Ayrıca MFA desteği ile SMS doğrulama, mobil doğrulama uygulamaları veya güvenlik anahtarları kullanılarak ek güvenlik katmanı oluşturulabilir.<br>

***

### Authentication'ın Önemi

Kimlik doğrulama mekanizmalarının güvenli olması, yetkisiz erişimlerin önlenmesinde kritik rol oynar. Zayıf kimlik doğrulama yöntemleri; hesap ele geçirme, veri ihlalleri ve yetkisiz sistem erişimleri gibi ciddi güvenlik sorunlarına yol açabilir.

Kurumsal ortamlarda merkezi kimlik yönetimi sayesinde kullanıcı hesapları daha kolay yönetilebilir, erişim yetkileri kontrol altında tutulabilir ve güvenlik politikalarının uygulanması kolaylaşır.<br>

***

### Avantajları ve Sınırlamaları

#### Avantajları

* Yetkisiz kullanıcıların sisteme erişmesini engeller.
* Merkezi kullanıcı yönetimi sağlar.
* LDAP, Active Directory ve SSO sistemleriyle entegre çalışabilir.
* Çok faktörlü kimlik doğrulama (MFA) desteği sunabilir.
* Güvenlik politikalarının merkezi olarak uygulanmasına katkı sağlar.

#### Sınırlamaları

* Yanlış yapılandırılan kimlik doğrulama sistemleri güvenlik açıklarına neden olabilir.
* Eski kimlik doğrulama protokolleri yeterli güvenliği sağlayamayabilir.
* Harici kimlik sağlayıcılarına bağımlılık oluşabilir.
* MFA kullanılmadığında hesap ele geçirme riski artabilir.<br>

***

## Yaygın Kullanılan Authentication Teknolojileri

Authentication süreçlerinde farklı ihtiyaçlara yönelik birçok teknoloji ve protokol kullanılmaktadır. Bu teknolojiler kullanıcıların güvenli şekilde doğrulanmasını ve kurumsal sistemlerle entegrasyon kurulmasını sağlar.

#### LDAP (Lightweight Directory Access Protocol)

LDAP, kullanıcı bilgilerini merkezi bir dizin servisinde saklamak ve yönetmek için kullanılan en yaygın kimlik doğrulama protokollerinden biridir. Kurumlarda kullanıcı hesaplarının merkezi olarak yönetilmesini sağlar. Birçok SPM platformu LDAP entegrasyonu sayesinde kullanıcıları mevcut kurumsal dizin üzerinden doğrulayabilir.

#### Microsoft Active Directory (AD)

Active Directory, Microsoft tarafından geliştirilen kurumsal dizin hizmetidir. Kullanıcı hesaplarını, bilgisayarları, grupları ve güvenlik politikalarını merkezi olarak yönetir. Özellikle Windows tabanlı kurumsal ortamlarda en yaygın kimlik doğrulama altyapılarından biridir.

#### Microsoft Entra ID (Azure Active Directory)

Microsoft Entra ID (eski adıyla Azure Active Directory), bulut tabanlı kimlik ve erişim yönetimi hizmetidir. SSO, MFA ve koşullu erişim (Conditional Access) gibi gelişmiş güvenlik özellikleri sunar. Bulut tabanlı uygulamalarla yaygın olarak entegre edilmektedir.

#### OAuth 2.0

OAuth 2.0, kullanıcı parolasını paylaşmadan farklı uygulamalara güvenli yetkilendirme yapılmasını sağlayan açık bir standarttır. "Google ile Giriş Yap" veya "GitHub ile Giriş Yap" gibi senaryolarda yaygın olarak kullanılmaktadır.

#### OpenID Connect (OIDC)

OpenID Connect, OAuth 2.0 üzerine geliştirilmiş modern bir kimlik doğrulama protokolüdür. Kullanıcının kimliğinin doğrulanmasını sağlar ve web ile mobil uygulamalarda yaygın olarak kullanılmaktadır.

#### SAML (Security Assertion Markup Language)

SAML, özellikle kurumsal ortamlarda Tek Oturum Açma (Single Sign-On - SSO) amacıyla kullanılan XML tabanlı bir kimlik doğrulama standardıdır. Kullanıcıların tek bir oturum açma işlemiyle birden fazla kurumsal uygulamaya erişmesini sağlar.

#### Keycloak

Keycloak, açık kaynaklı bir Kimlik ve Erişim Yönetimi (IAM) platformudur. LDAP, Active Directory, OAuth 2.0, OpenID Connect ve SAML desteği sunar. SSO, MFA ve kullanıcı yönetimi gibi özellikleri sayesinde birçok kurum tarafından tercih edilmektedir.

#### Okta

Okta, bulut tabanlı ticari bir kimlik ve erişim yönetimi platformudur. Çok sayıda uygulamayla entegre çalışabilir ve SSO ile MFA desteği sunar. Özellikle büyük ölçekli şirketlerde yaygın olarak kullanılmaktadır.<br>

***

### Authentication Teknolojilerinin Karşılaştırılması

<table data-search="false"><thead><tr><th>Teknoloji</th><th>Öne Çıkan Özelliği</th></tr></thead><tbody><tr><td><strong>LDAP</strong></td><td>Merkezi dizin tabanlı kimlik doğrulama</td></tr><tr><td><strong>Microsoft Active Directory</strong></td><td>Windows ortamlarında kullanıcı ve grup yönetimi</td></tr><tr><td><strong>Microsoft Entra ID</strong></td><td>Bulut tabanlı kimlik ve erişim yönetimi</td></tr><tr><td><strong>OAuth 2.0</strong></td><td>Güvenli yetkilendirme standardı</td></tr><tr><td><strong>OpenID Connect (OIDC)</strong></td><td>Modern kimlik doğrulama protokolü</td></tr><tr><td><strong>SAML</strong></td><td>Kurumsal Single Sign-On (SSO)</td></tr><tr><td><strong>Keycloak</strong></td><td>Açık kaynak IAM ve SSO platformu</td></tr><tr><td><strong>Okta</strong></td><td>Bulut tabanlı kurumsal kimlik yönetimi</td></tr></tbody></table>

***

### SPM ile İlişkisi

SPM platformlarında Authentication modülü, kullanıcıların güvenli şekilde sisteme erişmesini sağlar ve mevcut kurumsal kimlik altyapılarıyla entegrasyon kurar. Böylece kullanıcı yönetimi merkezi hale gelir, erişim yetkileri güvenli şekilde kontrol edilir ve platformun diğer modülleriyle birlikte bütünleşik bir güvenlik yönetimi sağlanır.<br>

***

### Örnek

Bir kurumda çalışan kullanıcılar şirket hesaplarıyla SPM platformuna giriş yapmaktadır. Platform, LDAP veya Microsoft Entra ID entegrasyonu sayesinde kullanıcı bilgilerini doğrular ve kullanıcının rolüne göre erişim yetkilerini otomatik olarak belirler. Eğer MFA etkinleştirilmişse kullanıcıdan giriş sırasında ek doğrulama istenir. Bu sayede yalnızca yetkili kullanıcıların platforma erişmesi sağlanır.
