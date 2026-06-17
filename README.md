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
