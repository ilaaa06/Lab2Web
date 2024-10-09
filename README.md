# Lab2Web
Nama: Nur Laila   
Nim: 312310149 (TI 23 A1)
## 1. Membuat dokumen HTML
```sh 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CSS Dasar</title>
</head>
<body>
<header>
<h1>CSS Internal dan <i>Inline CSS</i></h1>
</header>
<nav>
<a href="lab2_css_dasar.html">CSS Dasar</a>
<a href="lab2_css_eksternal.html">CSS Eksternal</a>
<a href="lab1_tag_dasar.html">HTML Dasar</a>
</nav>
<!-- CSS ID Selector -->
<div id="intro">
<h1>Hello World</h1>
<p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman
Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat
adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML
dan CSS.</p>
<!-- CSS Class Selector -->
<a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
</div>
</body>
</html>
```
Selanjutnya buka pada brwoser untuk melihat hasilnya.
![Cuplikan layar 2024-10-09 204902](https://github.com/user-attachments/assets/e66a17f1-f447-44fe-82c7-974d6d34168b)

## 2. Mendeklarasikan CSS Internal
Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen.
```sh
<head>
<title>CSS Dasar</title>
<style>
body {
font-family:'Open Sans', sans-serif;
}
header {
min-height: 80px;
border-bottom:1px solid #77CCEF;
}
h1 {
font-size: 24px;
color: #0F189F;
text-align: center;
padding: 20px 10px;
}
h1 i {
color:#6d6a6b;
}
</style>
</head>
```
Selanjutnya simpan perubahan yang ada, dan lakukan refresh pada browser untuk melihat
hasilnya.
![Cuplikan layar 2024-10-09 205413](https://github.com/user-attachments/assets/9e9b4ad8-284b-4553-9953-e748baf8334d)
  
## 3. Menambahkan Inline CSS
Kemudian tambahkan deklarasi inline CSS pada tag <p> seperti berikut.
```sh
<p style="text-align: center; color: #ccd8e4;">
```  
Simpan kembali dan refresh kembali browser untuk melihat perubahannya.
![Cuplikan layar 2024-10-09 210520](https://github.com/user-attachments/assets/3dfc9f1a-2a6c-459a-be15-fc2d066fafee)

## 4. Membuat CSS Eksternal
Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut.
![image](https://github.com/user-attachments/assets/cb33251a-d85c-40de-a2f5-1c8d48737c88)
Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut.  
```sh
nav {
background: #20A759;
color:#fff;
padding: 10px;
}
nav a {
color: #fff;
text-decoration: none;
padding:10px 20px;
}
nav .active,
nav a:hover {
background: #0B6B3A;
}
```  
Kemudian tambahkan tag `<link>` untuk merujuk file css yang sudah dibuat pada bagian `<head>`
```sh
<head>
<!-- menyisipkan css eksternal -->
<link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
```  
Selanjutnya refresh kembali browser untuk melihat perubahannya.
![Cuplikan layar 2024-10-09 211646](https://github.com/user-attachments/assets/856e6889-f150-4140-b79b-c606dbfadbea)

## 5. Menambahkan CSS Selector
Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file
style_eksternal.css, tambahkan kode berikut.
```sh
/* ID Selector */
#intro {
background: #418fb1;
border: 1px solid #099249;
min-height: 100px;
padding: 10px;
}
#intro h1 {
text-align: left;
border: 0;
color: #fff;
}
/* Class Selector */
.button {
padding: 15px 20px;
background: #bebcbd;
color: #fff;
display: inline-block;
margin: 10px;
text-decoration: none;
}
.btn-primary {
background: #E42A42;
}
```
Kemudian simpan kembali dan refresh browser untuk melihat perubahannya.  
![Cuplikan layar 2024-10-09 211901](https://github.com/user-attachments/assets/490aad7e-1f9c-4fba-b9c1-2da0c5497a78)

# JAWABAN Tugas
### JAWABAN SOAL NO 1
```sh
<p style="text-align: center; color: #c97e05; font-size: 16px; font-family: Arial; background-color: #8f0505; border: 1px solid #000; padding: 10px; margin: 20px;">
```
pada CSS saya ubah dengan
```sh
}
.btn-primary {
    background: #d8e42a;
}
```
![image](https://github.com/user-attachments/assets/921fb2d3-f742-41a2-bf60-22ca28561a51)

### JAWABAN SOAL NO 2
`h1 {...}` adalah selektor universal yang akan memberikan gaya kepada semua elemen `<h1>` di seluruh halaman HTML, tanpa memperhatikan di mana letaknya. sedangkan `#intro h1 {...}` adalah selektor kombinasi yang lebih spesifik, di mana hanya elemen `<h1>` yang berada di dalam elemen dengan `id="intro"` yang akan mendapat gaya CSS tersebut.

### JAWABAN SOAL NO 3
Jika ada deklarasi CSS internal, eksternal, dan inline pada elemen yang sama, maka prioritasnya adalah:
Inline CSS memiliki prioritas tertinggi.
Internal CSS (di dalam tag `<style>`) memiliki prioritas setelah inline.
Eksternal CSS (file `.css` terpisah) memiliki prioritas terendah.
CONTOH:
```sh
<!DOCTYPE html>
<html>
<head>
    <style>
        /* Internal CSS */
        p {
            color: green;
        }
    </style>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <p style="color: red;">Teks ini menggunakan inline CSS.</p>
</body>
</html>
```
File styles.css (Eksternal CSS):
```sh
p {
    color: blue;
}
```
Dalam contoh di atas, meskipun ada eksternal CSS yang menyetel warna menjadi biru, dan internal CSS menyetel warna menjadi hijau, inline CSS menyetel warna menjadi merah, sehingga teks paragraf akan tampil berwarna merah di browser karena inline CSS memiliki prioritas tertinggi.

### JAWABAN SOAL NO 4
Jika suatu elemen memiliki ID dan Class yang masing-masing memiliki deklarasi CSS, maka ID akan memiliki prioritas yang lebih tinggi dibandingkan dengan Class, karena selektor ID lebih spesifik.  
CONTOH:  
HTML:
```sh
<p id="paragraf-1" class="text-paragraf">
    Ini adalah paragraf dengan ID dan Class.
</p>
```
CSS:
```sh
/* Class CSS */
.text-paragraf {
    color: blue;
    font-size: 14px;
}

/* ID CSS */
#paragraf-1 {
    color: red;
    font-size: 16px;
}
```
Pada contoh ini, meskipun `class .text-paragraf` memberikan warna biru dan ukuran font 14px, deklarasi `ID #paragraf-1` akan lebih diutamakan, sehingga teks akan berwarna merah dengan ukuran font 16px di browser karena ID memiliki prioritas lebih tinggi.  

