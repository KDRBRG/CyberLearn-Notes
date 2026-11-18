# LLM Güvenliği Temelleri

Bu notta Büyük Dil Modellerinin (Large Language Models – LLM) nasıl çalıştığı, temel mimari kavramları ve bu sistemlerin neden geleneksel yazılımlardan farklı güvenlik riskleri taşıdığı ele alınmaktadır.

## 1. Büyük Dil Modelleri (LLM) Nedir?

Büyük Dil Modelleri, çok büyük metin veri kümeleri üzerinde eğitilen ve verilen girdiye uygun metinler üretebilen yapay zekâ modelleridir. Soru yanıtlama, özetleme, çeviri, kod üretme ve metin sınıflandırma gibi görevlerde kullanılabilirler.

LLM'ler bir metni insanlar gibi anlamak yerine, eğitim sırasında öğrendikleri örüntülerden yararlanarak sıradaki token için olasılık tahmini yapar. Bu nedenle akıcı ve ikna edici görünen bir yanıt her zaman doğru olmak zorunda değildir.

### Temel kavramlar

- **Token:** Modelin işlediği metin birimidir. Bir token kelimenin tamamı, kelimenin bir parçası, noktalama işareti veya boşlukla ilişkili bir parça olabilir.
- **Tokenizasyon:** Metnin model tarafından işlenebilecek tokenlara ayrılması işlemidir.
- **Parametre:** Eğitim sırasında öğrenilen ve modelin davranışını belirleyen sayısal ağırlıklardır.
- **Bağlam penceresi (Context Window):** Modelin tek bir istekte dikkate alabildiği girdi ve çıktı tokenlarının toplam sınırıdır. Sınır modele göre değişir.
- **Prompt:** Modelden bir görev gerçekleştirmesini isteyen girdidir.
- **System prompt:** Uygulama tarafından modele verilen rol, davranış ve görev yönergeleridir.
- **User prompt:** Kullanıcının modele gönderdiği istektir.

## 2. Transformer Mimarisi

Modern LLM'lerin önemli bir bölümü Transformer mimarisine dayanır. Transformer, metindeki tokenlar arasındaki ilişkileri hesaplayarak bağlamı değerlendirmeye yardımcı olur.

Önceki sıralı mimarilerden farklı olarak Transformer, eğitim sırasında bir dizideki tokenlar arasındaki ilişkileri paralel biçimde hesaplayabilir. Bu yaklaşımın temel bileşenlerinden biri **öz-dikkat (Self-Attention)** mekanizmasıdır.

### Öz-dikkat (Self-Attention)

Self-Attention, bir dizideki her tokenın diğer tokenlarla ne ölçüde ilişkili olduğunu hesaplar. Böylece model, bir kelimenin anlamını değerlendirirken cümlenin başka bölümlerindeki ilgili kelimelerden de yararlanabilir.

Örneğin:

> “Ayşe kitabı Zeynep'e verdi çünkü o kitabı bitirmişti.”

Buradaki “o” zamirinin hangi kişiye veya bağlama gönderme yaptığını anlamak için cümlenin diğer bölümleri arasındaki ilişki değerlendirilir.

Self-Attention mekanizmasında yaygın olarak Query (Q), Key (K) ve Value (V) temsilleri kullanılır:

\[
Attention(Q,K,V)=softmax\left(\frac{QK^T}{\sqrt{d_k}}\right)V
\]

- **Query (Q):** Bir tokenın hangi bilgiyi aradığını temsil eder.
- **Key (K):** Diğer tokenların eşleştirme için kullanılan temsilleridir.
- **Value (V):** Dikkat ağırlıklarıyla birleştirilen bilgi temsilleridir.
- **Softmax:** İlişki puanlarını ağırlıklara dönüştürür.
- **\(d_k\):** Ölçekleme amacıyla kullanılan anahtar vektör boyutudur.

Bu işlem, modelin bağlamdaki ilgili bilgilere ağırlık vermesini sağlar.

## 3. LLM'ler Nasıl Eğitilir?

LLM geliştirme süreci kullanılan modele ve yönteme göre değişebilir. Genel olarak aşağıdaki aşamalar görülür:

