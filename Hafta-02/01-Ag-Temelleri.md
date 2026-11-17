# Ağ Temelleri

> **Amaç:** Bilgisayar ağlarının temel kavramlarını, ağ cihazlarını, iletişim modellerini, protokolleri ve IP adresleme / subnetting işlemlerini kendi cümlelerimle öğrenmek.
>
> Bu dosya; kavram açıklamaları, kısa örnekler, komutlar ve siber güvenlik açısından önemli noktaları bir araya getirir.

## İçindekiler

1. [Ağlara Giriş ve Standartlar](#1-ağlara-giriş-ve-standartlar)
2. [Ağ Türleri](#2-ağ-türleri)
3. [Ağ Cihazları ve İletim Ortamları](#3-ağ-cihazları-ve-iletim-ortamları)
4. [Ağ Topolojileri](#4-ağ-topolojileri)
5. [İletişim Modları ve Türleri](#5-iletişim-modları-ve-türleri)
6. [Ağ Modelleri](#6-ağ-modelleri)
7. [OSI Modeli](#7-osi-modeli)
8. [TCP/IP Modeli](#8-tcpip-modeli)
9. [Protokoller ve Portlar](#9-protokoller-ve-portlar)
10. [IP ve MAC Adresleri](#10-ip-ve-mac-adresleri)
11. [IP Subnetting](#11-ip-subnetting)

---

## 1. Ağlara Giriş ve Standartlar

### Bilgisayar ağı nedir?

Bilgisayar ağı; bilgisayar, sunucu, telefon, yazıcı ve ağ cihazları gibi sistemlerin veri alışverişi yapabilmek ve kaynak paylaşabilmek için birbirine bağlanmasıdır.

Ağlar sayesinde cihazlar dosya, yazıcı, internet bağlantısı ve uygulama gibi kaynakları paylaşabilir. İnternet, dünya çapında birbirine bağlı çok sayıda ağın oluşturduğu en büyük ağ örneğidir.

### Ağ standartları ve protokolleri

Farklı üreticilerin geliştirdiği cihazların birlikte çalışabilmesi için ortak standartlara ve iletişim kurallarına ihtiyaç vardır.

- **Standart:** Bir teknolojinin nasıl çalışacağına ilişkin ortak teknik tanımları belirler.
- **Protokol:** Cihazların veri gönderirken ve alırken uyması gereken kuralları tanımlar.

Öne çıkan kuruluşlar:

| Kuruluş | Temel rolü |
|---|---|
| IEEE | Ethernet ve kablosuz ağlar gibi birçok ağ standardını geliştirir. |
| IETF | İnternet protokollerinin standartlaşması üzerinde çalışır. |
| ISO | Uluslararası standartlar geliştirir; OSI referans modeliyle bilinir. |
| ITU | Telekomünikasyon alanında uluslararası standartlar yayımlar. |
| ANSI | ABD'de standartların koordinasyonunda rol oynar. |
| W3C | Web teknolojileri için standartlar ve yönergeler geliştirir. |

**Örnek:** Ethernet teknolojisi IEEE 802.3 ailesiyle, kablosuz yerel ağlar ise IEEE 802.11 ailesiyle ilişkilidir.

### Neden önemlidir?

Standartlar ve protokoller olmadan farklı cihazların aynı ağ üzerinde anlaşması zorlaşır. Siber güvenlikte de protokollerin doğru yapılandırılması önemlidir; eski veya şifresiz protokoller saldırganların trafiği okumasına ya da değiştirmesine imkân verebilir.

## 2. Ağ Türleri

Ağlar kapsadıkları coğrafi alana ve kullanım amaçlarına göre sınıflandırılabilir.

| Ağ türü | Açıklama | Örnek |
|---|---|---|
| **PAN** | Kişisel cihazlar arasında kısa mesafeli ağ | Telefon ile Bluetooth kulaklık |
| **LAN** | Sınırlı bir alandaki yerel ağ | Ev, ofis veya laboratuvar ağı |
| **MAN** | Şehir veya büyük kampüs ölçeğindeki ağ | Bir şehirdeki kurum ağları |
| **WAN** | Geniş coğrafi alanları birbirine bağlayan ağ | Farklı şehirlerdeki şubelerin ağı |
| **Internet** | Dünya çapındaki ağların birbirine bağlandığı küresel ağ | Web sitelerine erişim |
| **Intranet** | Bir kurumun kendi içinde kullandığı özel ağ ve hizmetler | Şirket içi portal |

**Not:** İnternet ile intranet aynı şey değildir. İnternet genel kullanıma açık küresel ağdır; intranet ise kurum içi erişim için tasarlanır. Kurumlar intranetlerine uzaktan erişimi VPN gibi yöntemlerle sağlayabilir.

## 3. Ağ Cihazları ve İletim Ortamları

### Temel ağ cihazları

| Cihaz | Görevi |
|---|---|
| **NIC (Network Interface Card)** | Cihazın ağa bağlanmasını sağlayan ağ arayüzüdür. Kablolu veya kablosuz olabilir. |
| **Hub** | Gelen veriyi bağlı olduğu diğer portlara yayar. Hedef seçimi yapmaz; günümüzde çoğunlukla switch kullanılır. |
| **Switch** | Yerel ağda Ethernet çerçevelerini MAC adreslerine göre uygun porta iletir. |
| **Router** | Farklı IP ağları arasında paketleri yönlendirir. |
| **Modem** | İnternet servis sağlayıcısının erişim teknolojisine uygun sinyal dönüşümünü sağlar. |
| **Access Point (AP)** | Kablosuz cihazların yerel ağa bağlanmasını sağlar. |
| **Firewall** | Tanımlanmış güvenlik kurallarına göre ağ trafiğine izin verir veya trafiği engeller. |

### MAC adresi ve NIC

MAC adresi, ağ arayüzünü tanımlamak için kullanılan bağlantı katmanı adresidir. Ethernet MAC adresleri genellikle 48 bittir ve altı onaltılık (hexadecimal) oktet biçiminde gösterilir.

Örnek: `00:21:70:6F:06:F2`

### Kablolu iletim ortamları

- **Koaksiyel kablo:** İç iletken, yalıtkan ve dış koruyucu katmanlardan oluşur. Bazı kablo TV ve eski ağ uygulamalarında kullanılmıştır.
- **Bükümlü çift (Twisted Pair):** Birbirine dolanmış bakır tel çiftlerinden oluşur. Ethernet ağlarında yaygındır.
  - **UTP:** Ek ekranlama katmanı bulunmayan bükümlü çift kablo.
  - **STP:** Elektromanyetik parazite karşı ek ekranlama içeren bükümlü çift kablo.
  - Cat5e, Cat6 ve Cat6A gibi kategoriler kablonun desteklediği performans özelliklerini belirtir.
- **Fiber optik:** Veriyi ışıkla taşır; yüksek hız ve uzun mesafe avantajı sunar.
  - **MMF (Multimode Fiber):** Genellikle daha kısa mesafeli bağlantılarda kullanılır.
  - **SMF (Singlemode Fiber):** Daha uzun mesafeli bağlantılar için uygundur.

### Konnektör ve kablolama

- **RJ-45:** Ethernet bakır kablolamada yaygın kullanılan 8P8C konnektör için kullanılan yaygın isimdir.
- **RJ-11:** Telefon bağlantılarında yaygındır.
- **DB-9:** Bazı seri bağlantılarda kullanılır.
- **T568A ve T568B:** Ethernet kablolarında renk sıralamasını belirleyen kablolama düzenleridir.
- **Düz kablo (Straight-through):** İki uçta aynı kablolama standardı kullanılır.
- **Çapraz kablo (Crossover):** Uçlarda farklı kablolama düzenleri kullanılır; klasik olarak benzer türde cihazları doğrudan bağlamakta kullanılmıştır. Modern cihazların çoğunda Auto MDI-X bulunduğu için her zaman gerekli değildir.

## 4. Ağ Topolojileri

Topoloji, ağ cihazlarının fiziksel veya mantıksal olarak nasıl bağlandığını gösterir.

| Topoloji | Açıklama | Avantaj / dezavantaj |
|---|---|---|
| **Star (Yıldız)** | Cihazlar merkezi bir switch veya hub'a bağlanır. | Yönetimi kolaydır; merkez cihaz arızalanırsa ağın büyük bölümü etkilenir. |
| **Bus (Veriyolu)** | Cihazlar ortak bir ana kabloyu paylaşır. | Basit yapıdadır; ana kablodaki arıza ağı etkileyebilir. |
| **Ring (Halka)** | Cihazlar halka biçiminde birbirine bağlanır. | Veri belirli bir halka düzeninde ilerler; arıza etkisi kullanılan teknolojiye bağlıdır. |
| **Tree (Ağaç)** | Birden fazla yıldız yapısı hiyerarşik biçimde bağlanır. | Büyük ağları düzenlemeyi kolaylaştırır. |
| **Mesh (Örgü)** | Cihazlar arasında birden fazla bağlantı bulunur. | Yedeklilik sağlar; kablolama ve yönetim maliyeti artabilir. |
| **Point-to-Point (Noktadan Noktaya)** | İki nokta arasında doğrudan bağlantı kurulur. | Basit ve doğrudan iletişim sağlar. |
| **Hybrid (Hibrit)** | Birden fazla topoloji birlikte kullanılır. | İhtiyaca göre esnek tasarım yapılabilir. |

**Full Mesh:** Her düğüm diğer tüm düğümlere doğrudan bağlıdır.  
**Partial Mesh:** Yalnızca bazı düğümler arasında birden fazla doğrudan bağlantı vardır.

## 5. İletişim Modları ve Türleri

### İletim yönüne göre

- **Simplex:** Veri yalnızca tek yönde akar. Örnek: Geleneksel tek yönlü yayın.
- **Half Duplex:** İki taraf da veri gönderebilir ancak aynı anda gönderim yapmaz; sırayla iletişim kurar.
- **Full Duplex:** İki taraf aynı anda veri gönderip alabilir.

### Alıcı sayısına göre

- **Unicast:** Bir göndericiden tek bir alıcıya iletişim.
- **Multicast:** Bir göndericiden belirli bir alıcı grubuna iletişim.
- **Broadcast:** Aynı yerel yayın alanındaki tüm uygun cihazlara gönderim.

**Güvenlik notu:** Broadcast ve multicast trafiğinin kapsamı ağ tasarımına bağlıdır. VLAN ve alt ağlar yayın alanlarını sınırlandırmaya yardımcı olur.

## 6. Ağ Modelleri

Ağ modelleri, iletişim sürecini katmanlara ayırarak açıklamayı kolaylaştırır. Her katman belirli görevleri üstlenir ve komşu katmanlara hizmet sunar.

İki temel referans/model yaklaşımı:

- **OSI modeli:** İletişimi yedi katmanda açıklar.
- **TCP/IP modeli:** İnternet iletişiminin temelinde bulunan dört katmanlı modeldir.

Katmanlı yaklaşımın faydaları:

1. Karmaşık iletişim sürecini daha küçük görevlere ayırır.
2. Farklı üreticilerin sistemlerinin birlikte çalışmasını kolaylaştırır.
3. Sorun giderirken problemin hangi katmanda olabileceğini belirlemeye yardımcı olur.
4. Protokollerin görevlerini birbirinden ayırır.

## 7. OSI Modeli

OSI (Open Systems Interconnection) modeli, ağ iletişimini yedi katmana ayıran referans modelidir. Farklı sistemlerin nasıl iletişim kurduğunu anlamak ve ağ sorunlarını katmanlara göre incelemek için kullanılır.

### OSI katmanları

| Katman | Adı | Temel görev | Örnek |
|---:|---|---|---|
| 7 | Uygulama (Application) | Uygulamaların ağ hizmetlerine erişmesini sağlar. | HTTP, FTP, SMTP, DNS |
| 6 | Sunum (Presentation) | Veri biçimi, kodlama, sıkıştırma ve şifreleme gibi işlemlerle ilgilenir. | UTF-8, veri biçimleri, şifreleme |
| 5 | Oturum (Session) | Uygulamalar arasındaki oturumların kurulması, yönetilmesi ve sonlandırılmasıyla ilgilenir. | Oturum yönetimi işlevleri |
| 4 | Taşıma (Transport) | Uçtan uca iletişim, segmentasyon, portlar ve aktarım kontrolü. | TCP, UDP |
| 3 | Ağ (Network) | Mantıksal adresleme ve ağlar arası yönlendirme. | IPv4, IPv6, router |
| 2 | Veri Bağlantı (Data Link) | Çerçeveleme, MAC adresleme ve bağlantı düzeyinde hata tespiti. | Ethernet, switch |
| 1 | Fiziksel (Physical) | Bitlerin elektriksel, optik veya radyo sinyalleriyle taşınması. | Kablo, konnektör, hub, repeater |

### Katmanların görevleri

**1. Fiziksel katman**
- Bitlerin fiziksel ortamdan iletilmesini tanımlar.
- Kablo, konnektör, sinyal ve fiziksel bağlantı özellikleri bu katmanla ilgilidir.
- Simplex, half-duplex ve full-duplex gibi iletim modları fiziksel iletişim bağlamında ele alınabilir.
- Örnek donanımlar: repeater ve hub.

**2. Veri bağlantı katmanı**
- Veriyi çerçeveler (frame) hâlinde taşır.
- Yerel bağlantıda MAC adreslerini kullanır.
- Çerçevelerde hata tespiti yapılabilir; Ethernet'te FCS/CRC bu amaçla kullanılır.
- Switch'ler temel olarak bu katmanda çalışır.

**3. Ağ katmanı**
- IP adresleme ve farklı ağlar arasında yönlendirme görevlerini üstlenir.
- Router'lar IP paketlerini hedef ağa doğru iletir.
- IPv4 ve IPv6 bu katmanın temel protokolleridir.

**4. Taşıma katmanı**
- Uygulamalar arasında uçtan uca veri aktarımını sağlar.
- TCP bağlantı kurma, sıralama, onaylama ve yeniden iletim gibi güvenilirlik mekanizmaları sunar.
- UDP bağlantı kurmadan veri gönderir; teslim ve sıralama garantisi sağlamaz.
- Port numaraları uygulama/hizmet trafiğinin ayrıştırılmasına yardımcı olur.

**5. Oturum katmanı**
- Uygulamalar arasındaki iletişim oturumlarının başlatılması, sürdürülmesi ve sonlandırılmasıyla ilgilidir.

**6. Sunum katmanı**
- Verinin karşı sistem tarafından anlaşılabilecek biçimde temsil edilmesiyle ilgilenir.
- Kodlama, biçim dönüştürme, sıkıştırma ve şifreleme gibi işlevler bu katmanla ilişkilendirilir.

**7. Uygulama katmanı**
- Kullanıcı uygulamalarına ağ hizmetleri sunar.
- Web, e-posta, dosya aktarımı ve isim çözümleme gibi hizmetler bu katmandaki protokollerden yararlanır.
- Uygulama katmanı doğrudan bir tarayıcının kendisi değildir; uygulamaların kullandığı ağ protokollerini tanımlar.

### Kapsülleme (Encapsulation)

Gönderici cihazda veri üst katmanlardan alt katmanlara inerken her katman kendi kontrol bilgilerini ekler:

1. Uygulama verisi oluşur.
2. Taşıma katmanı veriyi TCP segmenti veya UDP datagramı olarak düzenler.
3. Ağ katmanı IP başlığı ekleyerek paketi oluşturur.
4. Veri bağlantı katmanı çerçeve oluşturur.
5. Fiziksel katman bitleri sinyal olarak iletir.

Alıcı cihazda işlem ters yönde gerçekleşir. Bu işleme **kapsül açma (decapsulation)** denir.

**Sorun giderme örneği:** Kablo bağlantısı yoksa öncelikle Fiziksel Katman; IP ağına ulaşılamıyorsa Ağ Katmanı; web hizmetine erişilemiyorsa DNS, port ve uygulama katmanı kontrolleri incelenebilir.

## 8. TCP/IP Modeli

TCP/IP modeli, internet iletişiminin temelinde bulunan protokol ailesini ve katmanlı yapıyı açıklar. Dört katmandan oluşur.

| TCP/IP katmanı | Görevi | OSI ile yaklaşık eşleşmesi |
|---|---|---|
| **Uygulama** | Web, e-posta, dosya aktarımı ve isim çözümleme gibi hizmetler | OSI 5, 6 ve 7 |
| **Taşıma** | Uçtan uca iletişim ve portlar | OSI 4 |
| **İnternet** | IP adresleme ve ağlar arası yönlendirme | OSI 3 |
| **Ağ erişimi** | Yerel ağda çerçeveleme ve fiziksel iletim | OSI 1 ve 2 |

### Uygulama katmanı

HTTP/HTTPS, DNS, SMTP, SSH, Telnet, FTP ve SNMP gibi protokoller bu katmanda değerlendirilir.

### Taşıma katmanı: TCP ve UDP

**TCP (Transmission Control Protocol)**
- Bağlantı odaklıdır.
- Sıralama, onaylama ve kayıp verinin yeniden iletilmesi gibi mekanizmalar sunar.
- Web erişimi, dosya aktarımı ve e-posta gibi güvenilir aktarım gerektiren uygulamalarda kullanılır.
- TCP segment başlığında kaynak/hedef portu, sıra numarası, onay numarası, bayraklar, pencere boyutu ve checksum gibi alanlar bulunur.

**TCP üçlü el sıkışma (Three-Way Handshake)**

1. **SYN:** İstemci bağlantı başlatmak için SYN gönderir.
2. **SYN-ACK:** Sunucu isteği kabul ettiğini belirten SYN-ACK yanıtı verir.
3. **ACK:** İstemci ACK gönderir ve bağlantı kurulmuş olur.

**UDP (User Datagram Protocol)**
- Bağlantı kurma aşaması gerektirmez.
- Teslim, sıralama veya yeniden iletim garantisi sağlamaz.
- Daha düşük ek yükle veri aktarabilir.
- Gerçek zamanlı ses/video, DNS sorguları ve gecikmeye duyarlı bazı uygulamalarda kullanılır.

UDP başlığında temel olarak kaynak portu, hedef portu, uzunluk ve checksum alanları bulunur.

### İnternet katmanı

**IP (Internet Protocol)**, kaynak ve hedef IP adreslerini kullanarak paketlerin ağlar arasında iletilmesini sağlar. IP tek başına teslim garantisi vermez.

Önemli protokoller:

- **IP:** Mantıksal adresleme ve paketlerin ağlar arasında iletilmesi.
- **ICMP:** Hata ve kontrol mesajları. `ping` aracı ICMP Echo Request/Reply mesajlarını kullanabilir.
- **ARP:** IPv4 yerel ağlarında bilinen bir IPv4 adresine karşılık gelen MAC adresini bulmaya yardımcı olur.

Komut örnekleri:

```bash
ping 8.8.8.8
arp -a
```

### Ağ erişim katmanı

Yerel ağ üzerindeki çerçeveleme, MAC adresleme ve fiziksel iletimle ilgilenir. Ethernet ve Wi-Fi bu katmanla ilişkilidir.

## 9. Protokoller ve Portlar

### Protokol ve port nedir?

**Protokol**, cihazların nasıl iletişim kuracağını belirleyen kurallar bütünüdür. **Port numarası** ise bir cihazdaki ağ trafiğinin hangi uygulama veya hizmete yönlendirileceğini belirlemeye yardımcı olan mantıksal tanımlayıcıdır.

TCP ve UDP port alanları 16 bittir; bu nedenle port numaraları `0–65535` aralığındadır.

Port aralıkları genel olarak:

- **0–1023:** Well-known (iyi bilinen) portlar.
- **1024–49151:** Registered (kayıtlı) portlar.
- **49152–65535:** Dynamic/Private (dinamik/özel) portlar.

Port kayıtları IANA tarafından yönetilir. Bir hizmetin tabloda yer alan varsayılan portu kullanması yaygındır ancak port numarası değiştirilebilir.

### Yaygın portlar

| Servis / protokol | Varsayılan port | Taşıma | Kullanım |
|---|---:|---|---|
| FTP | 20, 21 | TCP | Dosya aktarımı; 21 kontrol, klasik aktif FTP'de 20 veri bağlantısı için kullanılır. |
| SSH | 22 | TCP | Güvenli uzaktan terminal erişimi |
| SFTP | 22 | TCP | SSH üzerinden güvenli dosya aktarımı |
| Telnet | 23 | TCP | Şifresiz uzaktan terminal erişimi |
| SMTP | 25 | TCP | Sunucular arası e-posta aktarımı |
| DNS | 53 | UDP ve TCP | Alan adı çözümleme |
| DHCP | 67, 68 | UDP | IP yapılandırması; 67 sunucu, 68 istemci |
| TFTP | 69 | UDP | Basit dosya aktarımı |
| HTTP | 80 | TCP | Şifrelenmemiş web trafiği |
| POP3 | 110 | TCP | E-posta alma |
| NTP | 123 | UDP | Zaman eşitleme |
| IMAP | 143 | TCP | Sunucu üzerindeki e-postalara erişim |
| SNMP | 161 | Genellikle UDP | Ağ cihazlarını izleme ve yönetme |
| LDAP | 389 | TCP/UDP | Dizin hizmetlerine erişim |
| HTTPS | 443 | TCP; HTTP/3'te QUIC/UDP | TLS ile korunan web trafiği |
| SMB | 445 | TCP | Dosya ve yazıcı paylaşımı |
| LDAPS | 636 | TCP | TLS üzerinden LDAP |
| RDP | 3389 | TCP ve UDP | Uzak masaüstü erişimi |
| H.323 | 1720 | TCP | Ses/video iletişimi sinyalleşmesi |
| SIP | 5060, 5061 | TCP/UDP | Oturum başlatma; 5061 genellikle TLS |

### Önemli protokoller

**DNS (Domain Name System)**
- Alan adlarını IP adreslerine çözümlemeye yardımcı olur.
- Örnek: `example.com` alan adının IP adresini sorgulamak.
- Genellikle UDP 53 kullanır; TCP 53 de özellikle bölge transferleri ve bazı büyük yanıtlar için kullanılır.
- Komut:

```bash
nslookup example.com
```

**SNMP (Simple Network Management Protocol)**
- Router, switch ve sunucu gibi cihazların izlenmesi ve yönetilmesinde kullanılır.
- CPU, bellek ve arayüz durumu gibi bilgilerin izlenmesini sağlayabilir.
- İstekler için yaygın port UDP 161, trap mesajları için UDP 162'dir.
- Güvenlik açısından SNMPv1/v2c yerine uygun şekilde yapılandırılmış SNMPv3 tercih edilmelidir.

**LDAP ve LDAPS**
- LDAP, kullanıcı ve bilgisayar hesapları gibi dizin bilgilerinin sorgulanması ve yönetilmesi için kullanılır.
- LDAP için yaygın port TCP/UDP 389'dur.
- LDAPS, TLS ile korunan LDAP bağlantısıdır ve yaygın olarak TCP 636 kullanır.
- Active Directory ortamlarında dizin hizmetleriyle ilişkilidir.

**SMB (Server Message Block)**
- Dosya ve yazıcı paylaşımı gibi hizmetlerde kullanılır.
- Modern Windows ağlarında yaygın port TCP 445'tir.
- Gereksiz SMB erişimi, özellikle internetten erişim, güvenlik riski oluşturabilir.

**Telnet ve SSH**
- Telnet trafiği şifrelemeden iletir; kullanıcı adı ve parola gibi bilgiler ağ üzerinde okunabilir.
- SSH uzaktan erişimi şifreli biçimde sağlar.
- Yönetim için Telnet yerine SSH tercih edilmelidir.

**RDP (Remote Desktop Protocol)**
- Uzak Windows masaüstüne bağlanmayı sağlar.
- Varsayılan portu TCP 3389'dur; modern kullanımlarda UDP de devreye girebilir.
- RDP erişimi güçlü kimlik doğrulama, ağ kısıtlaması ve mümkünse VPN veya güvenli ağ geçidi arkasında korunmalıdır.

**FTP ve SFTP**
- FTP dosya aktarımı için kullanılır; standart FTP kullanıcı bilgilerini ve verileri şifrelemeden taşıyabilir.
- SFTP, SSH üzerinden çalışan ayrı bir güvenli dosya aktarım protokolüdür. FTPS ile aynı şey değildir.
- SFTP genellikle TCP 22 kullanır.

**E-posta protokolleri**
- **SMTP:** E-posta gönderimi ve sunucular arası aktarım.
- **POP3:** E-postaları sunucudan istemciye alma yöntemi.
- **IMAP:** E-postaları sunucu üzerinde klasör ve durum bilgileriyle yöneterek erişme yöntemi.

**HTTP ve HTTPS**
- HTTP, web istemcisi ile sunucu arasındaki istek/yanıt iletişimini sağlar.
- HTTPS, HTTP iletişimini TLS ile korur.
- SSL eski ve kullanımdan kaldırılmış bir teknolojidir; güncel güvenli web iletişiminde TLS kullanılır.

### Güvenlik açısından portları değerlendirme

- Bir portun açık olması tek başına sistemin savunmasız olduğu anlamına gelmez; hangi hizmetin dinlediği ve nasıl yapılandırıldığı önemlidir.
- Kullanılmayan hizmetler kapatılmalı veya erişimleri sınırlandırılmalıdır.
- SSH, RDP, SMB, LDAP ve veritabanı hizmetleri yalnızca ihtiyaç duyan ağlardan erişilebilir olmalıdır.
- Servis sürümleri güncel tutulmalı ve güçlü kimlik doğrulama uygulanmalıdır.

## 10. IP ve MAC Adresleri

### MAC adresi

MAC (Media Access Control) adresi, ağ arayüzünün veri bağlantı katmanında kullanılan adresidir.

- Ethernet MAC adresleri genellikle 48 bittir (6 bayt).
- Genellikle altı ikili hexadecimal grup ile gösterilir.
- Örnek: `00:21:70:6F:06:F2`
- İlk 24 bit çoğunlukla üreticiye ait OUI bilgisini temsil eder; kalan bölüm üretici tarafından arayüzleri tanımlamak için kullanılır.
- `FF:FF:FF:FF:FF:FF`, Ethernet broadcast hedef MAC adresidir.

**Önemli:** MAC adresleri yerel ağ iletişiminde kullanılır. MAC adresi her koşulda değişmez veya internette uçtan uca taşınır bir kimlik değildir; yazılımla değiştirilebilir (spoofing) ve router üzerinden geçerken Ethernet çerçevesindeki kaynak/hedef MAC adresleri her bağlantıda yeniden oluşturulur.

### IP adresi

IP adresi, cihazın veya ağ arayüzünün IP ağındaki mantıksal adresidir. IPv4 ve IPv6 olmak üzere iki temel sürüm bulunur.

### IPv4

IPv4 adresi 32 bitten oluşur ve dört oktet hâlinde, ondalık sayılarla gösterilir.

Örnek: `192.168.1.10`

| Oktet | Ondalık | İkili (binary) |
|---|---:|---|
| 1 | 192 | `11000000` |
| 2 | 168 | `10101000` |
| 3 | 1 | `00000001` |
| 4 | 10 | `00001010` |

Bir oktetteki bitlerin ağırlıkları soldan sağa `128, 64, 32, 16, 8, 4, 2, 1` şeklindedir.

Örnek olarak 192 sayısı:

`128 + 64 = 192`

Bu nedenle ikili gösterimi `11000000` olur.

### Ağ ve host bölümü

Bir IPv4 adresi, alt ağ maskesine göre iki mantıksal bölüme ayrılır:

- **Ağ bölümü:** Cihazın hangi IP ağına ait olduğunu belirtir.
- **Host bölümü:** O ağ içindeki arayüzü/cihazı tanımlar.

Ağ ve host bölümlerinin sınırını alt ağ maskesi veya CIDR öneki belirler.

### IPv4 adres bileşenleri

- **IP adresi:** Ağ arayüzünün mantıksal adresi.
- **Alt ağ maskesi:** IP adresinin ağ ve host bitlerini ayırır.
- **Varsayılan ağ geçidi:** Yerel ağ dışındaki hedeflere ulaşmak için paketin gönderildiği router arayüzünün IP adresidir.

Windows:

```powershell
ipconfig
ipconfig /all
```

Linux:

```bash
ip address
ip route
```

`ifconfig` bazı Linux sistemlerinde bulunabilir; modern dağıtımlarda `ip` komut ailesi yaygın olarak tercih edilir.

### IPv4 sınıfları hakkında

Geleneksel classful adresleme yaklaşımında IPv4 adresleri A, B ve C gibi sınıflara ayrılırdı:

| Sınıf | İlk oktet aralığı | Varsayılan önek | Geleneksel kullanım |
|---|---|---:|---|
| A | 1–126 | /8 | Büyük ağlar |
| B | 128–191 | /16 | Orta büyüklükte ağlar |
| C | 192–223 | /24 | Daha küçük ağlar |
| D | 224–239 | — | Multicast |
| E | 240–255 | — | Ayrılmış/deneysel aralık |

`127.0.0.0/8` loopback için ayrılmıştır. `0.0.0.0` da özel anlam taşır.

**Güncel not:** Günümüzde ağlar classful A/B/C varsayılanlarına göre değil, CIDR öneklerine göre planlanır. Sınıf bilgisi tarihsel ve temel kavramları anlamak açısından öğrenilir.

### Alt ağ maskesi ve CIDR

CIDR, ağ önek uzunluğunu `/n` biçiminde gösterir.

Örnek:

- `192.168.1.0/24`
- `/24` maskesi: `255.255.255.0`
- İkili maske: `11111111.11111111.11111111.00000000`

Burada ilk 24 bit ağ bölümünü, kalan 8 bit host bölümünü belirtir.

### IPv4 özel adres aralıkları

RFC 1918'e göre özel IPv4 adres aralıkları:

| Özel ağ | CIDR |
|---|---|
| `10.0.0.0 – 10.255.255.255` | `10.0.0.0/8` |
| `172.16.0.0 – 172.31.255.255` | `172.16.0.0/12` |
| `192.168.0.0 – 192.168.255.255` | `192.168.0.0/16` |

Bu adresler kurum ve ev içi ağlarda kullanılır; genel internette doğrudan yönlendirilebilir adresler değildir. İnternet erişimi çoğunlukla NAT gibi yöntemlerle sağlanır.

Diğer önemli özel aralıklar:

- `127.0.0.0/8`: Loopback.
- `169.254.0.0/16`: IPv4 link-local; otomatik yerel adresleme için kullanılabilir. RFC 1918 özel adres aralıklarından biri değildir.
- `0.0.0.0`: Bağlama ve varsayılan rota gibi bağlama göre farklı anlamları olan özel adres.

**Genel (public) IP:** İnternette yönlendirilebilir adres alanından tahsis edilir. Her IPv4 adresi public değildir; multicast, loopback, özel ve başka amaçlarla ayrılmış aralıklar bulunur.

### Loopback adresi

`127.0.0.1`, bilgisayarın kendi ağ yığınına erişmek için kullanılan yaygın loopback adresidir. `localhost` adı çoğunlukla loopback adreslerine çözülür.

Örnek:

```text
http://127.0.0.1
http://localhost
```

Yerel bilgisayarda çalışan bir web sunucusunu test etmek için kullanılabilir.

## 11. IP Subnetting

Subnetting, bir IP ağını daha küçük alt ağlara bölme işlemidir. Amaç IP adreslerini düzenli tahsis etmek, ağları mantıksal olarak ayırmak ve trafiği yönetmektir.

Alt ağlara bölme işlemi sırasında host bölümünden bit ödünç alınır. Ödünç alınan bit sayısı arttıkça oluşturulabilecek alt ağ sayısı artar; her alt ağdaki kullanılabilir host sayısı azalır.

### Temel kavramlar

- **Network address:** Alt ağı tanımlayan ilk adres.
- **Broadcast address:** IPv4 alt ağındaki tüm hostlara yayın yapmak için kullanılan son adres.
- **Usable host range:** Geleneksel IPv4 alt ağlarında network ve broadcast adresleri dışında kalan kullanılabilir adresler.
- **CIDR prefix:** Ağ bölümünün bit uzunluğu.

Klasik IPv4 alt ağlarında kullanılabilir host sayısı çoğunlukla:

`2^h - 2`

Burada `h`, host bitlerinin sayısıdır. Bu kuralın istisnaları vardır: örneğin `/31` point-to-point bağlantılarda iki adres de kullanılabilir; `/32` tek bir adresi ifade eder.

### FLSM (Fixed Length Subnet Masking)

FLSM'de oluşturulan tüm alt ağlar aynı önek uzunluğuna, dolayısıyla aynı büyüklüğe sahiptir.

**Örnek:** `192.168.1.0/24` ağını dört eşit alt ağa bölmek.

1. Dört alt ağ oluşturmak için 2 bit ödünç alınır: `2^2 = 4`.
2. Yeni önek `/24 + 2 = /26` olur.
3. `/26` maskesi `255.255.255.192` şeklindedir.
4. Her alt ağda 6 host biti kalır: `2^6 - 2 = 62` kullanılabilir host.

| Alt ağ | Ağ adresi | Kullanılabilir host aralığı | Broadcast |
|---:|---|---|---|
| 1 | `192.168.1.0/26` | `192.168.1.1 – 192.168.1.62` | `192.168.1.63` |
| 2 | `192.168.1.64/26` | `192.168.1.65 – 192.168.1.126` | `192.168.1.127` |
| 3 | `192.168.1.128/26` | `192.168.1.129 – 192.168.1.190` | `192.168.1.191` |
| 4 | `192.168.1.192/26` | `192.168.1.193 – 192.168.1.254` | `192.168.1.255` |

### VLSM (Variable Length Subnet Masking)

VLSM'de alt ağlar farklı büyüklüklerde oluşturulur. Böylece her ağın ihtiyacı kadar IP adresi ayrılarak adres alanı daha verimli kullanılabilir.

**Örnek ihtiyaçlar:**

- 1. ağ: 50 cihaz
- 2. ağ: 30 cihaz
- 3. ağ: 10 cihaz
- 4. ağ: 2 cihaz

Başlangıç ağı: `192.168.1.0/24`

Gerekli host bitleri:

| İhtiyaç | Host biti | Kullanılabilir host | Önek |
|---:|---:|---:|---:|
| 50 cihaz | 6 | 62 | /26 |
| 30 cihaz | 5 | 30 | /27 |
| 10 cihaz | 4 | 14 | /28 |
| 2 cihaz | 2 | 2 | /30 |

Alt ağlar genellikle en büyük ihtiyaçtan en küçüğe doğru yerleştirilir. Böylece adres blokları çakışmadan ayrılabilir.

| Ağ | Ağ adresi | Kullanılabilir host aralığı | Broadcast |
|---:|---|---|---|
| 50 cihaz | `192.168.1.0/26` | `192.168.1.1 – 192.168.1.62` | `192.168.1.63` |
| 30 cihaz | `192.168.1.64/27` | `192.168.1.65 – 192.168.1.94` | `192.168.1.95` |
| 10 cihaz | `192.168.1.96/28` | `192.168.1.97 – 192.168.1.110` | `192.168.1.111` |
| 2 cihaz | `192.168.1.112/30` | `192.168.1.113 – 192.168.1.114` | `192.168.1.115` |

### Subnetting yaparken izlenecek yol

1. Başlangıç IP adresini ve önek uzunluğunu belirle.
2. Her alt ağın kaç hosta ihtiyaç duyduğunu öğren.
3. Her ihtiyaç için yeterli host biti sayısını hesapla.
4. Gerekli CIDR önekini belirle.
5. Alt ağları çakışmayacak şekilde, genellikle büyükten küçüğe sırala.
6. Her alt ağ için network, kullanılabilir host aralığı ve broadcast adresini bul.
7. Ayrılan blokların başlangıç ve bitişlerini kontrol et.

### Subnetting neden güvenlik açısından önemlidir?

- Farklı departmanları veya sistem türlerini ayrı alt ağlarda tutmayı sağlar.
- VLAN ve firewall kurallarıyla birlikte kullanıldığında ağ segmentasyonunu destekler.
- Sunucu, kullanıcı ve yönetim ağlarını ayırarak erişim denetimini kolaylaştırır.
- Bir sistemdeki güvenlik olayının diğer ağ bölümlerine yayılmasını sınırlamaya yardımcı olabilir.

---

## Hızlı Tekrar

| Kavram | Hatırlanması gereken |
|---|---|
| LAN | Yerel alan ağı |
| WAN | Geniş alan ağı |
| Switch | MAC adresine göre yerel ağda çerçeve iletir |
| Router | IP ağları arasında paket yönlendirir |
| Firewall | Trafiği güvenlik kurallarına göre denetler |
| OSI | 7 katmanlı referans modeli |
| TCP/IP | 4 katmanlı internet modellemesi |
| TCP | Bağlantı odaklı, güvenilir aktarım mekanizmaları |
| UDP | Bağlantısız, teslim/sıralama garantisi olmayan aktarım |
| DNS | Alan adlarını IP adreslerine çözümler |
| SSH | Şifreli uzaktan erişim, varsayılan TCP 22 |
| HTTP / HTTPS | Web iletişimi; HTTPS TLS ile korunur |
| MAC | Yerel bağlantıda kullanılan arayüz adresi |
| IPv4 | 32 bit |
| IPv6 | 128 bit |
| CIDR | `/24` gibi ağ öneki gösterimi |
| FLSM | Eşit büyüklükte alt ağlar |
| VLSM | Farklı büyüklükte alt ağlar |

## Uygulama Komutları

Windows:

```powershell
ipconfig
ipconfig /all
ping 8.8.8.8
nslookup example.com
arp -a
```

Linux:

```bash
ip address
ip route
ping -c 4 8.8.8.8
nslookup example.com
arp -a
```

> **Güvenli laboratuvar alışkanlığı:** Ağ taraması veya servis kontrolü yaparken yalnızca sahibi olduğun ya da açıkça test iznin bulunan sistemleri hedefle.

---

*Bu dosya kişisel öğrenme notudur. Konular ilerledikçe yeni örnekler, laboratuvar çıktıları ve kendi açıklamalarım eklenebilir.*


---

# 12. Ağ Temelleri – Sınav Soruları ve Cevapları

Bu bölüm, Ağ Temelleri konularını tekrar etmek için hazırlanmış 16 soruluk değerlendirme sınavının cevaplarını ve kısa açıklamalarını içerir.

> **Not:** 2. soruda “internet kablosu” ifadesi Ethernet ağ kablosu anlamında kullanılmıştır. Bu bağlamda yaygın bağlantı konnektörü RJ-45'tir. Farklı internet erişim teknolojilerinde fiber optik veya koaksiyel bağlantılar da kullanılabilir.

### Sorular ve cevaplar

1. **Gelen veri paketlerini bağlı olduğu tüm portlara ileterek iletişim sağlayan ağ cihazı hangisidir?**  
   **Cevap: Hub.** Hub, aldığı veriyi hedef cihazı ayırt etmeden diğer portlarına iletir.

2. **Ethernet ağ kablolarında yaygın olarak hangi bağlantı konnektörü kullanılır?**  
   **Cevap: RJ-45.** Bükümlü çift Ethernet kablolarında yaygın kullanılan konnektördür.

3. **Ağ topolojileri hangi özellikler üzerinde farklılık gösterir?**  
   **Cevap:** Cihazların ağa fiziksel veya mantıksal olarak nasıl bağlandıkları ve aralarındaki iletişimin nasıl düzenlendiği.

4. **Full-Duplex iletişim modunun özelliği nedir?**  
   **Cevap:** İki tarafın aynı anda veri gönderip alabilmesi.

5. **OSI modeli kaç katmandan oluşur?**  
   **Cevap: 7 katman.**

6. **OSI modelinin Fiziksel Katmanı hangi işlevi yerine getirir?**  
   **Cevap:** Verileri bitler hâlinde fiziksel ortam üzerinden elektriksel, optik veya radyo sinyalleriyle iletir.

7. **Bilgisayar ağlarının çalışmasını katmanlara ayırarak daha ayrıntılı açıklamak için kullanılan model hangisidir?**  
   **Cevap: OSI modeli.**

8. **TCP/IP modelinde yer almayan OSI katmanı hangisidir?**  
   **Cevap: Oturum (Session) katmanı.** TCP/IP modelinde Uygulama, Taşıma, İnternet ve Ağ Erişimi katmanları bulunur.

9. **TCP/IP modelinde Taşıma Katmanı'nın temel işlevi nedir?**  
   **Cevap:** Uçtan uca iletişimi ve uygulamalar arasındaki veri aktarımını yönetmek; TCP veya UDP gibi protokollerle iletişimi sağlamaktır.

10. **TCP 3-Way Handshake sürecinde ilk gönderilen mesaj hangisidir?**  
    **Cevap: SYN.** İstemci bağlantı isteğini SYN bayrağıyla başlatır.

11. **Bir bilgisayarın ağ kartına özgü, üretici tarafından atanan donanım adresi hangisidir?**  
    **Cevap: MAC adresi.**

12. **IP adresi ile alan adları arasındaki çözümlemeyi sağlayan protokol hangisidir?**  
    **Cevap: DNS (Domain Name System).** DNS, alan adlarını IP adreslerine çözümler; ters DNS sorgularında IP adresinden alan adına ulaşılabilir.

13. **10.10.1.3/16 IP adresinin alt ağ maskesi nedir?**  
    **Cevap: 255.255.0.0.**

14. **10.10.1.3/16 IP adresinin ağ adresi nedir?**  
    **Cevap: 10.10.0.0.** İlk 16 bit ağ bölümünü belirtir.

15. **10.10.1.3/16 ağında kullanılabilecek en fazla host adresi sayısı kaçtır?**  
    **Cevap: 65.534.** Host bit sayısı 16'dır: \(2^{16}-2=65.534\). Geleneksel IPv4 ağlarında ağ ve yayın adresleri hostlara atanmaz.

16. **192.168.5.0/27 ağı 4 eşit alt ağa bölündüğünde 3. alt ağın ağ adresi nedir?**  
    **Cevap: 192.168.5.16/29.**

    **Hesaplama:**
    - Başlangıç ağı: `/27`
    - 4 alt ağ için 2 bit ödünç alınır: `/27 + 2 = /29`
    - Her `/29` alt ağında 8 adres bulunur.
    - Alt ağların başlangıç adresleri sırasıyla:
      - 1. alt ağ: `192.168.5.0/29`
      - 2. alt ağ: `192.168.5.8/29`
      - 3. alt ağ: `192.168.5.16/29`
      - 4. alt ağ: `192.168.5.24/29`

### Hızlı tekrar tablosu

| Konu | Hatırlanacak bilgi |
|---|---|
| Hub | Gelen veriyi diğer portlara iletir. |
| RJ-45 | Ethernet bakır ağ kablolarında yaygın konnektör. |
| Full-Duplex | Aynı anda gönderme ve alma. |
| OSI | 7 katman. |
| TCP/IP | 4 katmanlı model. |
| 3-Way Handshake | SYN → SYN-ACK → ACK |
| MAC | Ağ arayüzünün donanım adresi. |
| DNS | Alan adı ve IP adresi çözümlemesi. |
| `/16` | `255.255.0.0`, 65.534 kullanılabilir IPv4 host adresi. |
| `/27` ağını 4'e bölmek | Dört adet `/29` alt ağ oluşur. |
