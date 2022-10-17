# **Writing and Presentation Test Minggu ke-4**     

## **Hari ke-1: JavaScript Intermediate - Asynchronous - Fetch & Async Await**  
-   Asychronous `fetch` berguna untuk mengambil data pada API.
-   Untuk menangkap data API kita bisa menggunakan **Promise** dan juga **Async Await**.
-   Contoh penggunaan fetch dan async await:
    ```
    const getData = async () =>{
        let response = await fetch("https://digimon-api.vercel.app/api/digimon")
        let result = await response.json()
        console.log(result) // output : data digimon berupa array of object
    }
    ```
-   Cara menampilkan data API ke HTML:
    ```
    <!--HTML-->
    <body>
        <div id="digimon-list">
        </div>
    </body>
    ```
    ```
    //Javascript
    const getData = async () =>{
        let response = await fetch("https://digimon-api.vercel.app/api/digimon")
        let result = await response.json()
        
        result.forEach(item =>{
            document.getElementById('digimon-list').innerHTML +=
            `
            <div class='digimon-item'>
            <img src='${item.img}'>
            <h2>${item.name}</h2>
            </div>
            `
        })
    }
    getData()
    ```
    **OUTPUT**:
    ![result](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/result.png)

---

## **Hari ke-2: Git & GitHub Lanjutan**  
-   **Git&GitHub** merupakan tools wajib bagi seorang programmer, karena dengannya kerja programmer menjadi lebih tertata.
-   Dengan Git programmer dapat melakukan version control, sehingga ketika kita melakukan kesalahan kita bisa kembali ke checkpoint sebelumnya.
-   Dengan GitHub programmer dapat melakukan kolaborasi dengan programmer lainnya dengan mudah. Meskipun akan ada konflik antar kodingan, dengan git kita bisa tau bagian mana yang mengalami konflik.
-   Git merupakan version control dan GitHub merupakan layanan hosting repository yang memungkinkan programmer berkolaborasi.
-   Contoh berkolaborasi dalam GitHub:
    -   Leader membuat akun organisasi    

    ![git_add_org](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/git_add_org.png)
    -   Leader membuat repository dengan akun organisasi
    ![colab_newrepo](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/colab_newrepo.png)
    -   Leader membuat branch bernama `dev`    

    ![branch_dev](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/branch_dev.png)     

    -   Tiap anggota melakukan clone
    ![git_clone_1](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/git_clone_1.png)
    -   Switch ke branch dev
    ![switch_devv](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/switch_dev.png)
    -   Lakukan pull untuk mengupdate kode terbaru
    ![git_pull](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/git_pull.png)
    -   Tiap anggota membuat masing-masing branch(atau bisa juga membuat branch dengan nama berdasarkan fitur)
    ![each_branch](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/each_branch.png)
    -   Lalu masuk ke branch masing masing
    ![switch_each_branch](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/switch_each_branch.png)
    -   Kerjakan tugas masing-masing lalu git add,commit sperti biasa           
    add
    ![git_add](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/git_add.png)
    commit
    ![git_commit](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/git_commit.png)
    - Git merge dev untuk menghindari conflict
    ![merge_dev-t](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/merge_dev-t.png)
    -   Jika ada conflict,selesaikan
    -   Jika sudah aman push ke branch masig masing
    ![git_push](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/git_push.png)
    -   Lakukan pull request merge dev
    ![pull_req](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/pull_req.png)
    ![new_pull_req](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/new_pull_req.png)
    ![choose_to_pull](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/choose_to_pull.png)
    ![merge_pull_req-a](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/merge_pull_req-a.png)     

    assign ke leader     

    ![assign_toleader](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/assign_toleader.png)     
    
    ![create_pull_req](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/create_pull_req.png)
-   Jika ada conflict maka akan seperti ini
![git_conflict](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/git_conflict.png)
-   Klik 'Use the command line' lalu ikuti perintahnya
![git_resolving](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/git_resolving.png)


---

