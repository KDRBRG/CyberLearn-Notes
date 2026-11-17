# Ders 02 – Cyber Kill Chain

## İçindekiler

1. Cyber Kill Chain Nedir?
2. Keşif (Reconnaissance)
3. Silahlanma (Weaponization)
4. İletim (Delivery)
5. Sömürü (Exploitation)
6. Kurulum (Installation)
7. Komuta ve Kontrol (Command and Control)
8. Hedef Üzerindeki Eylemler (Actions on Objectives)
9. Savunma ve Tespit Mekanizmaları
10. Cyber Kill Chain ve MITRE ATT&CK Karşılaştırması
11. Yararlı Kaynaklar

---

# 1. Cyber Kill Chain Nedir?

## 1.1. Tanım

Cyber Kill Chain, siber saldırıların hangi aşamalardan geçerek gerçekleştirilebileceğini açıklayan bir güvenlik modelidir.

Model, saldırganın hedefe ulaşmak için gerçekleştirdiği faaliyetleri aşamalara ayırır. Güvenlik ekipleri bu aşamaları inceleyerek saldırının nerede tespit edilebileceğini ve nasıl engellenebileceğini belirleyebilir.

Cyber Kill Chain modeli, Lockheed Martin tarafından 2011 yılında yayımlanmıştır. Askerî hedefleme süreçlerinde kullanılan kill chain yaklaşımından esinlenerek siber saldırılara uyarlanmıştır.

Temel düşünce şudur:

**Bir saldırıyı durdurmak için saldırının son aşamasını beklemek gerekmez. Zincirin herhangi bir aşamasında müdahale edilmesi saldırının hedefe ulaşmasını engelleyebilir.**

## 1.2. Cyber Kill Chain'in Yedi Aşaması

Model yedi temel aşamadan oluşur:

1. Reconnaissance – Keşif
2. Weaponization – Silahlanma
3. Delivery – İletim
4. Exploitation – Sömürü
5. Installation – Kurulum
6. Command and Control – Komuta ve Kontrol
7. Actions on Objectives – Hedef Üzerindeki Eylemler

### Saldırı zincirinin genel görünümü

| Aşama | Saldırganın amacı | Savunmacının odak noktası |
|---|---|---|
| Reconnaissance | Hedef hakkında bilgi toplamak | Bilgi sızıntısını azaltmak |
| Weaponization | Saldırı aracını hazırlamak | Zararlı içerikleri analiz etmek |
| Delivery | Zararlı içeriği hedefe ulaştırmak | E-posta ve ağ trafiğini denetlemek |
| Exploitation | Güvenlik açığından yararlanmak | Açıkları kapatmak ve saldırıyı tespit etmek |
| Installation | Sistemde kalıcılık sağlamak | Şüpheli değişiklikleri izlemek |
| Command and Control | Ele geçirilen sistemle iletişim kurmak | Şüpheli ağ bağlantılarını tespit etmek |
| Actions on Objectives | Hedeflenen işlemi gerçekleştirmek | Veri kaybını ve zararı önlemek |

## 1.3. Cyber Kill Chain Neden Önemlidir?

Bu model, saldırıların yalnızca son aşamasına odaklanmak yerine tüm süreç boyunca değerlendirilmesine yardımcı olur.

Başlıca faydaları:

- Saldırıların aşamalara ayrılarak analiz edilmesini sağlar.
- Güvenlik ekiplerinin olası saldırı noktalarını anlamasına yardımcı olur.
- Tespit ve müdahale süreçlerinin geliştirilmesini destekler.
- Güvenlik kontrollerinin hangi aşamalarda uygulanabileceğini gösterir.
- Olay müdahale ve tehdit analizi çalışmalarına katkı sağlar.

## 1.4. Cyber Kill Chain'in Sınırlamaları

Cyber Kill Chain faydalı bir model olmakla birlikte her saldırıyı eksiksiz açıklayamaz.

Bazı sınırlamaları şunlardır:

- Saldırıları doğrusal bir süreç gibi gösterir; gerçek saldırılar her zaman bu sırayı izlemez.
- İç ağdan başlayan saldırıları açıklamakta sınırlı kalabilir.
- Bulut, kimlik ve hesap ele geçirme odaklı saldırıların tüm ayrıntılarını tek başına açıklayamaz.
- Modern saldırılarda bazı aşamalar atlanabilir veya birbiriyle iç içe geçebilir.

Bu nedenle Cyber Kill Chain, MITRE ATT&CK gibi diğer güvenlik modelleriyle birlikte değerlendirilebilir.

---

# 2. Keşif (Reconnaissance)

## 2.1. Keşif Nedir?

Keşif, saldırganın hedef sistem hakkında bilgi topladığı ilk aşamadır.

Saldırgan bu aşamada hedefin teknolojik altyapısını, çalışanlarını, alan adlarını, IP adreslerini, kullanılan servisleri ve olası güvenlik zayıflıklarını anlamaya çalışır.

Toplanan bilgiler sonraki saldırı aşamalarının planlanmasında kullanılabilir.

## 2.2. Keşif Türleri

Keşif faaliyetleri genel olarak pasif ve aktif olmak üzere iki grupta incelenir.

### Pasif Keşif (Passive Reconnaissance)

Hedef sistemle doğrudan etkileşime girmeden, açık kaynaklardan veya üçüncü taraf kaynaklardan bilgi toplama yöntemidir.

Bilgi kaynaklarına örnekler:

- Arama motorları
- Sosyal medya hesapları
- Şirket web siteleri
- Alan adı kayıtları
- Kamuya açık belgeler
- Açık kaynak istihbaratı (OSINT)

**Örnek:** Bir şirketin web sitesindeki çalışan profillerini inceleyerek kullanılan teknoloji ve görev dağılımı hakkında bilgi edinmek.

Pasif keşif, hedef sistem üzerinde doğrudan tarama yapılmasını gerektirmeyebilir. Ancak bilgi toplanan kaynakların ve kullanılan hizmetlerin kendi kayıtları bulunabilir.

### Aktif Keşif (Active Reconnaissance)

Hedef sistemle doğrudan iletişim kurularak bilgi toplanmasıdır.

Örneğin:

- Port taraması
- Servis sürümü tespiti
- Ağ keşfi
- Web dizini incelemesi
- Servislerin davranışlarının analiz edilmesi

Aktif keşif, hedef sistemin loglarına veya güvenlik izleme sistemlerine yansıyabilir.

## 2.3. OSINT Nedir?

OSINT (Open Source Intelligence), herkese açık kaynaklardan bilgi toplama ve bu bilgileri analiz ederek anlamlı istihbarat üretme sürecidir.

OSINT yalnızca siber güvenlikte kullanılmaz. Gazetecilik, araştırma, akademik çalışmalar ve kurumsal risk analizlerinde de kullanılır.

