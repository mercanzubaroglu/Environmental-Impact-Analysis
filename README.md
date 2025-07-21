# 🌱 Çevresel Etki Analizi / Environmental Impact Analysis

📂 **Veri seti bağlantısı / Dataset link**:  
🔗 [https://www.kaggle.com/datasets/khushikyad001/global-environmental-impact](https://www.kaggle.com/datasets/khushikyad001/global-environmental-impact)

- Çevresel sensör verilerini (örneğin sıcaklık, nem, ışınım vs.) içeren yapısal veri setidir.
- A structured data set containing environmental sensor data (e.g. temperature, humidity, radiation, etc.).
--- 

Bu proje, çevresel veriler üzerinde çeşitli veri bilimi ve makine öğrenmesi tekniklerini uygulayarak sürdürülebilirlik ve çevresel farkındalık oluşturmayı hedeflemektedir. Proje sürecinde eksik veri analizi, boyut indirgeme (PCA), kümeleme (KMeans), anomali tespiti (Isolation Forest) ve regresyon modellemesi (Random Forest) gibi yöntemlerle çevresel değişkenler incelenmiştir. Görselleştirme teknikleriyle bu analizlerin sonuçları desteklenmiş ve yorumlanabilir hale getirilmiştir.

This project aims to generate insights on sustainability and environmental awareness by applying various data science and machine learning techniques to environmental data. The workflow includes missing data imputation, dimensionality reduction (PCA), clustering (KMeans), anomaly detection (Isolation Forest), and regression modeling (Random Forest). The results are supported and visualized through a variety of effective plots.

---

### 🎯 Proje Amacı / Project Objective

Projenin temel amacı, çevresel değişkenlerin (örneğin sıcaklık, hava kalitesi, nem, CO₂ emisyonu gibi) analiziyle bu değişkenlerin çevre üzerindeki etkilerini anlamak ve modellemektir. Bu kapsamda:

- Verinin eksikliklerini gidermek,
- Boyutsal karmaşıklığı azaltmak,
- Verileri kümeleyerek benzer çevresel koşulları tespit etmek,
- Aykırı çevresel davranışları tanımlamak,
- Tahminsel modeller ile belirli çevresel çıktıları öngörmek

amaçlanmıştır.

The main goal is to understand and model the impact of environmental variables (e.g., temperature, air quality, humidity, CO₂ emissions). To achieve this, the project aims to:

- Handle missing values,
- Reduce dimensional complexity,
- Detect environmental clusters with similar characteristics,
- Identify anomalous patterns,
- Predict environmental outcomes using regression models.

---

### 🧠 Kullanılan Yöntemler / Applied Methods

#### 🔧 1. Eksik Veri Analizi / Missing Data Handling
- `SimpleImputer(strategy="mean")` kullanılarak eksik değerler ortalama ile doldurulmuştur.
- Bu adım veri tutarlılığı sağlamak ve modele hatalı girişleri engellemek için gereklidir.

#### ⚖️ 2. Verilerin Ölçeklenmesi / Data Scaling
- `StandardScaler()` ile veriler standart normal dağılıma (μ=0, σ=1) getirilmiştir.
- Özellikle PCA ve KMeans algoritmaları için bu adım hayati önem taşır.

#### 📉 3. Boyut İndirgeme / Dimensionality Reduction - PCA
- `Principal Component Analysis` (PCA) yöntemiyle çok boyutlu veriler iki bileşene indirgenmiştir.
- Bu hem görselleştirme kolaylığı hem de işlem yükünü azaltma açısından faydalıdır.

#### 🧩 4. Kümeleme / Clustering - KMeans
- `KMeans(n_clusters=3)` algoritması ile veriler benzerliklerine göre gruplandırılmıştır.
- Elde edilen kümeler, çevresel koşullara göre farklı bölgelerin/olayların temsilcisi olabilir.

#### 🚨 5. Anomali Tespiti / Anomaly Detection - Isolation Forest
- `Isolation Forest` algoritması kullanılarak çevresel uç değerler belirlenmiştir.
- Bu değerler veri bütünlüğünü tehdit eden ölçüm hataları ya da olağandışı olaylar olabilir.

#### 🌲 6. Regresyon Modeli / Regression - Random Forest
- `RandomForestRegressor` kullanılarak çevresel değişkenler ile hedef değişkenler (örneğin belirli bir emisyon seviyesi) tahmin edilmiştir.
- Bu model, değişkenlerin çevre üzerindeki etkilerini sayısal olarak ifade etmeye yardımcı olur.

---

### 📊 Görselleştirmeler / Visualizations

#### 🔸 Korelasyon Matrisi / Correlation Heatmap
- Özellikler arası ilişkiler görselleştirilmiştir.
- IRRADIATION ve bazı sıcaklık değişkenleri arasında güçlü pozitif korelasyon gözlemlenmiştir.

#### 🔸 PCA Bileşen Dağılımı / PCA Scatter Plot
- Boyut indirgeme sonrası örnekler 2D düzlemde gösterilmiştir.
- Küme yapıları bu grafikte net bir şekilde görülebilir.

#### 🔸 Kümelerin Görselleştirilmesi / KMeans Clusters
- Farklı kümeler farklı renklerle gösterilerek veri segmentasyonu analiz edilmiştir.

#### 🔸 Anomali Noktaları / Anomaly Points
- Isolation Forest sonucu aykırı noktalar kırmızı ile işaretlenmiştir.

#### 🔸 Özellik Önem Grafiği / Feature Importance Barplot
- Random Forest modeline göre en etkili çevresel değişkenler sıralanmıştır.

---

