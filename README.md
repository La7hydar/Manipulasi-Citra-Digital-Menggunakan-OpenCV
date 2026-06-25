# Manipulasi Citra Digital Menggunakan OpenCV 📸

Proyek ini merupakan bagian dari tugas individu mata kuliah **Pengolahan Sinyal Digital**. Eksperimen ini berfokus pada implementasi manipulasi dasar citra digital menggunakan Python dan OpenCV, serta analisis matematis terhadap perubahan nilai piksel, *brightness*, *contrast*, dan detail spasial citra.

## 👤 Identitas Mahasiswa
* **Nama:** Ahnaf Haidar
* **NIM:** 452024611107
* **Mata Kuliah:** Pengolahan Sinyal Digital

---

## 🚀 Fitur & Modul Eksperimen
Eksperimen dilakukan secara terstruktur melalui beberapa tahapan manipulasi citra berikut:
1. **Membaca & Menampilkan Citra:** Membaca berkas gambar asli dan menganalisis metadatanya (*shape, tipe data, min/max pixel*).
2. **Konversi Warna (BGR ke RGB):** Mengatasi perbedaan urutan kanal warna bawaan OpenCV agar representasi visual sesuai di Matplotlib.
3. **Resize Citra:** Menyelaraskan dimensi ordo dari dua citra berbeda menjadi ukuran yang sama ($600 \times 400$ piksel).
4. **Image Blending:** Menggabungkan dua citra menggunakan fungsi penjumlahan linear terbobot (`cv.addWeighted`) dengan berbagai variasi parameter $\alpha$ dan $\beta$.
5. **Image Negative:** Melakukan transformasi inversi warna menggunakan operasi pengurangan linear ($s = 255 - r$).
6. **Transformasi Logaritmik:** Meregangkan kontras pada area gelap menggunakan fungsi logaritma ($s = c \times \log(1 + r)$) dengan konversi tipe data untuk mencegah *overflow*.
7. **Transformasi Gamma (Power-Law):** Melakukan perbaikan kecerahan secara dinamis ($s = c \times r^\gamma$) dengan menguji 4 variasi nilai gamma ($\gamma = 0.4, 0.7, 1.5,$ dan $2.5$).

---

## 📂 Struktur Repositori
```text
├── image1.jpg               # Citra uji 1 (Lena)
├── image2.jpg               # Citra uji 2 (Baboon)
├── tugas_manipulasi_citra.ipynb  # Notebook eksperimen utama (Kaggle/Jupyter)
└── README.md                # Dokumentasi proyek
