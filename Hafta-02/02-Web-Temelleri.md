# 02 - Web Temelleri

İnternet üzerinde çalışan Web sisteminin temel kavramlarını, istemci-sunucu iletişimini, DNS çözümlemesini ve HTTP protokolünü açıklar.

## İçindekiler

1. [World Wide Web (WWW)](#1-world-wide-web-www)
2. [İnternet ve Web arasındaki fark](#2-internet-ve-web-arasındaki-fark)
3. [İstemci ve sunucu modeli](#3-istemci-ve-sunucu-modeli)
4. [Domain Name System (DNS)](#4-domain-name-system-dns)
5. [Hypertext Transfer Protocol (HTTP)](#5-hypertext-transfer-protocol-http)
6. [Bir web sitesine erişim süreci](#6-bir-web-sitesine-erişim-süreci)
7. [Web Temelleri – Sınav Soruları ve Cevapları](#7-web-temelleri--sınav-soruları-ve-cevapları)

---

## 1. World Wide Web (WWW)

**World Wide Web (WWW)**, internet üzerinde çalışan; metin, görsel, video ve diğer içerikleri birbirine bağlantılarla bağlayan bir bilgi paylaşım sistemidir.

Web sayfaları hiper-metin yapısını kullanır. Hiper-metin, bir dokümandan başka bir dokümana bağlantı (link) verilmesini sağlar. Kullanıcılar bu bağlantılara tıklayarak sayfalar arasında geçiş yapabilir.

### Web'in ortaya çıkışı

- World Wide Web, 1989 yılında CERN'de çalışan İngiliz bilgisayar bilimcisi **Tim Berners-Lee** tarafından önerildi ve geliştirilmeye başlandı.
- Temel amaç, farklı ülkelerde ve kurumlarda çalışan bilim insanlarının bilgileri kolayca paylaşabilmesiydi.
- Web'in temel teknolojileri:
  - **HTML (Hypertext Markup Language):** Web sayfalarının yapısını ve içeriğini tanımlar.
  - **URL (Uniform Resource Locator):** Web üzerindeki bir kaynağın adresini belirtir.
  - **HTTP (Hypertext Transfer Protocol):** İstemci ve sunucu arasında web kaynaklarının aktarılmasını sağlar.

## 2. İnternet ve Web arasındaki fark

İnternet ve Web birbiriyle ilişkili olsa da aynı şey değildir.

| Kavram | Açıklama |
|---|---|
| **İnternet** | Dünya genelindeki bilgisayar ağlarını birbirine bağlayan küresel ağ altyapısıdır. |
| **Web (WWW)** | İnternet üzerinde çalışan, web sayfaları ve bağlantılar aracılığıyla bilgi sunan hizmettir. |

İnternet; Web'in yanı sıra e-posta, dosya aktarımı, çevrimiçi oyunlar ve anlık mesajlaşma gibi farklı hizmetleri de destekler. Web, internetin sunduğu hizmetlerden yalnızca biridir.

**Kısaca:** İnternet altyapıdır; Web ise bu altyapı üzerinde çalışan hizmetlerden biridir.

## 3. İstemci ve sunucu modeli

İstemci-sunucu (client-server) modeli, bir istemcinin sunucudan veri veya hizmet talep ettiği, sunucunun da bu talebi işleyerek yanıt verdiği iletişim modelidir.

### İstemci (Client)

- Sunucudan bilgi veya hizmet isteyen taraftır.
- Bilgisayar, telefon, tablet veya bir yazılım olabilir.
- Web kullanımında tarayıcı, web sunucusuna istek gönderen istemci uygulamasıdır.

### Sunucu (Server)

- İstemcilerden gelen istekleri karşılayan ve yanıt üreten sistemdir.
- Web sayfalarını, dosyaları veya uygulama hizmetlerini barındırabilir.
- İstekleri işler ve gerekli verileri istemciye gönderir.

### İstemci-sunucu iletişimi nasıl gerçekleşir?

1. Kullanıcı tarayıcıya bir web sitesi adresi girer.
2. İstemci, ilgili sunucuya bir istek gönderir.
3. Sunucu isteği alır ve işler.
4. Sunucu, istenen içeriği yanıt olarak gönderir.
5. Tarayıcı gelen içeriği kullanıcıya görüntüler.

Sunucular özel donanımlı bilgisayarlar olabileceği gibi, uygun yazılım ve ağ bağlantısına sahip sıradan bilgisayarlar da sunucu olarak kullanılabilir. Sunucuların temel görevi istemcilere kaynak veya hizmet sağlamaktır.

## 4. Domain Name System (DNS)

**DNS (Domain Name System / Alan Adı Sistemi)**, alan adlarını IP adresleriyle eşleştiren dağıtılmış ve hiyerarşik isimlendirme sistemidir. İnsanların hatırlaması kolay alan adlarını, ağ cihazlarının iletişim kurarken kullandığı IP adresleriyle ilişkilendirir.

Örneğin, `www.example.com` bir alan adıdır. DNS sorgusu sonucunda bu alan adına ait IP adresi öğrenilebilir.

### DNS'nin gelişimi

- İnternetin ilk dönemlerinde bilgisayar adları ve IP adresleri merkezi olarak yönetilen `hosts.txt` dosyasında tutuluyordu.
- İnternet büyüdükçe bu dosyanın merkezi olarak yönetilmesi ve güncel tutulması zorlaştı.
- 1983 yılında Paul Mockapetris tarafından DNS mimarisi geliştirildi; DNS'nin ilk tanımları RFC 882 ve RFC 883 belgelerinde yayımlandı.

### Alan adı (Domain)

Alan adı, internet üzerindeki bir kaynağı tanımlamak için kullanılan, insanlar tarafından okunabilir isimdir.

Örnek: `www.example.com`

| Bölüm | Açıklama |
|---|---|
| `www` | Alt alan adı (subdomain) |
| `example` | İkinci düzey alan adı (second-level domain) |
| `com` | Üst düzey alan adı (top-level domain / TLD) |

Başka bir örnek: `hello.cars.com` alan adında `cars` ikinci düzey alan adıdır; `hello` alt alan adıdır.

### Üst düzey alan adı (TLD)

TLD, alan adının en sağındaki bölümüdür.

- **.com:** Yaygın olarak ticari amaçlı alan adlarında kullanılır.
- **.org:** Sıklıkla kuruluşlar ve kâr amacı gütmeyen yapılar tarafından kullanılır.
- **.gov:** İlgili ülkenin kurallarına göre devlet kurumları için ayrılmıştır.
- **.edu:** Bazı alan adı sistemlerinde eğitim kurumları için kullanılır.
- **.uk, .de, .tr:** Ülke kodu üst düzey alan adlarına (ccTLD) örnektir.
- **.tech, .photography:** Genel üst düzey alan adı (gTLD) örnekleridir.

TLD uzantıları bir sitenin niteliği hakkında fikir verebilir; ancak her uzantı için kullanım kuralları ve uygunluk şartları farklı olabilir.

### DNS sunucu türleri

DNS çözümlemesinde farklı görevleri olan sunucular bulunur.

#### 1. Recursive Resolver (Özyineli Çözücü)

- İstemci adına DNS sorgusunu çözmeye çalışır.
- Önce önbelleğinde (cache) uygun bir kayıt olup olmadığını kontrol eder.
- Kayıt yoksa DNS hiyerarşisindeki diğer sunuculara başvurarak yanıtı bulur.
- Bulduğu kayıtları belirli bir süre önbelleğe alabilir.

#### 2. Root Name Server (Kök Ad Sunucusu)

- DNS hiyerarşisinin en üst seviyesinde yer alır.
- Sorguyu ilgili TLD sunucusuna yönlendirmek için gerekli bilgiyi verir.
- Örneğin `.com` uzantılı alan adları için ilgili TLD sunucularına yönlendirme sağlar.

#### 3. Authoritative Name Server (Yetkili Ad Sunucusu)

- Belirli bir alan adına ait DNS kayıtlarının yetkili kaynağıdır.
- A, AAAA, MX ve CNAME gibi DNS kayıtları bu sunucularda bulunabilir.
- İstenen alan adına ilişkin kesin DNS yanıtını sağlar.

### DNS çözümleme süreci

Önbellekte yanıt bulunmadığı varsayımıyla genel süreç şöyledir:

1. **İstemci sorgusu:** Kullanıcı tarayıcıya `www.example.com` yazar. İşletim sistemi veya istemci, DNS sorgusu oluşturur.
2. **Recursive Resolver:** Sorgu, yapılandırılmış DNS çözücüye gönderilir. Çözücü önbelleğini kontrol eder.
3. **Kök sunucu:** Yanıt önbellekte yoksa çözücü kök DNS sunucusuna başvurur ve ilgili TLD sunucusunun bilgisini alır.
4. **TLD sunucusu:** Çözücü, örneğin `.com` TLD sunucusuna başvurur ve alan adının yetkili ad sunucularına ilişkin yönlendirme bilgisini alır.
5. **Yetkili ad sunucusu:** Çözücü, yetkili sunucudan `www.example.com` için istenen DNS kaydını talep eder.
6. **Yanıtın dönmesi:** Yetkili sunucudan alınan kayıt recursive resolver üzerinden istemciye iletilir ve önbelleğe alınabilir.
7. **Sunucuya bağlantı:** İstemci, öğrendiği IP adresini kullanarak web sunucusuyla iletişim kurar.

> **Önemli:** Bu adımlar, önbellekte yanıt bulunmadığı durumdaki genel akışı anlatır. Önbellekte geçerli kayıt varsa kök, TLD ve yetkili sunucu aşamalarının tamamı yeniden çalıştırılmayabilir.

## 5. Hypertext Transfer Protocol (HTTP)

**HTTP (Hypertext Transfer Protocol)**, Web üzerinde istemci ve sunucu arasında kaynak ve veri aktarımını sağlayan uygulama katmanı protokolüdür.

HTTP, istemci-sunucu modelini kullanır:

- İstemci sunucuya bir **request (istek)** gönderir.
- Sunucu isteği işler.
- Sunucu bir **response (yanıt)** gönderir.

Web sayfaları, resimler, videolar ve API verileri HTTP üzerinden aktarılabilir. HTTPS ise HTTP iletişimini TLS ile korur.

### HTTP isteğinin temel bileşenleri

Ders kapsamında HTTP isteği dört temel bileşenle ele alınır:

1. **URL:** İstenen kaynağın adresi.
2. **Method (Metot):** Sunucudan hangi işlemin istendiğini belirtir.
3. **Headers (Başlıklar):** İstekle ilgili ek bilgiler taşır.
4. **Request Body (İstek gövdesi):** Sunucuya gönderilen isteğe bağlı veriyi içerir.

Örnek istek:

```http
GET /index.html HTTP/1.1
Host: www.example.com
Cookie: SESSIONID=example-session-id
```

- `GET`: İstenen HTTP metodudur.
- `/index.html`: İstenen kaynağın yoludur.
- `HTTP/1.1`: Kullanılan HTTP sürümüdür.
- `Host`: Hedef sunucunun alan adını belirtir.
- `Cookie`: İstemci tarafından sunucuya gönderilen çerez bilgisidir. Oturum yönetiminde kullanılabilir.

### HTTP istek metotları

| Metot | Kullanım amacı |
|---|---|
| **GET** | Bir kaynağı almak için kullanılır. |
| **POST** | Sunucuya veri göndermek için kullanılır; form gönderimlerinde yaygındır. |
| **PUT** | Bir kaynağı oluşturmak veya mevcut kaynağı bütünüyle güncellemek için kullanılabilir. |
| **DELETE** | Belirli bir kaynağı silme isteği gönderir. |
| **HEAD** | GET'e benzer; yanıt gövdesi olmadan başlık bilgilerini ister. |
| **OPTIONS** | Bir kaynağın veya sunucunun desteklediği iletişim seçeneklerini/metotları sorgular. |
| **PATCH** | Bir kaynağın belirli bir bölümünü güncellemek için kullanılır. |
| **CONNECT** | İstemci ile hedef sunucu arasında tünel oluşturmak için kullanılır. |
| **TRACE** | İstek yolunu teşhis etmek amacıyla kullanılır; güvenlik nedeniyle birçok sunucuda devre dışı bırakılır. |

### HTTP istek başlıkları (Request Headers)

Başlıklar, isteğe ilişkin ek bilgi taşır. Genellikle `Başlık-Adı: Değer` biçimindedir.

Örnek:

```http
GET /api/info HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0
Accept: application/json
Accept-Language: tr-TR,tr;q=0.9
Authorization: Bearer example-token
Cache-Control: no-cache
Connection: keep-alive
Referer: https://www.example.org/
```

| Başlık | Açıklama |
|---|---|
| `Host` | İsteğin hedeflediği sunucu adını belirtir. |
| `User-Agent` | İsteği yapan tarayıcı veya istemci uygulaması hakkında bilgi verir. |
| `Accept` | İstemcinin kabul edebileceği yanıt içerik türlerini belirtir. |
| `Accept-Language` | Tercih edilen yanıt dilini belirtir. |
| `Authorization` | Kimlik doğrulama bilgisi veya erişim belirteci taşır. |
| `Cache-Control` | Önbellekleme davranışına ilişkin yönergeler içerir. |
| `Connection` | HTTP/1.x bağlantı yönetimiyle ilgili seçenekleri belirtir. |
| `Referer` | İsteğe yönlendiren önceki sayfanın adresini belirtebilir. |
| `Pragma` | Geriye dönük uyumluluk için kullanılan önbellek yönergelerini içerebilir. |
| `Content-Type` | Gönderilen gövdenin medya türünü belirtir. |

### HTTP istek gövdesi (Request Body)

Request Body, istemciden sunucuya gönderilen veriyi içerir. Özellikle `POST`, `PUT` ve `PATCH` metotlarıyla kullanılır.

Gövde içerisinde şunlar bulunabilir:

- Form verileri
- JSON veya XML biçiminde veriler
- Dosyalar
- Çok parçalı (`multipart/form-data`) içerikler

`Content-Type` başlığı, gövdedeki verinin biçimini sunucuya bildirir.

Örnek:

```http
POST /api/users HTTP/1.1
Host: example.com
Content-Type: application/json

{
  "username": "ornek_kullanici",
  "email": "user@example.com"
}
```

Bu örnekte istemci, JSON biçimindeki kullanıcı verisini sunucuya gönderir.

### HTTP yanıtları (Response)

Sunucu, istemcinin isteğine HTTP yanıtı gönderir. Yanıt genel olarak durum satırı, başlıklar ve varsa yanıt gövdesinden oluşur.

Örnek:

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 48

{
  "name": "Example User",
  "status": "active"
}
```

Durum satırı HTTP sürümünü, durum kodunu ve kısa açıklamasını içerir.

### Yaygın HTTP durum kodları

| Kod | Anlamı |
|---|---|
| **100 Continue** | İsteğin devamına izin verildiğini belirtir. |
| **101 Switching Protocols** | Sunucunun protokol değiştirme isteğini kabul ettiğini belirtir. |
| **200 OK** | İstek başarılı oldu. |
| **201 Created** | İstek sonucunda yeni bir kaynak oluşturuldu. |
| **202 Accepted** | İstek kabul edildi ancak işlem henüz tamamlanmadı. |
| **203 Non-Authoritative Information** | Yanıttaki bilgi, kaynağın yetkili sunucusundan farklı bir kaynaktan dönmüş olabilir. |
| **301 Moved Permanently** | Kaynak kalıcı olarak başka bir URL'ye taşındı. |
| **404 Not Found** | İstenen kaynak bulunamadı. |
| **500 Internal Server Error** | Sunucu isteği işlerken beklenmeyen bir hatayla karşılaştı. |

### HTTP ve HTTPS

- **HTTP**, istemci ile sunucu arasında web verilerinin aktarılmasını sağlar.
- **HTTPS**, HTTP iletişimini TLS kullanarak şifreler ve iletişimin bütünlüğü ile sunucu kimliğinin doğrulanmasına yardımcı olur.
- HTTPS, özellikle parola, oturum bilgisi ve kişisel veri gibi bilgilerin aktarımında önemlidir.

## 6. Bir web sitesine erişim süreci

Bir kullanıcı tarayıcıya `https://example.com` yazdığında genel olarak şu işlemler gerçekleşir:

1. **URL girilir:** Kullanıcı web adresini tarayıcıya yazar.
2. **DNS çözümlemesi yapılır:** Alan adına karşılık gelen IP adresi öğrenilir. Geçerli önbellek kaydı varsa DNS sorgusu daha kısa sürebilir.
3. **Sunucuya bağlantı kurulur:** İstemci, bulunan IP adresindeki sunucuya uygun taşıma ve güvenlik mekanizmalarıyla bağlanır. HTTPS için TLS oturumu da kurulur.
4. **HTTP isteği gönderilir:** Tarayıcı, istenen kaynağa ilişkin HTTP isteğini sunucuya iletir.
5. **HTTP yanıtı alınır:** Sunucu isteği işler ve durum kodu, başlıklar ve varsa içerikten oluşan yanıtı gönderir.
6. **Sayfa görüntülenir:** Tarayıcı HTML içeriğini işler. Sayfanın tamamlanması için CSS, JavaScript, resim ve diğer kaynaklar için ek istekler de gönderebilir.

> **Teknik not:** HTTP/1.1'de kalıcı bağlantı (persistent connection) varsayılan davranıştır. Bu nedenle her kaynak isteğinden sonra bağlantının mutlaka kapatılması gerekmez. HTTP/2 ve HTTP/3 de bağlantıların kullanımını farklı biçimlerde optimize eder.

---

## 7. Web Temelleri – Sınav Soruları ve Cevapları

Bu bölüm, 15 soruluk değerlendirme sınavına yönelik cevapları ve kısa açıklamaları içerir.

1. **WWW kısaltmasının tam açılımı nedir?**  
   **Cevap: World Wide Web.**

2. **İnternet ile Web arasındaki temel fark nedir?**  
   **Cevap:** İnternet, dünya genelindeki ağları birbirine bağlayan altyapıdır. Web ise internet üzerinde çalışan bilgi paylaşım hizmetidir.

3. **Web'in kullanıcılara sunduğu özelliklerden biri nedir?**  
   **Cevap:** Hiper-metin bağlantıları aracılığıyla web sayfaları ve kaynaklar arasında geçiş yapabilmek.

4. **Sunucuların temel amacı nedir?**  
   **Cevap:** İstemcilerden gelen istekleri karşılamak, veri veya hizmet sunmak.

5. **İstemci-sunucu modelinde istemcinin rolü nedir?**  
   **Cevap:** Sunucudan bilgi veya hizmet talep etmek ve gelen yanıtı kullanmak.

6. **DNS kısaltmasının tam açılımı nedir?**  
   **Cevap: Domain Name System (Alan Adı Sistemi).**

7. **`hello.cars.com` alan adında second-level domain nedir?**  
   **Cevap: `cars`.**

8. **Recursive resolver, hangi TLD sunucusuna başvurması gerektiğini bilmiyorsa ilk olarak hangi sunuculara başvurur?**  
   **Cevap: Kök DNS sunucularına (Root Name Servers).**

9. **HTTP isteğinin dört temel bileşeni nelerdir?**  
   **Cevap:** URL, Method, Headers ve Request Body (istek gövdesi; isteğe bağlı).

10. **Form verilerini sunucuya göndermek için yaygın olarak kullanılan HTTP metodu nedir?**  
    **Cevap: POST.**

11. **Belirli bir kaynağı almak için kullanılan HTTP metodu nedir?**  
    **Cevap: GET.**

12. **OPTIONS HTTP metodunun kullanım amacı nedir?**  
    **Cevap:** Bir kaynağın veya sunucunun desteklediği iletişim seçeneklerini ve HTTP metotlarını sorgulamak.

13. **İstek başarılı bir şekilde işlendiğinde hangi HTTP durum kodu verilir?**  
    **Cevap: 200 OK.**

14. **HTTP 404 durum kodu ne anlama gelir?**  
    **Cevap: Not Found (İstenen kaynak bulunamadı).**

15. **İsteği yapan tarayıcı veya istemci uygulamasının türü ve sürümü hakkında bilgi veren HTTP başlığı nedir?**  
    **Cevap: User-Agent.**

### Hızlı tekrar tablosu

| Kavram | Hatırlanacak bilgi |
|---|---|
| WWW | World Wide Web |
| HTML | Web sayfasının yapısını tanımlar. |
| URL | Web kaynağının adresini belirtir. |
| HTTP | İstemci-sunucu arasında web verisi aktarır. |
| İnternet | Küresel ağ altyapısıdır. |
| Web | İnternet üzerinde çalışan hizmettir. |
| Client | İstek gönderen taraf. |
| Server | İsteği karşılayan ve hizmet sunan taraf. |
| DNS | Alan adlarını IP adresleriyle eşleştirir. |
| Recursive Resolver | İstemci adına DNS sorgusunu çözer. |
| Root DNS | İlgili TLD sunucusuna yönlendirme bilgisi verir. |
| Authoritative DNS | Alan adına ait yetkili kayıtları sağlar. |
| POST | Sunucuya veri göndermek için yaygın kullanılır. |
| GET | Kaynak almak için kullanılır. |
| OPTIONS | Desteklenen iletişim seçeneklerini sorgular. |
| 200 | OK – Başarılı. |
| 404 | Not Found – Kaynak bulunamadı. |
| User-Agent | İstemci yazılımı hakkında bilgi verir. |
