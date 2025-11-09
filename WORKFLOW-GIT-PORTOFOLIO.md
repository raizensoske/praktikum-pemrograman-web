# WORKFLOW GIT PORTOFOLIO WEBSITE

## Langkah 1: Persiapan dan Pembuatan Folder Project

**Tujuan:**  
Menyiapkan struktur awal folder project yang akan digunakan sebagai website portfolio.

**Langkah-langkah:**
1. Buka terminal atau Command Prompt.  
2. Buat folder baru untuk project portfolio dengan perintah berikut:

```bash
mkdir tugas-akhir
cd tugas-akhir
```

3. Buat dua file utama, yaitu `index.html` dan `style.css`.

**Struktur Folder Awal:**
```
portofolio-raizen/
├── index.html
├── style.css
└── assets/
```

---

## Langkah 2: Inisialisasi Repository Git

**Tujuan:**  
Membuat repository lokal agar setiap perubahan project dapat dicatat oleh Git.

**Perintah yang digunakan:**
```bash
git init
```

**Hasil:**  
Sebuah folder `.git` akan terbentuk secara otomatis, menandakan repository lokal berhasil dibuat.

---

## Langkah 3: Commit Awal (Struktur Dasar Website)

**Tujuan:**  
Membuat commit pertama yang berisi struktur dasar HTML dan CSS.

**Kode Sebelum:**
`index.html` (versi awal)
```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfolio Raizen</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
</body>
</html>
```

`style.css` (versi awal)
```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  color: #333;
}
```

**Perintah Git:**
```bash
git add .
git commit -m "Inisialisasi proyek: struktur dasar HTML dan CSS"
```

---

## Langkah 4: Penambahan Section Header dan Navigasi

**Tujuan:**  
Menambahkan bagian header dengan elemen navigasi utama.

**Kode Sebelum:**  
Bagian `<body>` masih kosong.

**Kode Sesudah:**
```html
<header>
  <div class="container header-inner">
    <h1 class="brand">raizen</h1>
    <nav>
      <a href="#about">Tentang</a>
      <a href="#projects">Proyek</a>
      <a href="#contact">Kontak</a>
    </nav>
  </div>
</header>
```

`style.css` tambahan:
```css
header {
  background: #004aad;
  color: white;
  padding: 1rem 0;
  text-align: center;
}
nav a {
  color: white;
  text-decoration: none;
  margin: 0 10px;
}
```

**Commit:**
```bash
git add index.html style.css
git commit -m "Menambahkan section header dan navigasi"
```

---

## Langkah 5: Penambahan Section About Me

**Tujuan:**  
Menambahkan bagian “Tentang Saya” berisi informasi pribadi.

**Kode Tambahan (index.html):**
```html
<section id="about">
  <h2>Tentang Saya</h2>
  <p>Saya Raizen, seorang mahasiswa IT yang sedang belajar web development menggunakan HTML dan CSS.</p>
</section>
```

**CSS Tambahan:**
```css
section {
  padding: 20px;
}
h2 {
  color: #004aad;
}
```

**Commit:**
```bash
git add index.html style.css
git commit -m "Menambahkan section About Me"
```

---

## Langkah 6: Penambahan Section Projects (Versi Awal)

**Tujuan:**  
Menampilkan daftar proyek sederhana.

**Kode Tambahan (index.html):**
```html
<section id="projects">
  <h2>Proyek Saya</h2>
  <ul>
    <li>Website Portfolio</li>
    <li>Sistem Informasi Akademik</li>
    <li>Desain UI Mobile App</li>
  </ul>
</section>
```

**CSS Tambahan:**
```css
ul {
  padding-left: 20px;
}
```

**Commit:**
```bash
git add index.html style.css
git commit -m "Menambahkan section Projects (versi awal)"
```

---

## Langkah 7: Penambahan Section Footer dan Kontak

**Tujuan:**  
Menambahkan bagian footer untuk informasi hak cipta dan kontak email.

**Kode Tambahan (index.html):**
```html
<footer id="contact">
  <p>Hubungi: <a href="mailto:raizen@example.com">raizen@example.com</a></p>
  <p>© 2025 Raizen. Semua hak dilindungi.</p>
</footer>
```

**CSS Tambahan:**
```css
footer {
  background-color: #f5f5f5;
  text-align: center;
  padding: 10px;
}
```

**Commit:**
```bash
git add index.html style.css
git commit -m "Menambahkan footer dan kontak"
```

---

## Langkah 8: Penambahan Responsivitas

**Tujuan:**  
Menambahkan aturan CSS agar tampilan website lebih responsif pada perangkat seluler.

