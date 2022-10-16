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
    ![result]()

---

## **Hari ke-2: Git & GitHub Lanjutan**  
-   

---

## **Hari ke-3: Responsive Web Design & Bootstrap 5**  