OSINT kaynaklarına örnekler:

- Arama motorları
- Sosyal medya
- Kamuya açık veri tabanları
- Alan adı kayıtları
- Şirket ve kurum web siteleri
- Teknik dokümantasyonlar

**Örnek:** Bir kurumun yayımladığı teknik dokümanlarda kullanılan yazılım ve altyapı bilgilerini incelemek.

## 2.4. Google Dorking

Google Dorking, arama motorlarının gelişmiş arama operatörlerini kullanarak belirli türdeki herkese açık içerikleri bulma yöntemidir.

Örnek operatörler:

| Operatör | Açıklama |
|---|---|
| `site:` | Belirli bir alan adındaki sonuçları arar |
| `filetype:` | Belirli dosya türlerini arar |
| `intitle:` | Sayfa başlığında belirli kelimeleri arar |
| `inurl:` | URL içerisinde belirli ifadeleri arar |

Örnek arama:

```text
site:example.com filetype:pdf
```

Bu arama, belirtilen alan adıyla ilişkili PDF dosyalarını bulmaya yardımcı olur.

**Güvenlik açısından önemi:** Kurumlar istemeden hassas belgeleri veya teknik bilgileri herkese açık hâle getirebilir.

**Savunma önerileri:**
- Web sunucularındaki dosya izinlerini kontrol etmek.
- Hassas belgeleri herkese açık dizinlerde tutmamak.
- Eski dosyaları ve yedekleri düzenli olarak incelemek.
- Arama motorlarında indekslenen içerikleri denetlemek.

## 2.5. Keşif Araçları

### TheHarvester

Açık kaynaklardan alan adı, e-posta adresi, alt alan adı ve benzeri bilgileri toplamaya yardımcı olan bir araçtır.

Kullanım alanları:
- OSINT çalışmaları
- Alan adı araştırması
- Kurumsal saldırı yüzeyinin anlaşılması

### Shodan

İnternete açık cihazları ve servisleri aramaya yarayan bir arama motorudur.

Shodan üzerinden şu tür bilgiler araştırılabilir:
- İnternete açık sunucular
- Ağ cihazları
- Açık servisler
- Servis ve yazılım bilgileri
- Bazı cihazlara ait banner bilgileri

**Önemli:** Shodan'ın gösterdiği bilgiler, Shodan'ın tarama altyapısının topladığı verilere dayanır. Veriler güncel olmayabilir. Shodan kullanmak hedef sistem üzerinde doğrudan tarama yapmakla aynı şey değildir.

### Nmap

Nmap, ağ keşfi ve güvenlik denetimlerinde kullanılan bir araçtır.

Başlıca kullanım alanları:
- Ağdaki cihazları keşfetmek
- Açık portları belirlemek
- Servisleri tanımlamak
- Servis sürümlerini incelemek
- Ağın yapısı hakkında bilgi edinmek

Yetkili bir laboratuvar ortamında örnek kullanım:

```bash
nmap -sV 192.168.1.10
```

Bu komut, hedefte tespit edilebilen servislerin sürüm bilgilerini incelemeye çalışır.

Bir diğer örnek:

```bash
nmap -sS 192.168.1.10
```

Bu komut TCP SYN taraması gerçekleştirir.

**Teknik not:** SYN taraması tam TCP bağlantısını tamamlamadan sonuç elde etmeye çalışır. Ancak bu, taramanın tespit edilemeyeceği anlamına gelmez. Güvenlik duvarları ve IDS/IPS sistemleri bu tür faaliyetleri kaydedebilir.

### Gobuster ve Dirb

Web uygulamalarında belirli dizin ve dosya yollarının keşfedilmesine yardımcı olan araçlardır.

Örneğin bir web uygulamasında herkese açık olup olmadığı kontrol edilmesi gereken eski yönetim dizinleri bulunabilir.

Bu araçlar yalnızca yetkili test ortamlarında kullanılmalıdır.

## 2.6. Keşif Aşamasına Karşı Savunma

- Gereksiz bilgileri herkese açık paylaşmamak.
- Kullanılmayan servisleri kapatmak.
- Ağ cihazlarını düzenli olarak denetlemek.
- Güvenlik duvarı kurallarını gözden geçirmek.
- Web sunucusu hata mesajlarında gereksiz teknik ayrıntı göstermemek.
- Yetkisiz tarama faaliyetlerini loglar üzerinden takip etmek.
- Kurumun dışarıdan görülebilen varlıklarını düzenli olarak incelemek.

---

# 3. Silahlanma (Weaponization)

## 3.1. Weaponization Nedir?

Silahlanma, saldırganın topladığı bilgiler doğrultusunda saldırıda kullanacağı araçları veya zararlı içeriği hazırladığı aşamadır.

Bu aşamada saldırgan, hedefin özelliklerine uygun bir saldırı yöntemi belirlemeye çalışır.

Cyber Kill Chain modelinde bu aşama genellikle hedef sistemle doğrudan etkileşim gerçekleşmeden önce, saldırganın kendi ortamında yürütülür.

## 3.2. Exploit ve Payload İlişkisi

Silahlanma aşamasında iki kavram önemlidir:

**Exploit:** Bir güvenlik açığından yararlanmak için kullanılan yöntem veya kod.

**Payload:** Güvenlik açığı kullanıldığında gerçekleştirilmesi amaçlanan işlem veya kod.

Kavramsal olarak:

```text
Exploit + Payload = Saldırı için hazırlanan içerik
```

Örnek olarak bir saldırganın eski bir yazılım sürümündeki güvenlik açığını hedeflediğini düşünelim.

- Exploit, ilgili güvenlik açığını tetiklemeyi amaçlar.
- Payload ise açığın kullanılmasının ardından gerçekleştirilmek istenen işlemi temsil eder.

Bu kavramlar birbirinden farklıdır; her exploit zararlı bir payload içermek zorunda değildir.

## 3.3. Zararlı İçerik Türleri

Saldırılarda farklı dosya ve içerik türleri kötüye kullanılabilir.

Örnekler:
- Zararlı Office belgeleri
- PDF dosyaları
- Betik dosyaları
- HTA dosyaları
- Çalıştırılabilir dosyalar
- Zararlı bağlantılar

Bir dosyanın uzantısı tek başına güvenli veya zararlı olduğunu göstermez.

## 3.4. Reverse Shell ve Bind Shell

Silahlanma aşamasında karşılaşılabilecek kavramlardan ikisi Bind Shell ve Reverse Shell'dir.

**Bind Shell:** Hedef sistem belirli bir port üzerinden bağlantı bekler.

**Reverse Shell:** Hedef sistem dışarıdaki başka bir sisteme bağlantı başlatır.

