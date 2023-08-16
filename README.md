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
- Perusahaan dapat melakukan perubahan budaya kerja pada seluruh jajaran baik pimpinan dan karyawan agar tidak terjadi toxic culture.

## 4. Build an Automated Resignation Behavior Prediction using Machine Learning

