"# jurnal-week-5" 

1. Pengertian Bootstrap [10 poin] Jelaskan apa itu Bootstrap dan apa kegunaannya! 
2. Memasang Bootstrap [10 poin] Ada beberapa cara untuk mengimpor atau menggunakan Bootstrap pada project. Sebutkan caracaranya! 
3. Grid dan Breakpoint [10 poin] Jelaskan mengenai class grid dan kegunaan breakpoint! 
4. Class Bootstrap [10 poin] Sebutkan minimal lima class yang disediakan oleh Bootstrap beserta kegunaannya! 
5. Gambar Responsif [10 poin] Bagaimana cara agar foto atau gambar pada website responsif menyesuaikan ukuran layar perangkat? 

JAWAB:

1. Bootstrap adalah framework CSS open-source untuk membangun tampilan website yang responsif.
2. Memasang dengan CDN dengan membuat proyek HTML lalu memasang link pada head (link) dan bodynya (scripts), Memasang dengan mengunduh file resmi bootstrap
3.  Grid adalah style dengan 2 dimensi, memiliki column dan row
    PENJELASAN BREAKPOINT (titik patah responsif):
         ┌──────────────┬──────────────┬──────────────┐

         │ Class prefix │ Layar        │ CSS setara   │

         ├──────────────┼──────────────┼──────────────┤

         │ .col-        │ < 576px (xs) │ (selalu)     │

         │ .col-sm-     │ ≥ 576px      │ min-width:576px│

         │ .col-md-     │ ≥ 768px      │ min-width:768px│

         │ .col-lg-     │ ≥ 992px      │ min-width:992px│

         │ .col-xl-     │ ≥ 1200px     │ min-width:1200px│

         └──────────────┴──────────────┴──────────────┘

         Total kolom dalam 1 baris = 12.

         Contoh: col-md-8 + col-md-4 = 12 (full width saat ≥768px)
    sumber: bootstrap-pengenalan.html (line: 174)
4.  .navbar           → membuat elemen jadi bar navigasi

    .navbar-expand-md → navbar melebar (horizontal) saat layar ≥ md (768px)

                        Di bawah md, navbar collapse jadi tombol hamburger.
                        [md di Bootstrap = @media (min-width: 768px) di CSS biasa]
    .navbar-dark      → teks & ikon navbar berwarna terang (untuk bg gelap)

    .bg-dark          → background gelap (Bootstrap utility color)

    .container        → membatasi lebar konten ke lebar tertentu (responsif)
    
    sumber: bootstrap-pengenalan.html (line: 102)
5. Gunakan class img-fluid pada tag <img>. Class ini menerapkan max-width: 100% dan height: auto, sehingga gambar mengecil mengikuti lebar elemen induknya dan proporsinya tetap, tapi tidak melebihi ukuran aslinya.