Bu iki yaklaşımın farkı bağlantıyı hangi tarafın başlattığıdır.

Güvenlik ekipleri, bu tür bağlantı davranışlarını ağ trafiği ve uç nokta kayıtları üzerinden inceleyebilir.

## 3.5. Obfuscation (Kod Gizleme)

Obfuscation, kodun veya içeriğin insanlar ya da analiz araçları tarafından anlaşılmasını zorlaştıracak şekilde değiştirilmesidir.

Zararlı yazılım analizinde saldırganlar, kodun yapısını gizlemek veya imza tabanlı tespitleri zorlaştırmak amacıyla bu yöntemi kullanabilir.

Ancak obfuscation, kodu otomatik olarak güvenli veya tespit edilemez hâle getirmez.

## 3.6. Encoding, Encryption ve Packing

Bu kavramlar birbirine karıştırılmamalıdır.

| Kavram | Açıklama |
|---|---|
| Encoding | Veriyi belirli bir gösterim biçimine dönüştürme |
| Encryption | Veriyi anahtar kullanarak okunamaz hâle getirme |
| Packing | Programın yapısını veya depolanma biçimini değiştirerek analizini zorlaştırma |
| Obfuscation | Kodun anlaşılmasını zorlaştırma |

Örneğin Base64 bir encoding yöntemidir; şifreleme değildir.

Bir içeriğin Base64 ile kodlanması, içeriğin gizli veya güvenli olduğu anlamına gelmez.

## 3.7. Metasploit ve Msfvenom

Metasploit, güvenlik testleri ve zafiyet doğrulama çalışmalarında kullanılan bir çerçevedir.

Msfvenom ise Metasploit Framework içerisinde payload üretimi ve çıktı biçimlendirme amacıyla kullanılan araçtır.

Bu araçlar güvenlik uzmanları tarafından kontrollü laboratuvar ortamlarında kullanılabilir.

**Savunma açısından dikkat edilmesi gerekenler:**
- Bilinmeyen çalıştırılabilir dosyalar analiz edilmelidir.
- Uç nokta güvenlik sistemleri etkin olmalıdır.
- Şüpheli süreçler ve dosya davranışları izlenmelidir.
- Dosyaların kaynağı ve bütünlüğü doğrulanmalıdır.

**Önemli:** Bir dosyanın kodlanmış veya paketlenmiş olması tek başına zararlı olduğunu göstermez. Aynı şekilde bu yöntemler zararlı içeriğin güvenlik ürünlerini kesin olarak atlatmasını sağlamaz.

---

# 4. İletim (Delivery)

## 4.1. Delivery Nedir?

İletim aşaması, saldırganın hazırladığı zararlı içeriği veya saldırı aracını hedefe ulaştırmaya çalıştığı aşamadır.

Bu aşamada saldırgan, hedef kullanıcının veya sistemin içerikle etkileşime geçmesini amaçlayabilir.

## 4.2. Phishing (Oltalama)

Phishing, kullanıcıları kandırarak hassas bilgilerini ele geçirmeyi veya zararlı içeriklerle etkileşime girmelerini sağlamayı amaçlayan sosyal mühendislik yöntemidir.

Saldırganlar kendilerini güvenilir bir kurum veya kişi gibi gösterebilir.

Örnekler:
- Sahte banka e-postaları
- Sahte parola sıfırlama bağlantıları
- Kargo bildirimi gibi görünen mesajlar
- Sahte kurumsal giriş sayfaları

### Phishing Türleri

**Spear Phishing:** Belirli bir kişiyi veya kurumu hedefleyen kişiselleştirilmiş oltalama saldırısıdır.

**Whaling:** Üst düzey yöneticiler gibi önemli hedeflere yönelik oltalama saldırısıdır.

**Smishing:** SMS mesajları üzerinden gerçekleştirilen oltalama saldırısıdır.

**Vishing:** Telefon görüşmeleri üzerinden gerçekleştirilen oltalama saldırısıdır.

## 4.3. E-posta Güvenliği

E-posta saldırıları, zararlı bağlantıların veya eklerin kullanıcılara ulaştırılmasında sık kullanılan yöntemlerdendir.

E-posta güvenliğinde bazı doğrulama mekanizmaları bulunur.

### SPF (Sender Policy Framework)

Bir alan adının hangi posta sunucularından e-posta göndermeye yetkili olduğunu belirlemeye yardımcı olur.

### DKIM (DomainKeys Identified Mail)

E-postaya dijital imza eklenmesini sağlar. Alıcı taraf, imzayı doğrulayarak mesajın imza kapsamındaki bölümlerinin bütünlüğünü ve imza sahibi alan adının kontrolünü değerlendirebilir.

### DMARC (Domain-based Message Authentication, Reporting and Conformance)

SPF ve DKIM sonuçlarını alan adı hizalamasıyla birlikte değerlendirir. Alan adı sahibinin başarısız doğrulamalar için nasıl politika uygulanacağını belirlemesine ve rapor almasına yardımcı olur.

### SPF, DKIM ve DMARC Karşılaştırması

| Mekanizma | Temel görevi |
|---|---|
| SPF | Gönderen IP adresinin alan adı adına e-posta göndermeye yetkili olup olmadığını kontrol etmek |
| DKIM | E-postanın imzasını doğrulamak |
| DMARC | SPF/DKIM sonuçlarını alan adı hizalaması ve politika ile değerlendirmek |

**Önemli:** Bu mekanizmalar e-posta sahteciliği riskini azaltmaya yardımcı olur ancak her oltalama saldırısını tek başına engellemez.

E-posta başlıklarında bulunan Return-Path veya X-Mailer gibi alanlar da tek başına bir mesajın zararlı olduğunu kanıtlamaz. E-posta değerlendirmesi birden fazla teknik göstergeyle yapılmalıdır.

## 4.4. Drive-by Download

Kullanıcının bir web sitesini ziyaret etmesi sırasında, yeterli güvenlik kontrolleri bulunmadığında istenmeyen dosyaların indirilmesi veya zararlı içeriğin çalıştırılmasıyla sonuçlanabilen saldırı yaklaşımıdır.

Korunma yöntemleri:
- Tarayıcı ve işletim sistemini güncel tutmak.
- Güvenilir olmayan sitelerden uzak durmak.
- Uç nokta koruma sistemlerini kullanmak.
- Tarayıcı güvenlik ayarlarını yapılandırmak.

## 4.5. Watering Hole Attack

Saldırganın hedeflediği kişilerin sıklıkla ziyaret ettiği bir web sitesini ele geçirmeye veya zararlı içerik sunacak şekilde değiştirmeye çalıştığı saldırı türüdür.

Örneğin belirli bir sektörde çalışanların sık kullandığı bir web sitesi hedef alınabilir.

