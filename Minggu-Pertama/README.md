
# **Writing and Presentation Test Minggu ke-1**

## **Hari Ke-1 :**

## **I. Unix Command Line**

- ### **Definisi CLI, Shell dan Filesystem**
    *   Shell merupakan perantara antara user dengan komputer(ke OS lalu hardware) untuk berkomunikasi berbasis teks.
    *   Command Line Interface(CLI) merupakan shell yang menerima perintah berbasis teks,yang nantinya akan dijalankan oleh OS.
    *   Contoh CLI sendiri yaitu, command prompt, dan bash untuk windows, dan ada juga zsh untuk os mirip UNIX.
    *   <div align="justify">Ketika kita mengakses folder atau file melalui sebuah terminal,yang pertama kita lalui adalah root directory masuk ke folder lalu mungkin ada sub-folder lagi dan yang terakhir ada file. Ini disebut bisa disebut tree filesystem structure.
    *   Sebuah OS mengatur direktori dan file-nya dengan filesystem berbentuk pohon.
    *   Dengan CLI atau shell kita bisa mengakses/manipulasi filesystem tersebut.
- ### **Navigasi file dan direktori**
    *   `pwd` merupakan perintah untuk mengetahui lokasi kita saat ini.
    *   `ls` merupakan perintah untuk mengetahui isi dari direktori itu sendiri.
    *   `cd` merupakan perintah untuk berpindah-pindah direktori.

- ### **Manipulasi file dan direktori**
    *   `touch` , perintah untuk membuat suatu file.
    *   `mkdir` , perintah untuk membuat suatu direktori/file.
    *   `head` , perintah untuk melihat beberapa baris awal dari sebuah teks.
    *   `tail` , perintah untuk melihat beberapa baris akhir dari sebuah teks.
    *   `cat` , perintah untuk melihat isi sebuah file.
    *   `cp` , perintah untuk menyalin file. Jika ingin menyalin direktori gunakan `cp -r`.
    *   `mv` , perintah untuk memindahkan file. Jika ingin memindahkan direktori gunakan `mv -r`.
    *   `mv` , juga bisa digunakan untuk menamai ulang file dan direktori(untuk direktori `mv -r`).
>Ketika kita rename sebuah file atau direktori menggunakan `mv` dengan nama yang sudah digunakan di dalam satu direktori,maka file atau direktori lama tersebut akan hilang dan digantikan dengan yang baru.
*   `rm`  , perintah untuk menghapus sebuah file. Jika ingin menghapus direktori gunakan `rm -r`.
>Tambahkan `-rf` ketika ingin menghapus file secara permanen(tidak masuk ke recyle bin). Dan juga ketika menghapus direktori yang ada isinya gunakan `-rf`. (contoh: `rm -rf text.txt`)   

&emsp;

## **II. Git & GitHub Dasar**

- ### **Definisi Git dan GitHub**
    *  Git adalah _version control_ terdistribusi diciptakan oleh Linus Torvalds pada tahun 2005. Diciptakan untuk melacak perubahan-perubahan yang terjadi di dalam file proyek yang dikerjakan oleh banyak orang maupun sendiri.
    *  GitHub adalah layanan _hosting_ Git repository berbasis web dan orang-lain bisa mengakses dan mengubahnya. Dan itu semua terlacak.        

   Perbedaannya adalah **Git** merupakan _software_ dengan tampilan _command line tool_ yang terpasang di sistem lokal yang berfungsi untuk melakukan kontrol versi _source code_ sehingga segala perubahan tercatat. Sedangkan **GitHub** merupakan layanan hosting Git repository berbasis web dengan tampilan GUI ( _Graphical User Interface_ ) yang berfungsi untuk sentralisasi _source code_ .

- ### **Cara Penggunaan Git dan GitHub**
    1. Konfigurasi awal Git
        - Setting nama dan email    
         `git config --global user.name "Name"` , dan 
        `git config user.name useremail@example.com `
    2. Membuat repository di GitHub
        - Sign up/Sign in GitHub
        - Di _Home Page_ klik _new_ seperti gambar berikut :    
        ![new_repository](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Pertama/images/new%20repo.png "new_repo")
        - Buat Repository-nya, lalu copy link repository-nya seperti gambar berikut :
        ![copy_link](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Pertama/images/copy_link.png)
    3. Memasang git dan publish project
        - `git init` di dalam terminal dengan profile Git Bash(visual studio code) seperti berikut:
        ![git_init](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Pertama/images/git_init.png)
        - `git add .` untuk menambahkan file baru pada repository yang sudah dipilih.
        - `git commit -m "msg"` untuk menyimpan perubahan di lokal.
        - `git branch -M main` untuk buat branch dengan nama main.
        - `git remote add origin <url>`untuk mengatur dimana kita akan _publish_,bagian <url> isi dengan repository yang telah dicopy-kan.
        - `git push -u origin main` publish proyek yang sudah terpasang git ke GitHub.
    4. Cloning GitHub ke local machine
        - `git clone <url>` url diisi dengan proyek link di GitHUb yang ingin di clone ke komputer kita.   

