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
  
