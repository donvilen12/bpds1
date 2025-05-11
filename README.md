# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan *Edutech*

## ***Business Understanding***

Bisnis edutech merupakan bagian dari sektor edukasi yang memanfaatkan teknologi *digital* untuk menyediakan solusi pendidikan inovatif. Dengan perkembangan teknologi *digital*, internet, dan perangkat *mobile*, *edutech* telah mengalami perkembangan pesat karena memungkinkan akses pendidikan yang lebih mudah, terjangkau, dan terpersonal secara global. Berikut adalah beberapa poin lebih detail mengenai perkembangan dan potensi bisnis *edutech*:

### Aksesibilitas Global 
Salah satu keunggulan utama *edutech* adalah kemampuannya untuk menyediakan akses pendidikan ke seluruh dunia. Dengan adanya internet, orang-orang dari berbagai latar belakang dan lokasi geografis dapat mengakses materi pembelajaran tanpa batasan fisik. Hal ini membuka pintu bagi pendidikan yang lebih inklusif dan merata di seluruh dunia.

### Pembelajaran Interaktif 
*Edutech* menyediakan *platform* pembelajaran yang interaktif dan menarik. Berbagai fitur seperti video pembelajaran, simulasi, *game* edukatif, dan diskusi *daring* meningkatkan keterlibatan siswa dalam proses pembelajaran. Ini membantu meningkatkan pemahaman dan retensi materi pelajaran.

### Pembelajaran Adaptif 
Fitur kunci *edutech* adalah kemampuannya untuk menyediakan pembelajaran yang adaptif. *Platform edutech* menggunakan teknologi seperti kecerdasan buatan (*AI*) dan analisis data untuk memahami gaya belajar dan kebutuhan individual siswa. Dengan demikian, siswa dapat belajar sesuai dengan kecepatan dan gaya belajar mereka sendiri.

### Personalisasi 
*Edutech* memungkinkan personalisasi pembelajaran yang lebih baik. Dengan menganalisis data tentang kemajuan belajar dan preferensi siswa, *platform edutech* dapat menyajikan materi yang sesuai dengan kebutuhan individu. Ini memungkinkan pengalaman belajar yang lebih efektif dan efisien.

### Peluang Bisnis 
Pertumbuhan pesat dalam bisnis *edutech* menawarkan banyak peluang bisnis yang menjanjikan. Mulai dari pengembangan *platform* pembelajaran, konten *digital*, solusi manajemen sekolah, hingga pelatihan guru dan konsultasi edukasi, ada banyak area di mana perusahaan dapat berinovasi dan berkontribusi dalam transformasi pendidikan global.

### Kolaborasi dengan Institusi Pendidikan 
Banyak perusahaan *edutech* bekerja sama dengan institusi pendidikan formal seperti sekolah dan perguruan tinggi untuk menyediakan solusi pendidikan yang terintegrasi. Ini menciptakan peluang kolaborasi yang saling menguntungkan dan memperluas jangkauan bisnis *edutech*.


## **Permasalahan Bisnis**

Jaya Jaya Maju merupakan salah satu perusahaan multinasional di bidang *edutech* yang telah berdiri sejak tahun 2000. Ia memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. Walaupun telah menjadi menjadi perusahaan yang cukup besar, Jaya Jaya Maju masih cukup kesulitan dalam mengelola karyawan. Hal ini berimbas tingginya *attrition rate* (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) hingga lebih dari 10%.

Permasalahan *attrition rate* ini mengakibatkan adanya biaya tambahan dalam perekrutan, pelatihan ulang, serta menurunkan produktivitas dan kualitas layanan. Perusahaan ingin mengidentifikasi pola *attrition*, faktor-faktor yang mempengaruhi perpindahan karyawan, dan mengambil langkah-langkah proaktif untuk meningkatkan retensi bakat dan memastikan kesinambungan operasional yang stabil.

## **Cakupan Proyek**

Untuk mengatasi permasalahan *attrition* karyawan dalam bisnis *edutech*, akan digunakan pendekatan dan metode/teknik berikut:

### Pemahaman Data (*Data Understanding*)
- Mengumpulkan data historis tentang perpindahan karyawan, termasuk informasi profil karyawan, performa kerja, kepuasan kerja dan faktor-faktor lain yang terkait.
- Mempelajari tipe dan karakteristik *dataset*.

### Persiapan Data (*Data Preparation*)
- Membersihkan dan mengolah data untuk mengatasi *missing values*, data duplikat, dan masalah lain yang mungkin mempengaruhi kualitas analisis.
- Melakukan proses transformasi data seperti *encoding* kategori, normalisasi, dan pemilihan fitur yang relevan untuk analisis.
- Menjelajahi korelasi antar variabel untuk memahami hubungan di antara variabel-variabel tersebut.

