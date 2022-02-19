# Resume

Version Control System merupakan sistem manajemen project yang mencatat setiap perubahan termasuk siapa yang mengubah dan apa yang diubah dengan tujuan untuk mentrack setiap perubahan yang kita lakukan atau tim lakukan. Kemudian seiring dengan berkembangnya internet, Version Control System menjadi terpusat pada satu server, apabila server mati maka para developer tidak dapat mengerjakan apa-apa dikarenakan tidak bisa mengakses file yang terdapat di server, basis centralized dimulai oleh CVS pada tahun 1986, Perforce pada tahun 1995, Subversion pada tahun 2000, kemudian Microsoft Team Foundation Server pada tahun 2005. Developer bisa mengerjakan di lokal yang kemudian bisa menggunakan command untuk melakukan perintah seperti push atau pull dari / ke server. Contoh Version Control System distributed antara lain Git, Mercurial, dan Bazaar yang dimulai pada tahun 2005.

Git merupakan salah satu version control system populer yang digunakan para developer untuk mengembangkan software secara bersama-sama. Git dibuat oleh Linus Torvalds pada tahun 2005, contoh penggunaan git yaitu misalkan terdapat remote computer atau server, dan ada 3 user yang terhubung pada server tersebut, dimana ketiga user tersebut dapat pull code dari server, apabila melakukan perubahan ketiga usertersebut dapat melakukan push code ke server, dan server akan mencatat perubahan yang dilakukan oleh salah satu user tersebut. Pada folder project kita akan terbagi 2 jenis files, yaitu files dan folder project kita dan konfigurasi git yang akan berisi seperti history dan sebagainya, biasanya konfigurasi ini akan bernama .git dan secara default akan di hidden oleh system. Di git kita dapat melakukan undo apabila latest code terdapat bug atau error, kita bisa kembali ke suatu point sebelumnya yang dinamakan commit.

Saat push data ke server, itu dinamakan commit yang berisi dari commit message dan files yang diubah. Untuk menambah file dari lokal ke github, kita bisa menjalankan perintah git add nama file atau titik yang akan memasukkan semua file yang dipilih ke dalam Staging Area, kemudian untuk commit ke dalam repository github kita dapat menjalankan perintah git commit -m . Perintah git commit akan menyiapkan semua files yang didalam staging area ke repository, dan untuk mensynchronization files ke dalam repository github kita akan gunakan perintah git push -u origin . Untuk commit message di usahakan untuk menulis message perubahan yang jelas, agar setiap orang yang melihat dapat mengerti apa yang diubah.

Untuk melihat perbedaan yang telah dibuat, bisa digunakan git diff. Branches akan memudahkan untuk mengontrol code yang akan di deploy. Pull request digunakan apabila kita ingin meminta lead dev untuk mengecek dan merge branch yang kita buat ke branch development utama. Pada menu selanjutnya kita bisa masukan base menjadi tujuan branch, dan compare merupakan branch yang kita ingin merge, tidak lupa isikan detail di write agar memudahkan lead dev untuk mengecek kode kita.

Salah satu cara yang terbaik adalah gunakan merge bercabang atau no fast forward agar lebih memudahkan cara membaca.
Beberapa workflow terbaik antara lain:

-   Jangan ganggu branch Master
    Branch master digunakan ketika product telah benar-benar siap untuk dideploy. Hanya gunakan pull request untuk branch master.
-   Hindari edit langsung pada branch development
    Walaupun terdapat bug kecil, lebih baik buat branch feature baru dan membuat pull request setelah selesai.
-   Terapkan fitur hanya ke development
    Push semua fitur baru ke development untuk di test dan dipastikan tidak ada bug.
-   Terpakan development ketika selesai
    Jika sudah dipastikan tidak ada bug, buat pull request dari development ke master.
