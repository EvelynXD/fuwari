---
title: Teknik Sniffing Menggunakan Xerosploit
published: 2022-07-05
description: 'Man in the Midle Attack atau yang disingkat MitM adalah salah satu jenis cyber attack yang menyusup kedalam jaringan dan menyadap komunikasi yang sedang berlangsung antara pengguna jaringan dan web server tujuan.'
image: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgsfH2OoJM7LgIanpIERZTuxfpbbZlwG_VaVCZR2T60Grz_8g-PLs4S2N5OKqq-nAccUPsZ-vLoWkW92wpvhyp4SlkC3DaEvFJsEyH6mKmQN2oejL9OQUKlF0zCgAWF0s_bYvMDBhgtpwtbXxZJcrow_1UH2_uVDPocuZaK-LOb3BpwF_HqsQVDf4pyTQ/s1600-rw/xerosploit%20%5B99497A7%5D.png'
tags: ['Wireless Attack']
category: 'Technology'
draft: false 
lang: 'id'
---


:::warning[DISCLAIMER]
Tujuan artikel yang saya buat hanya untuk media edukasi/pembelajaran/dokumentasi. Kami percaya keamanan Cyber harus menjadi subjek yang familiar dalam upaya mencegah tindak kejahatan didunia informasi digital dan komputer. Jika ada, entah siapapun yang melakukan tindakan perusakan atau cybercrime yang disebabkan dari pembelajaran tutorial yang saya buat, dengan tegas saya menyatakan tidak bertanggung jawab kepada yang bersangkutan.
:::

* * *

Hai Internet, kali ini gw mw ngasih tawu pada kalian, gimana sih caranya melakukan sebuah teknik yang dinamakan sebagai sniffing, secara singkat sniffing itu adalah cara kita mendengarkan lalu lintas ataupun istilahnya mengintip sebuah lalu lintas jaringan.

Jadi, si Attacker atau si penyerang itu dia sudah terkoneksi dengan satu jaringan WI-FI yang sama dengan si korban, jadi ini adalah yang disebut dengan teknik penyerangan MITM (Man in the Midle Attack)

Pengertian Man in the Midle Attack
==================================

Man in the Midle Attack atau yang disingkat MitM adalah salah satu jenis cyber attack yang menyusup kedalam jaringan dan menyadap komunikasi yang sedang berlangsung antara pengguna jaringan dan web server tujuan.

MitM juga dapat menyamar sebagai jaringan asli dan membuat korban seolah-olah berada di jaringan yang benar sehingga tanpa sadar telah menjadi korban. Biasanya, pelaku akan membuat jaringan wifi palsu yang mirip dengan WI-FI asli untuk mengetahui penggunanya.

Saya akan mencontohkan cara penggunaan tools xerosploit  
jadi tampilan xerosploit adalah seperti ini:

![tampilan utama xerosploit](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi8I-f_BfssG-cWOcr8ck2RvOp65CvJP2Ra4-MwXa65mQ2XCrbdU5p2q5BPNwfftHeqffi6ocMtTuNiYZJ9f4DkW0w294IqHfSQzSdQZexKccPciGpE3mADcI-4Tzxdb95K_9vwrnawiTM3TdKUyyCHwjNFxSi4dTRnqhh7OMt8s7dg_acrwDBnTMgKdA/s1600/Teknik%20Sniffing%20Menggunakan%20Tools%20Xerosploit%20MITM%20_%20Kali%20Linux%20_%20Tutorial%20%2312.jpeg)

ada IP Address, MAC Address, Gateway, Iface, Hostname. Dan ini semua dari WI-FI saya, seperti itu dari tampilan halaman utamanya.

jika kalian bingung kalian bisa ketikan perintah help untuk menampilkan menu yang disediakan oleh xerosploit  
Nah, biasanya itu yang dipake adalah scan, jadi kita scan network di wifi kita itu siapa aja yang lagi konek pada pukul sekian dan hari ini misalnya.

Tampilan setelah mengetikan perintah scan:

[![xerosploit - tampilan setelah perintah scan](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj3P4fvaXrGlXVi0kqFnYzZRcEaeti38UkviJVr1sVnNf9L3IINO46GnukM2V2l6Suon43eetTa6ZQP9Ue7k94ykLvtbwu7f-5yULUvIwo2MuZfpc49zqurUvzqA9cSGlnQqh9XkLxx2MnZF_1qhjXlTVqMLBP3593rR6bthzlQd9juFuuqFGh76KUAWQ/s1600/Teknik%20Sniffing%20Menggunakan%20Tools%20Xerosploit%20MITM%20_%20Kali%20Linux%20_%20Tutorial%20%2312%20%281%29.jpeg)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj3P4fvaXrGlXVi0kqFnYzZRcEaeti38UkviJVr1sVnNf9L3IINO46GnukM2V2l6Suon43eetTa6ZQP9Ue7k94ykLvtbwu7f-5yULUvIwo2MuZfpc49zqurUvzqA9cSGlnQqh9XkLxx2MnZF_1qhjXlTVqMLBP3593rR6bthzlQd9juFuuqFGh76KUAWQ/s1600/Teknik%20Sniffing%20Menggunakan%20Tools%20Xerosploit%20MITM%20_%20Kali%20Linux%20_%20Tutorial%20%2312%20%281%29.jpeg)

jadi gini, kita cari dulu device korban yang mw di targetkan. Jadi, kita akan mengambil sebuah login username dan password si korban, kita harus tau dulu IP Addresnya korban, nah setelah itu kita dengarkan dengan command sniffing, dan si korban jika masuk ke sebuah website login yang protokolnya itu masih HTTP bukan HTTPS, kalo di HTTPS secara otomatis bakal terenkripsi, namun jika HTTP itu tidak ada protokol keamanannya jadi dia bisa terekam dengan jelas apa yang si korban masukan username dan passwordnya.

jika sudah menemukan IP Address si korban yang selanjutnya akan dilakukan adalah mengetikan ulang IP Address korban di terminal setelah itu kalian boleh ketikan **'help'** lagi maka akan seperti:.

[![xerosploit](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhPoNzvQDW4dyCZL1Wg87kfKrHKt-4JLT44XYK0z1HkQcPhQmPbUiavnmwC3Llu7YrYeRe3vuKTwam92UJlKGWoACVIlnpPFjTQfH9k1dij-eXIpw5Urs2Q7Gr4DhXmZ-BPkWqTM1Ggwg6xBEwZ9UbMd7_bpvqhMcsG6zoRFkEQdohstpX1wC-4W4gBXg/s1600/Teknik%20Sniffing%20Menggunakan%20Tools%20Xerosploit%20MITM%20_%20Kali%20Linux%20_%20Tutorial%20%2312%20%282%29.jpeg)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhPoNzvQDW4dyCZL1Wg87kfKrHKt-4JLT44XYK0z1HkQcPhQmPbUiavnmwC3Llu7YrYeRe3vuKTwam92UJlKGWoACVIlnpPFjTQfH9k1dij-eXIpw5Urs2Q7Gr4DhXmZ-BPkWqTM1Ggwg6xBEwZ9UbMd7_bpvqhMcsG6zoRFkEQdohstpX1wC-4W4gBXg/s1600/Teknik%20Sniffing%20Menggunakan%20Tools%20Xerosploit%20MITM%20_%20Kali%20Linux%20_%20Tutorial%20%2312%20%282%29.jpeg)

