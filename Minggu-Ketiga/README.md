# **Writing and Presentation Test Minggu ke-3**     

## **Hari ke-1: JavaScript intermediate - Array & Multidimensional Array**  

-   Dengan array programmer dapat menyimpan banyak data dalam 1 variabel dengan tipe data yang bisa lebih dari satu.
-   Contoh array:
    ```
    let buah = ["Nanas","Anggur","Jeruk"]

    console.log(buah[0]); // output : ['Nanas']
    console.log(buah[1]); // output : ['Anggur']
    console.log(buah[2]); // output : ['Jeruk']
    ```
    -   Dideklarasikan dengan `[]`, dimulai dari index[0]
-   Menampilkan array menggunakan for of:
    ```
    let buah = ["Nanas","Anggur","Jeruk"]

    for(let x of buah){
        console.log(x)
    }
    ```
-   Array multidimensi:
    ```
    let profile = [["Bambang", 21],["Cahyono", 32],["Asep",25]]
    console.log(profile[0][1]) // output : 21 
    console.log(profile[1][0]) // output : Cahyono
    console.log(profile[2][0]) // output : Asep
    ```
-   Menambahkan data ke dalam array:
    ```
    let buah = ["Durian","Melon"]
    buah.push("Mangga")
    console.log(buah) // output : ["Durian","Melon","Mangga"]
    ```
-   .forEach()
    ```
    let buah = ["Durian","Melon"]
    buah.push("Mangga")

    buah.forEach((number,index)=>{
    console.log('Index: ' + index + ' Value: ' + number);
    })
    ```
-   .map()
    ```
    const numbers = [1, 2, 3, 4];
    const newArr = numbers.map((num)=>{
    return num * 10
    })

    console.log(newArr); // output : [10,20,30,40]
    ```
---    

## **Hari ke-2: JavaScript Intermediate - Object & Array of Object**  
-   Object adalah tipe data yang menyimpan property dan nilai(bisa tipe data lainnya atau function)
-   Contoh object:
    ```
    let profile= {
        namaAwal : "Bambang",
        namaAkhir : "Wilson",
        umur : 21,
        namaLengkap : function(){
            return this.namaAwal + " " + this.namaAkhir;
        }        
    }
    console.log(profile) // output : { nama: 'Bambang', umur: 21, namaLengkap: [function:namaLengkap]}
    console.log(profile.namaAwal) // output : Bambang
    console.log(profile['umur']) // output : 21
    console.log(profile.namaLengkap()) // output : Bambang Wilson
    ```
-   Update object:
    ```
    let profile= {
        namaAwal : "Bambang",
        namaAkhir : "Wilson",
        umur : 21,
        namaLengkap : function(){
        return this.namaAwal + " " + this.namaAkhir;
        }        
    }
    profile = {namaAwal:"Duma"}
    console.log(profile) // output : { namaAwal: 'Duma' }
    ```
-   Delete object property:
    ```
    let profile= {
        namaAwal : "Bambang",
        namaAkhir : "Wilson",
        umur : 21,
        namaLengkap : function(){
        return this.namaAwal + " " + this.namaAkhir;
        }        
    }
    delete profile.namaLengkap;

    console.log(profile) // output : { namaAwal: 'Bambang', namaAkhir: 'Wilson', umur: 21 }
    ```
-   Nested object:
    ```
    let profile= {
        namaAwal : "Bambang",
        namaAkhir : "Wilson",
        umur : 21,
        keluarga : {
            anggotaKeluarga:{
                ayah : "Agus",
                ibu : "Elizabeth",
                kakak : "Leon",
                adik : "Siti"
            }
        }       
    }

    console.log(profile.keluarga.anggotaKeluarga.adik) // output : Siti
    ```
-   Menampilkan object menggunakan looping for in:
    ```
    let profile= {
        namaAwal : "Bambang",
        namaAkhir : "Wilson",
        umur : 21,
        keluarga : {
            anggotaKeluarga:{
                ayah : "Agus",
                ibu : "Elizabeth",
                kakak : "Leon",
                adik : "Siti"
            }
        }                
    }
    for (let data in profile){
        console.log(profile[data])
    }
    for (let data in profile.keluarga.anggotaKeluarga){
        console.log(profile.keluarga.anggotaKeluarga[data])
    }
    ```
-   Array of object:
    ```
    let dataSiswa = [
        {
            nama : "Kayden",
            umur : 18
        },
        {
            nama : "Nana",
            umur : 18
        }
    ]
    dataSiswa.forEach((listdataSiswa) => {
        console.log(listdataSiswa)
    })  // output : { nama: 'Kayden', umur: 18 }
        //          { nama: 'Nana', umur: 18 }
    ```
---    

## **Hari ke-3: JavaScript Intermediate - Rekursif & Modules**  
-   **Rekursif** adalah function yang melakukan perulangan dengan cara memanggil diri sendiri didalam dirinya sendiri.
    ```
    const recursion = () => {
        //kode

        recursion()
    }
    ```
-   Rekursif cocok untuk penyelesaian masalah pada matematika, fisika, kimia dan yang berhubungan dengan operasi hitung lainnya.
-   Dengan rekursif kode lebih mudah dibaca dan beberapa algoritma secara natural lebih cocok dengan rekursif.
-   Rekursif menggunakan memori lebih banyak dibanding iteratif(looping dll) jika data yang diuji banyak.
-   **Module** pada javascript adalah memisahkan kode ke beberapa file js terpisah dan saling terhubung menggunakan **export-import** dan menggunakan attribute `type='module'` pada tag script dalam html.

