# Ders 01 – Siber Güvenliğe Giriş

## İçindekiler

1. [Giriş ve Bilgi Güvenliği](#1-giriş-ve-bilgi-güvenliği)
2. [Hacker Kavramı ve Türleri](#2-hacker-kavramı-ve-türleri)
3. [Siber Güvenliğin Alt Alanları](#3-siber-güvenliğin-alt-alanları)
4. [Siber Güvenlikte Kariyer Alanları](#4-siber-güvenlikte-kariyer-alanları)
5. [Sızma Testi (Penetration Testing)](#5-sızma-testi-penetration-testing)
6. [Temel Teknik Bilgiler ve Kavramlar](#6-temel-teknik-bilgiler-ve-kavramlar)
7. [Yararlı Kaynaklar](#7-yararlı-kaynaklar)

---

# 1. Giriş ve Bilgi Güvenliği

## 1.1. Siber Güvenlik Nedir?

Siber güvenlik; bilgisayarları, sunucuları, ağları, yazılımları, mobil cihazları ve dijital verileri yetkisiz erişimlere, saldırılara, zararlı yazılımlara ve veri kayıplarına karşı korumayı amaçlayan çalışmaların bütünüdür.

Günümüzde bireyler ve kurumlar birçok işlemi dijital ortamda gerçekleştirmektedir. Bankacılık işlemleri, alışveriş, haberleşme, eğitim ve kamu hizmetleri bunlardan bazılarıdır.

Dijital sistemlerin kullanımının artması, bu sistemlerde bulunan bilgilerin korunmasını da önemli hâle getirmiştir.

Örneğin:
- Bir bankanın müşteri bilgilerinin korunması gerekir.
- Bir hastanenin hasta kayıtlarına yalnızca yetkili kişilerin erişebilmesi gerekir.
- Bir şirketin web sitesinin saldırılar nedeniyle hizmet dışı kalmaması gerekir.
- Bir kullanıcının sosyal medya hesabının ele geçirilmesi önlenmelidir.

Siber güvenliğin temel amacı yalnızca saldırıları engellemek değildir. Aynı zamanda saldırıları tespit etmek, etkilerini azaltmak, sistemleri kurtarmak ve gelecekte benzer olayların yaşanmasını önlemektir.

## 1.2. Bilgi ve Bilgi Güvenliği

**Bilgi**, işlenmiş, anlamlandırılmış ve bir amaç doğrultusunda kullanılabilen veridir.

Veriler tek başına anlamlı olmayabilir. Ancak düzenlenip yorumlandıklarında bilgiye dönüşebilir.

**Bilgi güvenliği**, bilginin yetkisiz erişim, değiştirilme, kaybolma veya kullanılamama gibi risklere karşı korunmasıdır.

Bilgi güvenliği yalnızca bilgisayarlarla ilgili değildir. Basılı belgeler, fiziksel arşivler ve sözlü olarak aktarılan bilgiler de korunmalıdır.

Örneğin:
- Bir şirketin müşteri listesinin korunması,
- Çalışanların maaş bilgilerinin gizli tutulması,
- Bir hastanın sağlık kayıtlarının değiştirilmemesi,
- Önemli belgelerin ihtiyaç duyulduğunda erişilebilir olması bilgi güvenliğinin kapsamına girer.

## 1.3. Bilgi Güvenliğinin Üç Temel İlkesi (CIA Triad)

Bilgi güvenliğinin temelini üç önemli ilke oluşturur. Bu ilkeler İngilizce karşılıklarının baş harfleriyle **CIA Triad** olarak adlandırılır.

### A. Gizlilik (Confidentiality)

Bilgilere yalnızca erişim yetkisi bulunan kişilerin ulaşabilmesini ifade eder.

Amaç, bilgilerin yetkisiz kişiler tarafından görülmesini veya ele geçirilmesini önlemektir.

**Örnekler:**
- Bir kullanıcının yalnızca kendi banka hesabını görüntüleyebilmesi.
- Hastanın sağlık kayıtlarına yalnızca yetkili sağlık personelinin erişebilmesi.
- Şirketin gizli belgelerinin yetkisiz çalışanlara açılmaması.

**Gizliliği sağlamaya yardımcı yöntemler:**
- Parola ve çok faktörlü kimlik doğrulama (MFA)
- Erişim kontrolü
- Yetkilendirme
- Veri şifreleme
- Kullanıcı hesaplarının düzenli denetlenmesi

### B. Bütünlük (Integrity)

Bilginin doğruluğunun ve tutarlılığının korunmasını ifade eder. Bilginin yetkisiz veya istenmeyen şekilde değiştirilmesini önlemeyi amaçlar.

**Örnekler:**
- Banka hesabındaki bakiyenin izinsiz değiştirilmemesi.
- Bir öğrencinin notunun yetkisiz şekilde düzenlenememesi.
- Bir dosyanın aktarım sırasında değiştirilip değiştirilmediğinin kontrol edilmesi.

**Bütünlüğü sağlamaya yardımcı yöntemler:**
- Hash algoritmaları
- Dijital imzalar
- Dosya bütünlüğü izleme (FIM)
- Erişim kontrolü
- Kayıt ve değişiklik takibi

Hash işlemi, veriden belirli uzunlukta bir özet değer üretilmesini sağlar. Dosyanın hash değeri değişmişse dosyanın içeriğinde bir değişiklik meydana gelmiş olabilir. Ancak bunun nedenini tek başına göstermez.

### C. Erişilebilirlik (Availability)

Bilgiye ve sistemlere ihtiyaç duyulduğunda erişilebilmesini ifade eder.

Bir sistem güvenli olsa bile kullanıcılar ihtiyaç duyduklarında sisteme ulaşamıyorsa erişilebilirlik açısından sorun yaşanır.

**Örnekler:**
- Bir bankacılık uygulamasının müşteriler tarafından kullanılabilir olması.
- Bir hastanenin kayıt sisteminin kesintisiz çalışması.
- Bir web sitesinin yoğun trafik altında hizmet vermeye devam etmesi.

**Erişilebilirliği sağlamaya yardımcı yöntemler:**
- Yedekleme
- Sistem ve ağ yedekliliği
- DDoS koruması
- Düzenli bakım
- Felaket kurtarma planları
- Kesintisiz güç kaynakları

### CIA Triad Özet Tablosu

| İlke | Temel soru | Örnek ihlal |
|---|---|---|
| Gizlilik | Bilgiyi kim görebilir? | Yetkisiz kişinin müşteri verilerini okuması |
| Bütünlük | Bilgi doğru ve değiştirilmemiş mi? | Bir kaydın izinsiz değiştirilmesi |
| Erişilebilirlik | Bilgiye ihtiyaç duyulduğunda ulaşılabiliyor mu? | DDoS saldırısı nedeniyle web sitesinin kapanması |

**Önemli:** Bir güvenlik olayı aynı anda birden fazla ilkeyi etkileyebilir. Örneğin fidye yazılımı bir yandan dosyaları erişilemez hâle getirirken diğer yandan verilerin gizliliğini de tehlikeye atabilir.

---

# 2. Hacker Kavramı ve Türleri

## 2.1. Hacker Nedir?

Hacker, bilgisayar sistemlerinin, ağların ve yazılımların çalışma mantığını anlayan; teknik bilgisini kullanarak bu sistemleri inceleyen veya değiştiren kişidir.

Hacker kavramı her zaman kötü niyetli kişileri ifade etmez. Bir sistemin güvenliğini geliştirmek için çalışan uzmanlar da teknik anlamda hacker olarak tanımlanabilir.

Bir kişinin yaptığı çalışmanın etik ve yasal olup olmadığını belirleyen önemli unsurlardan biri, sistem sahibinin izninin bulunmasıdır.

## 2.2. Hacker Türleri

Hackerlar genellikle amaçlarına ve davranışlarına göre farklı gruplara ayrılır.

### White Hat Hacker (Beyaz Şapkalı)

Sistemlerin güvenliğini geliştirmek amacıyla çalışan, yetkili ve etik güvenlik araştırmacılarıdır.

Görevleri arasında:
- Güvenlik açıklarını tespit etmek,
- Yetkili sızma testleri gerçekleştirmek,
- Bulguları raporlamak,
- Kurumların güvenlik önlemlerini geliştirmesine yardımcı olmak bulunur.

**Örnek:** Bir şirketin yazılı izin verdiği güvenlik testinde web uygulamasındaki bir açığı tespit edip şirkete raporlayan uzman.

### Black Hat Hacker (Siyah Şapkalı)

Kötü niyetli amaçlarla hareket eden ve yetkisiz faaliyetlerde bulunan kişilerdir.

Amaçları arasında:
- Bilgi çalmak,
- Sistemlere zarar vermek,
- Hesapları ele geçirmek,
- Fidye talep etmek,
- Yetkisiz erişim sağlamak bulunabilir.

**Örnek:** Bir kurumun sistemine izinsiz girerek müşteri bilgilerini çalan kişi.

### Gray Hat Hacker (Gri Şapkalı)

White Hat ve Black Hat yaklaşımları arasında değerlendirilen kişilerdir.

Bazen kötü niyet taşımadan güvenlik açığı araştırabilirler. Ancak sistem sahibinden izin almadan test yapmaları etik ve hukuki sorunlara neden olabilir.

**Örnek:** Bir web sitesinde güvenlik açığı bulan ancak önceden yetki almadan test gerçekleştiren araştırmacı.

### Ethical Hacker (Etik Hacker)

Sistem sahibinin izniyle, belirlenmiş kapsam ve kurallar doğrultusunda güvenlik testi yapan kişidir.

Etik hackerın amacı sisteme zarar vermek değil, güvenlik zayıflıklarını tespit ederek bunların giderilmesine yardımcı olmaktır.

**Önemli ayrım:** Teknik olarak bir açığı bulabilmek, o sistemi izinsiz test etme hakkı vermez. Güvenlik çalışmaları önceden belirlenmiş yetki ve kapsam içerisinde yürütülmelidir.

## 2.3. Algoritma ve Problem Çözme Mantığı

Siber güvenlikte yalnızca araç kullanmayı bilmek yeterli değildir. Problemleri analiz edebilmek ve çözüm üretebilmek de önemlidir.

Örneğin bir programın belirli bir matematiksel işlemi nasıl gerçekleştirdiğini incelemek, algoritmik düşünme becerisini geliştirebilir.

1'den 100'e kadar olan sayıların karelerinin toplamını hesaplayalım:

\[
1^2+2^2+3^2+\cdots+100^2
\]

Bu işlem için kullanılan genel formül:

\[
\frac{n(n+1)(2n+1)}{6}
\]

\(n=100\) olduğunda sonuç:

\[
\frac{100 \times 101 \times 201}{6}=338350
\]

Bu örnek, aynı problemin tek tek işlem yapmak yerine matematiksel bir formülle daha verimli çözülebileceğini gösterir.

Siber güvenlik uzmanları da karşılaştıkları problemleri analiz ederken algoritmik düşünmeden yararlanır.

---

# 3. Siber Güvenliğin Alt Alanları

Siber güvenlik çok geniş bir alandır. Her uzmanlık alanı farklı sistemleri, teknolojileri ve güvenlik ihtiyaçlarını ele alır.

## 3.1. Application Security (Uygulama Güvenliği)

Yazılımların geliştirilmesi, test edilmesi ve kullanıma sunulması sırasında güvenliğinin sağlanmasıyla ilgilenir.

Amaç, uygulamalarda oluşabilecek güvenlik açıklarını mümkün olduğunca erken tespit etmektir.

Başlıca çalışma konuları:
- Güvenli yazılım geliştirme
- Kaynak kod analizi
- Kimlik doğrulama ve yetkilendirme
- Güvenli oturum yönetimi
- Bağımlılık ve kütüphane güvenliği
- Güvenlik testleri

**Örnek:** Bir alışveriş uygulamasında kullanıcıların başka müşterilerin sipariş bilgilerine erişmesini engellemek.

## 3.2. Web Application Security (Web Uygulama Güvenliği)

İnternet tarayıcısı üzerinden kullanılan web uygulamalarının güvenliğini inceleyen alandır.

Web uygulamaları kullanıcı bilgileri, ödeme kayıtları ve kişisel veriler gibi önemli bilgileri işleyebilir. Bu nedenle uygulamanın hem sunucu hem de istemci tarafında güvenlik önlemleri bulunmalıdır.

Sık karşılaşılan güvenlik açıkları:

### SQL Injection (SQLi)

Uygulamanın veritabanıyla iletişim kurarken kullanıcı girdilerini güvenli şekilde işlememesi sonucunda ortaya çıkabilen bir güvenlik açığıdır.

Saldırgan, uygulamanın SQL sorgularını beklenmeyen biçimde etkilemeye çalışabilir.

**Olası sonuçlar:**
- Yetkisiz veri görüntüleme
- Verilerin değiştirilmesi
- Verilerin silinmesi
- Uygulamanın veritabanı güvenliğinin tehlikeye girmesi

**Korunma yöntemleri:**
- Parametreli sorgular kullanmak
- Kullanıcı girdilerini doğru şekilde işlemek
- Veritabanı hesaplarına gerekli en düşük yetkiyi vermek
- Güvenli kod geliştirme ve test süreçleri uygulamak

### Cross-Site Scripting (XSS)

Bir web uygulamasının kullanıcıya gösterdiği içerik üzerinden zararlı istemci tarafı betiklerin çalıştırılabilmesine neden olan güvenlik açığıdır.

**Olası sonuçlar:**
- Kullanıcı oturumunun tehlikeye girmesi
- Kullanıcı adına istenmeyen işlemler yapılması
- Sayfa içeriğinin değiştirilmesi
- Kullanıcının zararlı içeriklere yönlendirilmesi

**Korunma yöntemleri:**
- Çıktı kodlama (Output Encoding)
- Güvenli HTML işleme
- İçerik Güvenliği Politikası (CSP)
- Kullanıcı girdilerinin uygun şekilde doğrulanması

### Cross-Site Request Forgery (CSRF)

Kullanıcının oturumunun açık olmasından yararlanarak, kullanıcının istemediği bir işlemin gerçekleştirilmesine neden olabilen saldırı türüdür.

**Örnek:** Bir kullanıcının oturumu açıkken, kötü niyetli bir sayfanın onun adına yetkisiz bir işlem başlatmaya çalışması.

**Korunma yöntemleri:**
- CSRF token kullanımı
- SameSite cookie ayarları
- Hassas işlemlerde ek doğrulama
- İsteklerin kaynağının uygun şekilde kontrol edilmesi

### Insecure Direct Object Reference (IDOR)

Bir uygulamanın kullanıcıların erişebileceği kaynakları doğru şekilde yetkilendirmemesi sonucu ortaya çıkan güvenlik açığıdır.

**Örnek:** Bir kullanıcının URL'deki sipariş numarasını değiştirerek başka bir müşterinin sipariş bilgilerine ulaşabilmesi.

**Korunma yöntemleri:**
- Her istekte sunucu tarafında yetkilendirme kontrolü
- Kullanıcının yalnızca kendi kaynaklarına erişmesini sağlama
- Kaynak kimliklerinin tahmin edilmesinin zorlaştırılmasını tek başına güvenlik önlemi olarak görmeme

**Önemli:** IDOR'un temel nedeni genellikle yetkilendirme kontrolünün eksik olmasıdır. Sadece URL'deki numaraları gizlemek sorunu çözmez.

## 3.3. Network Security (Ağ Güvenliği)

Bilgisayar ağlarının, ağ cihazlarının ve ağ üzerinden aktarılan verilerin korunmasıyla ilgilenir.

Ağ güvenliğinin amacı, yetkisiz erişimleri önlemek, ağ trafiğini izlemek ve olası saldırıları tespit etmektir.

Başlıca konular:
- Firewall (Güvenlik Duvarı)
- IDS (Saldırı Tespit Sistemi)
- IPS (Saldırı Önleme Sistemi)
- VPN
- Ağ segmentasyonu
- Port ve servis analizi
- Ağ trafiği izleme
- Kablosuz ağ güvenliği

**Örnek:** Bir kurumun misafir Wi-Fi ağı ile şirketin iç ağını birbirinden ayırması.

## 3.4. Reverse Engineering (Tersine Mühendislik)

Bir yazılımın veya cihazın çalışma mantığını, iç yapısını ve davranışlarını inceleyerek nasıl çalıştığını anlamaya yönelik çalışmalardır.

Tersine mühendislik özellikle yazılım analizi ve zararlı yazılım araştırmalarında kullanılır.

Çalışma konuları:
- Programın davranışını analiz etmek
- Dosya ve ikili programları incelemek
- Yazılımın kullandığı işlevleri anlamak
- Zararlı yazılım analizleri yapmak
- Güvenlik zafiyetlerini araştırmak

**Örnek:** Şüpheli bir dosyanın sanal ve izole bir ortamda çalıştırılarak davranışlarının incelenmesi.

## 3.5. Cloud Security (Bulut Güvenliği)

Bulut sistemlerinde bulunan verilerin, uygulamaların, hesapların ve altyapının korunmasıyla ilgilenir.

Bulut hizmetlerinde yanlış yapılandırmalar önemli güvenlik riskleri oluşturabilir.

Başlıca konular:
- Bulut kimlik ve erişim yönetimi
- Veri şifreleme
- Güvenli yapılandırma
- Log ve etkinlik takibi
- Yedekleme
- Bulut ağ güvenliği

**Örnek:** Bir şirketin bulut ortamında sakladığı dosyaların herkese açık hâle gelmesini önlemek.

## 3.6. Mobile Application Security (Mobil Uygulama Güvenliği)

Android ve iOS gibi mobil platformlarda çalışan uygulamaların güvenliğini inceler.

Başlıca konular:
- Güvenli veri depolama
- API güvenliği
- Kimlik doğrulama
- Uygulama izinleri
- Şifreleme
- Güvenli iletişim
- Uygulama analizi

**Örnek:** Bir mobil bankacılık uygulamasında kullanıcı bilgilerinin cihaz üzerinde güvenli şekilde saklanması.

## 3.7. IoT Security (Nesnelerin İnterneti Güvenliği)

İnternete bağlanabilen fiziksel cihazların güvenliğini kapsar.

IoT cihazlarına örnek:
- Akıllı kameralar
- Akıllı ev sistemleri
- Akıllı saatler
- Sensörler
- Endüstriyel kontrol cihazları

Bu cihazlar bazen zayıf parolalar, güncel olmayan yazılımlar veya yanlış yapılandırmalar nedeniyle güvenlik riski oluşturabilir.

**Örnek:** Varsayılan parolası değiştirilmemiş bir güvenlik kamerasına yetkisiz erişim sağlanması.

## 3.8. Digital Forensics (Dijital Adli Bilişim)

Dijital cihazlarda bulunan verilerin ve izlerin incelenerek bir olayın nasıl gerçekleştiğinin anlaşılmasını amaçlar.

Dijital adli bilişim çalışmalarında delillerin güvenilirliği ve bütünlüğü önemlidir.

Başlıca çalışma alanları:
- Disk incelemesi
- Bellek (RAM) analizi
- Log incelemesi
- Ağ trafiği analizi
- Dosya sistemi incelemesi
- Dijital delillerin korunması

**Örnek:** Bir bilgisayara yapılan yetkisiz erişimin ardından sistem kayıtlarının incelenerek olay zaman çizelgesinin oluşturulması.

## 3.9. Threat Intelligence (Tehdit İstihbaratı)

Siber tehditler hakkında bilgi toplama, bu bilgileri analiz etme ve güvenlik kararlarında kullanma sürecidir.

Amaç, olası tehditleri daha iyi anlamak ve kurumların savunma kabiliyetini geliştirmektir.

İncelenebilecek bilgiler:
- Saldırgan gruplar
- Kullanılan saldırı yöntemleri
- Zararlı yazılım türleri
- Saldırılarda kullanılan IP adresleri ve alan adları
- Güvenlik açıkları
- Saldırı göstergeleri (IoC)

**Örnek:** Bir kurumun, belirli bir zararlı yazılım ailesinin kullandığı alan adları hakkında bilgi edinerek kendi ağındaki şüpheli bağlantıları araştırması.

---

# 4. Siber Güvenlikte Kariyer Alanları

Siber güvenlik alanında farklı görev ve uzmanlıklar bulunur. Bu görevler çoğunlukla saldırı simülasyonu, savunma, güvenlik koordinasyonu ve araştırma gibi alanlarda yoğunlaşır.

## 4.1. Red Team

Red Team, saldırgan bakış açısıyla hareket ederek bir kurumun güvenlik önlemlerini kontrollü ve yetkili testlerle değerlendirir.

Amaç, gerçek saldırganların yararlanabileceği güvenlik zayıflıklarını ortaya çıkarmaktır.

Görevleri:
- Bilgi toplama
- Güvenlik açıklarını araştırma
- Yetkili sızma testleri gerçekleştirme
- Saldırı senaryoları oluşturma
- Bulguları raporlama

## 4.2. Blue Team

Blue Team, kurumun sistemlerini ve ağlarını savunmaya odaklanır.

Amaç, tehditleri tespit etmek, saldırıları önlemek ve güvenlik olaylarına müdahale etmektir.

Görevleri:
- Sistem ve ağ trafiğini izlemek
- Güvenlik alarmlarını incelemek
- Şüpheli etkinlikleri araştırmak
- Güvenlik olaylarına müdahale etmek
- Güvenlik önlemlerini geliştirmek

Blue Team çalışmalarında SIEM, EDR, IDS/IPS ve firewall gibi teknolojiler kullanılabilir.

## 4.3. Purple Team

Purple Team, Red Team ve Blue Team çalışmalarının birbiriyle uyumlu hâle gelmesini sağlar.

Red Team'in gerçekleştirdiği kontrollü testlerden elde edilen sonuçlar, Blue Team'in tespit ve savunma yeteneklerini geliştirmek için kullanılır.

**Örnek:** Red Team belirli bir saldırı tekniğini test eder. Blue Team'in bu davranışı tespit edip edemediği değerlendirilir. Eksikler belirlenerek izleme kuralları ve savunma yöntemleri geliştirilir.

Purple Team yaklaşımı, saldırı ve savunma ekipleri arasındaki iş birliğini artırır.

## 4.4. Bug Bounty

Bug Bounty, kurumların güvenlik açıklarını bulmak amacıyla araştırmacılara sunduğu ödül programlarıdır.

Araştırmacılar, programın belirlediği kapsam ve kurallar içerisinde güvenlik testi yapar. Geçerli bulunan açıklar için ödül verilebilir.

Dikkat edilmesi gerekenler:
- Program kapsamı okunmalıdır.
- İzin verilmeyen sistemler test edilmemelidir.
- Kullanıcı verilerine zarar verilmemelidir.
- Bulgular programın bildirim kurallarına uygun şekilde raporlanmalıdır.

## 4.5. Ekiplerin Karşılaştırılması

| Ekip / Alan | Temel odak | Ana amaç |
|---|---|---|
| Red Team | Saldırı simülasyonu | Güvenlik zayıflıklarını ortaya çıkarmak |
| Blue Team | Savunma | Tehditleri tespit etmek ve engellemek |
| Purple Team | İş birliği | Saldırı ve savunma çalışmalarını geliştirmek |
| Bug Bounty | Güvenlik araştırması | Belirlenen kapsamda açık bulmak |

**Not:** Her kurumda bu ekipler ayrı departmanlar hâlinde bulunmayabilir. Küçük kurumlarda aynı kişi birden fazla güvenlik görevini üstlenebilir.

---

# 5. Sızma Testi (Penetration Testing)

## 5.1. Sızma Testi Nedir?

Sızma testi, bilgisayar sistemlerinin, ağların veya uygulamaların güvenliğini değerlendirmek amacıyla yetkili uzmanlar tarafından gerçekleştirilen kontrollü güvenlik testidir.

Sızma testinin amacı, bir saldırganın yararlanabileceği güvenlik açıklarını belirlemek ve bunların giderilmesine yardımcı olmaktır.

Sızma testi, yalnızca bir sisteme erişmeye çalışmaktan ibaret değildir. Testin kapsamı, kuralları, elde edilen bulgular ve iyileştirme önerileri de sürecin önemli parçalarıdır.

## 5.2. Sızma Testi Neden Yapılır?

- Güvenlik açıklarını tespit etmek
- Mevcut güvenlik önlemlerini değerlendirmek
- Yetkisiz erişim risklerini belirlemek
- Kurumun saldırılara karşı dayanıklılığını ölçmek
- Güvenlik yatırımlarına yön vermek
- Mevzuat veya kurum politikalarından doğan güvenlik ihtiyaçlarını desteklemek

## 5.3. Sızma Testinde Yetkilendirme ve Kapsam

Sızma testine başlamadan önce sistem sahibi veya yetkili kurum tarafından açık izin verilmelidir.

Test başlamadan önce şu konular belirlenmelidir:
- Hangi IP adresleri ve sistemler test edilecek?
- Hangi uygulamalar kapsam içerisinde?
- Hangi test yöntemlerine izin veriliyor?
- Test hangi tarihlerde yapılacak?
- Hizmet kesintisi riski nasıl yönetilecek?
- Acil durumda kiminle iletişim kurulacak?
- Bulgular nasıl raporlanacak?

**Önemli:** Yetkilendirme olmadan gerçekleştirilen güvenlik testleri hukuki ve etik sorunlara yol açabilir. Testin kapsamı dışında kalan sistemlere müdahale edilmemelidir.

## 5.4. Bilgi Seviyesine Göre Sızma Testleri

### Black Box Testing

Test uzmanına hedef sistem hakkında önceden çok az bilgi verilir veya hiç bilgi verilmez.

Bu yaklaşımda test uzmanı, dışarıdan bir saldırganın sahip olabileceği sınırlı bilgilerle çalışır.

**Örnek:** Bir web uygulamasının kaynak kodu ve iç mimarisi paylaşılmadan güvenlik testine başlanması.

### Grey Box Testing

Test uzmanına hedef sistem hakkında sınırlı bilgi verilir.

Örneğin:
- Standart kullanıcı hesabı
- Bazı ağ bilgileri
- Uygulamanın belirli teknik ayrıntıları

Bu yaklaşım, sınırlı iç bilgiye sahip bir kullanıcının oluşturabileceği riskleri değerlendirmeye yardımcı olabilir.

### White Box Testing

Test uzmanına hedef sistem hakkında ayrıntılı bilgi sağlanır.

Bu bilgiler şunları içerebilir:
- Kaynak kod
- Sistem mimarisi
- Ağ şeması
- Yapılandırma bilgileri
- Test hesapları

Bu yaklaşım, sistemin daha ayrıntılı incelenmesini sağlar.

## 5.5. Sızma Testinin Genel Aşamaları

Sızma testi metodolojisine göre aşamaların isimleri ve sıralaması değişebilir. Genel olarak aşağıdaki çalışmalar yürütülür:

1. **Planlama ve kapsam belirleme:** Yetki, hedefler ve test kuralları belirlenir.
2. **Bilgi toplama:** Hedef sistem hakkında izin verilen bilgiler elde edilir.
3. **Keşif ve analiz:** Açık portlar, servisler ve olası zayıflıklar araştırılır.
4. **Güvenlik açığının doğrulanması:** Bulgunun gerçekten güvenlik riski oluşturup oluşturmadığı kontrollü şekilde incelenir.
5. **Etki değerlendirmesi:** Açığın olası sonuçları belirlenir.
6. **Raporlama:** Bulgular, kanıtlar, riskler ve çözüm önerileri sunulur.
7. **Yeniden test:** Giderilen güvenlik açıklarının kapatılıp kapatılmadığı kontrol edilir.

## 5.6. Sızma Testi ve Güvenlik Metodolojileri

Güvenlik testlerinde farklı standartlar, rehberler ve metodolojiler kullanılabilir.

### OWASP

OWASP (Open Worldwide Application Security Project), uygulama güvenliği konusunda açık kaynaklı rehberler, projeler ve eğitim kaynakları sunan bir topluluktur.

Öne çıkan kaynakları:
- OWASP Top 10
- OWASP Web Security Testing Guide
- OWASP Application Security Verification Standard (ASVS)

Özellikle web uygulamalarının güvenliğini değerlendirmek ve güvenli yazılım geliştirme süreçlerini iyileştirmek için kullanılır.

### OSSTMM

OSSTMM (Open Source Security Testing Methodology Manual), güvenlik testlerinin yapılandırılmış bir metodoloji çerçevesinde yürütülmesine yardımcı olan bir kaynaktır.

Güvenliğin farklı kanallar üzerinden değerlendirilmesine odaklanır.

### NIST SP 800-115

NIST SP 800-115, teknik bilgi güvenliği testleri ve değerlendirmeleri için rehber niteliğindedir.

Testlerin planlanması, gerçekleştirilmesi, analiz edilmesi ve sonuçların raporlanması konularında yol gösterir.

**Önemli ayrım:** OWASP, OSSTMM ve NIST SP 800-115 aynı türde dokümanlar değildir. Farklı kapsam ve amaçlarla hazırlanmış kaynaklardır.

---

# 6. Temel Teknik Bilgiler ve Kavramlar

Siber güvenlik alanında ilerlemek için ağ, işletim sistemi ve yazılım güvenliğiyle ilgili bazı temel kavramların bilinmesi gerekir.

## 6.1. Fiziksel Port ve Mantıksal Port

Port kelimesi ağ ve bilgisayar donanımı konularında farklı anlamlarda kullanılabilir.

### Fiziksel Port

Bilgisayar veya ağ cihazları üzerinde bulunan fiziksel bağlantı noktalarıdır.

Örnekler:
- USB: Klavye, fare ve harici depolama cihazları bağlamak için kullanılır.
- Ethernet (RJ45): Kablolu ağ bağlantısı sağlar.
- HDMI: Görüntü ve ses aktarımında kullanılır.
- DisplayPort: Görüntü ve ses aktarımını sağlar.

### Mantıksal Port

Ağ iletişiminde bir cihaz üzerindeki hizmetlerin ve uygulamaların tanımlanmasına yardımcı olan sayısal bağlantı noktalarıdır.

Port numaraları 0 ile 65535 arasında değişir.

Örneğin bir sunucuda web hizmeti 443 numaralı port üzerinden çalışabilir.

**Önemli:** Fiziksel port, cihaz üzerindeki gerçek bağlantı noktasıdır. Mantıksal port ise ağ iletişiminde kullanılan sayısal bir tanımlayıcıdır.

## 6.2. TCP ve UDP

TCP ve UDP, internet protokol ailesinde taşıma katmanında kullanılan iki temel protokoldür.

### TCP (Transmission Control Protocol)

TCP, bağlantı odaklı iletişim sağlar.

Temel özellikleri:
- Veri aktarımından önce bağlantı kurar.
- Verilerin sıralı iletilmesini sağlar.
- Kayıp verilerin yeniden gönderilmesini destekler.
- Güvenilir veri aktarımı gereken uygulamalarda kullanılır.

**Örnek:** Web sayfalarının HTTPS üzerinden yüklenmesi ve dosya aktarımı gibi işlemler.

TCP bağlantısının kurulmasında üç aşamalı el sıkışma (Three-Way Handshake) kullanılır:

1. SYN
2. SYN-ACK
3. ACK

### UDP (User Datagram Protocol)

UDP, bağlantı kurma aşaması olmadan veri iletimine imkân verir.

Temel özellikleri:
- Daha düşük iletişim ek yükü sunar.
- Verilerin ulaşmasını veya sıralı olmasını garanti etmez.
- Gerçek zamanlı iletişim gerektiren uygulamalarda tercih edilebilir.

**Örnek:** DNS sorguları, çevrim içi oyunlar ve bazı ses/video iletişim uygulamaları.

### TCP ve UDP Karşılaştırması

| Özellik | TCP | UDP |
|---|---|---|
| Bağlantı | Bağlantı odaklı | Bağlantısız |
| Veri sırası | Sıralamayı sağlar | Garanti etmez |
| Yeniden iletim | Destekler | Yerleşik olarak sağlamaz |
| İletişim ek yükü | Daha fazla | Daha az |
| Kullanım | Güvenilir aktarım gereken işler | Gecikmenin önemli olduğu işler |

## 6.3. Yaygın Port Numaraları

Ağ servisleri belirli port numaralarını varsayılan olarak kullanabilir.

| Port | Protokol / Hizmet | Açıklama |
|---|---|---|
| 20 | FTP Data | FTP veri aktarımı |
| 21 | FTP Control | FTP kontrol bağlantısı |
| 22 | SSH | Güvenli uzaktan erişim |
| 23 | Telnet | Şifrelenmemiş uzaktan terminal erişimi |
| 25 | SMTP | E-posta aktarımı |
| 53 | DNS | Alan adı çözümleme |
| 67/68 | DHCP | IP adresi dağıtımı |
| 80 | HTTP | Şifrelenmemiş web iletişimi |
| 110 | POP3 | E-posta alma |
| 143 | IMAP | E-posta erişimi |
| 443 | HTTPS | Şifreli web iletişimi |
| 3306 | MySQL | Veritabanı hizmeti |
| 3389 | RDP | Uzak masaüstü bağlantısı |
| 5432 | PostgreSQL | Veritabanı hizmeti |

**Dikkat edilmesi gerekenler:**
- Port numaraları bir hizmetin varsayılan kullanımını gösterir.
- Bir hizmet farklı bir portta da çalışabilir.
- Bir portun açık olması tek başına sistemin savunmasız olduğu anlamına gelmez.
- Açık portlar ve servisler, güvenlik değerlendirmesinde diğer bilgilerle birlikte incelenmelidir.

## 6.4. Vulnerability (Güvenlik Açığı)

Bir sistemde, yazılımda veya yapılandırmada bulunan ve güvenliği olumsuz etkileyebilecek zayıflıktır.

Örnekler:
- Güncellenmemiş yazılımlar
- Zayıf parolalar
- Yanlış yapılandırılmış sunucular
- Eksik yetkilendirme kontrolleri
- Güvenli olmayan yazılım kodları

Bir güvenlik açığının bulunması, mutlaka saldırıya uğranıldığı anlamına gelmez. Açığın oluşturduğu risk ayrıca değerlendirilmelidir.

## 6.5. OWASP Top 10

OWASP Top 10, web uygulamalarında karşılaşılan önemli güvenlik risklerini anlamaya yardımcı olan bir farkındalık ve bilgilendirme kaynağıdır.

Geliştiriciler ve güvenlik uzmanları, web uygulamalarının hangi risklere karşı değerlendirilmesi gerektiğini anlamak için bu kaynaktan yararlanabilir.

Örneğin:
- Erişim kontrolü sorunları
- Güvenlik yapılandırma hataları
- Kriptografik koruma eksiklikleri
- Enjeksiyon açıkları
- Kimlik doğrulama sorunları

**Not:** OWASP Top 10 bir yazılım güvenlik aracı veya tek başına eksiksiz bir test metodolojisi değildir. Web uygulaması risklerini anlamaya yönelik bir kaynaktır.

## 6.6. CVE (Common Vulnerabilities and Exposures)

CVE, bilinen güvenlik açıklarının ortak bir kimlik sistemiyle tanımlanmasını sağlayan yapıdır.

Her CVE kaydı, belirli bir güvenlik açığına ait referans numarası içerir.

Örnek biçim:

`CVE-2021-44228`

Bu kimlik, Log4Shell olarak bilinen kritik Log4j güvenlik açığına aittir.

CVE numarası, güvenlik uzmanlarının aynı açık hakkında ortak bir referans üzerinden iletişim kurmasını kolaylaştırır.

## 6.7. CVSS (Common Vulnerability Scoring System)

CVSS, güvenlik açıklarının teknik ciddiyetini değerlendirmek için kullanılan puanlama sistemidir.

CVSS puanı, güvenlik ekiplerinin hangi açıkların öncelikli olarak ele alınması gerektiğini değerlendirmesine yardımcı olur.

CVSS v3.1'de puanlar 0.0 ile 10.0 arasında değerlendirilir.

| Puan aralığı | Ciddiyet |
|---|---|
| 0.0 | Yok |
| 0.1–3.9 | Düşük |
| 4.0–6.9 | Orta |
| 7.0–8.9 | Yüksek |
| 9.0–10.0 | Kritik |

**Önemli:** CVSS puanı tek başına kurumun gerçek riskini belirlemez. Açığın kurum açısından önemi, sistemin işlevi, maruz kalma durumu ve mevcut güvenlik önlemleri de değerlendirilmelidir.

## 6.8. Exploit

Exploit, bir güvenlik açığından yararlanmak için kullanılan yöntem veya koddur.

Bir exploit, belirli bir zafiyeti tetikleyerek sistemde istenmeyen bir davranışın ortaya çıkmasına neden olabilir.

**Örnek:** Bir yazılımdaki güvenlik açığından yararlanarak yetkisiz erişim elde etmeye çalışan kod.

Exploit kavramı güvenlik araştırmalarında da kullanılır. Uzmanlar, açıkların etkisini kontrollü ve izinli ortamlarda doğrulamak için exploit örneklerinden yararlanabilir.

## 6.9. PoC (Proof of Concept)

PoC, bir güvenlik açığının veya teknik iddianın uygulanabilir olduğunu göstermeye yönelik kanıt ya da örnektir.

PoC her zaman tam kapsamlı bir saldırı aracı değildir.

**Örnek:** Bir web uygulamasında yetkilendirme eksikliği bulunduğunu gösteren, zararsız ve kontrollü bir test senaryosu.

Exploit ile PoC aynı anlama gelmez. PoC bir durumun varlığını kanıtlamaya odaklanırken exploit, bir güvenlik açığından yararlanmak için kullanılan yöntem veya kod olabilir.

## 6.10. Zero-Day (Sıfırıncı Gün Açığı)

Zero-Day, üreticinin veya yazılım geliştiricisinin düzeltme yayımlayamadığı ya da savunma ekiplerinin henüz etkili bir çözüm uygulayamadığı güvenlik açıkları için kullanılan terimdir.

Bu açıklar, saldırganlar tarafından düzeltme veya koruma önlemleri hazır olmadan önce kullanılabilir.

Zero-Day açıkları özellikle tehlikeli olabilir çünkü kurumların bu açıkları kapatmak için henüz hazır bir güvenlik güncellemesi bulunmayabilir.

**Önemli ayrım:** Zero-Day terimi, her zaman açığın dünyadaki hiç kimse tarafından bilinmediği anlamına gelmez. Açığın üretici tarafından bilinmesi, saldırganlar tarafından keşfedilmesi ve bir düzeltmenin yayımlanması farklı durumlardır.

## 6.11. Shell Nedir?

Shell, kullanıcının işletim sistemiyle komutlar aracılığıyla iletişim kurmasını sağlayan arayüzdür.

Örneğin Windows'ta PowerShell ve Komut İstemi, Linux sistemlerde ise Bash yaygın olarak kullanılan komut satırı arayüzleridir.

Shell aracılığıyla:
- Dosyalar yönetilebilir.
- Sistem bilgileri görüntülenebilir.
- Programlar çalıştırılabilir.
- Ağ yapılandırmaları incelenebilir.
- Yönetim işlemleri gerçekleştirilebilir.

Siber güvenlik alanında shell kavramı, yetkili sistem yönetimi ve güvenlik analizinin yanı sıra saldırıların incelenmesinde de karşımıza çıkar.

## 6.12. Bind Shell

Bind Shell yaklaşımında hedef sistem belirli bir port üzerinden bağlantı bekler.

Başka bir ifadeyle hedef sistem bağlantı kabul eden taraf olur.

Bu yaklaşım, ağ güvenliği değerlendirmelerinde ve zararlı yazılım analizlerinde incelenebilen bir bağlantı türüdür.

## 6.13. Reverse Shell

Reverse Shell yaklaşımında hedef sistem, dışarıdaki belirli bir sisteme bağlantı başlatır.

Bu nedenle bağlantıyı başlatan taraf hedef sistemdir.

Güvenlik uzmanları, bu tür bağlantıları zararlı faaliyetlerin analizinde ve kontrollü laboratuvar çalışmalarında inceleyebilir.

### Bind Shell ve Reverse Shell Karşılaştırması

| Özellik | Bind Shell | Reverse Shell |
|---|---|---|
| Bağlantıyı bekleyen | Hedef sistem | Dış sistem |
| Bağlantıyı başlatan | Dış sistem | Hedef sistem |
| Temel yaklaşım | Hedefte port dinlenir | Hedeften dışarı bağlantı başlatılır |

## 6.14. Web Shell

Web Shell, web sunucusu üzerinde çalışabilen ve belirli koşullarda komut yürütülmesine imkân sağlayabilen betik veya dosyadır.

Saldırganlar, ele geçirdikleri web sunucularında kalıcılık sağlamak ve uzaktan komut çalıştırmak için Web Shell kullanabilir.

Güvenlik ekipleri açısından önemli inceleme konuları:
- Web dizinlerinde beklenmeyen dosyalar
- Şüpheli dosya değişiklikleri
- Olağan dışı web istekleri
- Sunucu süreçleri
- Dosya bütünlüğü kayıtları

Web Shell tespiti için log analizi, dosya bütünlüğü izleme ve sunucu güvenlik kontrolleri kullanılabilir.

## 6.15. IP Adresi ve IP Sürümleri

IP (Internet Protocol), ağ üzerindeki cihazların adreslenmesini ve birbirleriyle iletişim kurmasını sağlayan protokoldür.

Bir IP adresi, ağ iletişiminde cihazların veya ağ arayüzlerinin tanımlanmasına yardımcı olur.

### IPv4

IPv4, 32 bit uzunluğunda adresleme yapısını kullanır.

Dört bölümden oluşan ve noktalarla ayrılan sayısal gösterime sahiptir.

Örnek:

`192.168.1.10`

IPv4 adresleri teorik olarak yaklaşık 4,3 milyar farklı adres oluşturabilir.

Adres alanının sınırlı olması, IPv6'nın geliştirilmesinin önemli nedenlerinden biridir.

### IPv6

IPv6, 128 bit uzunluğunda adresleme yapısını kullanır.

Örnek:

`2001:db8:85a3::8a2e:370:7334`

IPv6, IPv4'e kıyasla çok daha geniş bir adres alanı sunar.

### IPv4 ve IPv6 Karşılaştırması

| Özellik | IPv4 | IPv6 |
|---|---|---|
| Adres uzunluğu | 32 bit | 128 bit |
| Gösterim | Noktalı ondalık | İki nokta üst üste ayrılmış onaltılık |
| Adres alanı | Daha sınırlı | Çok daha geniş |
| Örnek | 192.168.1.10 | 2001:db8::1 |

**Önemli:** IPv6, IPv4'ün doğrudan yerine her ortamda tek başına geçmiş değildir. Günümüzde iki protokol de kullanılmaktadır.

---

# 7. Yararlı Kaynaklar

Siber güvenlikte öğrenme sürecinin devam etmesi için güvenilir dokümantasyonlardan ve eğitim kaynaklarından yararlanmak önemlidir.

## 7.1. Hackviser

Siber güvenlik, sızma testi, araçlar ve sistem güvenliği konularında içerikler sunar.

- [Pentesting Tactics](https://hackviser.com/tactics/pentesting)
- [Hardening Tactics](https://hackviser.com/tactics/hardening)
- [Tools Tactics](https://hackviser.com/tactics/tools)

## 7.2. OWASP

Web uygulama güvenliği ve güvenli yazılım geliştirme konularında rehberler sunar.

- [OWASP Resmî Web Sitesi](https://owasp.org/)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)

## 7.3. NIST

Bilgi güvenliği, siber güvenlik standartları ve teknik rehberler yayımlar.

- [NIST Computer Security Resource Center](https://csrc.nist.gov/)
- [NIST SP 800-115](https://csrc.nist.gov/pubs/sp/800/115/final)

## 7.4. MITRE

Siber saldırı teknikleri ve tehdit davranışları hakkında kapsamlı bilgi sunar.

- [MITRE ATT&CK](https://attack.mitre.org/)

## 7.5. CVE ve CVSS Kaynakları

Güvenlik açıklarının kimliklerini, açıklamalarını ve teknik ciddiyetlerini incelemek için kullanılabilir.

- [CVE Programı](https://www.cve.org/)
- [National Vulnerability Database (NVD)](https://nvd.nist.gov/)
- [FIRST CVSS](https://www.first.org/cvss/)

---

# Genel Değerlendirme

Bu derste siber güvenliğin temel kavramları ve çalışma alanları incelenmiştir.

Öğrenilen başlıca konular:

- Siber güvenliğin amacı ve bilgi güvenliği kavramı
- CIA Triad: Gizlilik, Bütünlük ve Erişilebilirlik
- White Hat, Black Hat ve Gray Hat hacker türleri
- Siber güvenliğin farklı uzmanlık alanları
- Red Team, Blue Team, Purple Team ve Bug Bounty
- Sızma testi ve bilgi seviyesine göre test türleri
- OWASP, OSSTMM ve NIST kaynakları
- Fiziksel portlar ve mantıksal portlar
- TCP ve UDP protokolleri
- Yaygın port numaraları
- Vulnerability, CVE, CVSS, Exploit ve PoC
- Zero-Day, Shell, Bind Shell, Reverse Shell ve Web Shell
- IPv4 ve IPv6 adresleme yapıları

## Sonuç

Siber güvenlik, yalnızca saldırı araçlarını kullanmayı öğrenmekten ibaret değildir. Sistemlerin nasıl çalıştığını anlamak, riskleri değerlendirmek, güvenlik açıklarını tespit etmek ve uygun savunma yöntemlerini geliştirmek bu alanın temelini oluşturur.

Bu temel kavramlar, ağ güvenliği, sızma testi, olay müdahale, tehdit istihbaratı ve diğer uzmanlık alanlarında ilerlemek için başlangıç noktasıdır.
