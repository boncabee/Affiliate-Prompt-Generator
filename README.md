# Affiliate Prompt Generator 🚀

**Sistem Pintar Pembuat Prompt Kreatif Berurutan Khusus Foto, Video & Suara Menggunakan Pemrosesan Riil Gemini AI.**

Aplikasi berbasis web ini dirancang untuk membantu pemasar afiliasi (*affiliate marketers*) membuat storyboard promosi video 30 detik secara instan dan kohesif. Dengan memanfaatkan kekuatan model AI terbaru dari Google Gemini, generator ini menyusun narasi logis dari pembuka (*hook*), detail produk, demonstrasi produk, hingga ajakan bertindak (*call-to-action*).

---

## 🌟 Fitur Utama

- **Live Gemini AI Integration**: Terintegrasi langsung dengan API resmi Google Generative Language.
- **Model Selector**: Memungkinkan pengguna memilih model AI secara fleksibel (`gemini-1.5-flash`, `gemini-2.0-flash`, `gemini-2.5-flash`, dan `gemini-1.5-pro`).
- **Multimodal Product Photo Analysis**: Menganalisis foto produk yang diunggah pengguna (Langkah 1) menggunakan kemampuan multimodal Gemini AI guna menghasilkan 8 rekomendasi latar (*setting*) dan 8 suasana (*vibe*) yang sangat sesuai di Langkah 2.
- **Strategi & Gaya Promosi Kustom**: Pilihan gaya visual AI (*Photorealistic, Cinematic, Studio, dll.*) serta gaya suara voiceover (*Percakapan, Berwibawa, Ceria, dll.*).
- **Tag Placeholder Kustom (Karakter & Produk)**: Pilihan untuk menggunakan tag `[PROTAGONIST_MODEL]` dan `[PRODUCT_PLACEHOLDER]` guna menyederhanakan penyalinan prompt ke dalam template kerja.
- **Navigasi Cerdas & Hemat Token**: Jika pengguna telah membuat prompt dan kembali ke halaman strategi, aplikasi menyediakan tombol pintas kembali ke hasil sebelumnya tanpa memicu pemanggilan ulang API Gemini (mengurangi pemakaian token secara drastis).
- **Protokol Preview Tanpa API Key (Fallback Mock)**: Memungkinkan pengujian alur kerja aplikasi secara penuh tanpa memblokir pengguna jika API Key belum dikonfigurasi.
- **Clean Storyboard Export**: Hasil keluaran terbagi ke dalam 5 scene terstruktur yang dilengkapi tombol salin cepat untuk Prompt Gambar, Prompt Video, dan Naskah Suara (VO).
- **UI/UX Premium & Responsif**: Tampilan modern, transisi langkah animasi halus, status progress bar intuitif, serta penataan tata letak otomatis untuk mobile dan tablet.

---

## 🛠️ Tech Stack

Aplikasi ini dibangun menggunakan teknologi modern tingkat produksi:

1. **Frontend**: React 18, TypeScript (Type-safe strict mode), Tailwind CSS v3.
2. **Icons**: Lucide React.
3. **Build Tool & Dev Server**: Vite.
4. **Integration**: Google Generative AI REST API.

---

## 📂 Struktur Folder Proyek

Restrukturisasi proyek mengikuti standar produksi React:

```text
Affiliate-Prompt-Generator/
├── .git/                  # Repositori Git lokal
├── node_modules/          # Dependensi Node.js
├── src/                   # Source Code Utama
│   ├── App.tsx            # Komponen utama & state logic aplikasi
│   ├── main.tsx           # Entry point mounting React
│   └── index.css          # Setup stylesheet & Tailwind directives
├── index.html             # Template HTML dasar (mengarah ke /src/main.tsx)
├── tsconfig.json          # Konfigurasi compiler TypeScript
├── vite.config.ts         # Konfigurasi server & build Vite
├── tailwind.config.js     # Konfigurasi utilitas Tailwind CSS
├── postcss.config.js      # Integrasi plugin PostCSS
├── package.json           # File konfigurasi package & dependensi proyek
├── .gitignore             # Pengabaian file build & node_modules
└── README.md              # Dokumentasi lengkap proyek
```

---

## 🚀 Panduan Instalasi & Penggunaan Lokal

### Prasyarat
Pastikan Anda sudah menginstal [Node.js](https://nodejs.org/) (versi 18+) di komputer Anda.

### 1. Kloning Repositori & Masuk Direktori
```bash
git clone https://github.com/boncabee/Affiliate-Prompt-Generator.git
cd Affiliate-Prompt-Generator
```

### 2. Instal Dependensi
```bash
npm install
```

### 3. Jalankan Server Pengembangan
```bash
npm run dev
```
Aplikasi akan secara otomatis terbuka di peramban pada alamat `http://localhost:3000/`.

### 4. Build untuk Produksi
```bash
npm run build
```
Hasil kompilasi siap pakai untuk hosting statis akan berada di dalam direktori `dist/`.

---

## ⚙️ Konfigurasi API

1. Dapatkan API Key Gemini gratis melalui [Google AI Studio](https://aistudio.google.com/).
2. Masukkan API Key Anda pada kartu konfigurasi di bagian atas aplikasi. API Key disimpan dengan aman di penyimpanan lokal peramban Anda (`localStorage`).
3. Jika tidak menggunakan API Key, aplikasi secara otomatis berjalan dalam **Mode Preview (Mock)** menggunakan generator mock data cerdas untuk menayangkan demo storyboard.

---

## 🤝 Kontribusi

Kontribusi selalu diterima! Silakan buka *issue* baru atau ajukan *pull request* untuk meningkatkan kinerja, memperbaiki bug, atau menambahkan fitur baru pada aplikasi ini.

---

## 📝 Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE).