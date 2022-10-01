# **Writing and Presentation Test Minggu ke-2**     

## **Hari ke-1: Javascript Dasar Scope dan Function**   

-   Scope dalam javascript adalah konsep dalam flow data variabel.
-   Scope menentukan bisa atau tidaknya variabel diakses.Contohnya variabel yang di dalam function tidak bisa diakses diluar function.
-   Ada 3 tipe scope dalam Javascript:
    -   Global scope, variabel langsung dideklarasikan dalam sebuah code(tidak didalam function atau block).
    -   Function scope/local scope, variabel dideklarasikan dalam sebuah function dan yang diluar function tersebut tidak bisa mengaksesnya.
    -   Block scope/local scope, variabel dideklarasikan di dalam `{}` , variabel yang ada di dalam blok tersebut tidak bisa diakses dari luar block kecuali variabel tersebut dideklarasikan menggunakan `var`. Yang mempunyai block scope adalah `let` dan `const`.   
-   Function adalah block code yang dimaksudkan untuk menyelesaikan suatu masalah/tugas.
-   Keuntungan menggunakan function adalah programmer tidak perlu menulis ulang code ketika ada suatu masalah/tugas yang sejenis, cukup memanggil function-nya saja.
-   Dalam sebuah function ada 3 komponen yang penting yaitu, parameter, perintah-nya dan argumen.
    ```
        function functionName(parameter){
                code
        }
        functionName(argument)
    ```     
-   Data dalam parameter akan digunakan untuk melakukan tugas dalam function tersebut.
-   Argument adalah inputan-nya.
-   Default parameter adalah nilai default function jika function dipanggil tetapi tidak memakai argumen.
    ```
    function greetings(nama="anonymous"){
        return `Hello ${nama}`
    }
    console.log(greetings()) //output : Hello anonymous
    ```
-   Kita juga bisa memanggil function didalam function
    ```
    function getPHI(){
        return 3.14
    }

    function luaslingkaran(r){
        return getPHI()*r*r
    }
    console.log(luaslingkaran(4)) //output : 50.24
    ```
-   Dalam versi Javascript terbaru(ES6) ada yang namanya **Arrow Function** yaitu cara penulisan function
    ```
    functionName = () =>{

    }
    ```
-   Dengan Arrow Function, programmer dapat menghemat waktu penulisan code.
-   Single Line Block:
    ```
    const luasLingkaran = r => 3.14*r*r;

    console.log(luasLingkaran(4)) // output : 50.24
    ```
-   Multi Line Block:
    ```
    const luasLingkaran = r => {
        const result = 3.14*r*r
        return result;
    }

    console.log(luasLingkaran(4)) // output : 50.24    
    ```
-   Contoh kasus:   
    Buat sebuah function untuk toko online kita. Ikuti poin-poin dibawah ini:   
        a. Function mempunyai 2 parameter yaitu nama pembeli dan produk yang dibeli    
        b. Function akan mengembalikan nilai "Terima kasih (nama pembeli) telah membeli produk (produk yang dibeli)"    
        c. Panggil function dengan menggunakan console.log()    
    Penyelesaian:
    ```
    const qabul = (namaPembeli, produk) => {
        return `Terima kasih ${namaPembeli} telah membeli ${produk}.`
    }

    console.log(qabul("Syahri","pulpen")) // output : Terima kasih Syahri telah membeli pulpen.
    ```       
--- 

## **Hari ke-2: Javascript Dasar Data Type Built in Prototype & Method** 

-   Tipe data primitif javascript:
    -   Number
    -   String
    -   Boolean
    -   Null
    -   Undefined
-   Tipe data non-primitif javascript:
    -   Array
    -   Function
    -   Object
-   Math property:
    -   `Math.E`               
    -   `Math.LN2`             
    -   `Math.LN10`            
    -   `Math.LOG2E`           
    -   `Math.LOG10E`          
    -   `Math.PI `             
    -   `Math.SQRT1_2`
    -   `Math.SQRT2`
-   Math method:
    -   `Math.abs(x)`
    -   `Math.pow(x,y)`
    -   `Math.sqrt(x)`
    -   `Math.cbrt(x)`
    -   `ath.round(x)`
    -   `Math.floor(x)`
    -   `Math.ceil(x)`
    -   `Math.random()`
    -   `Math.max(x,y,z,...,n)`
    -   `Math.min(x,y,z,...,n)`
---
## **Hari ke-3: Javascript Dasar DOM**     
-   DOM atau _Document Object Model_  adalah interface yang memungkinkan developer untuk memanipulasi konten, struktur, dan style situs web.
-   DOM mengambil elemen-elemen HTML dalam bentuk tree, yang paling atas adalah `html` yang paling bawah biasanya attribute atau konten.
-   Cara mengambil elemen HTML adalah sebagai berikut:
    -   `document.getElementById()`, mengambil elemen HTML berdasarkan Id-nya
    -   `document.getElementsByClassName()`, mengambil elemen HTML berdasarkan class name-nya
    -   `document.getElementByTagName()`, mengambil elemen HTML berdasarkan tag name-nya
    -   `document.querySelectorAll()`, mengambil elemen HTML berdasarkan css selector-nya
-   Traversing atau menjelajang element HTML:
    -   `parentNode`
    -   `childNodes[nodenumber]`
    -   `firstChild`
    -   `lastChild`
    -   `nextSibling`
    -   `previousSibling`

---
## **Hari ke-4: Javascript Dasar DOM Manipulating Elements and Styles**
-   `InnerHTML`, mengambil/mengubah isi element HTML
    ```
    <!-- html -->
    <p id="demo">Hello, World!</p>
    ```
    ```
    //js
    let demo = document.getElementById("demo")
    demo.innerHTML = "Hello, You!"
    console.log(demo)    //output : Hello, You!
    ```
-   `element.attribut`, mengambil/mengubah/memberi nilai attribute HTML
    ```
    <!-- html -->
    <img src="https://bit.ly/2FKluzq" alt="Cat" id="cat-image" />
    ```
    ```
    let catImage = document.getElementById("cat-image");

    console.log(catImage.src); // Output: https://bit.ly/2FKluzq
    console.log(catImage.alt); // Output: Cat

    catImage.src = "https://bit.ly/3j6YdWJ";
    catImage.alt = "Fish";
    catImage.width = "400";

    console.log(catImage.src); // Output: https://bit.ly/3j6YdWJ
    console.log(catImage.alt); // Output: Fish
    console.log(catImage.width); // Output: 400
    ```
-   `element.setAttribute`, fungsinya hampir sama dengan `element.attribute` bedanya `element.setAttribute` adalah DOM method sedangkan `element.attribute` adalah DOM property
    ```
    <!-- html -->
    <img src="https://bit.ly/2FKluzq" alt="Cat" id="cat-image" />
    ```
    ```
    // js
    let catImage = document.getElementById("cat-image");

    catImage.setAttribute("src", "https://bit.ly/3j6YdWJ");
    catImage.setAttribute("alt", "Fish");
    catImage.setAttribute("width", "400");

    console.log(catImage.src); // Output: https://bit.ly/3j6YdWJ
    console.log(catImage.alt); // Output: Fish
    console.log(catImage.width); // Output: 400
    ```
---
## **Hari ke-5: Javascript Dasar Scope dan Function** 
    
---

