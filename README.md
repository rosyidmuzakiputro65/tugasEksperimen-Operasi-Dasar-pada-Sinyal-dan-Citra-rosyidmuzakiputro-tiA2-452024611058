# tugasEksperimen-Operasi-Dasar-pada-Sinyal-dan-Citra-rosyidmuzakiputro-tiA2-452024611058
## 1. Judul Project
**Implementasi Operasi Dasar Sinyal 1D / Citra 2D & Validasi Matematis Sistem Linier**

## 2. Nama Mahasiswa
* **Nama:** Rosyid Muzaki Putro
* **Kelas:** A2
* **NIM:** 452024611058

## 3. Deskripsi Singkat Project
Project ini merupakan perangkat simulasi dan analisis berbasis Python Jupyter Notebook untuk memenuhi modul praktikum Pengolahan Sinyal Digital (PSD). Fokus utama dari project ini adalah mengeksplorasi bagaimana operasi aljabar dasar (penjumlahan, penggeseran/translasi, dan amplifikasi/penskalaan) memengaruhi struktur data satu dimensi (sinyal audio/sinusoidal diskrit) dan dua dimensi (matriks citra digital). Selain itu, proyek ini menyediakan skrip pengujian berbasis kode untuk membuktikan prinsip **Homogenitas** dan **Additivitas** pada sistem linier versus non-linier.

## 4. Library yang Digunakan
* **NumPy:** Digunakan untuk manipulasi array N-dimensi, kalkulasi matriks cepat, dan operasi element-wise sinyal/citra.
* **Matplotlib (Pyplot):** Digunakan untuk visualisasi plot sinyal diskrit (stem plot) dan visualisasi histogram citra.
* **OpenCV (cv2):** Digunakan untuk membaca gambar, melakukan penyelarasan dimensi citra (*resizing*), translasi citra, dan penanganan saturasi intensitas (*clipping via cv2.add*).

## 5. Cara Menjalankan Notebook
1. **Persiapan Lingkungan (Environment):**
   Pastikan Anda telah menginstal Python 3.x dan pengelola paket `pip`.
2. **Instalasi Dependensi:**
   Buka terminal atau command prompt, lalu jalankan perintah berikut:
   ```bash
   pip install numpy matplotlib opencv-python jupyter
   Menjalankan Jupyter Notebook:Arahkan terminal ke direktori project ini dan ketik:Bashjupyter notebook
Eksekusi Kode:Buka file Eksperimen_PSD_452024611058.ipynb melalui dashboard Jupyter, lalu jalankan setiap cell secara berurutan (Shift + Enter).

6. Struktur Folder ProjectPlaintext📦 psd-operasi-dasar-sinyal
 ┣ 📂 data
 ┃ ┗ 📜 citra_uji.png               # File gambar asli (dimensi 512x512 piksel)
 ┣ 📂 output
 ┃ ┗ 📜 laporan_eksperimen.pdf      # Dokumen laporan resmi yang di-generate
 ┣ 📜 Eksperimen_PSD_452024611058.ipynb # Jupyter Notebook utama berisi source code
 ┗ 📜 README.md                     # File dokumentasi utama project (file ini)

7. Ringkasan Hasil EksperimenSinyal 1D:
Penjumlahan dengan unit step mengakibatkan pergeseran sumbu referensi (DC offset) sebesar +1 pada indeks $n \ge 5$. Penggeseran nilai $k > 0$ menggeser grafik ke kanan (time-delay), dan nilai $\alpha$ mengalikan amplitudo secara linear (faktor negatif membalik fase sebesar $180^\circ$).Citra 2D: Operasi penjumlahan meningkatkan kecerahan (brightness), di mana nilai $> 255$ mengalami integer overflow jika menggunakan matriks biasa atau terpotong rapi (clipping) pada nilai 255 menggunakan OpenCV. Operasi translasi sukses menggeser posisi koordinat objek namun meninggalkan area kosong berwarna hitam (nilai 0). Penskalaan dengan $\alpha$ mengubah kontras citra secara drastis melalui peregangan sebaran histogram.Uji Linieritas: Sistem $T_1(x) = 2x$ terbukti LINIER karena selisih homogenitas dan additivitasnya sama dengan 0. Sistem $T_2(x) = x^2$ terbukti NON-LINIER akibat munculnya komponen produk silang ($2x_1x_2$) pada hukum kuadrat penjumlahan.

8. Kesimpulan
SingkatEksperimen ini berhasil membuktikan secara komputasional dan teoretis bahwa manipulasi sinyal 1D dan 2D diatur secara ketat oleh hukum aljabar linear. Pemahaman mengenai batas nilai piksel (rentang uint8), penanganan clipping, serta pemenuhan prinsip superposisi pada sistem linier merupakan pondasi krusial dalam merancang aplikasi pengolahan sinyal dan pengenalan citra digital di dunia industri nyata.
