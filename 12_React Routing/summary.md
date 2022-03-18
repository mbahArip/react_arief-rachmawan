# 12 React Routing

## Resume

Pada materi ini saya mempelajari:

-   Router
-   URL Parameter
-   Router Hooks

### Router

#### Apa itu Router?

Router merupakan modul dalam react yang berfungsi untuk melakukan proses navigasi pada Single Page Application.

#### Single vs Multi Page Application

Single Page Application adalah salah satu jenis aplikasi website yang dimana hanya ada 1 halaman untuk menangani semua aktivitas yang terjadi dalam aplikasi tersebut.  
Multi Page Application adalah jenis aplikasi website dimana aplikasi perlu memuat ulang seluruh halaman web setiap kali membuat permintaan baru.

#### Kelebihan

| Single Page Application              | Multi Page Application                                                     |
| ------------------------------------ | -------------------------------------------------------------------------- |
| + Waktu loading lebih cepat          | + SEO Website akan lebih mudah dioptimasi                                  |
| + Tidak ada query tambahan ke server | + Memudahkan untuk mengubah halman tertentu untuk setiap kebutuhan berbeda |
| + Front-end yang cepat dan responsif | + Memudahkan tool analisis                                                 |
| + Meningkatkan user experience       |                                                                            |

#### Kekurangan

| Single Page Application               | Multi Page Application                                     |
| ------------------------------------- | ---------------------------------------------------------- | -------------------------------------------- |
| - Tidak bagus dalam hal SEO           | - Kecepatan download website jauh lebih lama dibanding SPA |
| - Berat saat di load pertama kali     | - Perlu mengintegrasikan antara front-end dan back-end     |
| - Kurang aman dibanding website biasa | - Lebih sering membutuhkan maintenance dan update          |
| - Masalah kompatibilitas              | -                                                          | Akan lebih sering menemukan masalah performa |

#### Instalasi React Router

React Router dapat di install dengan cara membuka command prompt dan mengetik:

```node
npm i react-router-dom
```

#### Komponen React Router DOM

React router memiliki beberapa komponen, yaitu:

-   BrowserRouter, digunakan sebagai router yang menggunakan API History dari HTML5, sehingga dapat menggunakan location untuk singkronkan UI dengan URL. Di dalam object location sendiri mempresentasikan dimana lokasi aplikasi sekarang.
-   Route, digunakan sebagai pengarah jalannya lalu lintas suatu aplikasi web, terdapat 2 atribut yaitu path dan component. Path merupakan url pada browser, sedangkan Component merupakan komponen yang akan dirender.
-   Switch, digunakan untuk membungkus kumpulan beberapa komponen route. Exact bertugas untuk memastikan route hanya merendeer komponen yang memiliki path yang cocok.
-   Link, digunakan untuk berpindah antar halaman. Atribut to berfungsi untuk menentukan url yang akan dituju.

### URL Parameter

Parameter URL adalah suatu parameter yang nilainya ditetapkan secara dinamis di URL halaman.

#### Kegunaan

Beberapa kegunaan URL Parameter antara lain:

-   Paginasi
-   Penyortiran dan Penyaringan
-   Pencarian
-   Menggambarkan

#### Cara menggunakan URL Parameter

URL Parameter dapat digunakan dengan cara memanggil `this.props.match.params`.

### Router Hooks

Ada beberapa router hooks yang dapat digunakan, antara lain:

-   useHistory  
    useHistory memberi kita akses ke instance riwayat yang dapat digunakan untuk navigasi.
-   useLocation  
    useLocation akan mengembalikan object location yang mewakili lokasi URL saat ini.
-   useParams  
    useParams akan mengembalikan object yang berisi parameter yang dikirimkan dari URL.
-   useRouteMatch  
    useRouteMatch mencoba mencocokan URL saat ini dengan cara yang sama seperti `<Route>`, sebagian besar berguna untuk mendapatkan akses ke data kecocokan tanpa benar-benar merender Route.

---

## Task
