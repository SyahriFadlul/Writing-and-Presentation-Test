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
-   `element.style.property`, memberi/mengubah nilai css element HTML
    ```
    <!-- html -->
    <h1 id="demo" style="color: blue;">Hello, World!</h1>
    ```
    ```
    // js
    let demo = document.getElementById("demo");

    console.log(demo.style.color); // Output: blue

    demo.style.color = "red";
    demo.style.fontSize = "18px";

    console.log(demo.style.color); // Output: red
    console.log(demo.style.fontSize); // Output: 18px
    ```    
---
## **Hari ke-5: Javascript Dasar DOM Form & Events** 
-   Events:
    -   click
    -   submit
    -   focus
    -   blur
    -   hover
    -   change
    -   scroll
    -   dll
-   Cara menggunakan events:
    -   Menggunakan HTML Attribute
    `<h1 onlick="alert('selamat datang')">click me</h1>`
    -   Menggunakan event property
    ```
    <html>
    <body onclick="myFunction(event)">

    <p>Click on any elements in this document to find out which element triggered the onclick event.</p>

    <h1>This is a heading</h1>

    <button>This is a button</button>

    <p id="demo"></p>

    <script>
    function myFunction(event) { 
    var x = event.target;
    document.getElementById("demo").innerHTML = "Triggered by a " + x.tagName + " element";
    }
    </script>

    </body>
    </html>
    ```
    -   Menggunakan addEventListener()
    ```
    <html>
    <body>

    <h1>The Document Object</h1>
    <h2>The addEventListener() Method</h2>

    <p>Click anywhere in the document to display "Hello World!".</p>

    <p id="demo"></p>

    <script>
    document.addEventListener("click", myFunction);

    function myFunction() {
    document.getElementById("demo").innerHTML = "Hello World";
    }
    </script>

    </body>
    </html>
    ```
-   Validasi Form:
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>

    <script src="login.js" defer></script>
  </head>
  <body>
    <div class="container">
      <form id="sign-in">
        <h1>Sign In</h1>

        <div class="field">
          <label for="username">username</label>
          <input type="text" id="username" name="username" />
        </div>

        <div class="field">
          <label for="password">password</label>
          <input type="text" id="password" name="password" />
        </div>

        <button type="submit">login</button>
      </form>
    </div>
  </body>
</html>
```

```
let loginForm = document.querySelector("#sign-in")
let inputUsername = document.querySelector('#username')
let inputPassword = document.querySelector('#password')

let user = {
  username: "syahri",
  password: "123"
}

loginForm.addEventListener("submit", (event) => {
  event.preventDefault()

  let userLogin = {
    username: inputUsername.value,
    password: inputPassword.value
  }

  console.log(userLogin);

  let login = userLogin.username == user.username && 
              userLogin.password == user.password;

  if (login) {
    console.log("selamat anda berhasil login")
  } else {
    console.log("username dan password anda salah");
  }

  loginForm.reset()


})
```
---

