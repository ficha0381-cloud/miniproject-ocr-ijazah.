# miniproject-ocr-ijazah.
# Mini Project: OCR Nomor Ijazah dan Deteksi Indikasi Tanda Tangan

## 1. Deskripsi Proyek

Mini project ini dibuat untuk menerapkan pengolahan citra digital dalam membaca nomor ijazah menggunakan Optical Character Recognition (OCR) serta mendeteksi indikasi tinta pada area tanda tangan kepala sekolah.

Proyek ini menggunakan Python dan beberapa library pengolahan citra untuk meningkatkan kualitas gambar sebelum dilakukan proses OCR. Pengujian dilakukan pada sembilan gambar dengan kondisi kualitas yang berbeda, seperti gambar buram, kontras rendah, noise tinggi, resolusi rendah, dan kompresi JPEG.


## 2. Metode yang Digunakan

Metode yang digunakan dalam proyek ini meliputi:

1. **Grayscale**
   Mengubah gambar berwarna menjadi gambar abu-abu untuk menyederhanakan proses pengolahan citra.

2. **CLAHE (Contrast Limited Adaptive Histogram Equalization)**
   Meningkatkan kontras lokal gambar agar karakter nomor ijazah lebih mudah terlihat, terutama pada gambar dengan kontras rendah.

3. **Denoising**
   Mengurangi noise atau bintik-bintik pada gambar sehingga karakter lebih mudah dikenali oleh sistem OCR.

4. **Adaptive Thresholding**
   Mengubah gambar menjadi hitam-putih berdasarkan kondisi pencahayaan lokal untuk membantu memisahkan karakter dari latar belakang.

5. **Region of Interest (ROI)**
   Memotong bagian gambar yang berisi nomor ijazah dan area tanda tangan agar pemrosesan lebih terfokus.

6. **Optical Character Recognition (OCR)**
   Menggunakan Tesseract OCR untuk membaca dan mengekstrak angka dari area nomor ijazah.

7. **Character Error Rate (CER)**
   Digunakan untuk mengukur tingkat kesalahan hasil OCR dengan membandingkan teks hasil pengenalan terhadap nomor ijazah acuan (*ground truth*). Semakin rendah nilai CER, semakin akurat hasil pengenalan karakter.

8. **Deteksi Indikasi Tinta Tanda Tangan**
   Dilakukan dengan menghitung rasio piksel gelap pada area tanda tangan. Hasilnya digunakan sebagai indikator sederhana adanya tinta, bukan untuk membuktikan keaslian tanda tangan.

## 3. Hasil dan Analisis Enhancement Berdasarkan CER

Evaluasi dilakukan menggunakan Character Error Rate (CER) untuk mengetahui seberapa akurat hasil OCR dalam membaca nomor ijazah setelah proses preprocessing.

Nilai CER dihitung dengan membandingkan hasil OCR dengan nomor ijazah acuan yang telah ditentukan. Metode enhancement dengan nilai CER rata-rata paling rendah dianggap paling efektif untuk dataset yang diuji karena menghasilkan kesalahan pengenalan karakter yang lebih sedikit.

**Hasil eksperimen:**

* Metode enhancement paling efektif: **[isi nama metode dengan CER terendah]**
* Nilai rata-rata CER: **[isi nilai CER dari hasil eksperimen]**

Berdasarkan hasil evaluasi, metode **[nama metode]** memperoleh nilai CER paling rendah dibandingkan metode lainnya. Hal ini menunjukkan bahwa metode tersebut memberikan hasil pengenalan nomor ijazah yang paling akurat pada dataset pengujian.

Hasil ini terbatas pada gambar dan pengaturan eksperimen yang digunakan. Metode dengan CER terendah belum tentu memberikan hasil terbaik pada semua jenis dokumen atau kondisi gambar.

## 4. Dataset

Dataset terdiri dari sembilan gambar dengan variasi kualitas, yaitu:

* Gambar berkualitas tinggi
* Gambar dengan kontras rendah
* Gambar buram
* Gambar dengan noise tinggi
* Gambar beresolusi rendah
* Gambar dengan pencahayaan rendah
* Gambar dengan perubahan warna
* Gambar dengan artefak kompresi JPEG
* Gambar dengan gabungan beberapa gangguan kualitas

Dataset digunakan untuk menguji kemampuan preprocessing dan OCR dalam menghadapi variasi kualitas citra.


## 5. Teknologi dan Library

Proyek ini menggunakan:

* Python
* Google Colab
* OpenCV
* Tesseract OCR
* Pytesseract
* NumPy
* Pandas
* Matplotlib
* Jiwer

## 6. Output Program

Output dari program ini meliputi:

* Hasil preprocessing gambar.
* Hasil ekstraksi nomor ijazah menggunakan OCR.
* Indikasi tinta pada area tanda tangan.
* Nilai CER untuk mengevaluasi akurasi OCR.
* Tabel ringkasan hasil eksperimen.
* File CSV hasil evaluasi.

**7. Cara Menjalankan Program (How to Run)**

Program dijalankan menggunakan Google Colab. Berikut langkah-langkahnya:

Buka https://colab.research.google.com/.
Unggah atau buka file notebook proyek dengan format .ipynb.
Jalankan sel instalasi library dan impor seluruh library yang dibutuhkan.
Unggah sembilan gambar dataset ketika diminta oleh program.
Jalankan setiap sel kode secara berurutan dari awal hingga akhir.
Periksa hasil preprocessing dan hasil pembacaan nomor ijazah menggunakan OCR.
Jalankan evaluasi CER untuk membandingkan hasil OCR dengan nomor ijazah acuan.
Periksa tabel ringkasan dan visualisasi hasil evaluasi.
Unduh file CSV hasil eksperimen jika diperlukan.

## 8. Kesimpulan

Proyek ini menunjukkan penerapan pengolahan citra digital dan OCR untuk membantu membaca nomor ijazah pada gambar dengan kondisi kualitas yang berbeda. Metode preprocessing digunakan untuk meningkatkan keterbacaan karakter sebelum proses OCR dilakukan.

Efektivitas metode enhancement dievaluasi menggunakan CER. Metode dengan nilai CER rata-rata paling rendah dipilih sebagai metode paling efektif berdasarkan hasil eksperimen. Evaluasi ini membantu mengetahui pengaruh preprocessing terhadap akurasi pengenalan karakter.

Deteksi tinta tanda tangan hanya digunakan sebagai indikasi sederhana berdasarkan piksel gelap, sehingga tidak dapat digunakan untuk memastikan keaslian tanda tangan.