Savunma yöntemleri:
- Tarayıcı güvenliğini sağlamak.
- Web trafiğini izlemek.
- Güncel güvenlik yamalarını uygulamak.
- Zararlı içerik ve yönlendirmeleri analiz etmek.

## 4.6. USB Baiting ve HID Saldırıları

Saldırganlar, merak uyandıran USB bellekleri hedef kişilerin bulabileceği yerlere bırakabilir.

Amaç, kullanıcının bilinmeyen USB belleği bilgisayara takmasını sağlamaktır.

Bazı özel USB cihazları kendilerini klavye gibi tanıtarak önceden belirlenmiş tuş girdilerini gönderebilir. Rubber Ducky bu tür HID tabanlı cihazlara örnektir.

**Savunma yöntemleri:**
- Bilinmeyen USB cihazlarını kullanmamak.
- Kurumlarda USB kullanımını sınırlandırmak.
- Cihaz kontrol politikaları uygulamak.
- Kullanıcıları sosyal mühendislik konusunda eğitmek.
- Uç nokta davranışlarını izlemek.

**Teknik not:** Modern Windows sistemlerinde USB belleğin takılması, içindeki her programın otomatik olarak çalışacağı anlamına gelmez. Ancak klavye gibi davranan HID cihazları farklı bir risk oluşturabilir.

---

# 5. Sömürü (Exploitation)

## 5.1. Exploitation Nedir?

Exploitation, saldırganın hedef sistemdeki bir güvenlik açığından yararlanarak beklenmeyen veya yetkisiz bir işlem gerçekleştirmeye çalıştığı aşamadır.

Bu aşamada saldırgan, keşif sırasında belirlediği zayıflıklardan yararlanmayı hedefleyebilir.

## 5.2. CVE Nedir?

CVE (Common Vulnerabilities and Exposures), bilinen güvenlik açıklarının ortak kimlik numaralarıyla tanımlanmasını sağlayan sistemdir.

CVE numarası, güvenlik ekiplerinin belirli bir açık hakkında ortak bir referans üzerinden iletişim kurmasına yardımcı olur.

Örnek:

`CVE-2017-0144`

Bu CVE, SMBv1 ile ilişkili ve EternalBlue saldırısıyla bilinen güvenlik açığıyla bağlantılıdır.

## 5.3. Zero-Day Açıkları

Zero-Day, üreticinin henüz düzeltme yayımlamadığı veya savunma açısından giderilmemiş güvenlik açıkları için kullanılan terimdir.

Bu tür açıklar, saldırganlar tarafından yama veya etkili koruma önlemleri bulunmadan önce kullanılabilir.

Zero-Day açıklarına karşı savunma için:
- Sistem davranışlarını izlemek.
- Uç nokta güvenlik çözümlerini kullanmak.
- Ağ trafiğini analiz etmek.
- Gereksiz servisleri kapatmak.
- En az ayrıcalık ilkesini uygulamak önemlidir.

## 5.4. Saldırı Türleri

### İşletim Sistemi ve Servis Açıkları

İşletim sistemi veya ağ servislerinde bulunan güvenlik açıklarından yararlanılmasıdır.

Örnek olarak güncel olmayan bir SMB hizmetindeki güvenlik açığı verilebilir.

### Web Uygulaması Açıkları

Web uygulamalarındaki güvenlik zayıflıkları saldırı amacıyla kullanılabilir.

Örnekler:
- SQL Injection
- Yetkilendirme hataları
- Command Injection
- Güvenli olmayan dosya yükleme

### Client-Side Açıkları

Kullanıcının cihazında veya tarayıcısında çalışan yazılımları etkileyen güvenlik açıklarıdır.

Örneğin güncel olmayan bir tarayıcı bileşenindeki zafiyet hedef alınabilir.

## 5.5. Command Injection

Command Injection, bir uygulamanın kullanıcı girdisini güvenli şekilde işlememesi nedeniyle işletim sistemi komutlarının beklenmeyen biçimde çalıştırılabilmesine yol açan güvenlik açığıdır.

Olası sonuçlar:
- Yetkisiz komut çalıştırılması
- Dosyalara erişim
- Sistem bilgilerinin elde edilmesi
- Uygulamanın çalıştığı hesap yetkileri dahilinde işlemler gerçekleştirilmesi

Korunma yöntemleri:
- Kullanıcı girdilerini güvenli şekilde doğrulamak.
- İşletim sistemi komutlarını mümkünse doğrudan çalıştırmamak.
- Parametreleri güvenli API'lerle iletmek.
- Uygulamayı en düşük yetkiyle çalıştırmak.
- Güvenlik testleri gerçekleştirmek.

## 5.6. Buffer Overflow

Buffer Overflow, bir programın ayrılan bellek alanından daha fazla veri yazılması sonucunda bellek taşması meydana gelmesidir.

Bu durum programın çökmesine, beklenmeyen davranışlara veya uygun koşullarda güvenlik açıklarına neden olabilir.

Bellek güvenliğinin sağlanması için:
- Güvenli programlama yöntemleri kullanılmalıdır.
- Girdi uzunlukları kontrol edilmelidir.
- Güvenli bellek yönetimi uygulanmalıdır.
- Modern işletim sistemlerinin koruma mekanizmaları etkin olmalıdır.

### DEP ve ASLR

**DEP (Data Execution Prevention):** Belleğin belirli bölgelerinde kod çalıştırılmasını sınırlandırmaya yardımcı olur.

**ASLR (Address Space Layout Randomization):** Bellekteki bazı alanların adreslerini rastgeleleştirerek saldırganın sabit adreslere dayanmasını zorlaştırır.

Bu mekanizmalar bellek tabanlı saldırıların etkisini azaltmaya yardımcı olur; ancak bütün açıkları tek başına ortadan kaldırmaz.

## 5.7. Exploitation Aşamasına Karşı Savunma

- Güvenlik yamalarını zamanında uygulamak.
- Kullanılmayan servisleri kapatmak.
- Web uygulamalarında güvenli kod geliştirmek.
- WAF kullanmak.
- EDR ve antivirüs çözümlerinden yararlanmak.
- Ağ segmentasyonu uygulamak.
- Sistemleri en az ayrıcalık ilkesiyle yapılandırmak.
- Güvenlik testleriyle açıkları düzenli olarak doğrulamak.

---

# 6. Kurulum (Installation)

## 6.1. Installation Nedir?

Installation, saldırganın hedef sistemde erişimini sürdürmek veya tekrar erişim elde etmek amacıyla kalıcılık sağlamaya çalıştığı aşamadır.

Saldırgan, ilk erişimden sonra sistem yeniden başlatılsa bile faaliyetlerini sürdürebilecek mekanizmalar oluşturmaya çalışabilir.

