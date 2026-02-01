MNIST El Yazısı Rakam Sınıflandırma (PCA & Logistic Regression)
Bu proje, makine öğrenmesi dünyasının klasik veri seti olan MNIST üzerinde, veri boyutunu optimize ederek (PCA kullanarak) sınıflandırma işleminin nasıl yapıldığını göstermektedir.

Proje Özeti
Bu çalışmada, 784 piksellik (28x28) el yazısı rakam görsellerini, bilgi kaybını minimumda tutarak daha düşük boyutlara indirdik
ve ardından Lojistik Regresyon algoritması ile bu rakamların hangi sayı olduğunu tahmin eden bir model eğittik.


İşlem Adımları
Veriyi Yükleme: fetch_openml ile 70.000 adet rakam görseli yüklendi.

Görselleştirme: Veri seti içerisindeki rakamların nasıl göründüğünü anlamak için örneklemeler yapıldı.

Veri Ölçeklendirme (Scaling): StandardScaler kullanılarak piksel değerleri modelin daha hızlı öğrenebileceği bir aralığa getirildi.

Boyut Azaltma (PCA): * Verinin %95 varyansını (bilgisini) koruyacak şekilde Temel Bileşen Analizi (PCA) uygulandı.

Bu işlemle veri boyutu 784'ten 327'ye düşürülerek işlem hızı optimize edildi.

Model Eğitimi: PCA ile sıkıştırılmış veriler LogisticRegression (lbfgs solver) algoritmasına verildi.

Tahmin: Model, test setindeki daha önce görmediği rakamları başarıyla tahmin etti.

Sonuçlar
Giriş Boyutu: 784 Özellik (Piksel)

PCA Sonrası Boyut: 327 Özellik

Korunan Bilgi Oranı: %95

Algoritma: Logistic Regression
