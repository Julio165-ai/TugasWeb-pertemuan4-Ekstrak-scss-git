# Uji Coba SCSS ke CSS

Tugas Portofolio 4 - Pemrograman Web
Nama: Juliotama Stefanus Sitepu | NIM: 4253550030

## Deskripsi
Proyek kecil ini mencoba alur kerja **SCSS** (Sass): menulis gaya di file `.scss`, lalu dikompilasi otomatis menjadi file `.css` yang dipakai oleh halaman HTML. Hasilnya berupa halaman sederhana berisi sebuah kartu dengan judul, paragraf, dan tombol.

## Struktur File
| File | Keterangan |
|------|------------|
| `index.html` | Halaman web yang menampilkan kartu "Halo UNIMED" |
| `style.scss` | Sumber gaya yang ditulis dengan SCSS (file yang diedit) |
| `style.css` | Hasil kompilasi dari `style.scss` (dibuat otomatis) |
| `style.css.map` | Source map hasil kompilasi, membantu debugging di browser |

Catatan: `index.html` memanggil `style.css`, jadi nama file CSS di `<link>` harus sama persis dengan file hasil kompilasi.

## Fitur SCSS yang Dipakai
1. **Variabel**: warna disimpan sekali lalu dipakai berulang, sehingga mudah diubah.
   ```scss
   $warna-utama: #2563eb;
   $warna-bg: #f8fafc;
   $warna-teks: #1e293b;
   $putih: #ffffff;
   ```
2. **Nesting**: aturan untuk `h1`, `p`, dan `.tombol` ditulis di dalam `.kartu`, sehingga lebih rapi dan tidak berulang.
   ```scss
   .kartu {
     h1 { color: $warna-utama; }
     .tombol { background-color: $warna-utama; }
   }
   ```
3. **Selector `&`**: dipakai untuk efek hover pada tombol.
   ```scss
   .tombol {
     &:hover { background-color: #1d4ed8; }
   }
   ```

## Cara Menjalankan
1. Buka folder proyek di **Visual Studio Code**.
2. Pasang ekstensi **Live Sass Compiler** (penerbit Glenn Marks).
3. Buka `style.scss`, lalu klik **Watch Sass** di status bar bagian bawah sampai tertulis *Watching...*.
4. Setiap kali `style.scss` disimpan (**Ctrl+S**), file `style.css` dan `style.css.map` dibuat atau diperbarui otomatis.
5. Buka `index.html` di browser (atau lewat ekstensi **Live Server**) untuk melihat hasilnya.

## Hasil
Halaman menampilkan kartu putih di tengah layar dengan judul berwarna, deskripsi singkat, dan tombol **Masuk** yang berubah warna saat disentuh kursor.

![c:\Users\HP\OneDrive\Pictures\Screenshots 1\Screenshot 2026-10-10 081117.png](screenshots/hasil.png)

## Kesimpulan
SCSS membuat penulisan CSS lebih singkat dan terstruktur lewat variabel dan nesting. File `.scss` tidak dibaca langsung oleh browser, sehingga perlu dikompilasi menjadi `.css` terlebih dahulu.