1. **Ön eğitim (Pretraining):** Model, büyük miktarda veri üzerinden dil örüntülerini öğrenir. Yaygın yaklaşımlardan biri, verilen token dizisine göre sonraki tokenı tahmin etmektir.
2. **Göreve uyarlama (Fine-tuning):** Model belirli görevlerde daha başarılı olması için ek verilerle eğitilebilir.
3. **Denetimli ince ayar (Supervised Fine-Tuning – SFT):** Model, örnek girdi ve beklenen yanıt çiftleriyle istenen yanıt biçimlerine uyarlanır.
4. **İnsan geri bildirimiyle uyum (ör. RLHF):** İnsan tercihleri veya geri bildirimleri kullanılarak modelin yanıtlarının daha yararlı ve güvenli olması hedeflenebilir.

Zararlı istekleri reddetme ve güvenli yanıt verme davranışları; SFT, tercih verileriyle uyum ve diğer güvenlik eğitimleri gibi eğitim ve uyarlama süreçleriyle şekillendirilebilir. Bu davranışlar tek başına kusursuz bir güvenlik sınırı oluşturmaz.

## 4. Prompt Yapısı ve Talimatlar

LLM tabanlı uygulamalarda modelin davranışı, farklı kaynaklardan gelen talimat ve verilerle şekillenir.

Basitleştirilmiş bir örnek:

```text
SYSTEM:
Bir eğitim asistanısın. Yanıtlarını açık ve anlaşılır ver.

USER:
Öz-dikkat mekanizmasını açıklar mısın?
```

- **System prompt**, uygulamanın modele vermek istediği genel rolü ve davranış yönergelerini tanımlar.
- **User prompt**, kullanıcının o anki isteğini içerir.
- Bazı uygulamalarda geliştirici talimatları, araç çıktıları, RAG belgeleri ve konuşma geçmişi de bağlama eklenebilir.

Önemli güvenlik noktası: System prompt, gizli bilgi saklamak için güvenli bir kasa değildir. API anahtarları, parolalar ve erişim belirteçleri gibi sırlar prompt içine yerleştirilmemeli; uygulamanın güvenli yapılandırma ve gizli bilgi yönetimi mekanizmalarında tutulmalıdır.

## 5. Yapay Zekâ Güvenliği Neden Farklıdır?

Geleneksel yazılımlarda programın davranışı çoğunlukla açıkça tanımlanmış kurallar ve kod tarafından belirlenir. LLM tabanlı sistemlerde ise çıktı, modelin öğrendiği örüntülere ve o anki bağlama göre olasılıksal biçimde üretilir.

| Geleneksel yazılım | LLM tabanlı sistem |
|---|---|
| Çoğunlukla açık kurallar ve kod üzerinden çalışır. | Öğrenilmiş parametreler ve bağlam üzerinden çıktı üretir. |
| Aynı koşullarda çoğunlukla aynı sonucu verir. | Üretim ayarlarına bağlı olarak aynı isteme farklı yanıtlar verebilir. |
| Girdi çoğunlukla belirli biçim ve türlerle doğrulanır. | Doğal dil girdisi belirsiz, çok anlamlı ve yönlendirilebilir olabilir. |
| Güven sınırları genellikle kod ve sistem mimarisiyle tanımlanır. | Talimatlar ve güvenilmeyen veriler aynı model bağlamında bulunabilir. |

### Deterministik ve olasılıksal davranış

- **Deterministik sistem:** Aynı koşullar ve girdiler altında aynı çıktıyı üretmesi beklenir.
- **Olasılıksal sistem:** Olasılık dağılımına göre çıktı üretir; aynı girdi farklı zamanlarda farklı sonuçlara yol açabilir.

LLM çıktısının değişkenliği; sıcaklık (temperature), örnekleme yöntemi, model sürümü, sistem durumu ve diğer üretim ayarlarından etkilenebilir. Sıcaklığın düşük olması değişkenliği azaltabilir ancak her durumda tamamen ortadan kaldırmaz.

### LLM'lere özgü güvenlik sorunları

