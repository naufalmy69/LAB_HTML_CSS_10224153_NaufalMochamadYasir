# Jawaban Praktikum: <NaufalMochamadYasir> (<10224153>)

## Bagian 1: Pemanasan
1.  Selector: nav a.active:hover
    Deklarasi: color: red;
    Property: color
    value: red
    preudo-class: hover

2.  Block: <p>, <li>, <h2>
    Inline: <span>, <a>, <strong>

3.  A dan B
    dikarenakan <p> pada bagian A dan B berada di dalam class=box
    sedangkan <p> pada bagian C dan D malah menjadi diantara class=box itu sendiri sehingga <p> nya sendiri yang menjadi box.

4.  Merah(red).
    dikarenakan #title adalah ID. dan ID lebih kuat daripada class maupun nama tag.

5.  Salah dikarenakan tag <strong> ada setelah <p> di tutup.
    seharusnya: <p>Hello <strong>world</strong></p>

## Bagian 3: Prediksi Selector Golf
P1. 
    (a) weekly hack nights. (green)
        karena "weekly hack nights." adalah elemen <p> di dalam <section>, sehingga section p lebih spesifik daripada p.
    (b) bring your own laptop. (oranye)
        karena "bring your own laptop." memiliki class note. sehingga selector .note lebih spesifik daripada section p.
    (c) © 2026 Student Affairs (biru)
        karena "© 2026 Student Affairs" adalah <p> di dalam <footer> dan tidak terkena section p maupun note, sehingga menggunakan aturan p.
P2. 
    1. #tech p
    2. .club p
    3. main section p
    4. p
Setelah diuji (hasil sebenarnya):
(a) green
(b) oranye
(c) biru

## Bagian 4: Box model
Q1 (content-box):
Lebar kartu = 300px + 16px + 16px + 1px + 1px = 334px
Q2 (border-box):
Dengan box-sizing: border-box, width 300px sudah mencakup content, padding, dan border. jadi lebar kartu dari tepi ke border = 300px.
Lebar content = 300px - 32px - 2px = 266px.
Pengecekan DevTools:
Content: 762px x 119.797px
padding: 16px
Border: 1px
Margin: 0px (atas, kiri, kanan), 24px (bawah).

## Bagian 5: Tabel debug
| # | Baris | Bug | Perbaikan | Cara menemukannya |
|---|-------|-----|-----------|-------------------|
| 1 | CSS body | `colour` bukan property CSS yang benar | Ubah menjadi `color` | Membaca kode / DevTools |
| 2 | CSS header | Kurang `;` setelah background | Tambahkan `;` | Membaca kode |
| 3 | CSS .Card | Nama class berbeda dengan HTML | Ubah `.Card` menjadi `.card` | Membandingkan CSS dengan HTML |
| 4 | CSS #newsList | `18 px` memiliki spasi | Ubah menjadi `18px` | Membaca kode / DevTools |
| 5 | CSS footer | Value `centre` salah | Ubah menjadi `center` | Membaca kode / DevTools |
| 6 | HTML h1 | Tag dibuka `h1` tetapi ditutup `h2` | Ubah menjadi `</h1>` | Validator HTML |
| 7 | HTML nav | Tanda kutip `href` kurang | Tambahkan `"` setelah `about.html` | Validator HTML |
| 8 | CSS/HTML ID | `#news-list` berbeda dengan `id="newsList"` | Samakan menjadi `#newsList` | Membandingkan CSS dengan HTML |
| 9 | HTML img | Tidak memiliki atribut `alt` | Tambahkan `alt="Campus News"` | Validator / accessibility checking |

## Bagian 6: Tabel Code Review
| # | Baris | Masalah | Mengapa penting | Perbaikan saya |
|---|-------|---------|-----------------|----------------|
| 1 | `<html>` | Tidak ada `lang` pada `<html>` | Membantu browser dan teknologi pembaca layar mengetahui bahasa halaman | Tambahkan `lang="id"` |
| 2 | `.header` | Menggunakan width `1200px` | Tidak responsif pada layar yang lebih kecil | Gunakan `max-width` dan layout yang responsif |
| 3 | `.nav a` | Menggunakan `!important` | Membuat CSS lebih sulit dipelihara dan dilawan oleh selector lain | Hapus `!important` |
| 4 | Struktur body | Banyak menggunakan `<div>` untuk struktur halaman | Kurang semantik dan sulit dipahami | Gunakan `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>` |
| 5 | Judul halaman | Tidak menggunakan heading yang benar | Struktur heading penting untuk struktur dokumen dan aksesibilitas | Gunakan `<h1>` dan `<h2>` |
| 6 | `<b>` pada nama kampus | Menggunakan `<b>` untuk judul | `<b>` hanya memberi tampilan tebal, bukan struktur heading | Gunakan `<h1>` |
| 7 | `style=""` | Menggunakan inline CSS | Sulit dirawat dan melanggar aturan styling yang sudah dilatih | Pindahkan CSS ke stylesheet |
| 8 | `<br><br>` | Menggunakan `<br>` untuk mengatur jarak | `<br>` seharusnya untuk pergantian baris, bukan layout | Gunakan `margin` dan `padding` CSS |
| 9 | `<img>` | Tidak memiliki `alt` | Buruk untuk aksesibilitas jika gambar tidak dapat dilihat | Tambahkan `alt` yang bermakna |
| 10 | Form | Input tidak memiliki `<label>` | Pengguna dan screen reader sulit mengetahui fungsi input | Tambahkan `<label>` dan atribut `for` |

Refleksi:
1. Menurut saya, masalah yang paling sulit disadari dari tampilan      browser adalah masalah struktur HTMl dan accesibility, soalnya kalau dilihat sekilas, halamannya tetap terlihat normal dan bisa digunakan.
2. Walaupun halaman tersebut tetap bisa dibuka dan digunakan, masalahnya tetap penting karena bisa membuat kode sulit dikembangkan dan kurang nyaman untuk pengguna tertentu. selain itu, kalau strukturnya tidak rapi, developer lain juga akan sulit memahami kodenya.
3. saya akan membiasakan diri mengecek kembali HTMl dan CSS sebelum dikumpulkan, terutama struktur tag, selector, dan accesibility. saya juga akan menggunakan W3C Validator untuk memastikan tidak ada error.

## Bagian 7: Exit ticket
1. Anatomi sebuah aturan CSS terdiri dari selector, property, dan value. selector menentukan elemen mana yang mau diberi style, sedangkan property dan value menentukan bagian apa yang diubah dan seperti apa hasilnya.
2. yang masih agak bingung bagi saya adalah perbedaan specificity antar selector, terutama ketika beberapa selector bisa mengenai elemen yang sama.
3. Sekarang saya sudah cukup paham terkait beberapa struktur html dasar dan menghubungkannya dengan CSS tanpa harus mencari contoh dari internet. saya juga sekarang sudah dapat memahami tentang langkah2 html seperti kemarin dan juga css nya.

