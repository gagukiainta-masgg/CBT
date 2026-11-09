# Panduan Hosting & Update Aplikasi "mas GG CBT Pro"

Paket ini berisi file siap rilis (**production-ready**) untuk platform simulator ujian **mas GG CBT**:
1. `index.html` — Aplikasi utama mandiri (sudah mencakup seluruh kode HTML, CSS, JavaScript, rumus LaTeX/KaTeX, ekstrak PDF.js, logo **mas GG**, serta 60 butir soal & gambar OSN-K IPA SD 2025).
2. `template_paket_soal_masGG.json` — Contoh file template JSON untuk upload paket soal baru.
3. `template_paket_soal_masGG.csv` — Contoh file template CSV (bisa dibuka dan diedit di Microsoft Excel / Google Sheets).

---

## A. Cara Meng-online-kan Pertama Kali (Gratis & Profesional)

### Opsi 1: Menggunakan Cloudflare Pages (Paling Direkomendasikan — Bandwidth Unlimited)
1. Ekstrak (Unzip) file `masgg-cbt-deploy.zip` ini di komputer Anda sehingga menjadi satu folder bernama `masgg-cbt`.
2. Buka [https://dash.cloudflare.com/](https://dash.cloudflare.com/) dan daftar/masuk gratis.
3. Di menu sebelah kiri, pilih **Workers & Pages** -> klik tombol **Create** -> pilih tab **Pages** -> klik **Upload assets**.
4. Beri nama proyek Anda, misalnya: `masgg-cbt` (nanti alamat web Anda menjadi `https://masgg-cbt.pages.dev`).
5. Tarik (*drag and drop*) folder hasil ekstrak tadi (yang berisi `index.html`), lalu klik **Deploy site**.
6. Dalam 10 detik aplikasi **mas GG CBT** Anda sudah online dan bisa diakses dari HP maupun laptop di seluruh Indonesia.

### Opsi 2: Menggunakan Netlify Drop (Super Cepat Tanpa Konfigurasi)
1. Ekstrak (Unzip) file `masgg-cbt-deploy.zip` menjadi satu folder.
2. Buka [https://app.netlify.com/drop](https://app.netlify.com/drop).
3. Tarik (*drag and drop*) folder tersebut langsung ke kotak di layar. Website langsung aktif seketika.

---

## B. Cara Meng-update Kode / Revisi di Kemudian Hari (Sangat Mudah!)

Aplikasi ini **100% mendukung update dan evaluasi berkala** kapan saja tanpa mengubah alamat link website Anda:

### 1. Jika Ada Revisi Fitur / Desain / Kode Aplikasi
* Anda cukup meminta revisi atau penambahan fitur di ruang chat Gemini ini (atau mengunggah kembali file `index.html` Anda ke chat ini untuk dimodifikasi).
* Setelah saya memberikan file `index.html` (atau `.zip`) versi terbaru:
  * **Di Cloudflare Pages:** Masuk ke proyek `masgg-cbt` Anda -> klik **Create new deployment** -> unggah file `index.html` yang baru -> klik **Save and Deploy**. Link ujian siswa **tetap sama** (`https://masgg-cbt.pages.dev`) dan otomatis menampilkan versi terbaru!
  * **Di Netlify:** Masuk ke menu **Deploys** -> tarik (*drag & drop*) folder/file baru ke kotak *Need to update your site? Drag and drop your site output folder here*.

### 2. Jika Ingin Menambah Paket Soal Baru Secara Permanen (Agar Muncul di Semua Perangkat Siswa)
* Masuk sebagai **Admin** di aplikasi (`ID Pengguna: admin`, `Kode Akses: admin123`).
* Buka menu **📤 Upload & Template** (unggah file PDF/CSV/JSON soal baru) atau **🛠️ Kroscek Developer & Gemini AI** (untuk memperbaiki pembahasan/kunci jawaban).
* Klik tombol **💾 Export Paket Aktif (.json)** untuk menyimpan hasil perbaikannya, atau minta saya di chat ini untuk menanamkan paket soal baru tersebut langsung ke dalam `index.html` utama Anda.

---

## C. Informasi Login Default
* **Login Peserta (User):**
  * **Nama Lengkap / ID Pengguna:** Bebas (nama siswa masing-masing)
  * **Kode Akses:** Kosongkan
* **Login Administrator / Developer (Rahasia):**
  * **ID Pengguna:** `admin`
  * **Kode Akses / Kata Sandi:** `admin123`
