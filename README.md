# Mini-Project 5 - Improving Employee Retention by Predicting Employee Attrition Using Machine Learning
## Ringkasan
Sumber daya manusia (SDM) merupakan aset utama yang perlu dikelola dengan baik oleh perusahaan agar tujuan bisnis dapat tercapai dengan efektif dan efisien. Pada mini project ini akan menghadapi permasalahan sumber daya manusia yang ada di perusahaan. Fokus utamanya yaitu  mengetahui cara menangani karyawan agar tetap bertahan di perusahaan yang ada pada saat ini yang berakibat bengkaknya biaya untuk rekrutmen karyawan serta pelatihan untuk karyawan baru. Dengan mengetahui faktor utama yang menyebabkan karyawan tidak merasa, perusahaan dapat segera menanggulanginya dengan membuat program-program yang relevan pada permasalahan karyawan. 
## 1. Data Preprocessing
Tahap awal yang harus dilakukan adalah mempersiapkan data mentah menjadi data yang bersih dan siap diolah. Data preprocessing yang dilakukan diantaranya adalah menangani berbagai permasalahan data seperti data yang kosong, data yang tidak sesuai, hingga mengidentifikasi data-data yang tidak dibutuhkan.
### Menangani Data Null
- Terdapat 6 feature yang memiliki data null.
- Pada feature IkutProgramLOP memiliki data null paling banyak yaitu 258, sehingga dilakukan action drop feature.
- Pada 5 feature yang lain dilakukan action drop data null.
### Mengganti Value yang Tidak Sesuai
- Pada feature PernahBekerja memiliki unique value : '1, yes' kemudian dilakukan action me-replace value 'yes' menjadi 1.
### Membuang Data yang Tidak Diperlukan
- Pada dataset, feature yang memiliki 1 unique value (konstanta) adalah feature PernahBekerja. Sehingga dilakukan action drop feature PernahBekerja.

## 2. Annual Report on Employee Number Changes
Pada tahap ini dilakukan analisis perkembangan jumlah karyawan di perusahaan setiap tahunnya sehingga didapatkan kondisi perusahaan terkini apakah dalam keadaan yang sehat atau mengkhawatirkan.
![image](https://github.com/hadasadida/Mini-Project-5-Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/assets/124650679/31b616a8-9c91-46c6-a8c8-1a515163d3e3)
- Jumlah hiring karyawan menurun setiap tahun.
- Jumlah karyawan resign paling tinggi terjadi pada tahun 2017.
- Jumlah karyawan resign sempat turun di tahun 2014 - 2015, namun mengalami kenaikan paling tinggi di tahun 2017.
- Kondisi perusahaan berada pada tahap yang mengkhawatirkan.

## 3. Resign Reason Analysis for Employee Attrition Management Strategy
Pada tahap ini dilakukan analisis tentang divisi pekerjaan apa yang paling rentan untuk resign serta alasan resign seperti apa yang bisa di handle oleh perusahaan demi kepentingan perbaikan management.
![image](https://github.com/hadasadida/Mini-Project-5-Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/assets/124650679/d412584c-88f5-4f55-93fb-82817e0c646f)
- Jumlah karyawan resign paling banyak berada pada divisi Data Analyst dengan jenjang karir fresh graduate.
- Berbagai macam performa karyawan dan alasan resign memiliki jumlah porsi yang sama dalam hal karyawan melakukan resign, namun jumlah tertinggi berada pada performa karyawan bagus dan alasan resign toxic culture.
- Perusahaan dapat melakukan perbaikan dengan merubahan budaya kerja pada seluruh jajaran baik pimpinan maupun karyawan agar tidak terjadi toxic culture.

## 4. Build an Automated Resignation Behavior Prediction using Machine Learning
![image](https://github.com/hadasadida/Mini-Project-5-Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/assets/124650679/01b53cda-bdf7-4cf0-a9c1-637a1dfaf9a7)
### Data Preprocessing
#### Handle Missing Value
Terdapat missing value pada kolom TingkatPendidikan, TanggalResign, TanggalResign_tahun. Dilakukan action mengisi missing value dengan nilai mode.
#### Handle Duplicated Data
Tidak ada data duplikat.
#### Handle Outlier
![image](https://github.com/hadasadida/Mini-Project-5-Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/assets/124650679/18059c02-6094-4dfb-a362-20e4d53b79e1)
![image](https://github.com/hadasadida/Mini-Project-5-Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/assets/124650679/c6d83647-23e8-4a42-93ae-d27515017ead)
Dilakukan handle outlier dengan z-score.
#### Feature Engineering
- Membuat feature baru yaitu Resign yang nantinya akan berfungsi sebagai target.
- Membuat pengelompokan berdasarkan jenis divisi pekerjaan yaitu divisi_data, divisi_engineering, divisi_product.
- Menggabungkan feature pekerjaan dan alasan resign.
- Melakukan feature encoding pada feature StatusPernikahan, JenisKelamin, StatusKepegawaian, JenjangKarir, PerformancePegawai, TingkatPendidikan, Resign dan Pekerjaan_AlasanResign.
### Model Training - Model Selection - Hyperparameter Tuning
#### Imbalanced Learning 
![image](https://github.com/hadasadida/Mini-Project-5-Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/assets/124650679/a9286250-f358-4aa7-ad98-019be7eddcd9) 
- Digunakan imbalanced learning oversampling smote untuk menyeimbangkan jumlah target. 
#### Machine Learning  
![image](https://github.com/hadasadida/Mini-Project-5-Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/assets/124650679/d43b4a39-49d5-4015-9d31-fe28b356d219)
- Dilakukan modeling menggunakan 6 machine learning untuk mendapatkan hasil terbaik yaitu decision tree, logistic regression, knn, adaboost, xgboost dan random forest. Dihasilkan score masing-masing ML score setelah dilakukan hyperparameter tuning pada tabel di atas.
- Dipilih model Xgboost karena menghasilkan score ROC-AUC paling baik.
  
#### Feature Importance 
![image](https://github.com/hadasadida/Mini-Project-5-Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/assets/124650679/f96bafec-f411-4457-9537-19e8109b6f88)

#### Shap Value
![image](https://github.com/hadasadida/Mini-Project-5-Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/assets/124650679/5709caa1-48f9-40b2-b642-984173f30308)

- Fitur jenjang karir merupakan fitur paling penting dalam menentukan karyawan berpeluang untuk resign atau tidak.
- Semakin besar jumlah ketidakhadiran karyawan, semakin besar karyawan berpeluang untuk resign.
- Semakin bagus performance karyawan, semakin besar karyawan berpeluang untuk resign.
- Semakin tinggi tingkat pendidikan karyawan, semakin besar karyawan berpeluang untuk resign.
- Semakin rendah skor kepuasan pegawai, semakin besar karyawan berpeluang untuk resign.
  