- **Prompt Injection:** Güvenilmeyen girdilerin modelin talimatlarını etkilemeye veya mevcut yönergeleri geçersiz kılmaya çalışmasıdır.
- **Hassas Bilgi İfşası:** Kişisel verilerin, gizli belgelerin veya uygulamaya ait hassas bilgilerin yanıta sızmasıdır.
- **Halüsinasyon:** Modelin gerçekte doğru olmayan bilgileri ikna edici biçimde üretmesidir.
- **Aşırı Yetkilendirme (Excessive Agency):** Modele ihtiyaç duyduğundan fazla araç veya işlem yetkisi verilmesidir.
- **RAG Zehirlenmesi:** Bilgi getirme sistemine kötü amaçlı veya yanıltıcı belgeler eklenerek model yanıtlarının etkilenmesidir.
- **Çıktıların Güvensiz İşlenmesi:** Model çıktısının doğrulanmadan kod, komut, HTML veya başka bir sistem girdisi olarak kullanılmasıdır.

## 6. Güvenlik İçin Temel Yaklaşım

LLM güvenliği yalnızca modele “güvenli davran” talimatı vermekle sağlanamaz. Modelin çevresindeki uygulama, veri kaynakları, araçlar ve erişim kontrolleri de korunmalıdır.

Temel ilkeler:

1. **Güvenilmeyen girdiyi doğrula:** Kullanıcı girdilerini ve dış kaynaklardan gelen içerikleri güvenilir talimat olarak kabul etme.
2. **En az ayrıcalık ilkesini uygula:** Modele ve araçlara yalnızca görev için gerekli yetkileri ver.
3. **Sırları prompt dışında tut:** API anahtarlarını ve parolaları güvenli yapılandırma veya secret management çözümlerinde sakla.
4. **Erişimi sınırla:** RAG belgelerinde ve konuşma hafızasında kullanıcı/rol bazlı erişim kontrolleri uygula.
5. **Çıktıyı doğrula:** Model çıktısını çalıştırmadan veya başka bir sisteme aktarmadan önce kontrol et.
6. **İnsan denetimi kullan:** Önemli, geri alınması zor veya yüksek etkili işlemlerde kullanıcı onayı ve insan kontrolü sağla.
7. **İzleme ve kayıt tut:** Şüpheli istekleri, araç kullanımını ve güvenlik olaylarını takip et.
8. **Katmanlı savunma kur:** Tek bir güvenlik kontrolüne bağlı kalma.

## 7. Kısa Değerlendirme

- Transformer mimarisinde tokenlar arasındaki ilişkilerin hesaplanmasında hangi mekanizma temel rol oynar?  
  **Cevap:** Öz-dikkat (Self-Attention).

- Tokenizasyon ne anlama gelir?  
  **Cevap:** Metnin modelin işleyebileceği token birimlerine ayrılmasıdır.

- Context window neyi ifade eder?  
  **Cevap:** Modelin bir istekte dikkate alabildiği token bağlamının sınırını ifade eder.

- Prompt Injection neden mümkün olabilir?  
  **Cevap:** Talimatlar ve güvenilmeyen girdiler aynı model bağlamında yer alabildiğinden, girdiler modelin davranışını etkilemeye çalışabilir.

- API anahtarları system prompt içinde tutulmalı mıdır?  
  **Cevap:** Hayır. Gizli bilgiler prompt dışında, uygulamanın güvenli yapılandırma ve secret management mekanizmalarında tutulmalıdır.

- LLM güvenliğinde neden katmanlı savunma gerekir?  
  **Cevap:** Tek bir kontrol aşılabilir veya yanlış yapılandırılabilir. Birden fazla bağımsız kontrol riski azaltır.

## Kaynaklar

- [OWASP GenAI Security Project – LLM Top 10](https://genai.owasp.org/llm-top-10/)
- [Attention Is All You Need – Vaswani et al. (2017)](https://arxiv.org/abs/1706.03762)

---

**Not:** Bu doküman eğitim amaçlı öğrenme notudur. LLM mimarileri, eğitim yöntemleri ve güvenlik uygulamaları modele ve kullanılan platforma göre değişebilir.
