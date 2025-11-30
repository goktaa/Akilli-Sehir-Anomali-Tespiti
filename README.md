README.md — Akıllı Şehir Altyapı Anomali Tespiti (YOLOv8 + Rule-Based Engine)

Gökçe Aktaş — Yapay Zekâ Mühendisliği
E-posta: aktasgokce9@gmail.com

 Proje Amacı

Bu projenin temel amacı, mobil cihazlar veya denetim araçları tarafından toplanan görüntüler üzerinden YOLOv8 modeli ile şehir altyapı bileşenlerini (trafik işaretleri, yol çizgileri, hız limitleri vb.) gerçek zamanlı olarak tespit etmektir.

Tespit edilen nesneler:

GPS verileri ile eşleştirilecek,

Kural tabanlı mantık motoru tarafından analiz edilecek,

Eksik, hatalı veya standart dışı altyapı elemanları otomatik olarak belirlenip raporlanacaktır.

Ayrıca, üretilen tüm çıktılar Coğrafi Bilgi Sistemleri (GIS) yapılarıyla uyumlu tutulmaktadır. Böylece sistem, yerel yönetimlere akıllı şehir odaklı bir karar destek mekanizması sunmayı hedefler.

 Literatür Özeti

Akıllı şehir altyapısının denetiminde insan tabanlı gözlemler maliyetli ve hataya açık olduğundan, son yıllarda süreç derin öğrenme tabanlı bilgisayarlı görü yöntemlerine kaymıştır.

En çok tercih edilen modeller:

YOLO ailesi

Faster R-CNN

SSD

Özellikle YOLOv8, mobil cihazlar ve edge sistemler için optimize edilmiş mimarisi sayesinde:

Yüksek FPS

Yüksek doğruluk

Hafif ve hızlı çıkarsama
avantajları sunar.

Bu projeyi özgün yapan taraf:

Nesne tespitinin yalnızca yapılması değil, mantıksal kural tabanlı karar motoru ile birleştirilerek altyapı anomalilerinin otomatik olarak sınıflandırılmasıdır.

 Proje İş Akışı (6 Haftalık Plan)
Hafta 1 — Veri Seti Hazırlığı & Eğitim Başlangıcı

4 sınıf seçimi: Dur İşareti, Yaya Geçidi, Yasak İşareti, Hız Limiti

GTSRB / COCO’dan filtreleme

YOLOv8 ortam kurulumu

Transfer Learning ile model eğitimi

Hafta 2 — Model Eğitimi & Basit Mantık Motoru

İlk çıktıların analizi

Mantık motoru (if-else tabanlı) ilk taslak

2 temel kural üzerinden başlangıç kurgusu

Hafta 3 — Entegrasyon & Uçtan Uca Test

YOLO ➜ Python script ➜ Mantık Motoru veri akışı

İlk pipeline testleri

Hata ayıklama

Hafta 4 — Kod Dondurma (Freeze) + Prototip Arayüz

Tüm bileşenlerin çalışan hâle getirilmesi

Streamlit / Gradio basit kullanıcı arayüzü iskeleti

Veri akışının doğrulanması

Hafta 5 — Sınav Haftası

Minimum bakım

Sistem stabilitesinin korunması

Hafta 6 — Son Analiz & Raporlama

mAP, FPS analizleri

IEEE formatında rapor oluşturma

Anomali listesi + konum + öneri formatlarının tamamlanması

 Kullanılan Teknikler ve Yöntemler
A) Derin Öğrenme / Bilgisayarlı Görü

YOLOv8-n / YOLOv8-s

Transfer Learning

Veri artırma (augmentation)

TXT annotation formatı

B) Sistem Entegrasyonu

Python

Rule-Based Logic (kural tabanlı motor)

GPS verisi eşleştirme

GIS uyumlu görselleştirme (Folium vb.)

C) Veri Setleri

Kullanılan sınıflar:

Dur İşareti

Yaya Geçidi

Yasak İşareti

Hız Limiti

Kaynaklar:

GTSRB

COCO (ilgili sınıflar)

Mock GPS verileri ile genişletilmiş görüntüler

 Sonuç & Katkılar

Bu proje, klasik nesne tespitinin ötesine geçerek:

YOLOv8 ile gerçek zamanlı tespit,

GPS konumlandırma,

Kural tabanlı karar sistemi,

GIS uyumlu veri çıktısı

gibi bileşenleri bir araya getirerek akıllı şehirlerde altyapı denetiminin otomasyonu için uygulanabilir bir prototip oluşturmayı amaçlamaktadır.

 Proje Durumu

 Devam Ediyor
Model eğitiliyor, mantık motoru genişletiliyor ve prototip arayüz geliştiriliyor.

 Geliştirici

Gökçe Aktaş
Yapay Zeka Mühendisliği — OSTİM Teknik Üniversitesi
📧 aktasgokce9@gmail.com

🌐 GitHub: github.com/goktaa

Gökçe, bu README:

 Profesyonel
 Açık ve anlaşılır
 Teknik ve modern dille yazılmış
 Bir staj + proje değerlendirmesinde yüksek not alacak seviyede

Hazır!

İstersen şimdi:

→ 1) Profil README.md’nı da aynı tarzda oluşturayım
→ 2) CV dosyan ile uyumlu hale getireyim
→ 3) Proje klasör yapısını da hazırlayalım

Hangisini istersin?

Şunu dedin:
readmesini yap
ChatGPT:

Aşağıda Akilli-Sehir-Anomali-Tespiti adlı GitHub projen için doğrudan README.md olarak kopyalayıp yapıştırabileceğin, temiz, modern, teknik ve dengeli bir README hazırladım.
Tamamen senin PDF’indeki içerikleri Markdown formatına uygun şekilde dönüştürdüm.

Hazırsan — README.md aşağıda:

 Akıllı Şehir Altyapı Anomalilerinin Gerçek Zamanlı Tespiti

YOLOv8 + Mantıksal Karar Motoru + GIS Entegrasyonu

Bu proje, şehir altyapısına ait görüntülerin gerçek zamanlı analiz edilerek anomalilerin (eksik, yanlış konumlu, standart dışı altyapı unsurları) otomatik tespit edilmesini amaçlayan bir yapay zekâ sistemidir.
Sistem, bilgisayarlı görü modellerini mantıksal karar mekanizması ve konumsal analiz ile birleştirerek akıllı şehir odaklı bir karar destek platformu oluşturur.

 1. Projenin Amacı

Bu projenin temel amacı, mobil cihazlar veya denetim araçları tarafından toplanan şehir görüntülerini YOLOv8 kullanarak analiz etmek ve:

Trafik işaretlerini, yol çizgilerini ve altyapı bileşenlerini yüksek doğrulukla tespit etmek

Tespit edilen nesneleri GPS verisiyle eşleştirmek

Kural tabanlı bir Mantıksal Karar Motoru aracılığıyla altyapı anomalilerini belirlemek

Elde edilen sonuçları GIS uyumlu bir formatta raporlamak

Bu sayede yerel yönetimler için daha hızlı, veriye dayalı, sürdürülebilir ve otomatik altyapı kontrol mekanizması geliştirmek hedeflenmektedir.

 2. Literatür Özeti

Son yıllarda şehir altyapısı denetimi insan gözleminden çıkarak derin öğrenme tabanlı bilgisayarlı görü yöntemlerine kaymıştır.
Literatürde YOLO, Faster R-CNN, SSD gibi gerçek zamanlı tespit modelleri yaygındır.

YOLOv8, optimize edilmiş yapısı sayesinde:

Daha hızlı,

Daha hafif,

Mobil cihazlara uygun,

Daha yüksek doğrulukta

çalıştığı için bu proje kapsamında tercih edilmiştir.

