
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
    - HTML bersifat statis, hanya bisa menampilkan konten saja dan tidak bisa mengelola data seperti bahasa pemrograman yang dinamis.
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
&emsp;
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
        Dengan live server semua perubahan langsung diterapkan tanpa harus refresh halaman web.    


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
-   **Deploy project di Netlify**
    1.  Daftar dengan github.
    2.  Import project dari github.
    3.  Pilih repository.
    4.  Ikuti perintah selanjutnya.
    5.  Beres

---

##  **Hari Ke-3 : CSS**    
-   CSS atau _Cascading Style Sheets_ adalah bahasa yang digunakan untuk mengatur tampilan elemen pada bahasa markup.
-   Struktur CSS :
```
.elementHTML {
    property : value;
}
```
-   Ada 3 cara untuk menggunakan CSS dalam HTML yaitu:
    -   Inline,jadi kita menggunakan attribut untuk styling-nya.Contoh:     
    `<p style="font-size:14px; color=red;">BEEEAANNNZZ</p>`
    -   Internal,yaitu menggunakan tag `<style></style>` pada HTML.Contoh:    
    ```
    <html>
    <head>
        <style>
            p{
                color: red;
                font-size: 14px;
            }
        </style>
    </head>
    <body>
        <p>Hello World</p>
    </body>
    </html>
    ```
    -   Eksternal,yaitu menggunakan tag `<link>` dengan attribute lokasi file CSS.Contoh:     
    `<link rel="stylesheet" href="style.css" type="text/css">`   
-   **Desain Web Responsif**
    -   **Viewport** css adalah daerah yang menampilkan halaman web yang sedang kita akses.Cara menggunakannya yaitu  menambahkan attribut content pada tag meta di element head, seperti ini:    
    ```
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <head>
    ```        

    -   Menggunakan persentase untuk nilai lebar element seperti `width:40%` dll.
    -   Menggunakan satuan unit 'Vw' untuk besar font(1vw=1% lebar viewport)
    -   Menggunakan **Media Query** agar ketika user resizing browser, kontenpun akan beradaptasi sesuai perintah media query-nya
    -   Menggunakan Flexbox,dengan flexbox mengatur layout,posisi dan ukuran elemen jadi lebih mudah.
    -   Dalam menggunakan flexbox ada 2 hal penting yang harus diketahui terlebih dahulu, ada:
        -   Container/parent yaitu elemen yang membungkus dan mengatur tampilan dari element di dalamnya.
        -   Items/childern yaitu elemen dalam container yang diatur tampilannya.
    -   Contoh flexbox:
    ```
        .element{
            display:flex;
            flex-direction:row;
            justify-content:flex-start;
        }
    ```
    -   Code diatas membuat elemen menjadi flex dengan flex-direction nya row atau baris dan kontennya berada di start(kiri)
    -   Beberapa nilai property justify-content:
        -   flex-end, konten akan ditampilkan di akhir blok
        -   center, konten akan ditampilkan di tengah tengah blok
        -   space-between, tiap kontennya memiliki jarak satu sama lain
        -   space-around, tiap konten memiliki padding horizontal yang sama
---

##  **Hari Ke-4 : Algoritma**    

-   Algoritma adalah langkah-langkah logis untuk menyelesaikan suatu masalah.
-   Struktur Data adalah cara mengumpulkan dan mengatur data sedemikian rupa sehingga kita dapat melakukan operasi pada sebuah data dengan cara yang efektif.
-   Struktur data dengan Algoritma merupakan satu kesatuan, jika salah satunya buruk maka yang yang satunya juga jadi buruk.
-   Perbedaan algoritma dengan struktur data adalah, algoritma adalah langkah langkah untuk menyelesaikan masalah sedangkan struktur data mengatur data yang dibutuhkan dalam mengorganisir data.
-   Contoh Algoritma sederhana menambahkan string buah ke keranjang array:
    1. Start
    2. Declare an array
    3. Add index with buah
    4. Display keranjang
    5. Stop
-   **Contoh pseucode-nya:**
```
    Declare:
    Keranjang is ARRAY;
    Description:
    BEGIN
    ADD "Mangga" to keranjang
    ADD "Anggur" to keranjang
    DISPLAY keranjang.
    END
```
-   **Jika bahasa pemrogramannya:**
    ```
    let keranjang = []
    keranjang[0] = "mangga"
    keranjang[1] = "anggur"

    console.log(keranjang)
    ```         
-   **Contoh kasus:**   
    -   William ingin menampilkan deretan nilai dari 0 sampai N.
    -   N adalah nilai akhir yang diinputkan.
    -   Jika William menginput N dengan nilai 100, maka program akan menampilkan deretan nilai 1, 2, 3, 4, 5, … , 100
-   **Pseucode-nya:**
```
    Declare:
    INTEGER N = 100
    Description:
    Begin
    FOR LET i=0 up to N ;i++; DO{
      DISPLAY i  
    }
    END
```
-   Javascript code-nya:
```
    let N = 100;
    
    for(let i=0;i<=n;i++>){
        console.log(i);
    }
```

---

