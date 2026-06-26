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
