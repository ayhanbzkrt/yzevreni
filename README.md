# L’AI’brary — Yapay Zekânın Fantastik Dünyasını Keşfedin

**Türkçe | [English version](#english-version)**  
**AI’Han Academy · Ayhan Bozkurt · Ekim 2026**

**© 2026 Ayhan Bozkurt · AI’Han Academy · L’AI’brary. Tüm hakları saklıdır.** Kaynak kod, özgün tasarım, görseller, animasyonlar ve eğitim içerikleri hak sahibinin önceden alınmış yazılı izni olmadan kopyalanamaz, yeniden yayımlanamaz, uyarlanamaz veya ticari amaçlarla kullanılamaz. GitHub’da görüntülenebilir olması kullanım lisansı verildiği anlamına gelmez.

> Yapay zekâyı yalnızca okumak değil; **görmek, kurcalamak, kodlamak, karşılaştırmak ve neden–sonuç ilişkisini anlayarak öğrenmek** için tasarlanmış, Türkçe ve İngilizce destekli etkileşimli bir öğrenme evreni.

**L’AI’brary**, yapay zekâ okuryazarlığını ileri düzey teknik konularla buluşturan; özgün izometrik dünyalar, açıklamalı deneyler, tarayıcıda çalışan algoritmalar ve seçili açık kaynak araçlar içeren bir dijital öğrenme projesidir. Bir kitap/portal ekosistemi olarak kurgulanmıştır; teknik geçmişi olmayan ziyaretçilerden geliştiricilere, öğrencilerden eğitimcilere kadar farklı seviyelerde keşfe olanak tanır.

**Önemli ayrım:** Platformun bazı laboratuvarları doğrudan JavaScript ile *gerçek sayısal hesaplama* yapar. Bazıları eğitilmiş büyük modellerin davranışını açıklayan *öğretici simülasyonlardır*. Bazı özellikler ise ancak gerçek model ağırlığı, WebGPU, kamera izni veya ayrı servis mevcutsa çalışır. Bu üç durum aynı şeymiş gibi sunulmaz.

---

## İçindekiler

1. [Projenin amacı](#projenin-amacı)
2. [Üç bölüm ve 14 evren](#üç-bölüm-ve-14-evren)
3. [Öğrenme yaklaşımı](#öğrenme-yaklaşımı)
4. [Etkileşimli laboratuvarlardan örnekler](#etkileşimli-laboratuvarlardan-örnekler)
5. [Teknik mimari](#teknik-mimari)
6. [Kurulum ve çalıştırma](#kurulum-ve-çalıştırma)
7. [TR/EN, erişilebilirlik ve tasarım](#tren-erişilebilirlik-ve-tasarım)
8. [Testler ve doğrulama kapsamı](#testler-ve-doğrulama-kapsamı)
9. [Güvenlik, veri ve kullanım sınırları](#güvenlik-veri-ve-kullanım-sınırları)
10. [Kaynaklar ve geliştirme bağlantıları](#kaynaklar-ve-geliştirme-bağlantıları)
11. [Katkı, lisans ve iletişim](#katkı-lisans-ve-iletişim)

---

## Projenin amacı

Bir kavramı öğretmek yalnızca tanımını göstermek değildir. L’AI’brary’de kullanıcı önce bir problemi görür, terimin ne anlama geldiğini gündelik dilde öğrenir ve ardından **girdi veya parametreyi gerçekten değiştirerek** algoritmanın ya da iş akışının nasıl tepki verdiğini inceler.

Böylece aşağıdaki sorulara cevap arar:

- Bir öneri sistemi, arama algoritması veya sınıflandırıcı neden farklı sonuçlar üretir?
- Bir sinir ağında ağırlık, eşik veya öğrenme oranı değiştiğinde ne olur?
- Yapay zekâ ajanı hangi bilgiyle karar verir, nerede insan onayı gerekir?
- Kamera bir nesneyi nasıl bulur; metnin kaynağı nasıl doğrulanır?
- Modelin başarısı, adalet, maliyet, çevresel etki ve güvenlik birlikte nasıl değerlendirilir?

**Pedagojik ilke:** Önce kavrat → somut örnek göster → müdahale ettir → hesapla/görselleştir → sonucu anlaşılır biçimde açıkla → başka bir durumda yeniden denet.

İçerik, zorunlu quiz, “öğrendim” butonu veya gerekçesiz ilerleme puanına dayalı değildir.

---

## Üç bölüm ve 14 evren

Portalın ana atlasında üç bölüm ve **14 özgün öğrenme evreni** yer alır.

### I. Yapay Zekâ Evrenine Giriş

| Evren | Öğrenme ve uygulama odağı |
|---|---|
| **Veri Akademisi** | Veri okuryazarlığı, analiz, Python, veri düzenleme, görselleştirme ve deneysel düşünme. |
| **Arama Adaları** | Algoritmalar, arama stratejileri, veri yapıları ve problem çözme. |
| **Makine Öğrenmesi** | Sınıflandırma, regresyon, benzerlik, karar ağaçları, model davranışı ve ölçüm. |
| **Yapay Zekâ Atölyesi** | Temel kavramlar, pikseller, sözcükler, örüntüler ve gündelik hayat/kütüphane örnekleriyle deneyim. |
| **Yapay Zekâ Ajanları** | Planlama, araç kullanımı, görev yürütme, izinler, insan onayı ve ajan iş akışları. |
| **Doğal Dil İşleme (NLP)** | Metin temizleme, tokenizasyon, arama, sözcük ve dil örüntüleri, metin analizi. |

### II. Modeller ve Akıllı Sistemler

| Evren | Öğrenme ve uygulama odağı |
|---|---|
| **Derin Öğrenme** | Sinir ağları, geri yayılım, konvolüsyon, Transformer, ses/görüntü ve etkileşimli sayısal modeller. |
| **MLOps** | Veri ve model sürümleme, model yaşam döngüsü, dağıtım, hata bütçesi, drift ve izleme. |
| **Bilgisayarlı Görme** | Piksel, filtre, kenar, nesne tespiti, OCR, el/yüz/vücut işaret noktaları ve kamera deneyleri. |
| **MCP ve Gelişmiş RAG** | Belge alma, BM25 ve hibrit arama, kaynak pasajları, protokol düşüncesi ve kontrollü araç erişimi. |

### III. İnsan, Üretim ve Gelecek

| Evren | Öğrenme ve uygulama odağı |
|---|---|
| **Görünmez Yapay Zekâ ve Otonom İşletmeler** | Stok, lojistik, finans, müşteri hizmeti ve çok adımlı karar simülasyonları. |
| **Hibrit Zekâ ve İnsan–AI İş Birliği** | İnsan–AI görev bölüşümü, onay, düzeltme, güven kalibrasyonu, adalet ve ortak üretim. |
| **Prompt Mühendisliği ve Üretken Yapay Zekâ** | Prompt tasarımı, **Bağlam Mühendisliği (Context Engineering)**, BM25 bağlam seçimi, JSON doğrulama, ajan/test akışları ve isteğe bağlı gerçek model karşılaştırması. |
| **Yapay Zekâ Riskleri, Etik ve Gelecek** | Algoritmik adalet, hizalama, AGI/ASI tartışmaları, güvenilirlik, telif, gizlilik, istihdam ve çevresel etki. |

**Kapsam notu:** Evrenlerin ayrıntılı müfredatları ve laboratuvar sayıları birbirinden farklıdır. Her gösterimin aynı düzeyde gerçek model eğitimi yaptığı iddia edilmez.

---

## Öğrenme yaklaşımı

### Konuyu bilmeyen ziyaretçi için

Teknik terimler ilk geçtikleri yerde sade bir tanım ve somut kullanım bağlamıyla ele alınır.

Örneğin:

**kNN:** Kendisine en çok benzeyen örneklerin etiketlerine bakarak karar veren yöntem.

**RAG:** Yanıt vermeden önce ilgili belgeleri bulup modele bilgi sağlama yaklaşımı.

**HITL:** Kritik adımda insanın müdahale edebilmesi.

Kavramlar soyut şemada bırakılmaz; kütüphane kataloğu, ödünç analizi, rapor hazırlama, belge tarama veya gündelik kararlarla ilişkilendirilir.

### Deneyimin iskeleti

1. **Gör:** Sorunun gerçek hayattaki karşılığını ve sahnedeki girdiyi incele.
2. **Anla:** Yeni terimin ne işe yaradığını, varsa model varsayımını öğren.
3. **Değiştir:** Metin, belge, görüntü, eşik, görev dağılımı veya kod üzerinde müdahale yap.
4. **Hesapla:** Hesabın/yürütmenin sonucunu gerçek ölçümle izle.
5. **Karşılaştır:** İki koşulun farkını, sınırlarını ve hata nedenlerini tartış.

Burada amaç çok sayıda düğmeye basmak değil; **değişen girdinin değişen çıktısını görmek** ve nedenini anlamaktır.

---

## Etkileşimli laboratuvarlardan örnekler

- **Veri/Python:** Tarayıcı içinde Pyodide motoru yüklenebildiğinde Python kodunu değiştirip tekrar çalıştırma.
- **ML ve Derin Öğrenme:** Eşik, özellik, öğrenme parametresi veya filtreyi değiştirerek tahmin/aktivasyon değerlerini yeniden hesaplama.
- **MLOps:** Canary trafik yüzdesi, hata bütçesi ve veri kayması metriklerinin parametreye göre değişmesi.
- **Belge Arama:** Kendi TXT/MD/CSV/JSON gibi belgelerini işleyip BM25 ile arama; sonuçları kaynak pasajıyla birlikte inceleme.
- **Computer Vision:** Canvas üzerinden gerçek piksel/filtre hesabı; ayrıca desteklenen cihazlarda TensorFlow.js, OpenCV.js, OCR ve MediaPipe ile isteğe bağlı model/kamera deneyleri.
- **Hibrit Zekâ:** Görevleri insan–AI arasında yeniden dağıtma; onayı reddetme; güven, hata ve adalet ölçülerini hesaplama.
- **Prompt ve Bağlam:** Prompt mimarı, belge bağlamı oluşturma, JSON Schema doğrulama, kontrollü ajan akışı ve iki gerçek model bağlıysa yanıt karşılaştırması.
- **Risk ve Etik:** Sentetik grup kararlarında TPR/FPR ve seçilme farkı, piyasa yoğunlaşmasında HHI, enerji için güç × süre hesabı.

Eğitim içeriğinde **sentetik veri**, **kural/algoritma tabanlı simülasyon** ve **gerçek eğitilmiş model çıkarımı** ayrımı gösterilmelidir.

Bağlı olmayan bir modelin çıktısı uydurulmaz.

---

## Teknik mimari

### Tek dosyalı dağıtım

Temel dağıtım, **HTML + CSS + JavaScript + gömülü veri ve görseller** içeren tek bir dosyadır.

Ana evren atlası, giriş animasyonu, TR/EN metinleri ve farklı akademi modülleri aynı sayfa üzerinden açılır.

Temel atlas için npm/Node derleme zinciri zorunlu değildir.

```text
L’AI’brary
├── Intro / giriş animasyonu (TR / EN)
├── İzometrik evren atlası (14 ada)
│   ├── Bölüm I: Giriş (6 evren)
│   ├── Bölüm II: Modeller (4 evren)
│   └── Bölüm III: İnsan ve gelecek (4 evren)
├── Açıklamalı öğrenme sahneleri ve deney motorları
├── Yerel JS / Canvas / SVG hesaplamaları
├── İsteğe bağlı Python (Pyodide) ve tarayıcı modelleri
└── Bazı laboratuvarlarda isteğe bağlı yerel model servisi (Ollama)
```

### Kullanılan veya desteklenen teknoloji aileleri

| Katman | Teknolojiler / yaklaşım | Çalışma koşulu |
|---|---|---|
| Arayüz | HTML5, CSS, JavaScript, SVG, Canvas, animasyonlar | Ana dosyada |
| Hesaplama | Tarayıcı JavaScript'i, veri/istatistik algoritmaları, yerel arama | Çoğu deneyde yerel |
| Python | Pyodide / WebAssembly | İlk indirme ve tarayıcı belleği gerekebilir |
| NLP / LLM | Transformers.js, WebLLM, WebGPU/WASM | Destekli model, cihaz ve indirme gerekir |
| Görüntü / kamera | TensorFlow.js, OpenCV.js, MediaPipe, Tesseract.js | Model paketleri, HTTPS/localhost, izinler gerekir |
| Ses / zaman çizelgesi | Web Speech API, yerel ses ve zaman hesabı | Tarayıcı desteğine bağlı |
| Yerel model servisi | Ollama | Ayrı servis, kurulu modeller ve uygun bağlantı gerekir |

**Önemli:** Bu tablo her kütüphanenin her evrende koşulsuz çalıştığı anlamına gelmez. Paket sürümü, lisans, WebGPU desteği, erişim ve cihaz uyumluluğu ayrıca test edilmelidir.

GitHub Pages statik barındırma sağlar; kendi başına Python sunucusu, Ollama veya GPU arka ucu çalıştırmaz.

---

## Kurulum ve çalıştırma

### 1. Hızlı başlangıç

Depoya son bütünleşik dosyayı ekle:

```text
LAIbrary_Final_Senior_QA_2026.html
README.md
```

Bazı temel içerikler dosyaya çift tıklanarak açılabilir.

**Kamera, harici model indirmesi ve kimi tarayıcı güvenlik özellikleri için `localhost` ya da HTTPS tercih edilir.**

### 2. Yerel HTTP sunucusu (önerilen)

Terminalde HTML dosyasının bulunduğu klasöre geç:

```bash
python3 -m http.server 8765
```

Tarayıcıda şu adresi aç:

```text
http://localhost:8765/LAIbrary_Final_Senior_QA_2026.html
```

Chrome/Edge gibi güncel bir tarayıcı önerilir. WebGPU veya medya cihazı kullanan laboratuvarlar için tarayıcı ve donanım koşullarını kontrol et.

### 3. GitHub Pages ile yayımlama

1. Yeni bir GitHub deposu oluştur veya mevcut depoya dosyaları ekle.
2. HTML dosyasını kökte **`index.html`** olarak yayımla.
3. Depoda **Settings → Pages → Build and deployment → Deploy from a branch** yolunu seç.
4. Uygun dalı ve **`/(root)`** dizinini seçip yayımlamayı etkinleştir.
5. Yayımlandıktan sonra ana atlas, evren açılışları ve mobil görünümü gerçek HTTPS adresinde yeniden kontrol et.

> GitHub Pages yayını **statiktir**. Ollama, uzak API, büyük model indirimi ve API anahtarı gerektiren işlemler için uygun ayrı altyapı gerekir. API anahtarlarını HTML dosyasına veya GitHub deposuna gömme.

### 4. İsteğe bağlı gerçek model kullanımı

**WebLLM:** Uyumlu WebGPU cihazında model listesinden bir model seç ve indirme/yükleme tamamlandıktan sonra gerçek çıkarımı başlat. İlk açılış büyük bir indirme yapabilir; bellek yetersizliğinde işlem başarısız olabilir.

**Ollama:** Bilgisayarında Ollama ve kullanmak istediğin modeller kurulu olmalı; yerel API servisinin çalıştığını kontrol et. İlgili laboratuvarda model adını ve izin verilen yerel adresi seç. Tarayıcı erişimi, CORS ve güvenlik ayarları kurulumuna bağlıdır; internete açık, kimlik doğrulamasız servis oluşturma.

**Kamera/OCR:** Kamera iznini yalnız ilgili laboratuvarda ver. Model dosyalarının ilk yüklemesinde internet gerekebilir. Tarayıcı kaynakları ve kamera hataları geliştirici konsolundan incelenebilir.

---

## TR/EN, erişilebilirlik ve tasarım

- Türkçe ve İngilizce atlas/arayüz desteği; intro ekranında da TR/EN seçimi.
- İngilizce introda **“Skip Intro”** ve **“Enter the Universe”**; Türkçe introda **“Geç”** ve **“Evrene Gir”**.
- Açık/pastel estetik, özgün izometrik adalar ve konuya göre değişen deney görselleri.
- Mobil uyumlu yerleşim ve bazı geniş grafikler için kendi alanında kaydırma.
- Klavye, ekran okuyucu ve farklı tarayıcılarda kapsamlı erişilebilirlik denetimi hâlen geliştirilmesi gereken alandır; tam WCAG uyumu iddia edilmez.

**Tasarım ilkesi:** Sıradan kart/dashboard yığınları, boş prototipler veya yalnızca “başlat” düğmesiyle hazır cevabı gösteren sahneler hedef deneyim değildir.

Ana öğrenme öğesi, etkileşime tepki veren açıklamalı sahnenin kendisidir.

---

## Testler ve doğrulama kapsamı

23 Ekim 2026 tarihli **Senior QA** denetiminde raporlananlar:

| Kontrol | Raporlanan sonuç |
|---|---|
| Evren açılışları | **14/14** tıklama ile açıldı |
| NLP hesaplamaları | **36/36** ünite çağrısı boş olmayan çıktı verdi |
| ML, MLOps, MCP/RAG, Görünmez AI, Hibrit, Risk/Etik | **216** ünite girişinde iki koşullu sayısal kontrol |
| Prompt yerel çalışma alanları | **6** temel laboratuvarın çıktısı değişti |
| Mobil | Seçili evrenlerde **390 px** genişlik kontrolü |
| Intro | TR/EN ve evrene giriş akışı kontrol edildi |

**Bu kontroller bir üretim sertifikası değildir.**

Fiziksel kamerada bütün COCO/MediaPipe modelleri; farklı WebGPU cihazlarında WebLLM; iki gerçek Ollama modeli; tüm harici model paketleri; yüzlerce düğmenin tamamı ve her A/B deneyinin pedagojik kabulü uçtan uca doğrulanmış değildir.

---

## Güvenlik, veri ve kullanım sınırları

- Eğitim senaryolarındaki birçok veri kümesi **sentetiktir**; gerçek kurumsal veri veya bilimsel ölçüm olarak kullanılmamalıdır.
- Yerel hesaplama ve tarayıcı modeli farklıdır; ağ üzerinden indirilen model/açılan harici servis için bağlantı gerekir.
- Kullanıcının kamera, mikrofon, belge ve model bağlantısı izinleri bilinçli verilmelidir.
- Gerçek API anahtarları, erişim belirteçleri ve kişisel veriler kaynak koda gömülmemelidir.
- Prompt ve ajan laboratuvarlarındaki taslak araç çağrıları gerçek kurumsal eylem sayılmamalıdır; yetki ve insan onayı olmadan üretim işlemi başlatılmamalıdır.
- Kullanıcının düzenlediği JavaScript/Python kodları için güvenlik yalıtımı, özellikle herkese açık dağıtımda ayrıca değerlendirilmelidir.
- Hukuk, etik, AGI/ASI ve risk içerikleri eğitim amaçlıdır; hukuki görüş, düzenleyici uyum sertifikası veya geleceğe ilişkin kesin tahmin değildir.
- Akademik ve kurumsal kaynakların tarih, lisans ve güncelliği kullanım sırasında ayrıca doğrulanmalıdır.

---

## Kaynaklar ve geliştirme bağlantıları

Evrenlerin kendi içlerinde konuya özgü kaynakça, araştırma, eğitim ve resmî rehber bölümleri bulunur.

Projede karşılaşılan teknolojiler için başlıca geliştirici kaynakları:

- [Pyodide](https://pyodide.org/)
- [TensorFlow.js](https://www.tensorflow.org/js)
- [OpenCV.js](https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html)
- [MediaPipe](https://ai.google.dev/edge/mediapipe)
- [Transformers.js](https://huggingface.co/docs/transformers.js)
- [WebLLM](https://webllm.mlc.ai/)
- [Ollama](https://ollama.com/)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [UNESCO — Recommendation on the Ethics of Artificial Intelligence](https://www.unesco.org/en/artificial-intelligence/recommendation-ethics)

**İlgili AI’Han Academy çalışmalarından ilham alınan mimariler:**

- [Prompt Mimarisi ve Ajan Sistemleri](https://ayhanbzkrt.github.io/PROMPTVEAJANLAR/)
- [Prompt’tan Ajana](https://ayhanbzkrt.github.io/prompttanajana/)

Bu iki proje L’AI’brary ile ilişkili referans çalışmalardır; burada aynı uygulama veya aynı dağıtım olduğu iddia edilmez.

---

## Katkı, lisans ve iletişim

**Katkı alanları:** Erişilebilirlik, tarayıcı uyumluluğu, TR/EN içerik eşleştirmesi, performans, güvenli kod yürütme, gerçek model testleri, laboratuvar kabul testleri, kaynak kontrolü ve pedagojik iyileştirmeler.

Bir hata bildirirken mümkünse **evren adı, ünite, tarayıcı/işletim sistemi, beklenen ve gerçekleşen davranış, konsol hatası ve yeniden üretme adımları** ekle.

Kod katkılarında eski evrenleri, intro/görsel kimliği ve çalışan işlevleri koru; yeni işlevi gerçek veri veya tekrarlanabilir testle göster.

### Telif hakları ve kullanım koşulları

**© 2026 Ayhan Bozkurt. AI’Han Academy — L’AI’brary. TÜM HAKLARI SAKLIDIR.**

L’AI’brary'nin hak sahibine ait özgün **kaynak kodu, arayüz ve yazılım mimarisi, eğitim içerikleri, metinleri, senaryoları, öğrenme evrenleri, izometrik/3B tasarımları, illüstrasyonları, animasyonları, özgün ses ve görsel varlıkları, simülasyonları ve etkileşimli laboratuvar bileşenleri** telif hakkıyla korunur.

**Hak sahibinin önceden verilmiş açık ve yazılı izni olmadan**, projenin tamamı veya hak sahibine ait herhangi bir bölümü:

- Kopyalanamaz, çoğaltılamaz, indirilen kaynak kod üzerinden yeniden yayımlanamaz veya üçüncü kişilere dağıtılamaz.
- Başka bir web sitesi, uygulama, eğitim portalı, yazılım, kitap, çevrim içi kurs veya dijital ürüne aktarılamaz; değiştirilerek ya da uyarlanarak türev çalışma olarak yayımlanamaz.
- Ücretli/ücretsiz bir ticari ürünün, aboneliğin, danışmanlık hizmetinin, eğitim paketinin veya gelir getirici başka bir faaliyetin parçası olarak kullanılamaz; satılamaz, kiralanamaz ya da yeniden lisanslanamaz.
- Özgün görselleri, karakterleri, animasyonları, arayüzü veya öğrenme deneyleri izinsiz kopyalanarak ayrı bir ürün gibi sunulamaz.
- AI’Han Academy, L’AI’brary veya eser sahibinin adı; izinsiz ticari tanıtım, sponsorluk, ortaklık veya resmî onay izlenimi yaratacak biçimde kullanılamaz.

**GitHub deposunun herkese açık olması, kodun okunabilmesi veya bir sitenin tarayıcıda ziyaret edilebilmesi; kaynak kodu kopyalama, değiştirme, yeniden dağıtma veya ticari olarak değerlendirme izni vermez.**

Eser sahibini belirtmek (atıf yapmak) tek başına kullanım izni yerine geçmez.

İzin talepleri, kullanım amacı, kapsamı, süresi ve dağıtım şekli belirtilerek **Ayhan Bozkurt / AI’Han Academy**'ye yazılı olarak iletilmelidir.

Açık bir yazılı izin verilmediği sürece **tüm haklar saklıdır**. Bu depo, proje sahibinin ayrıca ve açıkça belirlediği bir lisans olmadıkça **açık kaynak kullanım lisansı altında yayımlanmış sayılmaz**.

**Üçüncü taraf istisnası:** Projede adı geçen veya kullanılan açık kaynak yazılımlar, kütüphaneler, model ağırlıkları ve üçüncü taraf varlıklar kendi lisansları altında değerlendirilir.

Bu telif bildirimi, üçüncü kişilerin eserleri üzerinde hak iddiası oluşturmaz ve yürürlükteki hukukun tanıdığı zorunlu istisnaları ortadan kaldırmaz.

### Proje sahibi

**Ayhan Bozkurt · AI’Han Academy**

- [GitHub](https://github.com/ayhanbzkrt)
- [Medium](https://medium.com/@ayhanbzkrt)
- [LinkedIn](https://www.linkedin.com/in/ayhanbozkurt/)
- [Kitapyurdu — Ayhan Bozkurt](https://www.kitapyurdu.com/yazar/ayhan-bozkurt/260288.html)

---

*L’AI’brary, tek başına bir sohbet aracı değil; yapay zekâyı anlamak, sorgulamak ve deneyerek öğrenmek için tasarlanmış bir dijital öğrenme evrenidir.*

---

# ENGLISH VERSION

# L’AI’brary — Explore the Fantastic World of Artificial Intelligence

**English | Turkish / English**  
**AI’Han Academy · Ayhan Bozkurt · October 2026**

**© 2026 Ayhan Bozkurt · AI’Han Academy · L’AI’brary. All rights reserved.**

Source code, original design, artwork, animations, and educational content may not be copied, republished, adapted, or used commercially without prior written permission from the rights holder.

Public visibility on GitHub does not grant a license.

> A bilingual, interactive AI learning universe designed to help people **see, explore, code, compare, and understand cause and effect**, rather than merely read definitions.

**L’AI’brary** combines AI literacy with advanced technical topics through original isometric worlds, explained experiments, browser-executed algorithms, and selected open-source tools.

It is designed as a book-and-portal learning ecosystem for curious beginners, students, educators, researchers, and developers.

**An essential distinction:** Some labs perform **real numerical computations** in JavaScript. Others are **educational simulations** explaining the mechanics of larger AI systems. Still others depend on **actual trained model weights, WebGPU, camera permissions, or external services**.

These modes are not interchangeable and are not presented as such.

---

## Contents

1. [Mission](#mission)
2. [Three chapters, 14 universes](#three-chapters-14-universes)
3. [Learning methodology](#learning-methodology)
4. [Examples of interactive labs](#examples-of-interactive-labs)
5. [Technical architecture](#technical-architecture)
6. [Getting started](#getting-started)
7. [Languages, accessibility, and visual design](#languages-accessibility-and-visual-design)
8. [Testing and verification scope](#testing-and-verification-scope)
9. [Security, data, and limitations](#security-data-and-limitations)
10. [Resources and related work](#resources-and-related-work)
11. [Contributing, license, and contact](#contributing-license-and-contact)

---

## Mission

Teaching AI means more than showing a term on screen.

In L’AI’brary, learners begin with an understandable problem, discover what the underlying concept means, and then **change actual inputs, parameters, or code** to observe how the algorithm or workflow responds.

The experience explores questions such as:

- Why do search, recommendation, and classification systems give different answers?
- How do network weights, thresholds, filters, and learning parameters affect an outcome?
- When may an AI agent take an action, and when is human approval required?
- How do computer vision systems detect objects?
- How can a generated claim be grounded in a source?
- How should accuracy, fairness, latency, cost, environmental impact, and safety be evaluated together?

**Teaching principle:** Understand → observe a concrete example → intervene → compute/visualize → explain → try a new situation.

Learning is not reduced to a mandatory quiz, a “mark as learned” button, or superficial completion points.

---

## Three chapters, 14 universes

The atlas contains **14 learning universes across three chapters**.

### I. Entering the AI Universe

| Universe | Main learning experience |
|---|---|
| **Data Academy** | Data literacy, analysis, Python, data preparation, visualization, and experimental thinking. |
| **Search Islands** | Algorithms, search strategies, data structures, and problem-solving. |
| **Machine Learning** | Classification, regression, similarity, decision trees, model behavior, and evaluation. |
| **AI Workshop** | Fundamentals, pixels, words, patterns, and hands-on everyday/library examples. |
| **AI Agents** | Planning, tool use, task execution, permissions, human approval, and agent workflows. |
| **Natural Language Processing** | Text preprocessing, tokenization, retrieval, language patterns, and text analytics. |

### II. Models & Intelligent Systems

| Universe | Main learning experience |
|---|---|
| **Deep Learning** | Neural networks, backpropagation, convolution, Transformers, audio/vision, and numerical models. |
| **MLOps** | Data/model versioning, lifecycle, deployment strategies, error budgets, drift, and monitoring. |
| **Computer Vision** | Pixels, filters, edges, detection, OCR, hand/face/body landmarks, and camera labs. |
| **MCP & Advanced RAG** | Document ingestion, BM25/hybrid retrieval, source passages, protocol concepts, and controlled tool access. |

### III. Humans, Creation & Future

| Universe | Main learning experience |
|---|---|
| **Invisible AI & Autonomous Enterprises** | Inventory, logistics, finance, customer-service workflows, and multi-step decisions. |
| **Hybrid Intelligence & Human–AI Collaboration** | Human–AI task allocation, approvals, correction, calibration, fairness, and co-creation. |
| **Prompt Engineering & Generative AI** | Prompt design, **Context Engineering**, BM25 context selection, JSON validation, agent/testing workflows, and optional real-model comparisons. |
| **AI Risks, Ethics & the Future** | Fairness, alignment, AGI/ASI debates, reliability, copyright, privacy, work, and environmental impact. |

**Scope note:** Detailed curricula and lab counts differ across universes.

Not every interactive model demonstrates full training of a production-scale AI system.

---

## Learning methodology

### Approachable from zero

Technical terms are explained on first use and connected to understandable experiences.

For example:

**kNN:** Deciding from the labels of the most similar examples.

**RAG:** Retrieving relevant documents before producing an answer.

**Human-in-the-loop (HITL):** Allowing meaningful human intervention at critical steps.

Lessons relate these ideas to library catalogs, circulation analysis, reports, document processing, or everyday decisions.

### The learning loop

1. **See:** Observe the real-world problem and its initial input.
2. **Understand:** Learn what the concept does and which assumptions it makes.
3. **Change:** Edit data, documents, thresholds, images, tasks, or code.
4. **Compute:** Observe recalculated metrics, visualizations, or actual tool execution.
5. **Compare:** Examine how outputs differ and why the technique can fail.

The objective is not to click as many controls as possible.

It is to understand **why an altered input produced an altered result**.

---

## Examples of interactive labs

- **Data and Python:** Editable Python code through Pyodide when the browser runtime can be loaded.
- **Machine and Deep Learning:** Numerical experiments in which changing a threshold, feature, learning parameter, or filter changes computed outputs.
- **MLOps:** Canary traffic allocation, error-budget calculations, and drift measurements.
- **Document Retrieval:** Loading supported local document types and retrieving source passages with BM25.
- **Computer Vision:** Actual Canvas pixel/filter operations; optional TensorFlow.js, OpenCV.js, OCR, and MediaPipe models on supported devices.
- **Hybrid Intelligence:** Reassigning tasks between humans and AI, rejecting approvals, and calculating error, calibration, and fairness metrics.
- **Prompt and Context Engineering:** Prompt composition, context assembly, JSON Schema validation, controlled agent steps, and comparing two real models when available.
- **Risks and Ethics:** Group-level TPR/FPR, selection-rate differences, market concentration (HHI), and energy computations using power × time.

The experience distinguishes **synthetic examples**, **algorithmic educational simulations**, and **actual trained-model inference**.

A disconnected or unsupported model is never treated as having generated an answer.

---

## Technical architecture

### Single-file distribution

The core release is one **HTML file with embedded CSS, JavaScript, curriculum data, and visual assets**.

It includes the intro, the bilingual atlas, and the learning modules.

No npm/Node build process is required to open the core atlas.

```text
L’AI’brary
├── Intro animation (TR / EN)
├── Isometric atlas (14 universes)
│   ├── Chapter I: Foundations (6)
│   ├── Chapter II: Models (4)
│   └── Chapter III: Humans and future (4)
├── Explained learning scenes and experiment engines
├── Local JavaScript / Canvas / SVG computation
├── Optional Python (Pyodide) and browser AI models
└── Optional local model server (Ollama) in selected labs
```

### Technology families

| Layer | Tools and approach | Runtime considerations |
|---|---|---|
| User interface | HTML5, CSS, JavaScript, SVG, Canvas, animation | Included in the main file |
| Local computations | JavaScript, statistics, algorithms, retrieval | Local in many labs |
| Python | Pyodide / WebAssembly | First-load download and memory requirements |
| NLP / LLM | Transformers.js, WebLLM, WebGPU/WASM | Compatible model, device, and downloads required |
| Vision / camera | TensorFlow.js, OpenCV.js, MediaPipe, Tesseract.js | External model packages, permissions, HTTPS/localhost |
| Audio / timelines | Web Speech API and local timeline calculations | Browser-dependent |
| Local model server | Ollama | Separate installation, models, and network permissions |

**Important:** This table does not promise that all dependencies work unconditionally in every lab or browser.

Versions, licenses, WebGPU capability, access, and model compatibility require verification.

GitHub Pages is a static host; it does not run a GPU backend, Ollama, or Python service for you.

---

## Getting started

### 1. Obtain the HTML

Place the final integrated file in the repository:

```text
LAIbrary_Final_Senior_QA_2026.html
README.md
```

Some core content can be opened by double-clicking the file.

**For camera features, model downloads, and stricter browser security features, use `localhost` or HTTPS instead.**

### 2. Run a local HTTP server (recommended)

From the folder containing the HTML:

```bash
python3 -m http.server 8765
```

Open:

```text
http://localhost:8765/LAIbrary_Final_Senior_QA_2026.html
```

A current Chrome/Edge browser is a practical starting point.

Check WebGPU, hardware, and media-device permissions when using model-intensive labs.

### 3. Publish with GitHub Pages

1. Create a repository or add the release to an existing one.
2. Publish the final HTML as **`index.html`** in the repository root.
3. Open **Settings → Pages → Build and deployment → Deploy from a branch**.
4. Select the intended branch and the **`/(root)`** folder.
5. After deployment, verify atlas navigation, the intro, language switching, and lab behavior on the actual HTTPS site.

> GitHub Pages is **static hosting**. Real Ollama connections, external APIs, model downloads, and secrets require appropriate separate infrastructure. Never embed private API keys in the HTML or repository.

### 4. Optional trained-model features

**WebLLM:** On a compatible WebGPU device, select a supported model and wait for the model download and initialization.

The first load may be substantial; memory or GPU incompatibilities can prevent inference.

**Ollama:** Install Ollama and the models you intend to use, then start and check the local service.

Select the available model names and allowed local endpoint within the corresponding lab.

Browser CORS and security settings depend on your environment. Avoid exposing unauthenticated endpoints publicly.

**Camera/OCR:** Grant permission only to the relevant lab. Model files may require a first-use download.

Browser developer tools can help diagnose blocked permissions or network errors.

---

## Languages, accessibility, and visual design

- Turkish and English atlas/UI support, including language switching in the intro.
- English intro controls: **“Skip Intro”** and **“Enter the Universe”**; Turkish: **“Geç”** and **“Evrene Gir”**.
- A light/pastel visual identity, original isometric islands, and topic-specific experimental visuals.
- Responsive layouts and localized scrolling for some wide diagrams.
- Full keyboard, screen-reader, and cross-browser accessibility conformance remains an area for further testing; complete WCAG compliance is **not claimed**.

**Design principle:** The target experience is not a pile of generic cards or dashboards, a static prototype, or a “Start” button revealing a canned answer.

The learning scene itself should respond to meaningful user input.

---

## Testing and verification scope

The **Senior QA report dated October 23, 2026** records:

| Check | Reported result |
|---|---|
| Universe navigation | **14/14** atlas clicks opened their modules |
| NLP numeric exercises | **36/36** module calls produced nonempty output |
| ML, MLOps, MCP/RAG, Invisible AI, Hybrid AI, Risks/Ethics | **216** unit entries with two-condition numerical checks |
| Prompt local labs | **6** primary labs produced changing outputs |
| Mobile | Selected universes checked at **390 px** viewport width |
| Intro | Language switching and entry flow checked |

**These results are not a production certification.**

End-to-end tests have *not* been completed for every physical camera, COCO/MediaPipe model, WebGPU device, two actual Ollama models, external model package, interactive control, or every curriculum A/B acceptance criterion.

---

## Security, data, and limitations

- Many educational datasets are explicitly **synthetic**; they should not be mistaken for institutional records or independently measured research data.
- Browser-side numerical computation is different from actual model inference. A downloaded model or external service may require network access.
- Camera, microphone, document, and model-service permissions should be granted deliberately.
- Never embed private user data, API keys, or authentication tokens in the page source.
- A proposed agent tool call is not a completed real-world action. Meaningful permission boundaries and human approval are required for production integrations.
- Execution isolation for user-authored JavaScript/Python must be reviewed before exposing such labs in a public, multi-user production setting.
- Legal, ethical, AGI/ASI, and future-risk lessons are educational material—not legal advice, regulatory certification, or certain forecasts.
- Verify source currency, licensing, and organizational policies whenever reusing course material.

---

## Resources and related work

Individual universes contain topic-specific references, research links, learning materials, and official guides.

Developer resources relevant to the portal include:

- [Pyodide](https://pyodide.org/)
- [TensorFlow.js](https://www.tensorflow.org/js)
- [OpenCV.js](https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html)
- [MediaPipe](https://ai.google.dev/edge/mediapipe)
- [Transformers.js](https://huggingface.co/docs/transformers.js)
- [WebLLM](https://webllm.mlc.ai/)
- [Ollama](https://ollama.com/)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [UNESCO — Recommendation on the Ethics of Artificial Intelligence](https://www.unesco.org/en/artificial-intelligence/recommendation-ethics)

**Related AI’Han Academy architecture references:**

- [Prompt Architecture & Agent Systems](https://ayhanbzkrt.github.io/PROMPTVEAJANLAR/)
- [From Prompt to Agent](https://ayhanbzkrt.github.io/prompttanajana/)

These are related reference projects, not claims that the sites are identical or share the same deployment.

---

## Contributing, license, and contact

**Contributions are especially useful for:** accessibility, browser compatibility, TR/EN consistency, performance, secure code execution, trained-model testing, lab acceptance tests, source verification, and instructional clarity.

A useful bug report includes the **universe, unit, browser/OS, expected versus actual result, console error, and reproduction steps**.

Contributions should preserve existing modules, intro behavior, visual identity, and working interactions; newly introduced behavior should be verified with reproducible tests.

### Copyright and permitted use

**© 2026 Ayhan Bozkurt. AI’Han Academy — L’AI’brary. ALL RIGHTS RESERVED.**

The original **source code, interface and software architecture, instructional content, text, educational scenarios, learning universes, isometric/3D designs, illustrations, animations, original audio and visual assets, simulations, and interactive laboratory components** belonging to the rights holder are protected by copyright.

**Without the rights holder's prior express written permission**, neither the entire project nor any rights-holder-owned part of it may be:

- Copied, reproduced, republished from downloaded source code, or redistributed to third parties.
- Incorporated into another website, app, learning platform, software product, book, online course, or digital product; modified or adapted into a published derivative work.
- Used, sold, rented, or sublicensed as part of a commercial product, subscription, consulting service, paid training package, or other revenue-generating activity.
- Presented as a separate product by copying original artwork, characters, animations, interface elements, or interactive learning experiences.
- Used in advertising or promotion in a manner implying unauthorized endorsement, sponsorship, affiliation, or approval by AI’Han Academy, L’AI’brary, or the author.

**A publicly visible GitHub repository, publicly readable source code, or a browser-accessible website does not grant permission to copy, modify, redistribute, or commercially exploit the project.**

Attribution alone does not constitute permission.

For licensing or permission requests, contact **Ayhan Bozkurt / AI’Han Academy** in writing and specify the purpose, scope, duration, and form of distribution.

Unless explicit written permission is granted, **all rights remain reserved**.

This repository is **not offered under an open-source license** unless the rights holder expressly specifies otherwise.

**Third-party materials:** Open-source dependencies, model weights, and other third-party assets remain governed by their respective licenses.

This notice does not claim ownership of third-party works or override mandatory exceptions under applicable law.

### Project owner

**Ayhan Bozkurt · AI’Han Academy**

- [GitHub](https://github.com/ayhanbzkrt)
- [Medium](https://medium.com/@ayhanbzkrt)
- [LinkedIn](https://www.linkedin.com/in/ayhanbozkurt/)
- [Kitapyurdu — Ayhan Bozkurt](https://www.kitapyurdu.com/yazar/ayhan-bozkurt/260288.html)

---

*L’AI’brary is more than a chatbot: it is a digital learning universe for understanding, questioning, and experimenting with artificial intelligence.*

---

**AI’Han Academy · Ayhan Bozkurt · 2026**

**© All Rights Reserved / Tüm Hakları Saklıdır.**
