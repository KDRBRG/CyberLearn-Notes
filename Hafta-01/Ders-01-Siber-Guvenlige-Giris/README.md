# Ders 01 – Siber Güvenliğe Giriş

## 1. Siber Güvenlik Nedir?

Siber güvenlik; bilgisayarları, ağları, yazılımları, sunucuları ve dijital verileri yetkisiz erişimlere, saldırılara, zararlı yazılımlara ve veri kayıplarına karşı korumayı amaçlayan çalışmaların bütünüdür.

Temel amaç, dijital sistemlerin güvenliğini ve sürekliliğini sağlamaktır.

### Bilgi Güvenliğinin Üç Temel İlkesi (CIA Triad)

Bilgi güvenliği üç temel ilkeye dayanır:

| İlke | Açıklama | Örnek |
|---|---|---|
| Gizlilik (Confidentiality) | Bilgiye yalnızca yetkili kişilerin erişebilmesi. | Bir kullanıcının başkasının hesabına erişememesi. |
| Bütünlük (Integrity) | Bilginin izinsiz değiştirilmemesi ve doğruluğunun korunması. | Bir banka bakiyesinin yetkisiz şekilde değiştirilmemesi. |
| Erişilebilirlik (Availability) | Bilgi ve sistemlerin ihtiyaç duyulduğunda kullanılabilir olması. | Bir web sitesinin kullanıcılar tarafından erişilebilir kalması. |

Bu üç ilke birlikte CIA Triad olarak adlandırılır.

## 2. Hacker Kavramı ve Türleri

Hacker, bilgisayar sistemlerinin, ağların veya yazılımların çalışma mantığını inceleyen ve teknik bilgisiyle bunlar üzerinde işlemler gerçekleştiren kişidir.

Hackerlar amaçlarına ve davranışlarına göre farklı gruplara ayrılabilir.

- **White Hat:** Sistemleri izinli olarak test eder, güvenlik açıklarını tespit eder ve giderilmesine yardımcı olur.
- **Black Hat:** Yetkisiz erişim, veri hırsızlığı veya sisteme zarar verme gibi kötü niyetli faaliyetlerde bulunur.
- **Gray Hat:** Her zaman kötü niyetli olmasa da bazen izinsiz güvenlik testleri gerçekleştirebilir.

**Ethical Hacker (Etik Hacker):** Kurum veya sistem sahibinin izniyle güvenlik testleri yapan kişidir. Çalışmalarını belirlenen kapsam ve yasal sınırlar içerisinde yürütür.

## 3. Siber Güvenliğin Alt Alanları

Siber güvenlik geniş bir alandır. Farklı uzmanlık alanları bulunur.

### Application Security
Yazılımların geliştirilme aşamasından kullanıma sunulmasına kadar güvenliğinin sağlanmasıdır.

### Web Application Security
Web uygulamalarındaki güvenlik açıklarını inceleyen alandır.

Önemli güvenlik açığı türleri:

- SQL Injection (SQLi): Veritabanı sorgularının kötüye kullanılabilmesi.
- Cross-Site Scripting (XSS): Web sayfası üzerinden zararlı istemci tarafı kodların çalıştırılması.
- Cross-Site Request Forgery (CSRF): Kullanıcının oturumundan yararlanılarak istemediği bir işlemin gerçekleştirilmesi.
- Insecure Direct Object Reference (IDOR): Yetkilendirme kontrollerindeki eksiklikler nedeniyle başka kullanıcılara ait kaynaklara erişilebilmesi.

### Network Security
Bilgisayar ağlarını yetkisiz erişimlere, saldırılara ve veri sızıntılarına karşı korumayı amaçlar.

### Reverse Engineering
Bir yazılımın veya cihazın çalışma mantığını inceleyerek nasıl çalıştığını anlamaya yönelik çalışmalardır. Zararlı yazılım analizi ve güvenlik araştırmalarında kullanılabilir.

### Cloud Security
Bulut ortamlarında bulunan verilerin, uygulamaların ve altyapının korunmasıdır.

### Mobile Application Security
Mobil uygulamaların ve mobil cihazlarda işlenen verilerin güvenliğini inceler.

### IoT Security
Akıllı cihazlar, sensörler ve internete bağlı fiziksel sistemlerin güvenliğini kapsar.

### Digital Forensics
Dijital ortamlardaki delillerin toplanması, korunması ve analiz edilmesiyle ilgilenir.

### Threat Intelligence
Siber tehditler hakkında bilgi toplama, analiz etme ve bu bilgileri güvenlik kararlarında kullanma sürecidir.

## 4. Siber Güvenlikte Kariyer Alanları

Siber güvenlikte farklı ekipler ve çalışma yaklaşımları bulunur.

### Red Team
Saldırgan bakış açısıyla hareket ederek kurumun güvenlik önlemlerini izinli testlerle değerlendirir.

### Blue Team
Sistemleri savunur; tehditleri izler, saldırıları tespit eder ve olaylara müdahale eder.

### Purple Team
Red Team ve Blue Team arasındaki iş birliğini güçlendirir. Saldırı testlerinden elde edilen sonuçların savunma sistemlerini geliştirmek için kullanılmasını sağlar.

### Bug Bounty
Kurumların belirlediği kapsam ve kurallar içerisinde güvenlik açıklarını bulan araştırmacıların, geçerli bulguları karşılığında ödül kazanabildiği programlardır.

Not: Her kurumda bu ekipler ayrı departmanlar şeklinde bulunmayabilir. Bir kişi veya ekip birden fazla sorumluluk üstlenebilir.

