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

# BAB III : PEMBAHASAN MASALAH
## 3.1 Algoritma ANN

```R
nurse_data <- read.csv("~/DAP/Project K-Means/project new/nurse_data.csv")
```
```R
View(nurse_data)
```
Untuk mengimport data ke Rstudio Kami menggunakan fungsi yang tersedia di Rstudio yaitu ‘read.csv()’

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
Kode di atas digunakan untuk membagi dataset nurse_data menjadi dua bagian: satu untuk pelatihan (training) dan satu untuk pengujian (testing), dengan proporsi 75% data untuk pelatihan dan 25% data untuk pengujian.

## Seleksi Fitur

Kode ini digunakan untuk membuat formula regresi linear dari kolom-kolom pertama hingga kesembilan dalam dataset nurse_data. Berikut adalah penjelasan langkah-langkahnya:

```R
feats<-names(nurse_data[,1:9])
```
Mengambil nama-nama kolom dari kolom pertama hingga kesembilan dalam dataset nurse_data dan menyimpannya dalam vektor feats.
```R
f<-paste(feats,collapse='+');f
```
Menggunakan fungsi paste untuk menggabungkan nama-nama kolom dalam vektor feats dengan operator +. Hasilnya adalah sebuah string yang berisi formula regresi linear dengan variabel-variabel tersebut yang dihubungkan oleh operator +. Contohnya, jika nama kolom adalah "X1", "X2", ..., "X9", maka hasilnya akan menjadi "X1+X2+...+X9".

f: Menampilkan hasil formula regresi linear yang telah dibuat.

## Pembuatan Formula

Kode di atas digunakan untuk membuat formula regresi linear yang bersifat dinamis dengan memasukkan nama kolom label sebagai respons variabel. 

```R
f1<-paste('label~',f);f1
```
Menggunakan fungsi paste untuk membuat formula regresi linear dengan memasukkan "label~" di depan string formula sebelumnya (f). Hasilnya adalah sebuah string formula regresi linear lengkap yang mencakup variabel label dan variabel-variabel prediktor yang telah ditentukan sebelumnya.

f1: Menampilkan hasil formula regresi linear yang telah dibuat, di mana respons variabel (label) dihubungkan dengan variabel-variabel prediktor.

```R
f2<-as.formula(f1);f2
```
Menggunakan fungsi as.formula untuk mengonversi string formula regresi linear (f1) menjadi objek formula yang dapat digunakan dalam fungsi-fungsi statistik di R.

f2: Menampilkan hasil formula regresi linear yang telah dikonversi menjadi objek formula.

## Menghilangkan Kolom

```R
nurse_data <- nurse_data[-7]
```
```R
nurse_data <- nurse_data[-7]
```
Menghilangkan kolom id dan kolom datetime di nurse_data

```R
train <- train[-7]
```
```R
train <- train[-7]
```
Menghilangkan kolom id dan kolom datetime di data train

