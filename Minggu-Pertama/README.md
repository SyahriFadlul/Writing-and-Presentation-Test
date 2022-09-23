
# **Writing and Presentation Test Minggu ke-1**

## **Day 1 :**

## **I. Unix Command Line**

*   Shell merupakan perantara antara user dengan komputer(ke OS lalu hardware) untuk berkomunikasi berbasis teks.
*   Command Line Interface(CLI) merupakan shell yang menerima perintah berbasis teks,yang nantinya akan dijalankan oleh OS.
*   Contoh CLI sendiri yaitu, command prompt, dan bash untuk windows, dan ada juga zsh untuk os mirip UNIX.
*   <div align="justify">Ketika kita mengakses folder atau file melalui sebuah terminal,yang pertama kita lalui adalah root directory masuk ke folder lalu mungkin ada sub-folder lagi dan yang terakhir ada file. Ini disebut bisa disebut tree filesystem structure.
*   Sebuah OS mengatur direktori dan file-nya dengan filesystem berbentuk pohon.
*   Dengan CLI atau shell kita bisa mengakses/manipulasi filesystem tersebut.
###   **A. Navigasi file dan direktori**
*   `pwd` merupakan perintah untuk mengetahui lokasi kita saat ini.
*   `ls` merupakan perintah untuk mengetahui isi dari direktori itu sendiri.
*   `cd` merupakan perintah untuk berpindah-pindah direktori.

### **B. Manipulasi file dan direktori**
*   `touch` , perintah untuk membuat suatu file.
*   `mkdir` , perintah untuk membuat suatu direktori/file.
*   `head` , perintah untuk melihat beberapa baris awal dari sebuah teks.
*   `tail` , perintah untuk melihat beberapa baris akhir dari sebuah teks.
*   `cat` , perintah untuk melihat isi sebuah file.
*   `cp` , perintah untuk menyalin file. Jika ingin menyalin direktori gunakan `cp -r`.
*   `mv` , perintah untuk memindahkan file. Jika ingin memindahkan direktori gunakan `mv -r`.
*   `mv` , juga bisa digunakan untuk menamai ulang file dan direktori(untuk direktori `mv -r`).
><div align="justify">Ketika kita rename sebuah file atau direktori menggunakan `mv` dengan nama yang sudah digunakan di dalam satu direktori,maka file atau direktori lama tersebut akan hilang dan digantikan dengan yang baru.
*   `rm`  , perintah untuk menghapus sebuah file. Jika ingin menghapus direktori gunakan `rm -r`.
><div align="justify">Tambahkan `-rf` ketika ingin menghapus file secara permanen(tidak masuk ke recyle bin). Dan juga ketika menghapus direktori yang ada isinya gunakan `-rf`. (contoh: `rm -rf text.txt`)   

&emsp;

## **II. Git & GitHub Dasar**

- ### **Definisi Git dan GitHub**
    *  Git adalah _version control_ terdistribusi diciptakan oleh Linus Torvalds pada tahun 2005. Diciptakan untuk melacak perubahan-perubahan yang terjadi di dalam file proyek yang dikerjakan oleh banyak orang maupun sendiri.
    *  GitHub adalah layanan _hosting_ Git repository berbasis web dan orang-lain bisa mengakses dan mengubahnya. Dan itu semua terlacak.        

   <div align="justify">Perbedaannya adalah **Git** merupakan _software_ dengan tampilan _command line tool_ yang terpasang di sistem lokal yang berfungsi untuk melakukan kontrol versi _source code_ sehingga segala perubahan tercatat. Sedangkan **GitHub** merupakan layanan hosting Git repository berbasis web dengan tampilan GUI (_Graphical User Interface_) yang berfungsi untuk sentralisasi _source code_.

- ### **Cara Penggunaan Git dan GitHub**
    1. Konfigurasi awal Git
        - Setting nama dan email    
         `git config --global user.name "Name"` , dan 
        `git config user.name useremail@example.com `
    2. Membuat repository di GitHub
        - Sign up/Sign in GitHub
        - Di _Home Page_ klik _new_ seperti gambar berikut :    
        ![new_repository](Minggu-Pertama/new_repo.png "new_repo")

##  **Day 2 : HTML**

##  **Day 3 : CSS**

##  **Day 4 : Algoritma**

##  **Day 5 : Javascript Dasar**dasd