# BAB I : PENDAHULUAN
## 1.1 Latar Belakang

Meningkatnya aksesibilitas teknologi wearable telah membuka pintu untuk terus memantau berbagai faktor fisiologis. Mendeteksi stres sejak dini telah menjadi hal yang sangat penting, membantu individu dalam mengelola kesehatan mereka secara proaktif terhadap dampak buruk dari paparan stres yang berkepanjangan. Makalah ini menyajikan hasil analisis deteksi stres eksklusif yang dikembangkan dalam lingkungan alami rumah sakit. Disusun selama wabah COVID-19, kumpulan data ini mencakup data biometrik perawat. Menganalisis stres di tempat kerja adalah hal yang rumit karena adanya beragam elemen sosial, budaya, dan psikologis yang melekat dalam menghadapi keadaan stres. Oleh karena itu, kumpulan data kami tidak hanya mencakup data fisiologis tetapi juga informasi kontekstual seputar peristiwa stres. Metrik fisiologis utama seperti aktivitas elektrodermal, detak jantung, dan suhu kulit subjek perawat terus dipantau. Selain itu, survei berkala yang dilakukan melalui ponsel pintar menangkap faktor-faktor yang berkontribusi terhadap kejadian stres yang terdeteksi. Basis data yang menampung sinyal-sinyal ini, kejadian stres, dan respons survei dapat diakses publik di Dryad.

Dataset yang digunakan dalam penelitian ini diambil dari platform Kaggle, Kaggel sendiri merupakan sumber terbuka yang menyediakan berbagai dataset untuk keperluan analisis dan penelitian. Dataset yang digunakan dalam penelitian ini adalah `Nurse Stress Prediction Wearable Sensors` masing-masing mewakili enam parameter. Referensi untuk dataset ini adalah:

Kaggle. `Nurse Stress Prediction Wearable Sensors`. Tersedia di:
[Nurse Stress Prediction Wearable Sensors](https://www.kaggle.com/datasets/priyankraval/nurse-stress-prediction-wearable-sensors)

Dalam analisis `Nurse Stress Prediction Wearable Sensors`, terdapat berbagai parameter yang harus diperhatikan, seperti 
1. X,Y,Z
2. EDA, HR,TEMP
3. id
4. datetime
5. label 
 
Penggunaan teknologi dan metode analisis yang tepat sangat penting untuk mendapatkan data yang akurat dan dapat diandalkan.

Dalam konteks ini, RStudio adalah salah satu perangkat lunak yang dapat digunakan untuk menganalisis kualitas air. RStudio adalah lingkungan pengembangan terintegrasi (IDE) untuk bahasa pemrograman R. RStudio menyediakan berbagai paket dan fungsi yang berguna dalam analisis data, termasuk analisis statistik, visualisasi, dan pemodelan. Dengan menggunakan RStudio, kita dapat menganalisis data kualitas air dengan lebih efisien dan efektif.

## 1.2 Rumusan Masalah

Berdasarkan latar belakang yang telah diuraikan, penelitian ini bertujuan untuk menjawab beberapa rumusan masalah sebagai berikut:

1. Bagaimana tingkat stres perawat dapat diukur secara objektif menggunakan teknologi wearable sensors?
2. Bagaimana implementasi algoritma Artificial Neural Network (ANN) dapat membantu dalam menganalisis data tingkat stres perawat?
3. Bagaimana algoritma K-means dapat digunakan untuk mengelompokkan pola tingkat stres perawat yang teridentifikasi?

## 1.3 Tujuan Penelitian

Tujuan dari penelitian ini adalah sebagai berikut:

1. Menganalisis tingkat stres perawat menggunakan data yang diperoleh dari teknologi wearable sensors.
2. Mengimplementasikan algoritma Artificial Neural Network (ANN) untuk memprediksi tingkat stres perawat.
3. Menerapkan algoritma K-means untuk mengelompokkan pola tingkat stres perawat yang teridentifikasi.

## 1.4 Manfaat Penelitian

Penelitian ini diharapkan dapat memberikan kontribusi pada pengembangan sistem prediksi tingkat stres perawat menggunakan teknologi wearable sensors dan algoritma data mining. Manfaat penelitian ini antara lain:

1. Meningkatkan pemahaman tentang faktor-faktor yang mempengaruhi tingkat stres perawat.
2. Memberikan landasan untuk pengembangan solusi atau intervensi yang dapat mengurangi tingkat stres perawat.
3. Menyediakan dasar empiris bagi penelitian lebih lanjut dalam penggunaan teknologi wearable sensors dan algoritma data mining dalam konteks kesehatan.

# BAB II : LANDASAN TEORI

## Algoritma ANN

```R
nurse_data <- read.csv("~/DAP/Project K-Means/project new/nurse_data.csv")
```
```R
View(nurse_data)
```

## Pembagian Data

```R
n<-round(nrow(nurse_data)*0.75);n
```
```R
set.seed(12);samp=sample(1:nrow(nurse_data),n)
```
```R
train=nurse_data[samp,]
```R
test=nurse_data[-samp,]
```

## Seleksi Fitur

```R
feats<-names(nurse_data[,1:9])
```
```R
f<-paste(feats,collapse='+');f
```

## Pembuatan Formula

```R
f1<-paste('label~',f);f1
```
```R
f2<-as.formula(f1);f2
```

## Menghilangkan Kolom

```R
nurse_data <- nurse_data[-7]
```
```R
nurse_data <- nurse_data[-7]
```
```R
train <- train[-7]
```
```R
train <- train[-7]
```

## Inisialisasi Model nn
```R
nn<-neuralnet(f2,train,hidden=7)
```
```R
str(f2)
```

## Pembaruan Formula
```R
f2 <- update(f2, . ~ . - id)
```
```R
print(f2)
```
```R
f2 <- update(f2, . ~ . - datetime)
```
```R
print(f2)
```
```R
nn<-neuralnet(f2,train,hidden=7)
```
```R
str(train)
```
```R
nn<-neuralnet(f2,train,hidden=7)
```
```R
library(neuralnet)
```
```R
nn<-neuralnet(f2,train,hidden=7)
```

## Visualisasi Model
```R
plot(nn)
```

## Prediksi Dengan Model
```R
pred<- compute(nn,test[1:7])
```

## Evaluasi Model
```R
nn <- neuralnet(label ~ X + Y + Z + EDA + HR + TEMP, data = train_data, hidden = 7)
```
```R
index_train <- sample(1:nrow(nurse_data), 0.7 * nrow(nurse_data))
```
```R
train_data <- nurse_data[index_train, ]
```
```R
test_data <- nurse_data[-index_train, ]
```
```R
nn <- neuralnet(label ~ X + Y + Z + EDA + HR + TEMP, data = train_data, hidden = 7)
```
```R
pred <- predict(nn, test_data)
```
```R
pred_class <- ifelse(pred > 0.5, 1, 0)
```
```R
conf_matrix <- table(pred_class, test_data$label)
```
```R
conf_matrix
```
```R
accuracy_nn <- sum(diag(conf_matrix)) / sum(conf_matrix)
```
```R
accuracy_nn
```