### *Machine Learning Modeling*
- Memisahkan data menjadi *training set* dan *testing set*.
- Melatih beberapa model menggunakan *training set*, dengan variabel target *attrition* dan variabel fitur yang relevan.
- Menyesuaikan *hyperparameter* model dan melakukan validasi model.

### *Evaluation*
- Menggunakan *testing set* untuk mengevaluasi kinerja model dengan metrik yang sesuai seperti *accuracy*, *precision*, *recall* dan *F1-score*.

### *Deployment*
- Menjalankan model *Logistic Regression* yang telah dibuat ke dalam lingkup produksi sehingga *user* dapat berinteraksi dengan model.

## **Persiapan**

Sumber data pelatihan: 
```
https://www.ibm.com/communities/analytics/watson-analytics-blog/watson-analytics-use-case-for-hr-retaining-valuable-employees/
```

*Setup environment - Anaconda*:
```
conda create --name hr-analytics python=3.11.12
conda activate hr-analytics
pip install -r requirements.txt
```

*Setup environment - Shell/Terminal*:
```
mkdir hr-analytics
cd hr-analytics
pipenv install
pipenv shell
pip install -r requirements.txt
```

Proyek *HR Analytic* ini menggunakan model **Logistic Regression** untuk memprediksi *Attrition Rate* berdasarkan data HR. Berkas yang digunakan adalah sebagai berikut: 
  - `logistic_regression_model.joblib` : Model *Logistic Regression* yang sudah dilatih.
  - `prediction.py` : *Script* Python untuk menjalankan proses prediksi.


Cara menjalankan prediksi:
  1. Persiapan *Environment*

     - Pastikan Anda sudah berada di *environment* Python yang sesuai. Anda bisa menggunakan `pipenv` atau `conda`
     - *Install* dependensi yang ada pada `requirements.txt`
  
  2. Format Input Data
     - Script `prediction.py` membutuhkan *input* data dalam format CSV dengan struktur kolom yang sesuai dengan data pelatihan `employee_data.csv`
  
  3. Menjalankan Prediksi
     
     - Gunakan perintah berikut di terminal untuk menjalankan prediksi:
       
      ```
      python prediction.py --input data.csv --output prediksi.csv
      ```

  4. Mendapatkan Hasil Prediksi
     - Hasil prediksi akan disimpan dalam berkas `prediksi.csv` dengan tambahan kolom `prediction` yang berisi *output* dari model.

  
## ***Business Dashboard***

*Dashboard* dibuat dengan menggunakan *Google Looker Studio* untuk menampilkan distribusi data dan pengaruh variabel-variabel data terhadap *Attrition Rate*. *Dashboard* dapat diakses pada *link* berikut ini:
```
https://lookerstudio.google.com/reporting/cb84048e-540f-4af7-9e5f-d6396b31ff2c
```

![erika_budiarti-dashboard](https://raw.githubusercontent.com/ERIKABUDIARTI/HR-Analytics/main/erika_budiarti-dashboard.png)


## ***Conclusion***

- Komposisi karyawan terdiri dari 60% Pria dan 40% Wanita, dengan mayoritas Generasi Milenial yang berada pada rentang umur 31-40 tahun.
- Tingkat perpindahan karyawan (*Attrition Rate*) sebesar 12.2% dari 1,470 karyawan dengan capaian tertinggi dari Departemen *'Research & Development'*.
- Kepuasan kerja tertinggi berada pada level menengah (*'Medium'*)
- Perpindahan karyawan (*Attrition Rate*) dipengaruhi oleh beberapa faktor seperti lembur (*Overtime*), persentase kenaikan gaji (*Percentage Salary Increase*), pengalaman kerja (*Experience*), dan level pekerjaan (*Job Level*)


### **Rekomendasi *Action Items***

Beberapa rekomendasi *action items* yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.

- Memperhatikan faktor-faktor yang berkontribusi pada tingkat kepuasan kerja 'menengah'. Lakukan survei atau wawancara untuk mengumpulkan umpan balik dari karyawan dan mengidentifikasi kendala yang perlu diperbaiki.
- Mengingat kelompok usia 31-40 tahun mengalami tingkat perpindahan tertinggi, telusuri alasan di balik tren ini dan implementasikan strategi untuk mempertahankan dan melibatkan karyawan dalam kelompok usia ini, seperti memberikan peluang kemajuan karier.
- Adanya korelasi antara bekerja lembur dan peningkatan perpindahan perlu dipertimbangkan untuk mengoptimalkan beban kerja, mencegah kelelahan dan memastikan keseimbangan hidup kerja yang sehat.
- Menyediakan lebih banyak peluang promosi bagi karyawan, mengevaluasi dan menyesuaikan struktur kompensasi terutama pada Departemen *'Research & Development'*.
