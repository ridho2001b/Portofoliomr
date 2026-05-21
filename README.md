# 🚀 RIDHO — Portfolio Pribadi M Ridho Nur Aziz

Website portofolio profesional yang dibangun dengan HTML, CSS, dan JavaScript murni.
Siap deploy ke **GitHub Pages** secara gratis dalam hitungan menit.

---

## ✨ Fitur Utama

| Fitur | Status |
|---|---|
| Dark / Light Mode | ✅ |
| Responsive (Mobile, Tablet, Desktop) | ✅ |
| Animasi scroll (Intersection Observer) | ✅ |
| Diary dengan localStorage | ✅ |
| Smooth scroll & back-to-top | ✅ |
| Tombol WhatsApp CTA | ✅ |
| Template & Tools section | ✅ |
| Single-file (no dependencies) | ✅ |

---

## 📁 Struktur File

```
ridho-portfolio/
├── index.html      ← Seluruh website (HTML + CSS + JS)
└── README.md       ← Dokumentasi ini
```

Satu file, nol dependensi eksternal. Google Fonts dimuat via CDN.

---

## 🚀 Cara Deploy ke GitHub Pages

### Langkah 1 — Siapkan Repository

```bash
# Buat folder lokal
mkdir ridho-portfolio && cd ridho-portfolio

# Inisialisasi git
git init
git add .
git commit -m "feat: initial portfolio"
```

### Langkah 2 — Push ke GitHub

1. Buat repository baru di [github.com/new](https://github.com/new)
2. Nama repository: `ridho-portfolio` (atau username.github.io untuk domain utama)
3. Set ke **Public**

```bash
git remote add origin https://github.com/USERNAME/ridho-portfolio.git
git branch -M main
git push -u origin main
```

### Langkah 3 — Aktifkan GitHub Pages

1. Buka tab **Settings** repository
2. Klik **Pages** di sidebar kiri
3. Source: pilih **Deploy from a branch**
4. Branch: `main`, folder: `/ (root)`
5. Klik **Save**

Website akan live di:
```
https://USERNAME.github.io/ridho-portfolio/
```

> Proses aktivasi membutuhkan 1–3 menit.

---

## ⚙️ Konfigurasi Wajib

Sebelum deploy, ganti placeholder berikut di `index.html`:

### Nomor WhatsApp
```html
<!-- Cari baris ini, ganti 6281234567890 dengan nomor kamu -->
href="https://wa.me/6281234567890?text=..."
```
Format: kode negara + nomor tanpa `+` atau `0` di depan.
Contoh: `628123456789` untuk `0812-3456-789`.

### Link Template Notion
```html
href="GANTI_DENGAN_LINK_NOTION_KAMU"
```
Cara mendapatkan link Notion: buka halaman → Share → Copy link.

### Link Template Obsidian
```html
href="GANTI_DENGAN_LINK_OBSIDIAN_KAMU"
```
Bisa berupa link GitHub releases, Google Drive, atau halaman penjelasan.

### Link Sosial Media
```html
<!-- Di bagian contact dan footer -->
href="https://github.com/username-kamu"
href="https://linkedin.com/in/username-kamu"
href="https://instagram.com/username-kamu"
```

### Foto Proyek (Opsional)
Ganti placeholder thumbnail proyek dengan gambar asli:
```html
<!-- Sebelum -->
<div class="project-thumb-placeholder">...</div>

<!-- Sesudah (gunakan tag img) -->
<img src="images/proyek-1.jpg" alt="Nama Proyek" class="project-thumb" />
```

---

## 🎨 Kustomisasi Tampilan

Semua warna dikontrol melalui CSS Variables di bagian `:root`:

```css
/* Dark Mode */
--accent-gold:   #d4af37;   /* Warna aksen utama */
--text-primary:  #e8e4d9;   /* Warna teks utama */
--bg-primary:    #080808;   /* Latar belakang */

/* Light Mode — di dalam [data-theme="light"] */
--accent-gold:   #b8860b;
```

---

## 📖 Fitur Diary

- Data disimpan di `localStorage` browser dengan key `ridho-diary-entries`
- Data **tidak** dikirim ke server, sepenuhnya privat di browser pengunjung
- Format data: array JSON `[{ id, title, body, date }]`
- Shortcut: `Ctrl + Enter` di textarea untuk menyimpan catatan

---

## 🌐 Font yang Digunakan

| Font | Penggunaan |
|---|---|
| Cormorant Garamond | Heading, judul besar, logo |
| Jost | Body text, navigasi, tombol |
| DM Mono | Label, tanggal, kode, tag |

---

## 📱 Breakpoints Responsif

| Breakpoint | Layout |
|---|---|
| ≥ 1025px | Desktop: 3 kolom skills, 3 kolom portfolio |
| 769–1024px | Tablet: 2 kolom skills & portfolio |
| ≤ 768px | Mobile: 1 kolom, hamburger menu |
| ≤ 480px | Small mobile: font lebih kecil |

---

## 🛠️ Custom Domain (Opsional)

Untuk menggunakan domain sendiri (misal `ridho.dev`):

1. Buat file `CNAME` di root repository:
   ```
   ridho.dev
   ```
2. Arahkan DNS domain ke GitHub:
   - Tipe A → `185.199.108.153`
   - Tipe A → `185.199.109.153`
3. Aktifkan HTTPS di Settings → Pages → Enforce HTTPS

---

## 📄 Lisensi

© 2025 M Ridho Nur Aziz. All rights reserved.
Website ini dibuat untuk penggunaan pribadi sebagai portofolio profesional.