Bu kavram siber güvenlikte **Persistence (Kalıcılık)** olarak da bilinir.

## 6.2. Persistence (Kalıcılık)

Kalıcılık, bir saldırganın sistemde elde ettiği erişimi zaman içerisinde korumaya yönelik teknikleri ifade eder.

Kalıcılık mekanizmaları farklı işletim sistemlerinde farklı şekillerde ortaya çıkabilir.

Örnekler:
- Başlangıçta çalışan programlar
- Zamanlanmış görevler
- Servisler
- Başlangıç klasöründeki dosyalar
- Web Shell
- Yetkisiz hesap veya erişim değişiklikleri

## 6.3. Windows Registry

Windows Registry, işletim sistemi ve uygulamalara ait yapılandırma bilgilerinin saklandığı merkezi kayıt sistemidir.

Bazı kayıt defteri alanları, kullanıcı oturumu açıldığında programların başlatılması için kullanılabilir.

Güvenlik açısından:
- Beklenmeyen başlangıç kayıtları incelenmelidir.
- Şüpheli kayıt defteri değişiklikleri izlenmelidir.
- Yetkisiz uygulama başlangıçları araştırılmalıdır.

**Not:** Registry üzerindeki her değişiklik zararlı değildir. Değişiklikler program güncellemeleri veya normal sistem işlemleri nedeniyle de oluşabilir.

## 6.4. Scheduled Tasks (Zamanlanmış Görevler)

Windows sistemlerinde belirli zamanlarda veya olaylar gerçekleştiğinde otomatik görevlerin çalıştırılmasını sağlar.

Linux sistemlerinde benzer amaçlarla cron gibi mekanizmalar kullanılabilir.

Saldırganlar bu mekanizmaları kötüye kullanarak kalıcılık sağlamaya çalışabilir.

Savunma açısından:
- Bilinmeyen görevler incelenmelidir.
- Görevlerin çalıştırdığı programlar doğrulanmalıdır.
- Görev oluşturma ve değiştirme kayıtları izlenmelidir.

## 6.5. Services ve Daemons

Windows sistemlerinde Services, Linux sistemlerinde ise daemon veya servis mekanizmaları arka planda çalışan hizmetleri ifade eder.

Saldırganlar bu mekanizmaları kötüye kullanarak sistem üzerinde kalıcılık sağlamaya çalışabilir.

Ancak her servis yönetici veya root yetkisiyle çalışmaz. Servisin yetkisi yapılandırmasına bağlıdır.

## 6.6. Startup Folder

Windows başlangıç klasörleri, kullanıcı oturumu açıldığında belirli uygulamaların otomatik başlatılmasını sağlayabilir.

Bu mekanizma kötüye kullanıldığında istenmeyen programların kullanıcı oturumuyla birlikte başlamasına neden olabilir.

## 6.7. Web Shell

Web Shell, web sunucusu üzerinde çalışabilen ve belirli koşullarda komut yürütülmesine imkân sağlayabilen betik veya dosyadır.

Saldırganlar ele geçirdikleri sunucularda Web Shell kullanarak erişimlerini sürdürmeye çalışabilir.

Savunma ekipleri:
- Web dizinlerindeki dosyaları izlemeli.
- Şüpheli dosya değişikliklerini incelemeli.
- Web sunucusu loglarını analiz etmeli.
- Gereksiz yazma izinlerini kaldırmalıdır.

## 6.8. Dropper ve Downloader

Bu iki kavram zararlı yazılımların sisteme ek bileşenler getirme yöntemleriyle ilişkilidir.

**Dropper:** Zararlı bileşenleri kendi içerisinde barındırabilir veya sistemde ortaya çıkarabilir.

**Downloader:** Genellikle başka bir kaynaktan ek dosya veya bileşen indirmek için kullanılır.

İkisi arasındaki temel fark, ek bileşenlerin nasıl sağlandığıdır.

## 6.9. FIM (File Integrity Monitoring)

FIM, dosyaların bütünlüğünü izlemek için kullanılan yöntemdir.

Dosyaların:
- Oluşturulması
- Silinmesi
- Değiştirilmesi
- İzinlerinin değiştirilmesi

gibi işlemlerinin takip edilmesine yardımcı olur.

Örneğin kritik bir sistem dosyasının beklenmedik şekilde değişmesi güvenlik alarmı oluşturabilir.

## 6.10. Kurulum Aşamasına Karşı Savunma

- Dosya bütünlüğü izleme kullanmak.
- Registry değişikliklerini takip etmek.
- Zamanlanmış görevleri denetlemek.
- Başlangıç uygulamalarını incelemek.
- Kullanıcı ve servis yetkilerini sınırlandırmak.
- Uygulama izin listeleri kullanmak.
- Şüpheli web dosyalarını analiz etmek.
- Sistem loglarını merkezi olarak toplamak.

AppLocker gibi uygulama kontrol mekanizmaları, belirlenen kurallara göre uygulamaların çalıştırılmasını sınırlandırmaya yardımcı olabilir. Ancak doğru yapılandırılmaları gerekir.

---

# 7. Komuta ve Kontrol (Command and Control – C2)

## 7.1. C2 Nedir?

Command and Control, saldırganın ele geçirilen sistemlerle iletişim kurmasını ve bu sistemleri uzaktan yönetmesini sağlayan iletişim aşamasıdır.

Saldırgan, hedef sistemdeki zararlı yazılımla iletişim kurarak komut göndermeye veya bilgi almaya çalışabilir.

C2 iletişimi, saldırının devam ettirilmesi ve hedef sistemlerin yönetilmesi açısından önemlidir.

## 7.2. C2 İletişim Yöntemleri

Saldırganlar farklı ağ protokollerini ve servisleri kullanarak iletişim kurmaya çalışabilir.

### HTTP ve HTTPS

Web trafiği üzerinden iletişim kurulabilir.

HTTPS, iletişimin içeriğini şifreleyerek ağ üzerinde okunmasını zorlaştırır. Ancak bağlantı bilgileri, trafik sıklığı ve davranış özellikleri yine de güvenlik ekipleri tarafından analiz edilebilir.

### DNS Tunneling

DNS protokolü üzerinden normal DNS trafiğine benzer şekilde gizli veri iletişimi kurulmaya çalışılmasıdır.

DNS tunneling şu amaçlarla kötüye kullanılabilir:
- Komuta ve kontrol iletişimi
- Veri aktarımı
- Ağ kısıtlamalarını kötüye kullanma

Savunma ekipleri olağan dışı DNS sorgularını, beklenmeyen alan adlarını ve anormal trafik hacmini inceleyebilir.

### ICMP

ICMP, ağ cihazları arasında hata ve kontrol mesajları iletmek için kullanılır.

