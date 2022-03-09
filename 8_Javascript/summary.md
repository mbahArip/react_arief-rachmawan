# 08 Javascript

## Resume

Pada materi ini saya mempelajari :

-   Apa itu javascript
-   Basic javascript
-   Javascript DOM

### Apa itu javascript

Javascript adalah bahasa pemrograman yang high level, scripting, untyped, dan interpreted. Kenapa menggunakan javascript?
- Mudah dimengerti oleh manusia
- Dibuat untuk berinteraksi dengan halaman web
- Tidak berpengaruh dengan type data
- Kita dapat menjalankannya selama kita memiliki browser
- Memiliki banyak framework
- Mudah dipelajari, sulit dikuasai

### Basic javascript

#### Values
Declaration adalah proses pembuatan variable untuk menyimpan data. Jenis-jenis variable yang ada di javascript antara lain:
- Var, umumnya kita jarang memakai ini
- Let, digunakan saat kita membutuhkan nilai yang dapat diubah
- Const, digunakan saat kita membutuhkan nilai yang tidak dapat diubah

Scoping menentukan dimana variable, function, dan object diatur dan dapat diakses.  
Ruang lingkup variable dikendalikan oleh lokasi deklarasi variable.
- Scope global, semua jenis variable dapat diakses
- Scope function / local, semua jenis variable tidak dapat diakses
- Scope block, hanya var saya yang dapat diakses

#### Destructuring
Destructuring adalah proses pembuatan variable dari sebuah array atau object.

Contoh:
```js
let array = [1, 2, 3];
const [a, b, c] = array;
console.log(a, b, c); //Output: 1 2 3
```

Spread syntax dapat digunakan ketika semua elemen dari array atau object perlu dimasukkan ke dalam sebuah daftar.

Contoh:
```js
let array1 = ['Budi', 'Siti' ,'Ayu'];
let array2 = ['Bandung', 'Jakarta', 'Bogor'];
let spread = [...array1, ...array2];
console.log(spread); //Output: ['Budi', 'Siti', 'Ayu', 'Bandung', 'Jakarta', 'Bogor']
```

#### Methods
Method merupakan sebuah fungsi yang terkait dengan object, dan membuat program sesederhana mungkin sesuai kegunaan masing-masing.

Contoh methods dan fungsinya:
- Concat, Menggabungkan 2 atau lebih array, dan mengebalikan array yang digabungkan
- Map, Mengubah sebuah array baru dengan hasil memanggil fungsi untuk setiap elemen array
- ForEach, Melakukan sebuah aksi untuk setiap elemen array
- Slice, Mengambil sebagian dari array
- Filter, Mengambil elemen array yang memenuhi kondisi
- Reduce, Melakukan operasi pada setiap elemen array menjadi nilai tunggal

#### Control Flow
Control flow adalah proses pengaturan alur eksekusi pada statement atau jalannya program sesuai keinginan.  
Control flow terbagi menjadi 2, yaitu:
- Pengulangan
- Pengkondisian

Contoh pengulangan:
- For
- While
- Do While

Contoh Pengkondisian:
- If ... Else
- Switch
- Block
- Try ... Catch
- Break
- Continue
- Throw

#### Function
Function adalah sebuah blok kode yang dapat dijalankan secara berulang kali dengan nama yang sama.

#### Classes
Class adalah sebuah blok kode yang dapat dijalankan secara berulang kali dengan nama yang berbeda.
Pada classes terdapat:
- Constructor, merupakan method yang akan terpanggil pertama kali ketika membuat object dari class tersebut.
- Method, merupakan fungsi yang berada di dalam class.
- Attributes, merupakan nilai yang dapat diakses oleh object dari class tersebut.
- Extend, digunakan untuk membuat kelas anak dari kelas induk. Akan mewarisi semua atribut dan metode dari kelas induk.

#### Async Wait
Apa itu Synchronous dan Asynchronous?
- Synchronous adalah proses mengeksekusi setiap perintah satu persatu sesuai urutan kode yang dituliskan.
- Asynchronous adalah proses mengeksekusi setiap perintah satu persatu, tetapi tidak sesuai urutan kode yang dituliskan.

Promise adalah objek yang merepresentasikan keberhasilan atau kegagalan pada sebuah event async yang ditunggu.

Callback adalah sebuah fungsi yang dapat dijadikan sebagai parameter untuk fungsi lain.

Function Async adalah sebuah fungsi yang mengembalikan sebuah Promise.

Await adalah sebuah keyword yang digunakan untuk menunggu sebuah Promise selesai.

### Javascript DOM
Javascript DOM adalah API untuk html yang merepresentasikan halaman web pada suatu dokumen menjadi sebuah object.

#### DOM Selection Method
- getElementById, mengambil elemen html yang memiliki id tertentu. **Return type: HTMLElement**
- getElementsByTagName, mengambil elemen html yang memiliki tag tertentu. Return type: HTMLCollection
- getElementsByClassName, mengambil elemen html yang memiliki class tertentu. **Return type: HTMLCollection**
- querySelector, mengambil elemen html yang memiliki selector tertentu. **Return type: HTMLElement**
- querySelectorAll, mengambil semua elemen html yang memiliki selector tertentu. **Return type: NodeList**

#### DOM Manipulation
- element.innerHTML, mengubah isi dari elemen html.
- element.style.\<propertyCSS>, mengubah property CSS dari elemen html.
- element.setAttribute, menambahkan atribut pada elemen html.
- element.classList.add, menambahkan class pada elemen html.

#### DOM Event
- onclick, aktif ketika elemen html diklik.
- onchange, aktif ketika elemen input diubah.
- onblur, aktif ketika elemen input meninggalkan focus.
- onmouseover, aktif ketika mouse berada diatas elemen html.
- onmouseout, aktif ketika mouse berada di luar elemen html.
- oncopy, aktif ketika elemen html di copy.

#### Event Handler
- Inline HTML Attribute, kita harus mengubah event di html dan js.
- Element method, kita hanya mengubah event di js.
- addEventListener, sama seperti element method, berbeda di pemberian perintah.

---

## Task

### Mengerjakan beberapa permasalahan dan soal javascript.

Untuk task ini saya diharuskan untuk menyelesaikan permasalahan yang ada di document task, dan menjawab pertanyaan mengenai permasalahan tersebut.

Hasil file untuk task ini dapat diakses di [Repository Github](https://www.github.com/mbaharip/Assignment-Javascript).
