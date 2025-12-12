# 🗳️ Sistem Pemilihan Kahima (E-Voting)

![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)
![Language](https://img.shields.io/badge/Language-PHP-blue?style=for-the-badge&logo=php&logoColor=white)
![Deployment](https://img.shields.io/badge/Deploy-Vercel-black?style=for-the-badge&logo=vercel&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-orange?style=for-the-badge)

**Sistem Pemilihan Kahima** adalah aplikasi *Electronic Voting* berbasis web yang dirancang untuk memodernisasi proses pemilihan Ketua Himpunan Mahasiswa. Aplikasi ini menggantikan metode konvensional (kertas) menjadi sistem digital yang **transparan, real-time, dan akurat**, serta menjamin prinsip **LUBER JURDIL** (Langsung, Umum, Bebas, Rahasia, Jujur, dan Adil).

---

## 📑 Daftar Isi

- [Overview Project](#-overview-project)
- [Fitur Utama (MVP)](#-fitur-utama-mvp)
- [Teknologi yang Digunakan](#-teknologi-yang-digunakan)
- [Struktur Project](#-struktur-project)
- [Skema Database](#-skema-database)
- [Cara Setup Local](#-cara-setup-local)
- [Cara Deploy ke Vercel](#-cara-deploy-ke-vercel)
- [Cara Kontribusi](#-cara-kontribusi)

---

## 📖 Overview Project

Proyek ini dibangun untuk mengatasi kendala dalam pemilihan manual seperti:
1.  **Inefisiensi:** Penghitungan suara manual yang memakan waktu lama.
2.  **Human Error:** Risiko kesalahan rekapitulasi data.
3.  **Kecurangan:** Potensi pemilih ganda atau surat suara tidak sah.

Sistem ini memastikan setiap mahasiswa hanya memiliki **satu hak suara** yang divalidasi melalui sistem login, dan hasil suara dapat dipantau secara langsung oleh publik setelah pemilihan ditutup.

---

## ✨ Fitur Utama (MVP)

Aplikasi ini mencakup fitur *Minimum Viable Product* (MVP) sebagai berikut:

### 👤 Panel Pemilih (User)
* **Secure Login:** Validasi akses menggunakan NIM dan Token/Password unik.
* **Kandidat Info:** Menampilkan profil, visi, dan misi setiap paslon.
* **One-Click Vote:** Antarmuka pemilihan yang mudah dan intuitif.
* **Vote Lock:** Akun otomatis terkunci setelah memberikan suara (mencegah *double vote*).

### 🛡️ Panel Admin
* **Dashboard Real-time:** Grafik perolehan suara (*Live Count*) yang update otomatis.
* **Manajemen Kandidat:** Tambah, Edit, dan Hapus data paslon (termasuk upload foto).
* **Manajemen DPT:** Import data Daftar Pemilih Tetap.
* **Kontrol Sesi:** Fitur untuk membuka atau menutup periode voting.
* **Rekapitulasi:** Export hasil pemilihan.

---

## 🛠 Teknologi yang Digunakan

*(Sesuaikan daftar ini dengan stack asli proyek Anda)*

-   **Frontend:** HTML5, CSS3, JavaScript (Chart.js untuk grafik).
-   **Backend:** PHP (Native/Laravel).
-   **Database:** MySQL / MariaDB.
-   **Tools:** Visual Studio Code, Git, XAMPP/Laragon.

---

## 📂 Struktur Project

```text
/
├── public/             # Aset publik (CSS, JS, Images)
├── src/                # Source code utama
│   ├── config/         # Konfigurasi koneksi database
│   ├── controllers/    # Logika backend (Auth, VoteController)
│   └── views/          # Tampilan antarmuka (UI)
├── database/           # File dump SQL (.sql)
├── index.php           # Entry point aplikasi
└── README.md           # Dokumentasi proyek

  ```
## Build your app

Continue building your app on:

**[https://v0.app/chat/projects/J9y1PaAyD02](https://v0.app/chat/projects/J9y1PaAyD02)**

## Skema Database

Sistem ini menggunakan relasi database sebagai berikut:
- users: Menyimpan data pemilih (NIM, Nama, Password, Status_Vote).
- candidates: Menyimpan data paslon (Nama, Visi, Misi, Foto, Jumlah_Suara).
- votes: Menyimpan rekam jejak suara masuk (User_ID, Candidate_ID, Timestamp).
- settings: Pengaturan sesi pemilihan (Waktu Buka/Tutup).

## 🤝 Cara Kontribusi

Kami sangat terbuka untuk kontribusi! Langkah-langkahnya:
- Fork repositori ini atau Git Clone.
- Buat Branch baru (git checkout -b fitur-baru).
- Commit perubahan Anda (git commit -m 'Menambahkan fitur log aktivitas').
- Push ke branch (git push origin fitur-baru).
- Buat Pull Request di GitHub.
   Changes are automatically pushed to this repository
4. Vercel deploys the latest version from this repository
