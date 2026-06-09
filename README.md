# ILoveKuantanPDF
Aplikasi web lokal (100% client-side) untuk menyisipkan stempel, tanda tangan, banner footer BSrE, dan tata letak TTE pada dokumen PDF (Tunggal, Massal, &amp; Ijazah Elektronik) secara presisi tanpa unggah server.

### 🌐 Akses Aplikasi Online
Anda dapat langsung mencoba dan menggunakan aplikasi ini melalui tautan berikut:
* **[🔗 Aplikasi Utama (Penyisip Gambar & Footer PDF)](https://aldesfi.github.io/ILoveKuantanPDF/add_image.html)**
* **[🔗 Aplikasi Pendukung (Pembuat Gambar TTE)](https://aldesfi.github.io/ILoveKuantanPDF/create_tte_image)**

# ILoveKuantanPDF 📄✨

**ILoveKuantanPDF** adalah aplikasi berbasis web (*client-side*) modern yang dirancang untuk mempermudah penyisipan aset gambar—seperti stempel resmi, tanda tangan digital, banner footer Sertifikasi Elektronik (BSrE), hingga **keperluan tata letak Dokumen Akademik seperti Ijazah Elektronik / TTE**—ke dalam dokumen PDF secara presisi. Aplikasi ini mendukung pemrosesan berkas tunggal dengan pratinjau langsung (*live preview*) maupun pemrosesan massal (*bulk process*).

Seluruh pemrosesan dokumen dilakukan secara **100% lokal di dalam peramban (browser) pengguna**. Tidak ada data berkas atau dokumen penting (seperti ijazah atau transkrip nilai) yang diunggah ke server luar, menjadikannya sangat aman dan menjaga kerahasiaan dokumen kedinasan/pribadi.

---

## 🔷 Fitur Utama

* **Penyisipan Gambar Multi-Layer:** Menyisipkan dua jenis aset gambar sekaligus (Gambar Utama & Banner Footer) dalam satu kali proses.
* **Akurasi Posisi Dua Arah:** Pengaturan dimensi (Lebar/Tinggi) dan koordinat posisi (X/Y) menggunakan kombinasi *slider* interaktif dan input angka manual (*pixel-perfect*). Sangat krusial untuk penempatan stempel/TTE pada ruang terbatas di lembar Ijazah/Sertifikat.
* **Pratinjau Langsung (Live Preview):** Simulasi peletakan gambar secara langsung di halaman pertama dokumen PDF sebelum dieksport.
* **Pemrosesan Massal (Bulk Process):** Memproses banyak file PDF sekaligus dalam satu antrean terminal internal dengan fitur unduh otomatis (*auto-download*). Cocok untuk penerbitan Ijazah atau Sertifikat massal.
* **Tanpa Ketergantungan Server (Serverless):** Memanfaatkan daya komputasi lokal menggunakan JavaScript modern.

---

## 📦 Pustaka & Library yang Digunakan

Proyek ini dibangun menggunakan pustaka sumber terbuka (*open-source*) terpercaya. Hak cipta dari masing-masing pustaka sepenuhnya dimiliki oleh pengembang aslinya dengan rincian lisensi sebagai berikut:

| Nama Pustaka | Kegunaan | Lisensi | Tautan Resmi |
| :--- | :--- | :--- | :--- |
| **PDF-LIB** (v1.17.1) | Modifikasi struktur file PDF, injeksi objek gambar, dan penyimpanan hasil enkapsulasi dokumen baru. | **MIT License** | [GitHub pdf-lib](https://github.com/Hopding/pdf-lib) |
| **PDF.js** (v3.4.120) | Melakukan *rendering* dan membedah dokumen PDF lama ke dalam elemen `<canvas>` HTML5 untuk keperluan pratinjau. | **Apache License 2.0** | [GitHub pdf.js](https://github.com/mozilla/pdf.js) |
| **Tailwind CSS** (v4) | Kerangka kerja utilitas CSS (*utility-first*) untuk membangun antarmuka pengguna (UI) yang responsif dan estetis. | **MIT License** | [Tailwind CSS](https://tailwindcss.com/) |

---

## ⚖️ Kepatuhan Hak Cipta & Lisensi Aset

Untuk memastikan aplikasi ini bebas dari isu pelanggaran hak cipta (*copyright infringement*):

1. **Kode Sumber Aplikasi:** Dikembangkan secara mandiri dengan memanfaatkan pustaka pihak ketiga berlisensi open-source resmi (**MIT** dan **Apache 2.0**). Kedua lisensi ini secara legal mengizinkan penggunaan, modifikasi, dan pendistribusian ulang kode untuk keperluan personal maupun komersial secara gratis.
2. **Kemandirian Perangkat Lunak & Fungsi TTE:** Aplikasi ini bertindak sebagai alat bantu utilitas/tata letak visual (*visual placer*). Aplikasi ini **tidak memalsukan ataupun menerbitkan** sertifikat digital/kriptografi TTE. Proses penandatanganan elektronik tersertifikasi (untuk Ijazah/Dokumen Resmi) tetap harus melalui otoritas resmi seperti BSrE / BSSN atau aplikasi penandatangan resmi instansi masing-masing.

---

## 🚀 Cara Menjalankan Aplikasi

Karena aplikasi ini sepenuhnya berbasis *client-side*, tidak diperlukan proses instalasi server, Node.js, ataupun database.

1.  Unduh atau salin kode file `index.html`.
2.  Buka berkas `index.html` tersebut menggunakan peramban web modern pilihan Anda (Google Chrome, Mozilla Firefox, Microsoft Edge, atau Safari).
3.  Aplikasi siap digunakan langsung, bahkan dalam kondisi **tanpa jaringan internet (offline)** jika aset library telah ter-caching dengan baik.

---

## 📌 Catatan Teknis Penggunaan Koordinat
Sistem tata letak file pada spesifikasi PDF murni menggunakan sistem kartesius di mana titik awal **koordinat (0,0) dimulai dari pojok KIRI-BAWAH kertas**, bukan dari kiri-atas seperti pada standarisasi elemen koordinat HTML CSS pada umumnya. Perhatikan dokumen seperti Ijazah yang memiliki orientasi Landscape agar penyesuaian nilai X dan Y disesuaikan dengan lebar kertas dokumen tersebut.