## Inisialisasi Model nn
Kode ini tampaknya merupakan usaha untuk membuat dan melatih model jaringan saraf menggunakan paket neuralnet di R.

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
library(neuralnet)
```
```R
nn<-neuralnet(f2,train,hidden=7)
```
Membuat dan melatih model jaringan saraf menggunakan fungsi neuralnet. Formula regresi linear (f2) digunakan sebagai formula model, train adalah dataset pelatihan, dan hidden=7 menunjukkan bahwa ada 7 node di lapisan tersembunyi.

## Visualisasi Model
```R
plot(nn)
```

## Prediksi Dengan Model
```R
pred<- compute(nn,test[1:7])
```
Kode di atas digunakan untuk menghitung output dari model jaringan saraf (nn) pada data pengujian (test) menggunakan fungsi compute pada 7 kolom pertama dari dataset pengujian.

## Evaluasi Model
```R
nn <- neuralnet(label ~ X + Y + Z + EDA + HR + TEMP, data = train_data, hidden = 7)
```
Membuat dan melatih model jaringan saraf dengan formula label ~ X + Y + Z + EDA + HR + TEMP menggunakan data pelatihan train_data. Jaringan saraf ini memiliki 7 node di lapisan tersembunyi.
```R
index_train <- sample(1:nrow(nurse_data), 0.7 * nrow(nurse_data))
```
Menghasilkan indeks acak sebanyak 70% dari jumlah baris dalam dataset nurse_data. Ini digunakan untuk membagi data menjadi subset pelatihan.
```R
train_data <- nurse_data[index_train, ]
```
Menggunakan indeks acak yang dihasilkan sebelumnya untuk memilih subset data pelatihan dari dataset nurse_data.
```R
test_data <- nurse_data[-index_train, ]
```
Membuat subset data pengujian dengan menggunakan baris yang tidak termasuk dalam subset pelatihan.
```R
nn <- neuralnet(label ~ X + Y + Z + EDA + HR + TEMP, data = train_data, hidden = 7)
```
Membuat dan melatih model jaringan saraf lagi pada subset data pelatihan yang baru.
```R
pred <- predict(nn, test_data)
```
Menggunakan model yang telah dilatih untuk membuat prediksi pada data pengujian test_data.
```R
pred_class <- ifelse(pred > 0.5, 1, 0)
```
Mengklasifikasikan hasil prediksi ke dalam dua kelas berdasarkan threshold 0.5.
```R
conf_matrix <- table(pred_class, test_data$label)
```
Membuat tabel kontingensi untuk mengevaluasi kinerja model.
```R
conf_matrix
```
Menampilkan tabel kontingensi.
```R
accuracy_nn <- sum(diag(conf_matrix)) / sum(conf_matrix)
```
 Menghitung akurasi model menggunakan nilai diagonal tabel kontingensi.
```R
accuracy_nn
```
Menampilkan nilai akurasi model.

## 3.2 Algoritma K-Means

```R
nurse_data <- read.csv("~/DAP/Project K-Means/project new/nurse_data.csv")
```
```R
View(nurse_data)
```
Untuk mengimport data ke Rstudio Kami menggunakan fungsi yang tersedia di Rstudio yaitu ‘read.csv()’
```R
library(ggplot2)
require(ggplot2)
```
Baris ini memuat library ggplot2, yang akan digunakan untuk membuat plot visualisasi data.
```R
nurse_data.clustering <- nurse_data
```
Untuk membuat salinan data asli (nurse_data) ke dalam variabel nurse_data.clustering.
```R
nurse_data <- as.matrix(nurse_data)
```
Mengonversi dataframe nurse_data menjadi matriks.
```R
str(nurse_data)
```

# Memilih Kolom yang Akan Digunakan
```R
nurse_data <- nurse_data[, c("EDA", "TEMP")]
View(nurse_data)
```
Untuk memilih hanya kolom "EDA" dan "TEMP" dari matriks nurse_data yang telah dihasilkan sebelumnya.

# Inisialisasi Variabel untuk K-Means
```R
cluster <- 3
c_initial <- c(0,1,2)
centroid <- nurse_data[1:cluster,]
cent_DF <- data.frame(c = c_initial, centroid)
```
Inisialisasi variabel yang diperlukan untuk proses K-Means, termasuk jumlah cluster (cluster), nilai awal untuk centroid (c_initial), serta inisialisasi variabel centroid dan cent_DF yang akan digunakan dalam visualisasi.

# Inisialisasi Matriks untuk Perhitungan Jarak
```R
d <- matrix(0, nrow = nrow(nurse_data), ncol = cluster)
c <- matrix(0, nrow = nrow(nurse_data), ncol = 1)
```
Inisialisasi matriks d dan c dengan nilai nol. Matriks d akan digunakan untuk menyimpan jarak antara setiap titik data dengan centroid, sedangkan matriks c akan menyimpan nomor cluster yang ditetapkan pada setiap titik data.
```R
updCentroid <- matrix(0, nrow = nrow(centroid), ncol = ncol(nurse_data))
status <- 10
iter <- 0
df <- data.frame(nurse_data)
updCentroid
```
Inisialisasi variabel updCentroid untuk menyimpan centroid yang diperbarui, variabel status yang digunakan untuk menentukan apakah iterasi K-Means sudah konvergen atau belum, variabel iter untuk menyimpan jumlah iterasi, dan dataframe df yang akan digunakan dalam visualisasi.

# Membuat Inisial Plot menggunakan ggplot2
```R
initPlot2 <- ggplot(df, aes(EDA, TEMP)) +
  geom_point(size=3) + geom_point(data=cent_DF, color=c("blue", "red", "green"), size=10)
