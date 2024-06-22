## Global AI Yapay Zeka Bootcamp Project
## Makine Öğrenimi ve Derin Öğrenme Modelleri Eğitimi ve Değerlendirilmesi
# 1. Giriş	
Bu proje, Fashion MNIST veri setindeki giysi görüntülerini sınıflandırmak için çeşitli makine öğrenimi ve derin öğrenme modellerinin eğitimini ve değerlendirilmesini amaçlamaktadır. Hedef, en iyi performansı elde eden modeli belirlemektir.

# 2. Veri Seti ve Ön İşleme
Kullanılan Veri Seti:  
Fashion MNIST Veri Seti:  
•	28x28 piksel boyutunda gri tonlamalı giysi görüntüleri  
•	10 farklı giysi sınıfı  
o	Eşofman altı  
o	Sweatshirt  
o	Elbise  
o	Ceket  
o	Sandalet  
o	Çanta   
o	Bot  
o	Sneaker  
o	Gömlek  
•	Veri seti ikiye ayrılmıştır: eğitim seti ve test seti. Eğitim seti, modeli eğitmek için kullanılırken, test seti modelin performansını değerlendirmek için kullanılır
•	Eğitim için 60,000 ve test için 10,000 örnek  

Veri Yükleme ve İnceleme:  
Veri seti, Keras kütüphanesi kullanılarak yüklenmiştir. Aşağıda örnek veri görselleştirilmesi yer almaktadır:  
  
Ön İşleme Adımları:  
•	Bu projede, aşağıdaki veri ön işleme adımları uygulandı:   
–	Verilerin bölünmesi: Veriler X_train, y_train, X_test ve y_test olarak bölündü.  
–	Eğitim kümesi 60.000, test kümesi ise 10.000 görüntüden oluşmaktadır.  
–	Veri boyutları: Veri boyutları yazdırıldı.
–	Görüntü boyutları: Görüntü boyutları yazdırıldı.
–	Sampling: Veri seti büyük olduğu için makine öğrenimi metotlarının eğitim süresi ve optimizasyon kısmı uzun sürdüğü için eğitim için 1000 test için 250 görüntü ile çalışıldı
–	Görselleştirme: 10 rastgele görüntü görselleştirildi.
–	Normalleştirme:  Görüntüler  0 ve 1 arasındaki değerlere ölçeklendirilerek normalize edildi.
–	Yeniden şekillendirme

# 3. Model Oluşturma
Kullanılan Modeller:
Bu projede, farklı makine öğrenmesi algoritmaları kullanarak modeller eğitilmiştir.
•	K-Nearest Neighbors (KNN)
•	Destek Vektör Makineleri (SVM)
•	Lojistik Regresyon
•	Karar Ağacı
•	Rastgele Orman(RF)
•	Gradient Boosting Machines (GBM)
•	LightGBM
•	XGBoost
•	CatBoost
Derin öğrenme algoritmaları da uygulanmıştır.
•	Yapay Sinir Ağları (ANN)
•	Evrişimli Sinir Ağları (CNN)

# 4. Model Eğitimi
Eğitim Süreci:
•	Bazı makine öğrenimi algoritmaları için hiperparametreler optimize edildi.(RF,LightGBM,XGBoost)
•	Model eğitim kümesi üzerinde eğitildi.
•	Modelin doğruluğu test kümesi üzerinde değerlendirildi.
•	ANN ve CNN de başarımı artırmak için katman sayısı, noron sayıları, epoch sayısı, düzenlileştirme yöntemleri vs üzerinde oynamalar yapıldı.

# 5. Model Değerlendirme
Metrikler:
Farklı metrikler farklı yönleri ölçer o yüzden problem farklı metrikler kullanılarak değerlendirildi.
•	Accuracy
•	Precision
•	Recall
•	F1 skoru
•	Roc-Auc

# 6. Sonuç ve Gelecek Çalışmalar
Genel Sonuçlar:
•	Makine öğrenimi metotlarında model eğitimi ve hiperparametre optimizasyonu süresi çok uzun sürdüğü için sampling işlemi yapılmıştır. Derin öğrenme ve makine öğrenimi metotlarını kıyaslayabilmek için derin öğrenme metotlarında da sampling işlemi kullanılmıştır.
•	 Birden fazla değerlendirme metriğiyle (accuracy,precision,recall,f1 vb.) ölçüm yapılmasına rağmen sonuçları karşılaştırmak için accuracy değeri baz alınmıştır.
•	Makine öğrenimi metotları arasında en iyi performansı 0.8520 accuracy değeri ile LightGBM göstermiştir.
•	 Derin öğrenme metotlarından en iyi performansı 0.8320 accuracy değeri ile ANN göstermiştir.
•	Her iki değeri kıyasladığımızda en iyi sonucu 0.8520 accuracy değeri ile LightGBM göstermiştir. Daha sonrasında XGBoost 0.8400 accuracy değeri ile performans göstermiştir. XGBoost’tan sonra en iyi performansı ANN 0.8320 accuracy değeri ile göstermiştir. Catboost 0.8280 ve GBM 0.8120 accuracy değeri ile iyi bir performans göstermiştir ancak fit etme süreleri çok uzun sürmektedir.


Gelecek Çalışmalar:
- Model performansını artırmak için daha fazla veri ve daha karmaşık modeller kullanılabilir.
- Farklı veri ön işleme teknikleri ve optimizasyon yöntemleri denenebilir.
- Diğer derin öğrenme mimarileri (ResNet, EfficientNet vb.) ile karşılaştırmalar yapılabilir.
