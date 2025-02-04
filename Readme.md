# Kredi Başvurusu Onay Tahmini Projesi

Bu projenin amacı, bir kredi başvurusunun onaylanıp onaylanmamasını tahmin etmek için bir makine öğrenimi modeli geliştirmektir. Proje, başvuranların çeşitli demografik ve finansal özelliklerini içeren bir veri setini kullanarak, bu özellikleri sayısal değerlere dönüştürmeyi, eksik verileri işlemeyi ve sonrasında bir makine öğrenimi modeli oluşturmayı içermektedir.

## 1. Veri İnceleme ve Temizleme

- İlk olarak, gerekli kütüphaneler içe aktarılır.
- Eğitim ve test veri setleri okunur, orijinal kopyalar alınır.
- Veri setinin sütunları, veri tipleri incelenir ve eksik veriler kontrol edilir.
- Bazı sütunlar sayısal değerlere dönüştürülerek veri seti temizlenir.

## 2. Veri Görselleştirme

Eğitim düzeyine, cinsiyete, medeni duruma, çocuk sayısına, patronluğa ve mülkiyet bölgesine göre başvuranların sayısı görselleştirilir.

## 3. Eksik Veri İşleme

- Seçilen sütunlardaki eksik değerler kontrol edilir.
- Eksik değerler ısı haritasıyla görselleştirilir.
- Eksik değerler belirli bir stratejiye göre doldurulur.

## 4. Veri Mühendisliği

- "Dependents" sütunu ayrı ikili sütunlara dönüştürülür.
- "Property_Area" sütunu kategorik değerlerden sayısal değerlere dönüştürülür.

## 5. Model Geliştirme

- Veri seti eğitim ve test setlerine ayrılır.
- Logistic Regression modeli kullanılarak başlangıç bir model oluşturulur.
- Modelin performansı değerlendirilir ve sonuçlar görselleştirilir.
- Logistic Regression modeli çeşitli hiperparametrelerle çapraz doğrulama yaparak ayarlanır.
- En iyi performans gösteren modelin sonuçları görselleştirilir.

## 6. Tahmin Yapma

- Kredi başvurusu için örnek bir veri oluşturulur.
- Oluşturulan model kullanılarak kredi başvurusunun onaylanıp onaylanmaması tahmin edilir.
- Tahmin sonucu ekrana yazdırılır.

## 7. Model Eğitimi

Öncelikle gerekli kütüphaneler yükleniyor, ardından veriyi eğitim ve test verisi olarak ayırıyoruz. Model olarak **Lojistik Regresyon** modeli seçiliyor. Modelin tahminleri ile gerçek etiketler arasındaki doğruluk ve F1 skoru hesaplanıyor.

### Hiperparametre Optimizasyonu Sonrası Model Skorları

İlk modelin doğruluk skoru (0.788177) ve F1 skoru (0.762562) gözlemleniyor. Belirli bir hiperparametre ayarı kullanarak doğruluk skoru ve F1 skoru artırılabiliyor.

### Çapraz Doğrulama

- **LogisticRegression** modelini `liblinear` çözücüsü ile oluşturur.
- Çapraz doğrulama (cross-validation) kullanılarak modelin performansı daha iyi değerlendirilir.

## 8. Tahmin Sonuçları

Model eğitildikten sonra, bir örnek veri seti oluşturulup model tahmin değerleri alınır. Veri setindeki sütunlar eğitimde kullanılan sütun isimleriyle aynı isim ve sırada olmalıdır.



## Kullanılan Kütüphaneler

- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-Learn**