initPlot2
ggsave(filename = "nurse_data, 3 Cluster - initial.png", width = 40, height = 20, unit = "cm")
```
Untuk membuat plot awal dengn ggplot2.

# Iterasi K-Means dengan Visualisasi dan Simpan Plot
```R
while (status != 0)
{
  iter <- iter + 1
  
  fn <- paste("nurse_data,", cluster, "Cluster - iter", iter, ".png", sep = " ")
```
Mengeksekusi proses K-Means clustering dalam loop while hingga konvergensi (status menjadi 0). Pada setiap iterasi, jarak antara setiap data dengan centroid dihitung, cluster baru ditentukan, dan hasil clustering divisualisasikan. Setiap plot disimpan dengan menggunakan ggsave.

# Perhitungan Jarak dan Penentuan Cluster

```R
for (j in 1:cluster) {
   for (i in 1:nrow(nurse_data)) {
      d[i, j] = sqrt(sum((as.numeric(nurse_data[i, 1:ncol(nurse_data)]) - as.numeric(centroid[j, 1:ncol(centroid)]))^2))
   }
}
```
Digunakan untuk menghitung jarak setiap data ke setiap centroid.
```R
for (i in 1:nrow(d)) {  
   min_indices <- which(d[i,] == min(d[i,]), arr.ind = TRUE)

   if (length(min_indices) > 0){
      c[i] <- min_indices[1] -1
    } else {
      # Menangani kasus ketika which mengembalikan vektor kosong
      # Pilihan Anda, misalnya, mungkin memberikan nilai default atau menandai baris ini untuk penanganan khusus
      # Sebagai contoh, kami mengatur nilai c menjadi -1 jika vektor kosong
      c[i] <- -1
    }
}
```
Digunakan untuk menetapkan nomor cluster pada setiap data berdasarkan jarak terkecil.

# Membuat Data Frame untuk Plot
```R
df <- data.frame(c, nurse_data)
```
Membuat data frame baru (df) yang menggabungkan kolom nomor cluster (c) dengan nurse_data.

# Membuat Data Frame untuk Centroid
```R
cent_DF <- data.frame(c = c_initial, centroid)
```
Membuat data frame baru (cent_DF) yang berisi kolom nomor cluster (c) dan nilai centroid awal (c_initial).

# Menggabungkan Data Frame untuk Plot dan Centroid
```R
gg <- merge(df, cent_DF, by="c")
```
Menggabungkan data frame df dan cent_DF berdasarkan kolom nomor cluster (c).

# Membuat Plot dengan ggplot2
```R
plot <- ggplot(gg, aes(EDA.x, TEMP.x, color=factor(c))) + geom_point(size=3) +
  geom_point(aes(x = EDA.y, y = TEMP.y), size=5) +
  geom_segment(aes(x = EDA.y, y = TEMP.y, xend = EDA.x, yend = TEMP.x))
```

# Menyimpan Plot sebagai File Gambar
```R
ggsave(plot, file = fn, width = 40, height = 20, units = "cm")
```

# Menghitung centroid baru berdasarkan data cluster baru
```R
compare <- cbind(nurse_data, c)

for (i in 1:cluster)
  {
    x <- subset(compare[,1:2], compare[,3] == i-1)
    
    for(j in 1:ncol(nurse_data))
    {
      updCentroid[i,j] <- mean(as.numeric(x[,j]))
    }
  }
```

# Pemeriksaan Kesamaan Centroid
```R
if(all(updCentroid == centroid)){
    status = 0
  }
  else {
    status = 1
    for (i in 1:cluster)
    {
      for (j in 1:ncol(centroid))
      {
        centroid[i,j] <- updCentroid[i,j]
      }
    } 
  }
}
```
Kita cek apakah semua nilai dalam matriks updCentroid sama dengan nilai dalam matriks centroid. Jika iya, maka kita anggap proses K-Means clustering sudah selesai (konvergen) dan set status menjadi 0. Jika tidak, kita set status menjadi 1, yang berarti kita perlu melanjutkan iterasi.

# Menggunakan K-Means Library
```R
nurse_data2 <- nurse_data
```

# Memilih atribut yang akan digunakan untuk clustering
```R
attributes <- nurse_data2[, c("EDA", "TEMP")]
```

# Menentukan jumlah cluster yang diinginkan
```R
num_clusters <- 3
```

# Melakukan clustering menggunakan K-Means
```R
kmeans_result <- kmeans(attributes, centers = num_clusters)
```

# Menampilkan hasil clustering
```R
print(kmeans_result)
```

# Menambahkan kolom cluster ke dalam data frame nurse_data
```R
nurse_data$Cluster <- as.numeric(kmeans_result$cluster)
```

# Melihat nurse_data dengan kolom Cluster yang telah ditambahkan
```R
head(nurse_data)
```

# Visualisasi hasil clustering dengan plot
```R
plot(attributes, col = kmeans_result$cluster, pch = 20, main = "nurse_data Clustering with K-Means")

points(kmeans_result$centers, col = 1:num_clusters, pch = 3, cex = 2)

legend("topright", legend = 1:num_clusters, col = 1:num_clusters, pch = 3)
```
