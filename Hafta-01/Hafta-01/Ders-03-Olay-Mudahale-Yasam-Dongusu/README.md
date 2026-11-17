# Ders 3 – Olay Müdahale Yaşam Döngüsü (Incident Response Lifecycle)

## 1. Olay Müdahale Nedir?

Olay Müdahale (Incident Response), bir kurumun karşılaştığı siber güvenlik olaylarını tespit etmek, analiz etmek, kontrol altına almak, ortadan kaldırmak ve sistemleri güvenli şekilde yeniden çalışır hâle getirmek için uyguladığı süreçtir.

**Temel amaçları:**
- Siber saldırının etkisini azaltmak.
- Veri kaybını ve sistem zararını önlemek.
- Saldırının kaynağını ve kapsamını belirlemek.
- Sistemleri güvenli hâle getirmek.
- Benzer olayların tekrar yaşanmasını önlemek.

### Event ve Incident Arasındaki Fark

- **Event (Olay):** Sistemde gerçekleşen ve gözlemlenebilen herhangi bir durumdur.
- **Incident (Güvenlik Olayı):** Bilgi güvenliğini tehdit eden veya güvenlik ihlaline işaret eden olaydır.

Örnek:
- Bir kullanıcının sisteme giriş yapması: Event.
- Bir saldırganın çalınmış hesapla sisteme girmesi: Incident.

### Güvenlik Ekipleri

- **SOC (Security Operations Center):** Güvenlik olaylarını sürekli izleyen ve analiz eden merkezdir.
- **CSIRT (Computer Security Incident Response Team):** Siber güvenlik olaylarına müdahale eden ekiptir.
- **CERT (Computer Emergency Response Team):** Bilgisayar güvenliği acil durumlarına müdahale ve koordinasyon sağlayan ekiptir.

---

## 2. Olay Müdahale Frameworkleri

Olay müdahalesi rastgele yapılmaz. Belirli standartlar ve yöntemler kullanılır.

### NIST SP 800-61

NIST'in olay müdahalesi rehberidir. Rev.2 sürümünde dört temel aşama bulunur:

1. Preparation (Hazırlık)
2. Detection and Analysis (Tespit ve Analiz)
3. Containment, Eradication and Recovery (Kontrol Altına Alma, Temizleme ve Kurtarma)
4. Post-Incident Activity (Olay Sonrası Faaliyetler)

**Not:** NIST SP 800-61 Rev.3, olay müdahalesini NIST Cybersecurity Framework 2.0 ile uyumlu şekilde ele alan daha güncel sürümdür.

### SANS PICERL

SANS tarafından yaygınlaştırılan olay müdahale yaklaşımıdır.

- Preparation: Hazırlık
- Identification: Tanımlama
- Containment: Kontrol altına alma
- Eradication: Ortadan kaldırma
- Recovery: Kurtarma
- Lessons Learned: Öğrenilen dersler

### Golden Hour (Altın Saat)

Bir güvenlik olayının tespit edilmesinden sonraki ilk saatler kritik öneme sahiptir.

Bu süreçte hızlı ve doğru müdahale edilmesi saldırının büyümesini önleyebilir.

---

## 3. Preparation (Hazırlık)

Hazırlık aşaması, saldırı gerçekleşmeden önce kurumun müdahaleye hazır hâle getirilmesidir.

Yapılması gerekenler:

- Olay müdahale ekibinin oluşturulması.
- Görev ve sorumlulukların belirlenmesi.
- İletişim planının hazırlanması.
- Sistemlerin ve ağın envanterinin çıkarılması.
- Log kayıtlarının tutulması.
- Güvenlik araçlarının hazırlanması.
- Yedekleme ve kurtarma planlarının oluşturulması.
- Çalışanlara güvenlik eğitimi verilmesi.

### Tabletop Exercise

