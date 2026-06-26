# Fisika Komputasi: Simulasi Model Ising 2D via Algoritma Metropolis
Selamat datang dalam tugas studi kasus komprehensif mengenai Model Ising 2 Dimensi (2D) dan Transisi Fasa Kelompok HeLo. Dalam tugas ini, kami akan menerapkan algoritma Monte Carlo Metropolis untuk mensimulasikan sistem kisi magnetik dua dimensi dan mengamati bagaimana perilaku kolektif partikel memicu terjadinya magnetisasi spontan serta transisi fasa makroskopis.
## Tujuan
membangun program simulasi, melakukan analisis matematis serta komputasional terhadap Model Ising 2D pada tiga rentang suhu yang berbeda di dalam Jupyter Notebook, kemudian memublikasikan hasil temuan sebagai portofolio web publik menggunakan GitHub Pages
## Kelompok HeLo
1. Loza Asmi Nahara Maharani - 01241011
2. Putri Herawati - 01241018
## Simulasi dan Analisis Kasus
Proses pengerjaan dilakukan dengan membuat berkas Jupyter Notebook baru di dalam direktori `notebooks/`. Implementasi algoritma Metropolis dilakukan secara mandiri yang mencakup pemilihan spin acak, perhitungan perubahan energi lokal ($\Delta E$) secara efisien, serta penerapan kriteria penerimaan Metropolis.

Analisis dibagi ke dalam tiga studi kasus berdasarkan kondisi termodinamika sistem:
* **Kasus 1: Fase Feromagnetik ($T = 1.0$)** – Mensimulasikan sistem di bawah suhu kritis ($T < T_c$). Mengamati bagaimana spin individu berorientasi searah secara spontan untuk membentuk domain magnetik yang seragam, sehingga nilai mutlak magnetisasi rata-rata mendekati satu ($|M| \approx 1$).
* **Kasus 2: Transisi Fasa & Kritikalitas ($T = 2.27$)** – Mengamati perilaku sistem pada titik suhu kritis teoritis ($T_c \approx 2.27$). Analisis fluktuasi kritis yang terjadi, pembentukan pola domain fraktal, dan runtuhnya keteraturan jarak jauh.
* **Kasus 3: Fase Paramagnetik ($T = 4.0$)** – Meneliti sistem pada rentang suhu tinggi ($T > T_c$). Menunjukkan bagaimana energi termal mendominasi interaksi antar-spin sehingga arah spin menjadi acak dan nilai magnetisasi rata-rata mendekati nol.  
Untuk setiap studi kasus di atas, wajib untuk:
  * Menginisialisasi kisi $N \times N$ (dengan $N = 20$) menggunakan konfigurasi acak (*Hot Start*) untuk merepresentasikan entropi maksimum sistem.
  * Menjalankan minimal 200.000 langkah Monte Carlo untuk memastikan sistem telah mencapai kesetimbangan termal sebelum pengumpulan data makrostate dilakukan.
  * Menghitung nilai magnetisasi rata-rata secara berkala (setiap 100 langkah).
  * Menampilkan visualisasi keadaan akhir kisi spin menggunakan peta warna biner (`cmap='binary'`) berdampingan dengan kurva riwayat magnetisasi rata-rata sepanjang fungsi waktu simulasi.
  * Menyusun interpretasi fisis ilmiah yang mendalam mengenai mekanika statistik yang mendasari fenomena tersebut menggunakan sel Markdown.
### Penggunaan AI (*Artificial Intelligence*)
Pada pengerjaan proyek *case-based* simulasi Model Ising 2D ini, kami memanfaatkan teknologi *Large Language Model* (LLM) sebagai alat bantu, yaitu:
* **Gemini 3.1 Pro (Google):** Digunakan untuk membantu optimasi sintaksis algoritma Metropolis pada potongan kode simulasi demi efisiensi perhitungan energi lokal, memberikan saran implementasi kode yang bersih, serta membantu pemformatan penulisan rumus fisika ke dalam standar $\LaTeX$.
* **Claude Sonnet 4.6 (Anthropic):** Digunakan secara komplementer untuk memvalidasi konsep fisika tingkat lanjut pada Model Ising seperti fenomena transisi fase, patah simetri spontan, penurunan persamaan energi lokal, serta membantu penataan komponen dokumen Markdown agar tersusun secara sistematis.
### Perangkat Lunak dan Lingkungan Komputasi

Proses perancangan kode, eksekusi simulasi Model Ising 2D, hingga penyusunan laporan akhir memanfaatkan ekosistem perangkat lunak dan lingkungan komputasi berikut:

* **Visual Studio Code (VS Code):** Digunakan sebagai editor utama untuk menulis, mengedit, dan menjalankan program Python, serta mempermudah proses *debugging* logika simulasi.
* **Jupyter Notebook:** Digunakan untuk menyusun laporan berbasis *literate programming* yang menggabungkan penjelasan teori, kode program, hasil simulasi, dan visualisasi grafik dalam satu dokumen terintegrasi.
* **Python 3.x beserta Library Ekosistem:** Digunakan sebagai bahasa pemrograman utama yang didukung oleh beberapa pustaka standar komputasi saintifik:
  * **NumPy:** Digunakan untuk mengolah data matriks dua dimensi sebagai representasi kisi spin serta mengoptimalkan perhitungan numerik.
  * **Matplotlib:** Digunakan untuk membuat visualisasi konfigurasi spasial spin akhir dan grafik riwayat magnetisasi secara rapi.
  * **Random:** Pustaka bawaan yang digunakan untuk menghasilkan bilangan acak pada pemilihan koordinat kisi dan evaluasi kriteria Metropolis.
* **GitHub dan GitHub Desktop:** Digunakan sebagai sistem kontrol versi (*Version Control System*) untuk menyimpan riwayat perubahan kode secara aman serta mengelola dokumentasi proyek secara publik.
