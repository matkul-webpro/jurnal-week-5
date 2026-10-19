# jurnal-week-5

Jurnal minggu 5: Bootstrap.

## Soal dan Jawaban

### 1. Pengertian Bootstrap [10 poin]

Bootstrap adalah framework CSS (dengan komponen JavaScript) open-source untuk membangun tampilan website yang responsif dan mobile-first.

Kegunaan:
- Mempercepat pembuatan tampilan karena menyediakan class CSS siap pakai.
- Menjamin tampilan responsif di berbagai ukuran layar.
- Menjaga konsistensi desain dan kompatibilitas antar browser.

### 2. Memasang Bootstrap [10 poin]

- **CDN**: menambahkan `<link>` CSS di `<head>` dan `<script>` JS di akhir `<body>`.

  ```html
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  ```
- **Download manual**: mengunduh file resmi Bootstrap, menaruhnya di folder project, lalu menautkannya lewat `<link>` dan `<script>`.
- **Package manager**: `npm install bootstrap` (atau yarn/composer).
- **Source Sass**: mengimpor file Sass Bootstrap untuk kustomisasi tema.

### 3. Grid dan Breakpoint [10 poin]

Grid adalah sistem layout Bootstrap yang membagi lebar halaman jadi 12 kolom. Susunannya `container` → `row` → `col`. Lebar kolom diatur dengan class `col-{breakpoint}-{1-12}`, misalnya `col-md-6` berarti kolom selebar 6 dari 12 kolom. Jika total kolom dalam satu `row` lebih dari 12, kolom sisanya turun ke baris berikutnya. Contoh: `col-md-8` + `col-md-4` = 12 (lebar penuh saat layar ≥ 768px).

Breakpoint adalah batas lebar layar tempat layout berubah, sehingga satu halaman bisa tampil berbeda di ponsel, tablet, dan desktop. Class dengan breakpoint berlaku mulai dari lebar tersebut ke atas, sedangkan class tanpa breakpoint (misal `col-12`) berlaku di semua ukuran.

| Class prefix | Lebar layar | CSS setara |
|---|---|---|
| `.col-` | < 576px (xs) | selalu berlaku |
| `.col-sm-` | ≥ 576px | `min-width: 576px` |
| `.col-md-` | ≥ 768px | `min-width: 768px` |
| `.col-lg-` | ≥ 992px | `min-width: 992px` |
| `.col-xl-` | ≥ 1200px | `min-width: 1200px` |

### 4. Class Bootstrap [10 poin]

| Class | Kegunaan |
|---|---|
| `.navbar` | Membuat elemen jadi bar navigasi |
| `.navbar-expand-md` | Navbar tampil horizontal saat layar ≥ 768px, di bawahnya collapse jadi tombol hamburger |
| `.navbar-dark` | Teks dan ikon navbar berwarna terang (untuk background gelap) |
| `.bg-dark` | Background gelap (utility warna) |
| `.container` | Membatasi lebar konten secara responsif dan memusatkannya |

### 5. Gambar Responsif [10 poin]

Gunakan class `img-fluid` pada tag `<img>`. Class ini menerapkan `max-width: 100%` dan `height: auto`, sehingga gambar mengecil mengikuti lebar elemen induknya dan proporsinya tetap, tapi tidak melebihi ukuran aslinya.

```html
<img src="foto.jpg" class="img-fluid" alt="Foto">
```

### 6. Membuat Tampilan dengan Bootstrap [50 poin]

Halaman login **Ruang Baca** ada di file `index.html`:

- Navbar dengan brand "Ruang Baca" di kiri dan menu Beranda, Tentang, Bantuan di kanan.
- Form login: judul, input Username dan Password, checkbox "Ingat saya", tombol Masuk, dan tautan "Lupa password?".
- Menggunakan grid Bootstrap agar form tetap terbaca di layar kecil.

Cara menjalankan: buka `index.html` di browser (butuh koneksi internet karena Bootstrap dimuat dari CDN).