Gerçek bir saldırı gerçekleştirmeden, senaryo üzerinden ekiplerin nasıl müdahale edeceğinin test edilmesidir.

### Baseline

Bir sistemin normal çalışma davranışını gösteren referans veridir.

Örneğin bir sunucunun normalde hangi saatlerde ve ne kadar trafik ürettiğinin bilinmesi, olağan dışı hareketleri tespit etmeyi kolaylaştırır.

### Kullanılabilecek Araçlar

- **Sysmon:** Windows sistemlerinde ayrıntılı olay kayıtları oluşturur.
- **FTK Imager:** Dijital delillerin adli kopyasını oluşturmak için kullanılır.
- **KAPE:** Dijital adli inceleme için veri toplama aracıdır.
- **Volatility:** Bellek (RAM) analizinde kullanılır.
- **Eric Zimmerman Tools:** Windows adli incelemelerinde kullanılan araç ailesidir.

---

## 4. Detection and Analysis (Tespit ve Analiz)

Bu aşamada güvenlik olayları tespit edilir ve gerçekten bir saldırı olup olmadığı araştırılır.

### Kullanılan Güvenlik Araçları

- **SIEM:** Farklı sistemlerden log toplar, ilişkilendirir ve şüpheli aktiviteleri tespit etmeye yardımcı olur.
- **EDR:** Uç noktalardaki şüpheli davranışları izler ve müdahale imkânı sağlar.
- **IDS:** Şüpheli ağ trafiğini tespit eder.
- **IPS:** Şüpheli ağ trafiğini tespit edip engelleyebilir.
- **Antivirus:** Zararlı yazılımları tespit etmeye ve engellemeye yardımcı olur.

### Triage (Önceliklendirme)

Tespit edilen olayların önem derecesine göre değerlendirilmesidir.

Örneğin:
- Düşük: Şüpheli ancak etkisi sınırlı aktivite.
- Orta: İncelenmesi gereken güvenlik uyarısı.
- Yüksek: Yetkisiz erişim şüphesi.
- Kritik: Aktif veri sızıntısı veya yaygın fidye yazılımı saldırısı.

### Log Analizi

Sistemlerde gerçekleşen işlemlerin kayıtları incelenir.

Örnekler:
- Windows Event ID 4104: PowerShell Script Block Logging kayıtlarıyla ilişkilidir.
- Web sunucusu logları: İstekleri, IP adreslerini ve HTTP durum kodlarını gösterir.
- Process kayıtları: Hangi uygulamanın hangi işlemi başlattığını gösterir.

**Önemli:** Tek bir log kaydı her zaman saldırı kanıtı değildir. Örneğin HTTP 200 kodu, bir isteğin başarılı şekilde yanıtlandığını gösterir; tek başına SQL Injection kanıtı değildir.

---

## 5. Containment (Kontrol Altına Alma)

Bu aşamada saldırının yayılması ve daha fazla zarar vermesi engellenir.

### Temel Müdahale Yöntemleri

- Etkilenen cihazı ağdan izole etmek.
- Şüpheli IP adreslerini engellemek.
- Ele geçirilmiş kullanıcı hesaplarını geçici olarak devre dışı bırakmak.
- Zararlı ağ trafiğini engellemek.
- Güvenlik duvarı kurallarını güncellemek.
- Ağ segmentasyonu uygulamak.

### Network Isolation

Saldırıya uğramış cihazın ağ bağlantısının kesilerek diğer sistemlere zarar vermesinin önlenmesidir.

### Virtual Patching

Sistemin kendisini hemen güncellemek mümkün olmadığında, WAF veya güvenlik duvarı gibi araçlarla açığın istismar edilmesini geçici olarak engellemektir.

### Dijital Delillerin Korunması

Müdahale sırasında delillerin bozulmamasına dikkat edilmelidir.

- RAM (bellek) kayıtları incelenebilir.
- Disk imajı alınabilir.
- Dosyaların hash değerleri hesaplanabilir.
- Delillerin kim tarafından ve ne zaman alındığı kaydedilmelidir.

