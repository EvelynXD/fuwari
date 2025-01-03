---
title: Menemukan Informasi Rahasia Dengan Google Dork
published: 2021-01-02
description: 'Google Dork merupakan suatu teknik yang memanfaatkan mesin pencarian Google untuk mendapatkan berbagai informasi penting atau sensitif yang tidak tersedia secara umum di dalam web.'
image: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjr0Xzem-i_AwS_PD_Uiwmw0RlfytQ03JPAqjr1DHXn26Zf_2x8TSyMONabNTUonW3-7HU2zlgTfj3-4hPnU44Qox3oRNN6AJ2TL_da-NLrv-rS4X78fjY3AiXs6js36zPynP8uRGCoizcwfQYHyS8DEjaPzDyZ1TftICNEw5LJ9O-6KirUm4N5wtqlsi0/s1600-rw/dork.jpg'
tags: [Osint]
category: 'Technology'
draft: false 
lang: 'id'
---

Hai Internet, kali ini saya akan membahas google dork.<br />
Sebelum kita mempraktekannya mari kita mengenal dulu apa itu google dork.

# Apa itu google dork
Google dork adalah salah satu fitur dari google yang digunakan google search, kita bisa search kek misalnya id atau kerentanan pada sql injection, database,Beberapa dari Anda mungkin tidak asing dengan arti Google Dork. Dengan kata lain, dork sendiri adalah tindakan memasukkan kata kunci ke mesin pencari Google. Tujuannya adalah untuk menemukan celah keamanan pada website yang akan diretas. Teknik ini dikenal sebagai dorking. Sederhananya, Google Dork adalah metode menggunakan mesin pencari Google untuk mendapatkan informasi sensitif yang tidak ada di Internet.<br>
Untuk lebih jelasnya bisa baca [Mengenal Apa itu Google Dork](https://idmetafora.com/news/read/2015/Mengenal-Apa-itu-Google-Dork-Pengertian-Fungsi-dan-Cara-Menggunakannya.html)

Dengan google dork kita bisa nulis di pencarian google seperti: "inurl:..", "intitle:.." dengan diikutin nama yang ingin kita cari.<br />
Google dork ini tergolong dalam salah satu teknik osint, yang dimana kita bisa mencari informasi rahasia berdasarkan apa yang ingin kita cari melalui pencarian google.

## Perbedaan intile dengan inurl

1. **intitle**<br>Fungsi: untuk mempermudah Google membatasi hasil searching pada halaman yang terdapat pada judul atau title. Dengan memanfaatkan title sebua situs, Anda bisa menggali berbagai macam informasi. Misalnya, Anda bisa mengetahui ciri-ciri sebua sistem server. Kita akan membahas hal ini pada bab tersendiri nantinya.<br /><br />
Contoh:”intitle:username password” (tanpa tanda kutip)<br /><br />
Maka hasil setelah anda browsing di internet akan muncul di bagian judul akan muncul Username dan pada isi halaman ada kata Password<br /><br />
Untuk pencarian yang lebih lengkap atau jika dalam pencarian terdapat dua query utama, sintaks yang kita gunakan adala: <b>allintitle</b><br /><br />
Contoh:”allintitle:password mdb” (tanpa tanda kutip). Metode ini membatasi hasil pencarian hanya pada dua judul utama di atas, yaitu: password dan mdb. Perlu diketahui bahwa sintaks allintitle: tidak dapat digabung dengan sintaks lainnya.<br /><br />
Selain  sintaks dua tadi intitle dan allintitle anda juga bisa mencoba sintaks ini…<br />
<b>intitle: “Welcome to IIS 4.0”
<br />intitle: “ColdFusion Administrator Login”</b>

2. <b>inurl</b><br />
Fungsi: untuk membatasi hasil pencarian hanya pada URL yang mengandung kata kunci yang dicari.<br /><br />
Contoh: “inurl:admin.mdb” (tanpa tanda kutip)<br /><br />
Dari contoh tersebut maka hasil pencarian hanya menampilkan URL yang memiliki informasi tentang admin.mdb. Contoh, isi lainnya yang cukup bermanfaat seperti: customer.mdb, dan users.mdb.<br /><br />  
Hal yang sama juga berlaku pada sintaks inurl: ini, yaitu meodifikasinya menjadi <b>allinurl</b>: Tujuannya adalah untuk menghasilkan URL yang hanya terdapat pada query pencarian utama. Perbedaan antara <b>allinurl</b>: dengan <b>inurl</b>: adalah, allinurl: tidak dapat digabung dengan sintaks lainnya. Sebaliknya inurl: dapat digabungkan dengan sintaks lain.<br /><br />
Sebagaia contohnya coba anda ketikan sintaks <b>inurl:admin pass</b>. Pada browser dan coba di cermati perbedaannya maka hasilnya adalah kata admin berada pada URL, sedangkan kata pass terdapat pada halaman isi.<br /><br />
Sekarang masukanlah sintaks <b>allinurl:admin pass</b>. Hasilnya dimana kata <b>admin</b> dan <b>pass</b> sama-sama berada pada URL. Sekarang tahukan bedanya. 

Untuk lebih lengkapnya kalian bisa baca: [Perintah Google Dork](https://belajarhackingtanpasoftware.wordpress.com/2013/04/05/dasar-dasar-google-hacking/)

disini kita coba cari halaman login admin:
![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiaOwdwY1_U3-GIaBEzlumD2nOn5JhZ16_fTZNPWpd8aPniBBQSUsZESxZZv04p1Hdbp_GCfW9WzgUsjSIONMN706JFHCgdfy5SNi_V3RvazHjPjxk0jqVnODOngvdAVEF8t9Y8k7Pwc30V9h-xYCTcLr36bLW7zA7UFyz5koPm9wQf82w2JciGBbZRrlw/s1600-rw/google-dork-01.png)
itu contoh dari **inurl"**

sekarang kita coba intile:
![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjaLB9zJdtHT-_6p5jYiCzwNW4cop0KNmTjjwZ5T15hvTHbIwGEjMh0LsdkzRBJ8BbUP90Ldc4tFKX5Amsk7Vsq7f71NI_8KqqYHUfOSAUVM1RudIT1GIqmNhUWZRX9mBMbyTaquiLjXR16Qvz87vH0TXy5aJgG3W0mi--1jYlKYR1AHyBBBkc9V8mtFvE/s1600-rw/google-dork-02.png)

Semua akan muncul yang ada nama barusan kita input mulai dari yang diindex google sampai yang belum terindex google semuanya akan tampil

Sekarang kita coba **db_password filetype.env**

ini nantinya tuh keliatan orang yang menyimpan passwordnya di websitenya, disini gw menggunakan <b>filetype.env</b> kalia bisa ubah filetypenya misal .txt atau yang lainlah.

sekarang kita langsung aja liat kerentanan dari sql injection

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjt8yKPywuliyN4B96NUnug0ed48rVCcQgB_xBrPq3doqlJ54BPeiVu8r_a2SQg75xC2QmEFR7JQQgdd5K45BC71mTwMIuFsvVzvkRbQywpUgwYRRLXo9vu4c0hZkoax0wZ5GEXtn8M87q_AH0zbTq8JFF1raSA-ikFNUKcCEjb2kVT6ghCTLSmky1REv8/s1600-rw/google-dork-03.png)

kalian juga bisa eksplore sendiri  linknya udah gw siapin disini: [https://gist.github.com/zhnlk/f01775e3bda2a0a1b5ac15f5a4feccc5/](https://gist.github.com/zhnlk/f01775e3bda2a0a1b5ac15f5a4feccc5/)

nanti kalian eksplore sendiri menggunakan google dork

Dork yang kuat untuk mengakses informasi sensitif yang tidak tersedia publik. Menguraikan konsep Google Dork, perbedaan intitle dan inurl, serta memberikan contoh penggunaannya, artikel ini mengajarkan cara efektif untuk mencari dan mendapatkan akses informasi yang seharusnya tersembunyi. Dengan menggali potensi kerentanan keamanan dalam halaman web, pembaca diberikan wawasan yang kuat tentang bagaimana memanfaatkan mesin pencari untuk mendapatkan wawasan yang lebih mendalam.

Penggunaan Google Dork, meskipun memiliki manfaat dalam hal pencarian informasi yang lebih spesifik, juga memiliki dampak negatif potensial<br>
Penting untuk diingat bahwa penggunaan Google Dork harus dilakukan dengan etika dan kehati-hatian, serta mematuhi hukum dan peraturan yang berlaku.