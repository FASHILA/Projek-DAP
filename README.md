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
## 2.1. Pengenalan Parameter Data

1. Variabel Orientasi (X, Y, Z)
Data orientasi terdiri dari tiga variabel, yaitu X, Y, dan Z, masing-masing memiliki 256 entri unik. Variabel ini menggambarkan orientasi suatu objek atau entitas dalam tiga dimensi.

2. Elektrodermal Activity (EDA)
EDA mencakup 274.452 entri unik dan mengukur aktivitas elektrodermal, yang dapat mencerminkan tingkat stres atau kecemasan pada subjek.

3. Heart Rate (HR)
Variabel Heart Rate memiliki 6.268 entri unik dan mengukur denyut jantung. Informasi ini dapat memberikan gambaran tentang tingkat aktivitas fisik atau emosional subjek.

4. Temperatur (TEMP)
Temperatur, dengan 599 entri unik, mencatat suhu fisik subjek. Perubahan dalam suhu tubuh dapat mencerminkan aktivitas fisiologis yang bermanfaat untuk pemahaman lebih lanjut tentang kondisi subjek.

5. Identifier (id)
Variabel kategorikal 'id' berisi 18 pengidentifikasi kategorikal yang mewakili individu atau kelompok tertentu dalam dataset.

6. Waktu (datetime)
Variabel datetime memiliki 10,6 juta entri unik yang merepresentasikan tanggal dan waktu setiap pengukuran. Analisis waktu dapat memberikan wawasan tentang pola atau tren temporal dalam data.

7. Kategori Kelas (Label)
Variabel 'label' berisi tiga entri unik yang mewakili status atau kelas tertentu. Kategori ini dapat digunakan untuk tugas klasifikasi dan pemahaman lebih lanjut tentang hubungan antara parameter lain dalam dataset.

## 2.2 Pengenalan tentang RStudio
RStudio adalah sebuah Integrated Development Environment (IDE) yang dirancang khusus untuk pengembangan aplikasi dan analisis data menggunakan bahasa pemrograman R. RStudio menyediakan berbagai fitur dan alat untuk memudahkan pengguna dalam menulis, menguji, dan menjalankan kode R, serta mengorganisir proyek dan menganalisis data. 

Contoh penggunaan RStudio Misalkan seorang data scientist ingin melakukan analisis data untuk sebuah proyek penelitian. Kita dapat mengimpor data, menulis dan menjalankan kode, menganalisis and visualisasi data, mengatur proyek, berbagi hasil, dll.

## 2.3 Algoritma dalam RStudio

Untuk melakukan analisis pada data `Nurse Stress Prediction Wearable Sensors` , terdapat berbagai algoritma dan teknik yang dapat digunakan. Berikut ini beberapa contoh penggunaan algoritma untuk analisis data 
`Nurse Stress Prediction Wearable Sensors`:

1. Artificial Neural Network (ANN) 

Artificial Neural Network (ANN) adalah model komputasi yang terinspirasi oleh jaringan saraf biologis, terdiri dari neuron dan bobot-bobot yang dapat disesuaikan. Tujuannya adalah memahami, mengklasifikasi, dan memprediksi pola kompleks dalam data dengan kemampuan adaptasi terhadap variasi data, melakukan pelatihan dan pembelajaran dari data, serta aplikasi dalam kecerdasan buatan untuk menangani masalah kompleks dan non-linier. ANN juga diarahkan untuk pemrosesan data non-linear dan generalisasi, sehingga dapat memberikan prediksi yang baik pada data yang belum pernah dilihat sebelumnya.

2. K-Means (Clustering)

K-means adalah algoritma klastering yang digunakan untuk mengelompokkan data ke dalam kelompok-kelompok berdasarkan kemiripan atribut. Fungsi utama k-means adalah mengidentifikasi pola, struktur, dan hubungan dalam data yang tidak terlihat secara langsung. Tujuannya adalah untuk mengorganisir data yang besar menjadi kelompok yang lebih kecil dan bermakna, memfasilitasi analisis data, segmentasi pasar, pengambilan keputusan, dan pemahaman yang lebih mendalam tentang data

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