---    

## **Hari ke-4: JavaScript Intermediate - Asynchronous Introduction & Promise**  
-   **Asynchronous** adalah menjalankan perintah secara bersamaan sambil menunggu perintah lainnya yang membutuhkan waktu lebih lama untuk dijalankan.
    ```
    function proses1() {
        console.log("proses 1 selesai dijalankan");
    }

    function proses2() {
        setTimeout(function () {
            console.log("proses 2 selesai dijalankan");
        }, 100);
    }

    function proses3() {
        console.log("proses 3 selesai dijalankan");
    }

    proses1();
    proses2();
    proses3();
    /*
    Hasil Output
    proses1 selesai dijalankan
    proses3 selesai dijalankan
    proses2 selesai dijalankan
    */
    ```
-   **Callback** adalah function yang dijalankan di parameter function lain.
    ```
    function proses1() {
        console.log("proses 1 selesai dijalankan");
    }

    function proses2(callback) {
        setTimeout(function () {
            console.log("proses 2 selesai dijalankan");
        }, 100);
    }

    function proses3() {
        console.log("proses 3 selesai dijalankan");
    }

    proses1();
    proses2(proses3);
    /*
    Hasil Output
    proses1 selesai dijalankan
    proses2 selesai dijalankan
    proses3 selesai dijalankan
    */
-   Callback dapat digunakan untuk mengatur order function yang harus berjalan terlebih dahulu.
-   **Asynchronous promise** mempunyai 3 pernyataan yaitu pending,fulfilled dan rejected


---

## **Hari ke-5: JavaScript Intermediate - Web Storage**  
-   **Web storage** adalah penyimpanan lokal yang berisi data-data tentang hasil interaksi user dengan web, sehingga web akan menggunakan data tersebut sebagai preferensi untuk user.
-   Ada 3 tipe web storage yaitu:
    -   **Cookies**, yaitu data kecil berukurang 4KB yang dikirim oleh web dan disimpan di komputer kita. Biasanya data yang tersimpan berbentuk _access token_ pengguna saat login atau data pencarian saat melakukan pencarian pada web tertentu.
    Hal ini yang biasanya dilakukan oleh situs pencarian untuk melacak pencarian kita dan menampilkan iklan yang berhubungan dengan pencarian kita sebelumnya. Kekurangannya adalah ukurannya hanya 4KB, membuat kerja browser lambat, dan juga ketika melakukan request ke server cookie juga akan ikut disertakan dan cookie ini tidak terenkripsi, dan juga ada tanggal kadaluarsanya.    
    Bentuk cookies biasanya berbentuk pasangan name-value :
    ```
    username = syahri
    ```

    -   **Local Storage**, web storage yang dapat menyimpan data berbentuk string sampai 5MB dan juga tidak ada tanggal kadaluarsanya sampai kita menghapusnya.Contoh local storage yaitu history pencarian kita.   
    Cara menyimpan data ke local storage yaitu dengan menggunakan method `setItem()`. Contoh
    ```
    <!--HTML-->
    <form>
        <input type="text" id="searchkey" name="searchkey" placeholder="Search Something"><br>
        <input type="submit" value="Search" onclick="onSearch()">
    </form>   
    ```
    ```
    // javascript
    let searchList = [];
    function onSearch() {
        let searchValue = document.getElementById('searchkey').value;
        searchList.push(searchValue) // memasukan kata pencarian ke dalam array
        
        let searchListString = JSON.stringify(searchList); // mengubah array menjadi string
        localStorage.setItem('searchKey', searchListString); // menyimpan pencarian dengan key 'searchKey'
    }
    ``` 
    Ketika mengisi field search dan menekan tombol search maka datanya akan tersimpan di local storage.
    Cara melihatnya inspect web page>application>local storage>web page saat ini.
    ![local_storage](https://github.com/SyahriFadlul/Writing-and-Presentation-Test/blob/main/Minggu-Ketiga/images/local_storage.png)
    Dan juga kita bisa mengambil data pada local storage menggunakan `localStorage.getItem('key',string)`.
    Jika ingin menghapus gunakan `localStorage.removeItem('key')`dan `localStorage.clear()` untuk menghapus semua data.
    -   **Session Storage**, yaitu penyimpanan data sementara ketika pengguna membuka web page dengan ukuran penyimpanan sebesar 5MB. Data penyimpanan akan hilang ketika pengguna menghapus web atau menutup web browser, jika pengguna hanya merefresh web page maka data masih tersimpan. Dan jika pengguna membuka web page yang sama dibeberapa tab maka Session storagenya pun berbeda.Cara melihat session storage sama seperti local storage, session storage berada dibawah local storage.
        -   `sessionStorage.setItem('key',string)` , untuk menambahkan data ke session storage.
        -   `sessionStorage.getItem('key')` , untuk mengambil data pada session storage.
        -   `sessionStorage.removeItem('key')` , untuk menghapus data pada session storage.
        -   `sessionStorage.clear()` , untuk menghapus semua data pada session storage.



