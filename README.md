## Parsing Data JSON untuk Laporan Keuangan Kas RT di Android

### Anggota Kelompok <br>

| Nama                      | NIM       | Kelas     | Mata Kuliah          |
| ------------------------- | --------- | --------- | -------------------- |
| Anggita Risqi Nur Clarita | 312210450 | TI.22.A.1 | Pemrograman Mobile 2 |
| Faizah Via Fadhillah      | 312210460 | TI.22.A.1 | Pemrograman Mobile 2 |
| Zahra Nurhaliza           | 312210364 | TI.22.A.1 | Pemrograman Mobile 2 |


**Deskripsi:**

Aplikasi Android ini dibuat untuk mempermudah pengelolaan keuangan Kas RT dengan menampilkan laporan keuangan yang terstruktur dan mudah dipahami. Laporan keuangan ini diperoleh dengan parsing data JSON dari Google Spreadsheets melalui API Spreadsheets.

**Fitur:**

* Menampilkan foto warga
* Menampilkan nama lengkap warga (nama depan dan belakang)
* Menampilkan alamat email warga
* Menampilkan alamat rumah warga
* Menampilkan jumlah iuran bulanan warga
* Menghitung total iuran individu warga
* Menghitung total iuran warga pada akhir rekap iuran bulanan
* Mencatat pengeluaran dari hasil iuran warga
* Menjelaskan pemanfaatan iuran warga

**Teknologi:**

* Android Studio
* Kotlin
* API Spreadsheets
* Google Spreadsheets

**Struktur Proyek:**

* **model:** Berisi kelas-kelas model data, seperti `DataItem.kt` dan `ResponseUser.kt`.
* **network:** Berisi konfigurasi API dan service, seperti `ApiConfig.kt` dan `ApiService.kt`.
* **res:** Berisi kode utama aplikasi Android, konfigurasi build, dan resources (seperti gambar, string, dan layout).
* **layout:** Berisi file-file layout XML yang digunakan untuk mendesain tampilan aplikasi.

**Penjelasan Kode:**

* File `MainActivity.kt` merupakan file utama yang berisi kode untuk menampilkan data dari JSON dan menampilkannya di layout.
* File `DataItem.kt` dan `ResponseUser.kt` merupakan kelas model data yang digunakan untuk memetakan data JSON ke objek Kotlin.
* File `ApiConfig.kt` berisi konfigurasi API, seperti URL endpoint dan API key.
* File `ApiService.kt` berisi interface API yang mendefinisikan method-method untuk melakukan request dan menerima response dari API.

**Langkah Penggunaan:**

1. Buat spreadsheet di Google Spreadsheets dengan kolom-kolom yang sesuai dengan data yang ingin ditampilkan (foto, nama, alamat, iuran, dll.).
2. Dapatkan link spreadsheet dari Google Spreadsheets.
3. Masukkan link spreadsheet di file `ApiConfig.kt`.
4. Tambahkan dependencies berikut di file `build.gradle` pada module `app`:

```
dependencies {
  ...
    implementation("androidx.recyclerview:recyclerview:1.3.2")
    implementation("com.github.bumptech.glide:glide:4.11.0")
    implementation("com.loopj.android:android-async-http:1.4.9")

    implementation("com.google.code.gson:gson:2.8.9")

    implementation("com.squareup.retrofit2:retrofit:2.6.4")
    implementation("com.squareup.retrofit2:converter-gson:2.6.4")

    implementation("com.squareup.okhttp3:logging-interceptor:3.8.0")
    debugImplementation("com.github.chuckerteam.chucker:library:3.3.0")
}
```

5. Build dan jalankan aplikasi di Android Studio.

**Catatan:**

* Pastikan data di spreadsheet sudah terstruktur dengan benar.
* Untuk menambahkan foto warga, upload foto ke Google Drive dan masukkan link fotonya di kolom spreadsheet.

**Link:**

* Youtube: [https://youtu.be/](https://youtu.be/61YldLe2ZFo)
* Laporan PDF: [https://drive.google.com/](https://drive.google.com/file/d/1uZyfI8NnE4GRZ-pMU7uHtjWuHqdcXszu/view?usp=sharing)

**Referensi:**

* API Spreadsheets: [https://www.apispreadsheets.com/](https://www.apispreadsheets.com/)
* Membuat Aplikasi Android dengan Kotlin: [https://developer.android.com/courses/kotlin-bootcamp/overview](https://developer.android.com/courses/kotlin-bootcamp/overview)

**Terima kasih!**

Terima kasih telah membaca penjelasan ini hingga akhir. Kami harap penjelasan ini bermanfaat dan membantu kalian memahami cara kerja aplikasi ini. 😉