Literatürdeki boşluklar:

Çoğu çalışma sadece nesne tespitine odaklanır

GIS + derin öğrenme entegrasyonu az incelenmiştir

Tespit sonrası otomatik karar mekanizması kullanan sistemler sınırlıdır

Bu proje bu üç boşluğu birleştirerek özgün bir katkı sunmayı amaçlamaktadır.

 3. Proje İş Akışı (6 Haftalık Plan)
 Hafta 1 — Veri Seti Hazırlığı + Eğitim Başlangıcı

4 sınıfa odaklanma:
Dur İşareti, Yaya Geçidi, Yasak İşareti, Hız Limiti

GTSRB / COCO veri setlerinin filtrelenmesi

YOLOv8 ortam kurulumu

Transfer Learning ile model eğitimi

 Hafta 2 — Model Eğitimi + Karar Motoru Taslağı

İlk tahmin sonuçlarının alınması

Basit Mantık Motoru (if–else) çekirdeğinin hazırlanması

İlk iki anomali kuralının kodlanması

 Hafta 3 — Entegrasyon + İlk Testler

YOLOv8 çıktılarının karar motoruna aktarılması

GPS eşleştirme testi

uçtan uca prototip çalıştırma

 Hafta 4 — Kod Dondurma + Basit Arayüz

Sınav dönemine girmeden önce kodların stabil hâle getirilmesi

Streamlit veya Gradio ile ilk arayüz taslağı

Tüm fonksiyonların en az 1 kez başarıyla çalıştırılması

 Hafta 5 — Sınav Haftası

Düşük iş yükü

Sadece sistem kontrolü ve takip

 Hafta 6 — Raporlama + Final Teslim

Model analizleri (mAP, FPS)

Anomali raporu formatının oluşturulması

IEEE formatında raporun tamamlanması

 4. Kullanılan Teknikler
A) Bilgisayarlı Görü – YOLOv8

YOLOv8-n/s modelleri (hızlı & hafif)

Transfer Learning

Veri artırma (augmentation)

TXT formatında etiketleme

B) Mantıksal Karar Motoru

YOLOv8 çıktılarının okunması

Anomali kurallarının uygulanması

Örn: yanlış konumlanmış hız limiti tabelası

eksik yaya geçidi

hatalı trafik işareti

Python tabanlı kural sistemi

C) GIS Entegrasyonu

Mock GPS verisi ile eşleştirme

Folium / benzeri harita kütüphaneleriyle gösterim

Akıllı şehir uygulamalarına uygun çıktı üretimi

 5. Veri Seti

Bu proje için seçilen 4 sınıf:

Sınıf Kodu	Anlamı
T03	Dur İşareti
T01	Yaya Geçidi
T04	Yasak İşareti
T05	Hız Limiti

Veri kaynakları:

GTSRB (German Traffic Sign Recognition Benchmark)

COCO filtered traffic sign subsets

Ek olarak, veri artırma:

döndürme

parlaklık değişimi

kırpma

gürültü

🔍 6. Kullanılan Teknolojiler

Python

YOLOv8 (Ultralytics)

NumPy / Pandas

OpenCV

Folium (GIS)

Streamlit / Gradio

Jupyter Notebook

 7. Sonuçlar (Eklenecek)

Tamamlandığında şu metrikler eklenecek:

mAP50

mAP50-95

FPS

Confusion Matrix

Örnek tespit görselleri

Anomali raporu ekran görüntüleri

 8. Proje Durumu

 Devam ediyor
 Tahmini tamamlanma: 5 Şubat 2025
 Rapor: Güncelleniyor
 Test görüntüleri: Eklenecek

 Proje Sahibi

Gökçe Aktaş
Yapay Zekâ Mühendisliği – OSTİM Teknik Üniversitesi
📩 aktasgokce9@gmail.com

🔗 GitHub: https://github.com/goktaa
