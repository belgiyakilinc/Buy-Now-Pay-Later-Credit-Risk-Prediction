# Buy Now Pay Later (BNPL) Credit Risk Prediction / Şimdi Al Sonra Öde Kredi Riski Tahmini


### Genel Bakış
Bu proje, "Şimdi Al Sonra Öde" (Buy Now, Pay Later - BNPL) sistemi için kredi riski ve temerrüt (default) olasılığını tahmin etmeyi amaçlamaktadır. Temel hedef, potansiyel riskleri doğru belirleyen güçlü bir makine öğrenmesi modeli kurmak ve işletme karlılığını en üst düzeye çıkaran **optimal karar eşiğini (threshold)** bulmak için maliyet-fayda analizi yapmaktır.

### Öne Çıkan Özellikler
* **Keşifçi Veri Analizi (EDA):** Veri dağılımlarını anlamak için `ydata-profiling`, KDE/Kutu grafikleri ve kategorik verilerdeki doğrusal olmayan ilişkileri yakalamak için **Phik (φk) korelasyon analizi** kullanılmıştır.
* **Veri Ön İşleme:** Kategorik değişkenler One-Hot ve Label Encoding ile dönüştürülmüştür. Sınıf dengesizliği (class imbalance) problemi `scale_pos_weight` kullanılarak yönetilmiştir.
* **Makine Öğrenmesi (Ensemble Model):** **XGBoost, LightGBM ve Lojistik Regresyon** algoritmalarının güçlü yönlerini birleştiren **Soft Voting** topluluk modeli geliştirilmiştir.
* **İş ve Kar Odaklı Optimizasyon:** Model başarısı sadece AUC-ROC veya F1-skoru gibi metriklerle ölçülmemiş; yanlış pozitif/negatif tahminlerin finansal maliyeti hesaplanmıştır. Net karı maksimize eden en uygun eşik değeri bulunarak baz senaryoya (baseline) göre ciddi kar artışı sağlanmıştır.


---

### Overview
This project focuses on predicting credit risk and default probability for a Buy Now, Pay Later (BNPL) dataset. The primary goal is to build a robust machine learning model that accurately identifies potential defaults and to perform a custom cost-benefit analysis to find the optimal decision threshold that maximizes business profitability.

### Key Features
* **Exploratory Data Analysis (EDA):** Detailed visual and statistical analysis including `ydata-profiling`, distribution plots (KDE, Boxplots), and **Phik (φk) correlation matrices** to capture non-linear relationships in mixed data types.
* **Data Preprocessing:** Handled categorical variables using One-Hot and Label Encoding. Addressed class imbalance using `scale_pos_weight` and stratified splitting.
* **Machine Learning Ensemble:** Built a robust **Soft Voting Classifier** combining the strengths of **XGBoost, LightGBM, and Logistic Regression**.
* **Business-Driven Optimization:** Moved beyond standard ML metrics (AUC-ROC, PR-AUC) by calculating the actual financial impact. Implemented a cost-benefit matrix to determine the optimal probability threshold, significantly outperforming the baseline profit.

### Technologies Used
* **Python** (Pandas, NumPy)
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn, XGBoost, LightGBM
* **Analysis:** Phik, YData-Profiling





### Kullanılan Teknolojiler
* **Python** (Pandas, NumPy)
* **Veri Görselleştirme:** Matplotlib, Seaborn
* **Makine Öğrenmesi:** Scikit-Learn, XGBoost, LightGBM
* **Analiz:** Phik, YData-Profiling