## **Hari ke-3: Responsive Web Design & Bootstrap 5**  
-   Responsive Web Design adalah metode designing yang bertujuan agar website dapat diakses berbagai device.
-   Dengan Responsive Web Design tampilan web akan menyesuaikan dengan device yang user gunakan sehingga tampilan tidak terlalu besar atau terlalu kecil.
-   Tools yang biasa digunakan adalah tools bawaan chrome yaitu  Chrome Dev tools, cara membukanya dengan menekan tombol `Ctrl`+`Shift`+`J` secara bersamaan. Tampilannya akan seperti ini:
![chrome_dev_tools](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/chrome_dev_tools.png)
-   `viewport` merupakan daerah pada layar device yang menampilkan halaman website.Cara penggunaanya adalah menambahkan tag meta pada bagian head di html.
```
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    </head>
```
-   `width=device-width` memberitahu browser untuk mengikuti lebar layar device.
-   `initiacl-scale=1.0` memberitahu browser tingkat pembesarannya(zoom level).
-   Relative Unit CSS merupakan ukuran relatif terhadap properti ukuran lainnya. Satuan Relative Unit CSS yang paling sering digunakan adalah:
    -   `em` , ukurannya mengacu pada parent elementnya (2em berarti ukurannya 2x dari ukuran parent elementnya).
    -   `rem` , ukurannya mengacu pada root element yaitu html itu sendiri (2rem berarti ukurannya 2x dari ukuran rootnya).
    -   `%` , ukurannya mengacu pada parent elementnya (20% berarti ukurannya 20% dari ukuran parent elementnya).
    -   `vw` , yaitu viewport width yang berarti mengacu pada lebar window browser (2vw berarti ukurannya 2% dari lebar viewport).
-   Media Query, dengannya kita bisa mengatur style elemen ketika kondisi resolusinya terpenuhi. Contohnya:
    ```
    @media only screen and (min-width:400px) and (max-width:600px){
        background-color: blue;
    }
    ```
    -   Dengan menggunakan _breakpoint_ diatas (min-width:400px , max-width:600px), ketika sebuah layar memiliki lebar lebih dari sama dengan 400px dan kurang dari sama dengan 600px maka backgroundnya akan berwarna biru.
-   Flexbox daat mengatur layout,posisi dan ukuran elemen jadi lebih mudah.
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
    -   Code diatas membuat elemen menjadi flex dengan flex-direction nya row atau baris dan kontennya berada di start(kiri).
    -   Beberapa nilai property justify-content:
        -   flex-end, konten akan ditampilkan di akhir blok.
        -   center, konten akan ditampilkan di tengah tengah blok.
        -   space-between, tiap kontennya memiliki jarak satu sama lain.
        -   space-around, tiap konten memiliki padding horizontal yang sama.
-   Dengan **grid** kita dapat dengan mudah mengatur layout menjadi lebih rapih. Dalam grid kita bisa ngatur baris dan kolomnya.
    ```
    <head>
        <style>
            .grid-container {
                height: 500px;
                display: grid;
                grid-template-columns: auto auto auto; 
                background-color: blue;  
                gap: 20px; 
                padding: 10px;             
                align-content: end;
                justify-content: center;                               
            }
            .grid-container > div{
                padding: 20px;
                background-color: aliceblue;
                
            }
        </style>
    </head>
    <body>
        <div class="grid-container">
            <div class="grid-item1">1</div>
            <div class="grid-item2">2</div>
            <div class="grid-item3">3</div>  
            <div class="grid-item4">4</div>
            <div class="grid-item5">5</div>
            <div class="grid-item6">6</div>  
            <div class="grid-item7">7</div>
            <div class="grid-item8">8</div>
            <div class="grid-item9">9</div>  
            <div class="grid-item10">10</div>  
            <div class="grid-item11">11</div>  
            <div class="grid-item12">12</div>  
        </div>
    <body>
    ```
    Output:     

    ![grid_container](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/grid_container.png)      

    -   Untuk menggunakan grid style kita gunakan `display:grid` atau `display:inline-grid`.
    -   `grid-template-columns: auto auto auto auto` berarti grid mempunyai 4 column yang ukurannya `auto`.
    -   Untuk membuat grid berdasarkan row gunakan `grid-template-rows`.
    -   `gap` digunakan untuk mengatur jarak antar item, bisa juga menggunakan `gap-column` untuk mengatur jarak antar kolomnya atau `gap-row` untuk mengatur jarak antar baris.
    -   `align-content` digunakan untuk mengatur item grid secara vertikal. Jika valuenya `end` maka item grid akan diletakan dibawah.
    -   `justify-content` digunakan untuk mengatur keseluruhan konten grid. Jika valuenya `center` maka konten grid akan diletakan ditengah. secara horizonta.Jika valuenya `space-between` maka tiap item memiliki ruang yang sama secara horizontal.