##  **Hari Ke-5 : Javascript Dasar**   
-   Dengan menambahkan javascript dalam web development, user bisa berinteraksi dengan web seperti memasukan data ke web,berpindah pindah halaman dan lain lain.
-   **Ada 2 cara menggunakan javascript dalam web development, yaitu:**
    1.  Internal, yaitu dengan menambahkan tag `<script>` kedalam html
    2.  Eksternal, yaitu menggunakan elemen `<script>` dalam html yang nantinya akan mengakses script.js.

-   **Ada 6 tipe data pada javascript yaitu:**
    1.  Number, yaitu angka-angka
    2.  String, yaitu kumpulkan karakter.
    3.  Boolean, yaitu true atau false.
    4.  Null, yaitu variable yang nilainya kosong atau null.
    5.  Undefined, yaitu variable yang belum dinyatakan tipe datanya.
    6.  Object, yaitu kumpulan data dengan tipe data bisa berbeda beda, ada propertinya dan tiap properti mempunyai nilai.
-   **Operator-operator Javascript:**
    -   Operator aritmatika:
        -   `+` ,penjumlahan ex: `let a = 1+1 console.log(a)//output: 2`
        -   `-` ,pengurangan ex: `let a = 1-1 console.log(a)//output: 0`   
        -   `*` ,perkalian ex: `let a = 1*1 console.log(a)//output: 1`
        -   `/` ,pembagian ex: `let a = 1/1 console.log(a)//output: 1`
        -   `**` ,eksponen ex: `let a = 1**1 console.log(a)//output: 1`
        -   `%` ,modulus ex: `let a = 1%1 console.log(a)//output: 0`
        -   `++` ,increment ex: `let a = 1 console.log(a++)//output: 2`
        -   `--` ,decrement ex: `let a = 1 console.log(a--)//output: 0`
    -   Assignment operator:   

    ![assignment_operator](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Pertama/images/assignment_operator.png)  
    -   Operator perbandingan:
        -   `==` , sama dengan (cek nilai)   
        ex: 
        ```
            let a = 2
            if(a == 2)console.log(true);
            else{console.log(false)} //output:true
        ```
        -   `===` , sama dengan (cek nilai dan tipe data)   
        ex: 
        ```
            let a = 2
            if(a === 2)console.log(true);
            else{console.log(false)} //output:true
        ```
        -   `!=` ,  tidak sama dengan (cek nilai)   
        ex: 
        ```
            let a = 2
            if(a != 2)console.log(true);
            else{console.log(false)} //output:false
         ```
        -   `!==` , tidak sama dengan (cek nilai dan tipe data)   
        ex: 
        ```
            let a = 2
            if(a !== 2)console.log(true);
            else{console.log(false)} //output:false
        ```
        -   `>` ,   lebih dari   
        ex: 
        ```
            let a = 2
            if(a > 2)console.log(true);
            else{console.log(false)} //output:false
        ```
        -   `<` ,   kurang dari   
        ex: 
        ```
            let a = 2
            if(a < 2)console.log(true);
            else{console.log(false)} //output:false
        ```
        -   `>=` ,  lebih dari sama dengan   
        ex: 
        ```
            let a >= 2
            if(a >= 2)console.log(true);
            else{console.log(false)} //output:true
        ```
        -   `<=` ,  kurang dari sama dengan   
        ex: 
        ```
            let a = 2
            if(a <= 2)console.log(true);
            else{console.log(false)} //output:true
        ```
        -   `? :` , ternary operator   
        ex: 
        ```
            let a = 2
            a == 2 ? console.log(true) : console.log(false) //output:true
        ```
-   **Conditional Javascript**   

    Dalam javascript ketika kita menemukan kasus dimana suatu perintah hanya akan dijalankan ketika variabel memenuhi suatu kondisi tertentu, maka kita akan menggunakan antara `if`,`if-else`,atau `switch-case` tergantung dengan kasusnya seperti apa.Contoh:
    **if-else**
    ```
    let nilai= 99;
    if(nilai == 100){
        console.log("Mainnya hebat")
    }else{
        console.log("Mainnya jelek")
    }
    ```
    **switch-case**
    ```
    let angka = 2;
    switch (angka){
        case 1 :
            console.log("Kamu bernasib sial")
            break;
        case 2 :
            console.log("Kamu bernasib untung")
            break;
    }
    ```   

-   **Looping Javascript**   

    Dalam javascript ketika kita ingin menjalankan perintah yang sama berulang-ulang, kita akan memakai `for`,`for of`,`for in`,`while`,atau `do-while` tergantung kasusnya seperti apa.Contoh:    
    **for loop**
    ```
    for(let i=1;i<=10;i++>){
        console.log(i)
    }
    ```   
    **for of loop**
    ```
    let keranjang =["Mangga","Apel","Jeruk","Melon","Durian"]
    for (let x of keranjang){
        console.log(x);
    }
    ```
    **for in loop**
    ```
    let data = {
        nama: "Syahri",
        umur: 21,
        hobi: "meloncat"
    }
    for (let x in data){
        console.log(x,':',data[x])
    }
    ```
    **while loop**
    ```
    let number = 1
    let isFound = false;
    while(!isFound){
        if (number == 69){
            isFound = true
            console.log(number)
        }
        number++
    }
    ```
    **do-while loop**
    ```
    let i = 1;
    do{
        i = i + 2;
        console.log(i);        
    }
    while(i<=10)
    ```