Bazı saldırganlar ICMP paketlerini kötüye kullanarak iletişim veya veri aktarımı gerçekleştirmeye çalışabilir.

### Diğer Servisler

Bazı saldırılarda FTP, SMTP veya meşru bulut servisleri de iletişim amacıyla kötüye kullanılabilir.

## 7.3. Beaconing

Beaconing, ele geçirilmiş sistemin belirli aralıklarla C2 sunucusuna bağlantı kurması davranışıdır.

Örneğin bir zararlı yazılım belirli aralıklarla dışarıdaki bir sunucuyla iletişim kurabilir.

Güvenlik ekipleri:
- Düzenli bağlantı aralıklarını
- Olağan dışı DNS sorgularını
- Bilinmeyen dış IP adreslerini
- Şüpheli veri aktarımını

inceleyerek bu davranışları tespit etmeye çalışır.

## 7.4. Jitter

Jitter, bağlantı zamanlamasındaki değişkenliği ifade eder.

Bazı zararlı yazılımlar sabit aralıklarla iletişim kurmak yerine bağlantı zamanlarını değiştirerek düzenli trafik örüntülerinin tespit edilmesini zorlaştırmaya çalışabilir.

## 7.5. DGA (Domain Generation Algorithm)

DGA, belirli algoritmalar kullanılarak çok sayıda alan adı üretilmesini sağlayan yöntemdir.

Bazı zararlı yazılımlar C2 iletişimi için bu yöntemi kullanabilir.

Savunma ekipleri:
- DNS sorgularını analiz edebilir.
- Alan adlarının karakter yapılarını inceleyebilir.
- Şüpheli alan adlarını tehdit istihbaratıyla karşılaştırabilir.
- Olağan dışı bağlantı davranışlarını takip edebilir.

## 7.6. C2 Aşamasına Karşı Savunma

- DNS trafiğini analiz etmek.
- Güvenlik duvarı ve proxy kayıtlarını incelemek.
- Ağ segmentasyonu uygulamak.
- Şüpheli dış bağlantıları araştırmak.
- EDR sistemleriyle uç nokta davranışlarını izlemek.
- Tehdit istihbaratı kaynaklarından yararlanmak.
- Olağan dışı bağlantı sıklıklarını tespit etmek.

**Önemli:** Şifreli HTTPS trafiği her zaman zararlı değildir. Bir bağlantının değerlendirilmesinde hedef alan adı, sertifika bilgileri, bağlantı sıklığı, süreç davranışı ve diğer göstergeler birlikte ele alınmalıdır.

---

# 8. Hedef Üzerindeki Eylemler (Actions on Objectives)

## 8.1. Actions on Objectives Nedir?

Bu aşama, saldırganın hedeflediği asıl işlemleri gerçekleştirmeye çalıştığı aşamadır.

Saldırganın amacı kuruma veya kullanıcıya göre değişebilir.

Örnek amaçlar:
- Veri çalmak
- Dosyaları şifrelemek
- Sistemleri kullanılamaz hâle getirmek
- Hassas bilgileri değiştirmek
- Finansal kazanç elde etmek
- Kurumun hizmetlerini aksatmak

## 8.2. Data Exfiltration (Veri Sızdırma)

Data Exfiltration, bir sistemden veya ağdan verilerin yetkisiz şekilde dışarı aktarılmasıdır.

Çalınabilecek verilere örnekler:
- Müşteri bilgileri
- Kimlik bilgileri
- Finansal kayıtlar
- Şirket belgeleri
- Kaynak kodları

Veri sızdırma faaliyetleri bazen normal ağ trafiği gibi görünmeye çalışabilir.

**Savunma yöntemleri:**
- DLP sistemleri
- Ağ trafiği analizi
- Veri erişim kontrolleri
- Şüpheli dosya aktarımının izlenmesi
- Hassas verilerin sınıflandırılması

## 8.3. Ransomware (Fidye Yazılımı)

Ransomware, dosyaları veya sistemleri kullanılamaz hâle getirerek mağdurdan fidye talep etmeyi amaçlayan zararlı yazılım türüdür.

Bazı modern saldırılarda saldırganlar dosyaları şifrelemeden önce verileri dışarı aktarabilir.

Bu durum **Double Extortion (Çifte Şantaj)** olarak adlandırılır.

Saldırgan hem sistemlerin yeniden kullanılabilmesi için hem de çalınan verilerin yayımlanmaması için fidye talep edebilir.

Savunma yöntemleri:
- Çevrim dışı veya değiştirilemez yedekler
- Güncel güvenlik yamaları
- MFA
- Ağ segmentasyonu
- EDR
- Kullanıcı farkındalığı
- Düzenli kurtarma testleri

## 8.4. Destruction ve Sabotaj

Saldırgan, sistemlere veya verilere zarar vermeyi amaçlayabilir.

Örnekler:
- Dosyaların silinmesi
- Veritabanlarının bozulması
- Sistem yapılandırmalarının değiştirilmesi
- Hizmetlerin çalışamaz hâle getirilmesi

Bu tür faaliyetler kurumun iş sürekliliğini ciddi şekilde etkileyebilir.

## 8.5. Resource Hijacking

Resource Hijacking, ele geçirilen sistem kaynaklarının saldırganın amaçları doğrultusunda kullanılmasıdır.

Örneğin bir bilgisayarın işlemci gücünün izinsiz kripto para madenciliğinde kullanılması.

Belirtileri:
- Olağan dışı CPU kullanımı
- Beklenmeyen süreçler
- Artan ağ trafiği
- Sistem performansında düşüş

## 8.6. Data Manipulation

Data Manipulation, sistemlerde bulunan verilerin yetkisiz veya kötü niyetli şekilde değiştirilmesidir.

Örnek:
Bir kurumun finansal kayıtlarında bulunan değerlerin değiştirilmesi.

Bu tür saldırılar yalnızca veri gizliliğini değil, veri bütünlüğünü de etkiler.

## 8.7. Lateral Movement (Yanal Hareket)

Lateral Movement, saldırganın ele geçirdiği bir sistemden ağ içerisindeki diğer sistemlere geçmeye çalışmasıdır.

Örneğin bir çalışanın bilgisayarına erişim sağlayan saldırganın, aynı ağdaki başka sunuculara ulaşmaya çalışması.

Saldırganın amacı daha fazla sisteme erişmek veya daha yüksek yetkiler elde etmek olabilir.

Lateral Movement için kötüye kullanılabilen yöntemler:
- Çalınmış kimlik bilgileri
- Uzak masaüstü servisleri
- SSH
- WMI
- PowerShell Remoting
- Ağdaki yanlış yapılandırmalar