-   Kita juga bisa memberikan style kepada item grid container.
    ```
    <head>
        <style>
            .grid-container {
                height: 500px;
                display: grid;
                grid-template-columns: auto auto auto auto; 
                background-color: blue;  
                gap: 20px; 
                padding: 10px;                                                       
            }
            .grid-container > div{            
                font-size: 36px;
                padding: 20px;
                background-color: aliceblue;
                text-align: center;            
            }
            .grid-item1 {
                grid-row: 1/3;
            }
            .grid-item2 {
                grid-column: 2/4;
            }
            .grid-item3 {
                grid-row-start: 2;
                grid-row-end: 4;

            }
            .grid-item8 {
                grid-area: 3/2/5/4
            }                
        </style>
    </head>
    <body>
        <div class="grid-container">
            <div class="grid-item1">1</div>
            <div class="grid-item2">2</div>
            <div class="grid-item3">3</div>  
            <div class="grid-item4">4</div>
            <div class="grid-item5">5</div>
            <div class="grid-item6">6</div>  
            <div class="grid-item7">7</div>
            <div class="grid-item8">8</div>
            <div class="grid-item9">9</div>
            <div class="grid-item10">10</div>  
            <div class="grid-item11">11</div>  
            <div class="grid-item12">12</div>                
        </div>
    <body>
    ```     

    ![grid_childs](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Keempat/images/grid_childs.png)      

    -   `grid-row:1/3` berarti item akan diletakan dimulai dari row-line 1 atau row 1 sampai row-line 3 atau sebelum row 3.
    -   `grid-column:2/4` berarti item akan diletakan di column-line 2 atau column ke 2 sampai column-line ke 4 atau sebelum column ke 4.
    -   Penggunaan `grid-row-start` `grid-row-end` sama saja seperti `grid-row: start/end`, hanya saja penulisannya lebih ringkas.
    -   `grid-area:3/2/5/4` berarti item diletakan di row-line 3 column-line 2 sampai row-line 5 column-line 4.
-   **Bootstrap** memudahkan programmer untuk memberikan style ke halaman website
-   Cara yang paling mudah menggunakan bootstrap yang pertama adalah insert code berikut di dalam `<head>`:
```
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
```
-   Setelah itu tinggal copy-paste styling yang diinginkan di website bootstrap.
-   contoh layout grid:
```
 <body>
<div class="container">
  <div class="row">
    <div class="col">
      Column
    </div>
    <div class="col">
      Column
    </div>
    <div class="col">
      Column
    </div>
  </div>
</div>
 </body>   
```
-   contoh content table:
```
<body>
<table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2">Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
</table>
</body>
```
-   contoh component accordion:
```
<body>
<div class="accordion" id="accordionExample">
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingOne">
      <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
        Accordion Item #1
      </button>
    </h2>
    <div id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne" data-bs-parent="#accordionExample">
      <div class="accordion-body">
        <strong>This is the first item's accordion body.</strong> It is shown by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingTwo">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
        Accordion Item #2
      </button>
    </h2>
    <div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo" data-bs-parent="#accordionExample">
      <div class="accordion-body">
        <strong>This is the second item's accordion body.</strong> It is hidden by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingThree">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
        Accordion Item #3
      </button>
    </h2>
    <div id="collapseThree" class="accordion-collapse collapse" aria-labelledby="headingThree" data-bs-parent="#accordionExample">
      <div class="accordion-body">
        <strong>This is the third item's accordion body.</strong> It is hidden by default, until the collapse plugin adds the appropriate classes that we use to style each element. These classes control the overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this with custom CSS or overriding our default variables. It's also worth noting that just about any HTML can go within the <code>.accordion-body</code>, though the transition does limit overflow.
      </div>
    </div>
  </div>
</div>
</body>
```
-   contoh css responsive:
```
// We deliberately hardcode the `bs-` prefix because we check
// this custom property in JS to determine Popper's positioning

@each $breakpoint in map-keys($grid-breakpoints) {
  @include media-breakpoint-up($breakpoint) {
    $infix: breakpoint-infix($breakpoint, $grid-breakpoints);

    .dropdown-menu#{$infix}-start {
      --bs-position: start;

      &[data-bs-popper] {
        right: auto;
        left: 0;
      }
    }

    .dropdown-menu#{$infix}-end {
      --bs-position: end;

      &[data-bs-popper] {
        right: 0;
        left: auto;
      }
    }
  }
}
$grid-breakpoints: (
  xs: 0,
  sm: 576px,
  md: 768px,
  lg: 992px,
  xl: 1200px,
  xxl: 1400px
);
```