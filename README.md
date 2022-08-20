# Asynchronous Pada JavaScript

> terdapat 3 fitur yang selalu dipakai ketika menggunakan JavaScript. kita perlu menjalankan eksekusi kode secara “asinkronus” ke dalam “event loop” dari proses utama JavaScript itu sendiri yaitu :

- Promise
- CallBack
- Await

> Deklarasikan Fungsi Promise

    Function GetUser(id) {
        return new Promise ((resolve, reject) => {
            if (id !== "" && id !== underfined) {
                resolve (id) ;
            } else {
                reject ("ID Harus Di Isi");
            }
        });
    }

Cara Penggunaan Promise

    GetUser ()
    .then ((response) => {
        console.log(response);
    })
    .catch ((error) =>{
        console.log(error);
    });

## Fetch Data
> "sebuah method pada API untuk mengambil resources dari jaringan, dan mengambil promise yang selesai (fullfilled) ketika ada response yang tersedia"
> Fetch Data merupakan fungsi atau alat kominikasi HTTP yang bertujuan untuk mengembalikan dan mengirim data pada suatu server.

HTTP Request:

1. Get = Mengambil data
2. Post = Mengirim Data
3. Put = Mengirim/Memperbaharui/update
4. Patch = update <= request tidak aman (Mengirim data secara parsial)
5. Delete = Menghapus Data

Fetch Get 1

    fetch ("https://pokeapi.co/api/v2/pokemon/pikachu/", {
        method: "GET"
    })

    .then ((response) => {
        return response.json();
    })
    .then((data) => {
        console.log(data)
    })
    .catch ((error) => {
        console.log(error);
    });

Fetch Get 2

    fetch ("https://pokeapi.co/api/v2/pokemon/pikachu/", {
            method: "GET"
    })
    .then (async (response) => {
        let convertData = await response.json();
        console.log(convertData)
    })
    .catch ((error) => {
            console.log(error);
    });

## Responsive Web Desain

> Responsive Web Design (RWD) ini bertujuan untuk membuat desain website kita dapat diakses dalam device apapun(layout dan mobile device). Device yang umumnya digunakan adalah laptop/pc, smartphone, dan tablet.

### Tambahkan tampilan di HTML
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        <img src="foto.jpg" style="max-width: 100%;" />
    </body>
    </html>

> pada html terdapat meta viewport yang digunakan untuk responsive seluler dan penambahan styling max-width pada tag body.

### Media Query

> Jenis Media Query untuk membantu web design kita menjadi responsive. umumnya hanya menggunakan 2 jenis media query yaitu **main-width** dan **mas-width**.

    Contoh:

    @media screen and (min-width: your pixel){

    }
    @media screen and (max-width: your pixel){

    }

> media query digunakan untuk membuat beberapa styles tergantung pada jenis device. ada 2 cara dalam menggunakan media query

1. membuat file css berbeda untuk masing-masing device
2. menggabungkan 1 file css untuk setting styling berbagai device.

### Breckpoint

> perubahan yang terjadi pada tampilan saat berganti device atau ukuran width disebut breckpoint.

### complex Breackpoint Media Query

> jika menginginkan tampilan yang ingin diterapkan pada range ukuran device tertentu. kita bisa membuat menjadi range media query

    contoh :

    body{
    background-color: white ;
    }

    @media screen and (min-width: 650px) and (max-width: 960px)
    body {
    background-color: aquamarine ;
    }

# **BOOTSTRAP**
> Bootstrap adalah kerangka kerja front-end gratis untuk pengembangan web yang lebih cepat dan mudah. Bootstrap menyertakan desain berbasis HTML dan CSS untuk formulir, tombol, tabel, nvigasi dan banyak lainnya. selain itu, bootstrap mampu membbuat desain responsif dengan mudah.
> komponen utama pada bootstrap :
- Bootstrap.css
- Bootstrap.js
> untuk dapat menggunakan Bootstrap di web, bisa dilakukan secara online melalui CDN dan secara offline dengan cara mendownload dari getbootstrap.com.
    Contoh

        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Document</title>

            <!-- cara memanggil css setelah file didownload -->
            <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css">

            <!-- cara memanggil css setelah file didownload -->
            <link rel="stylesheet" href="vendor/css/bootstrap.min.css">

        </head>
        <body>
        
            <!-- cara memanggil js bootstrap online -->
            <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js"></script>

            <!-- cara memanggil js bootstrap stlah file didownload -->
            <script src="vendor/js/bootstrap.bundle.js"></script>
        </body>
        </html> 

    