**Önemli:** Lateral Movement yalnızca Cyber Kill Chain'in son aşamasında gerçekleşmek zorunda değildir. Gerçek saldırılarda farklı aşamalarda ortaya çıkabilir.

## 8.8. Pass-the-Hash

Pass-the-Hash, bazı Windows kimlik doğrulama senaryolarında parola yerine ele geçirilmiş parola hash değerinin kötüye kullanılmasına dayanan saldırı tekniğidir.

Savunma yöntemleri:
- Ayrıcalıklı hesapları sınırlandırmak.
- Kimlik bilgilerini korumak.
- Yönetici hesaplarının kullanımını kontrol etmek.
- Ağ segmentasyonu uygulamak.
- Uç nokta güvenlik kayıtlarını izlemek.

## 8.9. Actions on Objectives Aşamasına Karşı Savunma

- Hassas verilere erişimi sınırlandırmak.
- DLP çözümleri kullanmak.
- Yedekleri düzenli olarak test etmek.
- Ağ segmentasyonu uygulamak.
- Ayrıcalıklı hesapları izlemek.
- Olağan dışı veri aktarımını tespit etmek.
- Olay müdahale planlarını hazır bulundurmak.

---

# 9. Savunma ve Tespit Mekanizmaları

Cyber Kill Chain yalnızca saldırganın faaliyetlerini anlamak için değil, savunma stratejisi oluşturmak için de kullanılabilir.

Savunma ekipleri her aşamada farklı güvenlik kontrolleri uygulayabilir.

## 9.1. Katmanlı Güvenlik Yaklaşımı

Tek bir güvenlik aracı bütün saldırıları engelleyemez.

Bu nedenle kurumlar birden fazla güvenlik katmanını birlikte kullanmalıdır.

Örnekler:
- Firewall
- IDS/IPS
- SIEM
- EDR
- Antivirüs
- E-posta güvenliği
- MFA
- DLP
- Yedekleme sistemleri
- Ağ segmentasyonu

Bir katmanda başarısızlık yaşansa bile diğer katmanlar saldırının etkisini azaltabilir.

## 9.2. Detect, Deny, Disrupt, Degrade, Deceive, Destroy

Cyber Kill Chain ile ilişkili savunma tartışmalarında farklı savunma eylemleri de ele alınabilir.

Bu kavramlar genel olarak şu şekilde açıklanabilir:

| Kavram | Açıklama |
|---|---|
| Detect | Tehdidi veya saldırı belirtisini tespit etmek |
| Deny | Saldırının hedefe ulaşmasını engellemek |
| Disrupt | Saldırının işleyişini kesintiye uğratmak |
| Degrade | Saldırının etkisini veya kapasitesini azaltmak |
| Deceive | Saldırganı yanıltmaya yönelik savunma yöntemleri kullanmak |
| Destroy | Tehdit oluşturan bileşenleri etkisiz hâle getirmek |

Bu terimler her kaynakta aynı kapsamda kullanılan evrensel bir standart değildir. Özellikle Destroy kavramı, bağlama göre farklı şekilde yorumlanabilir.

Savunma faaliyetleri, yetkili ve hukuka uygun müdahaleler çerçevesinde yürütülmelidir. Bu kavramlar izinsiz karşı saldırı anlamına gelmez.

## 9.3. IoC (Indicator of Compromise)

IoC, bir sistemin veya ağın güvenliğinin ihlal edilmiş olabileceğini gösteren teknik göstergelerdir.

IoC örnekleri:

- Şüpheli IP adresleri
- Zararlı alan adları
- Dosya hash değerleri
- Beklenmeyen dosyalar
- Şüpheli süreçler
- Olağan dışı ağ bağlantıları
- Zararlı yazılım izleri

### Hash Nedir?

Hash, bir veri üzerinden belirli uzunlukta özet değer üreten matematiksel işlemdir.

Dosya analizinde hash değerleri, dosyaların birbirleriyle karşılaştırılmasına yardımcı olabilir.

Yaygın algoritmalar:
- MD5
- SHA-1
- SHA-256

Güvenlik amaçlı bütünlük doğrulamasında modern ve uygun algoritmalar tercih edilmelidir. MD5 ve SHA-1 çakışma dayanıklılığı bakımından artık güvenli kriptografik özet algoritmaları olarak kabul edilmez.

## 9.4. IoC Nasıl Kullanılır?

IoC'ler farklı güvenlik sistemlerinde kullanılabilir.

Örneğin:
- SIEM sistemlerinde korelasyon yapmak.
- EDR sistemlerinde dosya ve süreçleri incelemek.
- Firewall üzerinden şüpheli bağlantıları kontrol etmek.
- DNS güvenliği sistemlerinde zararlı alan adlarını değerlendirmek.
- Tehdit istihbaratı platformlarıyla göstergeleri karşılaştırmak.

**Önemli:** Bir IoC'nin bulunması her zaman kesin saldırı kanıtı değildir. Göstergeler güncelliği, kaynağı ve bağlamı dikkate alınarak değerlendirilmelidir. Yanlış pozitifler de mümkündür.

## 9.5. SIEM Nedir?

SIEM (Security Information and Event Management), farklı sistemlerden log ve güvenlik olaylarını merkezi olarak toplayıp analiz etmeye yardımcı olan teknolojidir.

SIEM sistemleri:
- Log toplama
- Olay korelasyonu
- Alarm üretme
- Güvenlik izleme
- Olay araştırması
- Raporlama

gibi işlevler sunabilir.

## 9.6. Örnek Savunma Senaryosu

Bir kurumda çalışan kullanıcının şüpheli bir e-posta eki açtığını düşünelim.

Güvenlik ekipleri aşağıdaki kontrolleri gerçekleştirebilir:

1. E-posta güvenlik sistemi mesajı inceler.
2. Uç nokta güvenlik sistemi şüpheli dosyayı analiz eder.
3. SIEM, ilgili sistemdeki olay kayıtlarını toplar.
4. Güvenlik analisti şüpheli süreçleri araştırır.
5. Gerekirse cihaz ağdan izole edilir.
6. Olayın kapsamı ve etkisi belirlenir.
7. Zararlı bileşenler temizlenir ve sistem güvenli şekilde kurtarılır.

Bu senaryo, saldırının farklı aşamalarında farklı savunma kontrollerinin kullanılabileceğini gösterir.

---

# 10. Cyber Kill Chain ve MITRE ATT&CK Karşılaştırması

## 10.1. MITRE ATT&CK Nedir?

MITRE ATT&CK, gerçek dünyada gözlemlenen saldırgan davranışlarını taktikler ve teknikler üzerinden sınıflandıran bir bilgi tabanıdır.

Siber güvenlik ekipleri bu çerçeveyi:
- Tehdit analizi
- Saldırı davranışlarını anlama
- Savunma kontrollerini değerlendirme
- Tehdit avcılığı
- Güvenlik testleri
- Olay müdahale