---

##  **Hari Ke-2 : HTML**   

-   **Apa Itu HTML?**
    - HTML merupakan singkatan dari _Hypertext Markup Language_.
    - HTML bersifat statis, hanya bisa menampilkan konten saja dan tidak bisa mengelola data seperti bahasa pemrograman yang dinamis(C, C++, java, python dll).
    - HTML dalam _web development_ adalah sebagai kerangka web.     

-   **Tools pendukung HTML**     
Ketika kita ingin membuat sebuah HTML ada beberapa alat yang harus dimiliki yaitu :
    1.  **Browser**, dengan browser kita bisa melihat hasil codingan HTML yang sudah dibuat. Contoh browsernya yaitu, Chrome, Firefox, Opera dan lain-lain.
    2.  **Code Editor**, dengan code editor kita bisa membuat konten-konten HTML. Contoh code editor yang paling populer yaitu, Visual Studio Code.     
-   **Membuat HTML**   
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>HELLO WORLD</h1>
    
</body>
</html>
```    
-   Code di atas merupakan struktur HTML.
-   HTML tersusun sebagai kesatuan dari sebuah tingkatan (family tree relationship).
-   Saat sebuah element berada di dalam element lain, maka disebut child element, dan element yang membungkus child element disebut parent element.
-   Yang dimaksud dengan '_element_' adalah konten yang dibungkus dengan tag element, seperti berikut:   
`<p>Hello world</>`
-   Di awali opening tag `<p>` lalu konten berupa teks(bisa juga berupa gambar,video dan audio)`Hello World` dan diakhiri closing tag `</p>`.
-   **Menjalankan Code HTML**
    1.   Menjalankan code dengan klik kanan file html lalu _open with_ browser.
    ![open_with_broswer](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Pertama/images/open_with_browser.png)
    2.   Menjalankan code dengan _copy path_.
    ![copy_path](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Pertama/images/copy_path.png)
    Lalu paste path-nya.
    ![link_in_browser](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Pertama/images/link_in_browser.png)
    3.   Menjalankan code di terminal dengan perintah `start index.html`.
    ![terminal](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Pertama/images/terminal.png)
    4.   Menjalankan code dengan extension '_Code Runner_'.
    >   Ada berbagai macam cara untuk menjalankan code dengan _Code Runner_, salah satunya klik kanan pada halaman code.
    ![code_runner](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Pertama/images/code_runner.png)
    5.  Menjalankan code dengan extension '_Live Server_'.
    ![live_server](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Pertama/images/live_server.png)

-   **Tag HTML yang sering digunakan**
    -   `<p>` merupakan paragraf.
    -   `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>` merupakan heading.
    -   `<input>` merupakan tag inputan.
    -   `<button>` merupakan tombol.
    -   `<form>` untuk formulir.
    -   `<a>` untuk link.
    -   `<video>` untuk video.
    -   `<audio>` untuk audio.
    -   `<div>` untuk section.
    -   `<img>` untuk gambar.
    -   `<head>` , `<header>` , `<body>` , `<footer>` , `<aside>` merupkan bagian kerangka web.
    -   `<title>` untuk judul web.
    -   `<link>` biasanya untuk file eksternal CSS.
    -   `<script>` untuk menulis kode pemrograman web misalnya javascript.
    -   `<src>` untuk sumber sebuah gambar,audio dan video.
    -   `<ul>` , `<ol>` untuk menampilkan list.
    -   Dan lain lain.       
-   **Semantic HTML**
    Semantic HTML adalah elemen yang menyatakan makna atau tujuan dari element itu sendiri, contohnya `<header>` untuk membuat kop web dan letaknya paling atas dari element semantic lainnya. Contoh penggunaan HTML sebagai berikut:
```
<body>
    <header>My blog</header>

    <nav>
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
    </nav>

    <article>
        <h1>Hello there!</h1>
        <p>Perkenalkan nama saya Syahri</p>
    </article>

    <aside>
        Social Media
        <a href="#">Instagram</a>
        <a href="#">Facebook</a>
        <a href="#">Youtube</a>    
    </aside>

    <footer>
        Copyright &copy; 2022 by Syahri
    </footer>
    
</body>
``` 




---

##  **Hari Ke-3 : CSS**


---

##  **Hari Ke-4 : Algoritma**


---

##  **Hari Ke-5 : Javascript Dasar**