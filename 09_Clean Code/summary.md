# 09 Clean Code

## Resume

Pada materi ini saya mempelajari :

-   Apa itu Clean Code
-   Karakteristik Clean Code
-   Principle Clean Code

### Apa itu Clean Code

Clean code adalah istilah untuk code yang mudah dibaca, dipahami, dan diubah oleh programmer.  
Kenapa clean code?

-   Work Collaboration, semua orang harus bisa membaca apa yang kita kerjakan
-   Feature Development, membantu untuk mengerti fitur baru yang sedang dikerjakan
-   Faster Development, ketika code kita bersih maka kita akan lebih mudah mengerjakannya

### Karakteristik Clean Code

Karakteristik clean code adalah:

-   Mudah dipahami, mudah dibaca, mudah diubah
-   Mudah dieja dan dicari
-   Singkat namun mendeskripsikan konteks
-   Konsisten
-   Hindari penambahan konteks yang tidak perlu
-   Komentar berlebihan
-   Terlalu banyak argumen pada function

Saran formatting code:

-   Lebar baris code antara 80 - 120 karakter
-   1 class terdiri dari 300 - 500 baris
-   Baris code yang berhubungan saling berdekatan
-   Function dengan pemanggilnya berdekatan
-   Variable dengan pemanggilnya berdekatan
-   Memperhatikan indentasi
-   Menggunakan Prettier atau Formatter

### Principle Clean Code

#### KISS - Keep It So Simple

Menghindari membuat fungsi yang dibuat untuk melakukan lebih dari 1 hal.  
Tips untuk KISS:

-   Fungsi atau class harus kecil
-   Fungsi dibuat hanya untuk melakukan 1 tugas saja
-   Jangan menggunakan terlalu banyak argumen
-   Harus diperhatikan untuk mencapai kondisi yang seimbang, kecil, dan jumlahnya minimal

#### DRY - Don't Repeat Yourself

Menghindari duplikasi kode. Duplikasi kode terjadi karena sering copy paste kode yang sama.  
Untuk menghindari duplikasi kode, buatlah fungsi yang dapat digunakan secara berulang-ulang.

#### Refactoring

Refactoring adalah proses restrukturisasi kode yang dibuat, dengan cara mengubah struktur kode agar lebih baik.  
Prinsip KISS dan DRy dapat dicapai dengan cara refactor.

Teknik refactoring:

-   Membuat abstraksi
-   Memecah kode dengan fungsi / class
-   Perbaiki penamaan dan lokasi kode
-   Deteksi kode yang memiliki duplikasi

---

## Task

### Analysis dan Rewrite Code

Untuk task ini saya diharuskan untuk membenarkan 2 code yang diberikan.

1. Saya harus menganalysis code yang diberikan, dan menuliskan alasan tiap kekurangan.
2. Saya harus membenarkan code yang diberikan, mengikuti kebiasaan penulisan yang disarankan.

[Repository Github](https://www.github.com/mbaharip/Assignment-Clean-Code)