gibi çalışmalarda kullanabilir.

## 10.2. Taktik, Teknik ve Prosedür

MITRE ATT&CK içerisinde üç önemli kavram bulunur.

### Tactic (Taktik)

Saldırganın ulaşmak istediği amacı ifade eder.

Örneğin:
- Initial Access
- Execution
- Persistence
- Privilege Escalation
- Defense Evasion
- Credential Access
- Discovery
- Lateral Movement
- Collection
- Command and Control
- Exfiltration
- Impact

### Technique (Teknik)

Saldırganın belirli bir amaca ulaşmak için kullandığı yöntemi ifade eder.

Örneğin kimlik bilgilerini ele geçirme amacıyla kullanılan teknikler.

### Procedure (Prosedür)

Belirli bir saldırganın veya saldırı grubunun bir tekniği gerçek ortamda nasıl uyguladığını anlatır.

Kısaca:

- Taktik: Neden?
- Teknik: Nasıl?
- Prosedür: Nasıl uygulandı?

## 10.3. Cyber Kill Chain ve MITRE ATT&CK Farkları

| Özellik | Cyber Kill Chain | MITRE ATT&CK |
|---|---|---|
| Yapı | 7 aşamalı saldırı modeli | Taktik ve teknik matrisi |
| Yaklaşım | Üst seviyede saldırı süreci | Ayrıntılı saldırgan davranışları |
| Amaç | Saldırı zincirini anlamak | Teknikleri sınıflandırmak ve analiz etmek |
| Kullanım | Saldırının aşamalarını incelemek | Tespit, analiz ve savunmayı geliştirmek |
| Yapılandırma | Daha doğrusal | Daha esnek ve çok boyutlu |

## 10.4. İki Model Arasındaki Yaklaşık Eşleştirme

Cyber Kill Chain ile MITRE ATT&CK arasında birebir eşleşme bulunmaz. Ancak bazı aşamalar belirli taktiklerle ilişkilendirilebilir.

| Cyber Kill Chain | İlişkili MITRE ATT&CK alanları |
|---|---|
| Reconnaissance | Reconnaissance, Resource Development |
| Weaponization | Resource Development ve hazırlık faaliyetleri |
| Delivery | Initial Access |
| Exploitation | Initial Access, Execution veya ilgili teknikler |
| Installation | Persistence, Defense Evasion |
| Command and Control | Command and Control |
| Actions on Objectives | Collection, Exfiltration, Impact ve diğer taktikler |

Bu eşleştirme yaklaşık bir ilişkilendirmedir. Her saldırı aynı sırayı izlemek zorunda değildir.

## 10.5. Unified Kill Chain

Unified Kill Chain, farklı saldırı modellerini bir araya getirerek saldırı süreçlerini daha kapsamlı incelemeyi amaçlayan bir modeldir.

Paul Pols tarafından geliştirilen bu yaklaşım 18 aşama içerir.

Üç üst düzey bölüm üzerinden ele alınır:

- In: Hedef ortama ilk erişimin elde edilmesi
- Through: Ortam içerisinde ilerleme ve kontrol sağlama
- Out: Hedeflenen sonuçların elde edilmesi ve ortamdan veri çıkarılması gibi faaliyetler

Unified Kill Chain, modern saldırıların farklı aşamalarını daha ayrıntılı incelemeye yardımcı olabilir.

## 10.6. Hangi Model Ne Zaman Kullanılır?

**Cyber Kill Chain:** Saldırıların genel aşamalarını anlamak ve savunma noktalarını belirlemek için kullanılabilir.

**MITRE ATT&CK:** Saldırganın kullandığı teknikleri ayrıntılı olarak sınıflandırmak ve savunma kontrollerini değerlendirmek için kullanılabilir.

**Unified Kill Chain:** Saldırı sürecini daha geniş bir perspektifle incelemek için kullanılabilir.

Bu modeller birbirinin alternatifi olmak zorunda değildir. Birlikte kullanıldıklarında daha kapsamlı analiz yapılmasına yardımcı olabilirler.

---

# 11. Yararlı Kaynaklar

## Cyber Kill Chain
- [Lockheed Martin – Cyber Kill Chain](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html)

## MITRE ATT&CK
- [MITRE ATT&CK](https://attack.mitre.org/)
- [MITRE ATT&CK Enterprise Matrix](https://attack.mitre.org/matrices/enterprise/)

## Ağ Keşfi ve Güvenlik Araçları
- [Nmap](https://nmap.org/)
- [Shodan](https://www.shodan.io/)
- [TheHarvester](https://github.com/laramies/theHarvester)

## E-posta Güvenliği
- [SPF](https://www.rfc-editor.org/rfc/rfc7208)
- [DKIM](https://www.rfc-editor.org/rfc/rfc6376)
- [DMARC](https://www.rfc-editor.org/rfc/rfc7489)

## Güvenlik Araştırmaları
- [NIST](https://www.nist.gov/cybersecurity)
- [CVE](https://www.cve.org/)
- [CISA](https://www.cisa.gov/)

---

# Genel Değerlendirme

Bu derste Cyber Kill Chain modelinin yedi aşaması, saldırganların bu aşamalarda gerçekleştirebileceği faaliyetler ve savunma ekiplerinin uygulayabileceği güvenlik kontrolleri incelenmiştir.

Öğrenilen başlıca konular:

- Cyber Kill Chain modelinin amacı ve tarihçesi
- Yedi saldırı aşaması
- Pasif ve aktif keşif
- OSINT ve Google Dorking
- Nmap, Shodan, TheHarvester, Gobuster ve Dirb
- Exploit, Payload ve Obfuscation
- Phishing, SPF, DKIM ve DMARC
- Drive-by Download ve Watering Hole
- CVE ve Zero-Day
- Persistence ve FIM
- DNS Tunneling, Beaconing ve DGA
- Veri sızdırma ve fidye yazılımları
- Lateral Movement ve Pass-the-Hash
- IoC ve SIEM
- MITRE ATT&CK ve Unified Kill Chain

## Sonuç

Cyber Kill Chain, siber saldırıların farklı aşamalardan nasıl ilerleyebileceğini anlamak için kullanılan önemli bir modeldir.

Savunma açısından en önemli yaklaşım, saldırının yalnızca son aşamasına odaklanmamaktır. Keşif, iletim, sömürü ve kalıcılık gibi erken aşamalarda alınan önlemler saldırının ilerlemesini engelleyebilir.

Siber güvenlik ekipleri Cyber Kill Chain, MITRE ATT&CK ve diğer güvenlik kaynaklarını birlikte değerlendirerek daha kapsamlı savunma stratejileri geliştirebilir.
