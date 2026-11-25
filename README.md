# Kedai Kopi Senja

# TUGAS MINGGU 2
# 6a. Apa yang muncul di address bar setelah form dikirim, dan mengapa data form tampil di sana? Hubungkan dengan materi method HTTP di Minggu 1.

Ketika form dikirim, alamat pada address bar akan berubah menjadi seperti berikut:

`pesan.html?nama=Budi&wa=08123456789&menu=espresso&jumlah=2&cara=ambil&catatan=tanpa+gula`

Karena form menggunakan atribut method="get", informasi tersebut muncul pada URL. Metode GET akan mengirimkan data dalam bentuk query string melalui URL. Data yang ditampilkan setelah tanda tanya (?) dengan format name=value, dan tanda ampersand(&) memisahkan masing-masing data. 
Nama nilai pada setiap pasangan data dihitung dari atribut nama pada masing-masing elemen formulir. Ini terkait dengan perbedaan antara metode GET dan POST, yang dibahas minggu 1. Metode GET mengirimkan data melalui URL, sedangkan POST mengirimkan data melalui bagian body request, sehingga informasi tidak dapat dilihat lansgung pada address bar. Oleh karena itu, GET tidak disarankan untuk mengirimkan data yang sensitif atau rahasia. Pada saat itu, situs web tetap bersifat statis karena proses pengembangan server baru akan dimulai pada Minggu 6. 

# 6b. Pilih satu bagian halamanmu yang memakai element semantic. Mengapa kamu memilih element itu dan bukan <div>?

Di bagian atas setiap halaman, saya menggunakan "<nav>" untuk menu navigasi yang mengarah ke Beranda, Menu, dan Pesan. Ini disebabkan oleh fakta bahwa "<nav>" memberi tahu browser, pembaca layar, dan mesin pencari bahwa bagian ini berisi kumpulan link navigasi utama. Dengan menggunakan "<nav>," struktur halaman menjadi lebih jelas dan mudah diakses. Dengan menggunakan "<div>," elemen tidak memiliki makna, sehingga pembaca layar tidak dapat langsung menuju navigasi dan kode juga lebih sulit dibaca. 

# TUGAS MINGGU 3
# 8a. Sebutkan satu bagian yang kamu susun dengan Flexbox dan satu bagian dengan Grid. Mengapa pilihan itu cocok untuk kedua bagian tersebut?
Saya menggunakan Flexbox pada bagian header yang berisi nama kedai dan menu navigasi. Flexbox dipilih karena elemen-elemen tersebut disusun dalam satu baris, tetapi bisa berubah menjadi satu kolom saat dibuka melalui ponsel. Selain itu, Flexbox memudahkan saya mengatur posisi elemen, seperti nama kedai di sebelah kiri dan navigasi di sebelah kanan menggunakan justify-content: space-between.
Sedangkan Grid saya gunakan untuk menyusun card pada menu.html. Grid cocok digunakan karena card ditampilkan dalam beberapa baris dan kolom. Jumlah kolomnya juga bisa diatur dengan mudah menggunakan grid-template-columns, misalnya menjadi 1, 2, atau 3 kolom tanpa harus mengatur lebar card satu per satu.

# 8b. Ceritakan satu aturan CSS yang awalnya tidak berlaku. Apa yang kamu lihat di panel Styles, dan bagaimana kamu memperbaikinya?
Awalnya saya menggunakan selector a { color: ... } untuk mengubah warna link navigasi, tetapi warna link tidak berubah. Setelah saya cek melalui Developer Tools, ternyata ada aturan CSS lain yang memiliki specificity lebih tinggi sehingga aturan yang saya buat tidak diterapkan. Saya kemudian mengganti selector menjadi nav a agar lebih spesifik dan warna link bisa berubah sesuai yang diinginkan.