**Önemli:** Aktif saldırı sırasında RAM imajı almak her zaman ağ bağlantısını kesmekten daha öncelikli değildir. Karar, risk ve müdahale prosedürüne göre verilmelidir.

---

## 6. Eradication (Ortadan Kaldırma)

Bu aşamada saldırının kaynağı ve sistemde bıraktığı zararlı unsurlar temizlenir.

Yapılması gerekenler:

- Zararlı yazılımları kaldırmak.
- Güvenlik açıklarını kapatmak.
- Ele geçirilmiş hesapları güvenli hâle getirmek.
- Yetkisiz kullanıcıları ve erişimleri kaldırmak.
- Saldırganın oluşturduğu kalıcılık mekanizmalarını temizlemek.
- Gerekirse sistemi güvenilir bir imajdan yeniden kurmak.
- Parola, erişim anahtarı ve oturum belirteçlerini yenilemek.

### Root Cause Analysis (Kök Neden Analizi)

Saldırının hangi güvenlik açığı veya eksiklik nedeniyle gerçekleştiğinin araştırılmasıdır.

Örnek:

Bir saldırgan güncellenmemiş bir sunucudaki güvenlik açığından yararlanmışsa, yalnızca zararlı dosyayı silmek yeterli değildir. Güvenlik açığı da kapatılmalıdır.

---

## 7. Recovery (Kurtarma)

Bu aşamada sistemler güvenli şekilde tekrar çalışır hâle getirilir.

Yapılması gerekenler:

1. Sistemlerin temiz olduğu doğrulanır.
2. Güvenilir yedeklerden geri yükleme yapılır.
3. Gerekli güvenlik güncellemeleri uygulanır.
4. Sistemler test edilir.
5. Hizmetler kontrollü şekilde yeniden açılır.
6. Sistemler daha yakından izlenir.

### Increased Monitoring

Kurtarma sonrasında sistemlerin normalden daha dikkatli izlenmesidir.

Amaç, saldırganın yeniden erişim sağlamasını veya saldırının tekrarlanmasını önlemektir.

---

## 8. Post-Incident Activity (Olay Sonrası Faaliyetler)

Olay tamamen kontrol altına alındıktan sonra süreç değerlendirilir.

### Lessons Learned (Öğrenilen Dersler)

Yaşanan olaydan çıkarılan sonuçların değerlendirilmesi ve güvenlik süreçlerinin geliştirilmesidir.

### Incident Report (Olay Raporu)

Raporda genellikle şu bilgiler bulunur:

- Olayın başlangıç ve bitiş zamanı.
- Olayın nasıl tespit edildiği.
- Etkilenen sistemler.
- Saldırının türü.
- Uygulanan müdahaleler.
- Oluşan zarar.
- Alınması gereken ek önlemler.

### Önemli Performans Ölçütleri

- **MTTD (Mean Time to Detect):** Bir güvenlik olayının ortalama tespit edilme süresi.
- **MTTR (Mean Time to Respond/Recover):** Kullanılan tanıma göre ortalama müdahale veya kurtarma süresi.
- **False Positive:** Gerçekte tehdit olmayan bir durumun tehdit olarak algılanması.

Bu ölçütler güvenlik ekibinin performansını değerlendirmeye yardımcı olur.

---

## 9. Playbook (Müdahale Rehberi)

Playbook, belirli bir güvenlik olayı gerçekleştiğinde hangi adımların izleneceğini açıklayan önceden hazırlanmış müdahale rehberidir.

### Phishing Playbook

Oltalama saldırısı tespit edildiğinde uygulanabilecek adımlar:

1. Şüpheli e-posta incelenir.
2. Gönderen adresi ve e-posta başlıkları kontrol edilir.
3. Bağlantılar güvenli yöntemlerle analiz edilir.
4. Zararlı ekler incelenir.
5. Etkilenen kullanıcı belirlenir.
6. Gerekirse parola ve oturum bilgileri yenilenir.
7. Benzer e-postalar diğer kullanıcılardan kaldırılır.
8. Olay raporlanır.

### Ransomware Playbook

Fidye yazılımı saldırısında:

1. Etkilenen cihazlar izole edilir.
2. Saldırının yayılma durumu araştırılır.
3. Deliller korunur.
4. Saldırının kaynağı belirlenir.
5. Zararlı yazılım ve kalıcılık mekanizmaları temizlenir.
6. Güvenilir yedeklerden kurtarma yapılır.
7. Sistemler kontrollü şekilde tekrar açılır.

**Önemli:** Hassas dosyalar ve kurum verileri, gizlilik riski değerlendirilmeden VirusTotal gibi üçüncü taraf servislere yüklenmemelidir.

---

## 10. Legal and Communication (Hukuki Süreçler ve İletişim)

Siber güvenlik olaylarında yalnızca teknik müdahale yeterli değildir. Hukuki yükümlülükler ve iletişim süreçleri de önemlidir.

### Chain of Custody (Delil Zinciri)

Dijital delillerin kim tarafından, ne zaman ve hangi koşullarda alındığının ve kimlere teslim edildiğinin kayıt altına alınmasıdır.

Amaç, delillerin bütünlüğünü ve güvenilirliğini korumaktır.

### KVKK ve GDPR

- **KVKK:** Türkiye'de kişisel verilerin korunmasını düzenleyen kanundur.
- **GDPR:** Avrupa Birliği'nin kişisel verilerin korunmasına ilişkin genel düzenlemesidir.

GDPR kapsamında belirli kişisel veri ihlallerinin, koşullar oluştuğunda yetkili denetim makamına 72 saat içinde bildirilmesi gerekir. Bu süre her güvenlik olayına koşulsuz uygulanmaz.

KVKK kapsamında da kişisel veri ihlallerine ilişkin bildirim yükümlülükleri bulunmaktadır.

### Kriz İletişimi

Olay sırasında doğru kişilere, doğru zamanda ve doğru bilgiler aktarılmalıdır.

- Teknik ekipler teknik ayrıntıları paylaşır.
- Yönetim olayın etkisi ve alınan önlemler hakkında bilgilendirilir.
- Hukuk ve ilgili uyum ekipleri sürece dâhil edilir.
- Hassas bilgiler yalnızca bilmesi gereken kişilerle paylaşılır.

---

## Genel Özet

Olay müdahale süreci, bir siber saldırının etkisini azaltmak ve sistemleri güvenli hâle getirmek için uygulanır.

Temel süreç şu şekilde özetlenebilir:

1. **Preparation:** Saldırıya hazırlık yapılır.
2. **Detection & Analysis:** Tehdit tespit edilir ve analiz edilir.
3. **Containment:** Saldırının yayılması engellenir.
4. **Eradication:** Saldırının kaynağı ve zararlı unsurlar temizlenir.
5. **Recovery:** Sistemler güvenli şekilde yeniden çalıştırılır.
6. **Lessons Learned:** Olaydan ders çıkarılır ve güvenlik önlemleri geliştirilir.

**Unutma:** Olay müdahalesinde amaç yalnızca saldırıyı durdurmak değil, saldırının nedenini anlamak, sistemleri güvenli hâle getirmek ve aynı olayın tekrar yaşanmasını önlemektir.

## Yararlı Kaynaklar

- [NIST SP 800-61 Rev. 3](https://csrc.nist.gov/pubs/sp/800/61/r3/final)
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
- [SANS Incident Response](https://www.sans.org/)
- [MITRE ATT&CK](https://attack.mitre.org/)
- [KVKK](https://www.kvkk.gov.tr/)
- [GDPR](https://gdpr.eu/)