**CSS Tambahan:**
```css
@media (max-width: 600px) {
  nav a {
    display: block;
    margin: 5px 0;
  }
}
```

**Commit:**
```bash
git add style.css
git commit -m "Menambahkan CSS responsif untuk tampilan mobile"
```

---

## Langkah 9: Pembuatan Branch `fitur-gallery`

**Tujuan:**  
Membuat branch baru untuk menambahkan fitur galeri proyek tanpa mengubah branch utama.

**Perintah:**
```bash
git branch fitur-gallery
git checkout fitur-gallery
```

**Hasil:**  
Branch baru bernama `fitur-gallery` telah dibuat dan aktif.

---

## Langkah 10: Penambahan Fitur Galeri Proyek (Sebelum & Sesudah)

**Tujuan:**  
Mengubah section Projects menjadi tampilan galeri dengan gambar dan deskripsi.

**Sebelum (index.html):**
```html
<section id="projects">
  <h2>Proyek Saya</h2>
  <ul>
    <li>Website Portfolio</li>
    <li>Sistem Informasi Akademik</li>
    <li>Desain UI Mobile App</li>
  </ul>
</section>
```

**Sesudah (index.html):**
```html
<section id="gallery">
  <h2>Galeri Proyek</h2>
  <div class="gallery-container">
    <div class="project-card">
      <img src="assets/project1.png" alt="Project 1">
      <p>Website Portofolio</p>
    </div>
    <div class="project-card">
      <img src="assets/project2.png" alt="Project 2">
      <p>Sistem Informasi Akademik</p>
    </div>
    <div class="project-card">
      <img src="assets/project3.png" alt="Project 3">
      <p>Desain UI Mobile App</p>
    </div>
  </div>
</section>
```

**CSS Tambahan:**
```css
.gallery-container {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: center;
}
.project-card {
  border: 1px solid #ccc;
  border-radius: 10px;
  width: 200px;
  text-align: center;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}
.project-card img {
  width: 100%;
  border-radius: 10px 10px 0 0;
}
```

**Commit:**
```bash
git add index.html style.css assets/project1.png assets/project2.png assets/project3.png
git commit -m "Menambahkan fitur galeri proyek dengan gambar dan styling"
```

---

## Langkah 11: Merge Branch ke Main

**Tujuan:**  
Menggabungkan branch `fitur-gallery` ke branch utama (`main`).

**Perintah:**
```bash
git checkout main
git merge fitur-gallery -m "Merge branch fitur-gallery ke main"
```

**Hasil:**  
Perubahan dari branch `fitur-gallery` telah tergabung ke `main`.

---

## Langkah 12: Push ke GitHub

**Tujuan:**  
Mengunggah repository ke GitHub agar dapat diakses secara publik.

**Langkah-langkah:**
1. Buat repository di GitHub dengan nama `portofolio-raizen` (public).
2. Hubungkan repository lokal ke GitHub.

```bash
git remote add origin https://github.com/<username>/portofolio-raizen.git
git branch -M main
git push -u origin main
```

---

## Langkah 13: Dokumentasi Riwayat Commit

**Tujuan:**  
Menampilkan riwayat commit dalam bentuk grafik untuk dilampirkan sebagai bukti.

**Perintah:**
```bash
git log --graph --oneline --all
```

**Contoh Output:**
```
*   4b6d2e1 (HEAD -> main, origin/main) Merge fitur-gallery ke main
|| * a8c913d (fitur-gallery) Menambahkan fitur galeri proyek dengan styling
* | 9aef412 Menambahkan footer dan kontak
* | 7a8e13f Menambahkan section About Me
* | 1c2e91d Menambahkan header dan navigasi
* | 7a8e13f Inisialisasi proyek awal
```

**Instruksi:**  
Ambil **screenshot hasil perintah di atas** dan simpan dengan nama `gitlog-screenshot.png`.

---

## Langkah 14: Checklist Pengumpulan dan Penutup

**File yang Dikumpulkan:**
1. Tautan repository GitHub (public).  
2. Screenshot hasil perintah `git log --graph --oneline`.  
3. File `README.md` berisi deskripsi proyek dan cara penggunaan.

**Penutup:**  
Workflow ini menggambarkan seluruh proses pengembangan website portfolio menggunakan Git secara terstruktur, mulai dari inisialisasi, pengembangan bertahap, percabangan fitur, hingga publikasi ke GitHub. Dokumentasi commit membantu menjaga riwayat pengembangan proyek agar mudah dilacak dan dikelola.