## 5. Sızma Testi (Penetration Testing)

Sızma testi, bir sistemin güvenliğini değerlendirmek amacıyla yetkili kişiler tarafından gerçekleştirilen kontrollü güvenlik testidir.

Amaç, saldırganlar tarafından kullanılabilecek zayıflıkları tespit etmek ve kurumun güvenlik seviyesini artırmaktır.

### Sızma Testinin Temel Aşamaları

1. Kapsam ve yetkilendirmenin belirlenmesi.
2. Bilgi toplama.
3. Güvenlik açıklarının araştırılması.
4. Kontrollü doğrulama ve test.
5. Bulguların analiz edilmesi.
6. Raporlama ve iyileştirme önerileri.

### Bilgi Seviyesine Göre Sızma Testleri

- **Black Box:** Test uzmanına hedef sistem hakkında önceden çok az bilgi verilir veya hiç bilgi verilmez.
- **Grey Box:** Test uzmanına sınırlı bilgi veya kullanıcı erişimi sağlanır.
- **White Box:** Test uzmanına sistemin mimarisi, kaynak kodu veya yapılandırması gibi ayrıntılı bilgiler verilir.

### Güvenlik Testlerinde Kullanılan Referanslar

- **OWASP:** Özellikle web uygulama güvenliği alanında rehberler, risk sınıflandırmaları ve test kaynakları sunar.
- **OSSTMM:** Güvenlik testleri için yapılandırılmış bir metodoloji sunar.
- **NIST SP 800-115:** Teknik bilgi güvenliği testleri ve değerlendirmeleri için rehber niteliğindedir.

Bu kaynaklar aynı türde dokümanlar değildir; farklı amaçlarla kullanılabilir.

## 6. Temel Teknik Kavramlar

### Port Nedir?

Port, bir cihaz üzerindeki ağ iletişiminin hangi hizmet veya uygulamaya yönlendirileceğini belirlemeye yardımcı olan mantıksal numaradır.

Yaygın portlar:

| Port | Protokol / Hizmet | Kullanım |
|---|---|---|
| 21 | FTP | Dosya aktarımı |
| 22 | SSH | Güvenli uzaktan bağlantı |
| 23 | Telnet | Uzaktan bağlantı |
| 25 | SMTP | E-posta gönderimi |
| 53 | DNS | Alan adı çözümleme |
| 80 | HTTP | Web iletişimi |
| 443 | HTTPS | Şifreli web iletişimi |
| 3306 | MySQL | Veritabanı hizmeti |
| 3389 | RDP | Windows uzak masaüstü |
| 5432 | PostgreSQL | Veritabanı hizmeti |

Not: Port numaraları yaygın varsayılan kullanımlardır. Bir hizmet farklı bir portta da çalışabilir.

### Temel Güvenlik Terimleri

- **Vulnerability (Güvenlik Açığı):** Bir sistemin güvenliğini olumsuz etkileyebilecek zayıflık.
- **OWASP Top 10:** Web uygulamalarında önemli güvenlik risklerini tanıtan OWASP kaynaklarından biri.
- **CVE:** Bilinen güvenlik açıklarına verilen standart kimlik numarası sistemi.
- **CVSS:** Güvenlik açıklarının teknik ciddiyetini değerlendirmek için kullanılan puanlama sistemi.
- **Exploit:** Bir güvenlik açığından yararlanan yöntem veya kod.
- **PoC (Proof of Concept):** Bir güvenlik açığının varlığını göstermeye yönelik kavramsal veya teknik kanıt.
- **Zero-Day:** Üreticinin henüz düzeltme yayımlamadığı veya savunma açısından henüz giderilmemiş güvenlik açığı için kullanılan terim.
- **Shell:** İşletim sistemiyle komutlar aracılığıyla etkileşim kurmayı sağlayan arayüz.
- **Bind Shell:** Hedef sistemde belirli bir portu dinleyen kabuk bağlantısı yaklaşımı.
- **Reverse Shell:** Hedef sistemin dışarıdaki bir sisteme bağlantı başlatmasıyla kurulan kabuk bağlantısı yaklaşımı.
- **Web Shell:** Web sunucusu üzerinden komut çalıştırılmasına imkân verebilen zararlı veya kötüye kullanılabilir betik.

### IP Adresi

IP adresi, ağ üzerindeki cihazların birbirleriyle iletişim kurabilmesi için kullanılan mantıksal adresleme sistemidir.

- **IPv4:** 32 bit uzunluğundadır. Örnek: `192.168.1.10`
- **IPv6:** 128 bit uzunluğundadır ve IPv4'e göre çok daha geniş adres alanı sunar.

## 7. Yararlı Kaynaklar

- [Hackviser – Pentesting Tactics](https://hackviser.com/tactics/pentesting)
- [Hackviser – Hardening Tactics](https://hackviser.com/tactics/hardening)
- [Hackviser – Tools Tactics](https://hackviser.com/tactics/tools)
- [OWASP](https://owasp.org/)
- [NIST Computer Security Resource Center](https://csrc.nist.gov/)

## Öğrenme Özeti

Bu derste siber güvenliğin temel amacı, bilgi güvenliğinin üç ilkesi, hacker türleri, siber güvenlik uzmanlık alanları, Red/Blue/Purple Team yaklaşımları, sızma testi ve temel ağ-güvenlik kavramları ele alınmıştır.

Bir sonraki aşamada bu bilgiler değerlendirme soruları ve uygulama çalışmalarıyla pekiştirilebilir.