Nah, disini banyak sekali pilihan yang bisa dilakukan dan ini adalah perintah-perintah serunya dari tools xerosploit, disitu ada perintah yang paling terkenal yaiu dos attack yaitu kita bisa membanjiri lalu lintas internet si korban sehingga menjadi down / diskonek karena dia dibanjiri terlalu banyak data, istilahnya kepenuhan lah, dan juga ada sniff, sniff ini untuk merekam apa saja yang dibuka pada browser si korban, dan juga ada shaking web browser yang bisa bikin browser yang di tuju itu getar-getar, tentunya dia harus masuk ke website yang masih HTTP bukan HTTPS, okh langsung saja kita ketk **'sniff'** untuk mencium jejak lalu lintas korban selanjutnya ketik **'run'** dan **'y'** maka akan seperti:

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj75k_7pR0G4tenWB-S7mGFNiTaS912fNLzc-8MeWDhJwhVdJR_y7iV49U0sju27jqrzuDFx1h6h_GV2cSmT3Jn0FFqq6a8BAD1unZiLv-cnNw31fU3KcdwxufH44dLwgxdiev5motNBlozoANL16TShc7xti-FGU1SkEEpRU9I9dFUcEuH583YMrZE0A/s1600/Teknik_Sniffing_Menggunakan_Tools_Xerosploit_MITM__Kali_Linu.gif)

jika sudah kita akhiri dengan **'ctrl + c'** dan save lognya, cari folder xerosploit masuk ke xerosniff cari fil lognya dan klik dua kali kemudian secara otomatis bakal masuk ke dalam wiresharknya, setelah itu kalian ketik saja **'http'** lalu enter maka tampilannya seperti ini:

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEitxq-8HIt_21gA4253w0C81j1fCYfdPSyuC4Wd2o9mhNHJlhpchEGbaEL5lceqS4-1tP_gwtE7djFtBLXvR8ZFuiadVrH4ki4kiza3ubpfO4LhFJPCRGQbF_EtHJ3Ar5ZcO_nhFA6Nq92Cddz2_ZWnTDkv7y1TJMrAFFX5OyApYPXFSX1Sa9DgvKHJNQ/s1600/Teknik%20Sniffing%20Menggunakan%20Tools%20Xerosploit%20MITM%20_%20Kali%20Linux%20_%20Tutorial%20%2312%20%283%29.jpeg)

kemudian kalian cari yang **'POST'** klik dia kali pada bagian yang sudah dipilih dan akan muncul tab baru seperti ini:

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhLlJcosKfxdrrAICFPVZEKSpiiLnR49AfFc37sD8uG36Y3NsLhd4G8i8AcaSkaEYuF80JCIV2myf7TrO_9CSkQ99PVmgFR7DIe7ewXIo_nwJTaTKcCnDyIcPGvLUKIUnGTTpoNEUOy7vaILXaJcUBjYs0QzvJd9knusB0Z82uRmq1v2NlD4plbZveOuA/s1600/Teknik%20Sniffing%20Menggunakan%20Tools%20Xerosploit%20MITM%20_%20Kali%20Linux%20_%20Tutorial%20%2312%20%284%29.jpeg)

Nah, udh ketahuan password dan usernamenya, ya pastilah bakal ketauan jika situs tersebut itu tidak menggunakan protokol keamanan atau HTTP terlihat pada link sebelah kiri ikon gemboknya di coreng yang artinya website tersebut belum menggunakan protokol keamanan, memang tidak aman (connection is not secure)

Kesimpulan
==========

Sebelum melakukan login atau mengakses sebuah website, penting untuk memeriksa apakah gemboknya tidak disilang oleh Google dan pastikan bahwa situs yang ingin dikunjungi menggunakan protokol HTTPS yang aman.

Perlu dicatat bahwa penilaian terhadap keamanan suatu situs tidak hanya bergantung pada fakta bahwa gemboknya tidak disilang oleh Google dan menggunakan protokol HTTPS. Masih ada faktor-faktor lain yang perlu diperhatikan, seperti kebijakan privasi, reputasi situs, dan langkah-langkah keamanan tambahan.

jadi seperti inilah mengambil data login dari teknik sniffing melalui jaringan yang sama yang dinamakan dengan Man in the Midle Attack atau orang dalam di dalam sebuah jaringan yang terhubung sama.

oke baik, sekian pembahasan hari ini cukup menghengkerkan 😱 dan semoga bermanfaat untuk kalian semuannya, kurang lebihnya mohon maaf