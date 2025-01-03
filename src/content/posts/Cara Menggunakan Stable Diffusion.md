---
title: Cara Menggunakan Stable Diffusion
published: 2022-01-03
updated: 2022-02-29
description: 'Panduan praktis tentang bagaimana menggunakan teknik Stable Diffusion, sebuah metode yang efektif dalam analisis data dan pemrosesan sinyal.'
image: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg5kwXVGgubPo1yCn6dtowF-wqqCJH9ZzTumeiGvWbEbcIRQQ7Wx7SvypcwEahtF0tt4_OQQcnvhmHGebBvsiW_gRjZi_jyji5CGnl1sQbAQ_Di6aSxhpsSM0MdSbI8eECCgvipjUvHUXAPFpCbxD4FbnNDfv7GDvY3z5aCtzO02YMP4Rm3BP_i9HVLi4Ss/s1600-rw/New%20Project%203%20%5BC5DEEE7%5D.png'
tags: []
category: 'Technology'
draft: false 
lang: 'id'
---

Hai Internet, kali ini gw sempatkan waktu buat kalian [cara menggunakan stable diffusion](http://eevelynxd.blogspot.com/2023/02/cara-menggunakan-stable-diffusion.html)

okoklah langsung aja kita mulai, namun sebelum kita mulai alangkah baiknya bisa persiapkan terlebih dahulu seperti:

- Koneksi internet
- Akun google
- laptop / pc spek rendah🥔 atau medium (di hp saya kuranh tawu bisa atau gak)
- Niat

Spesifikasi device gk harus spek gemink

Pertama-tama kita buka link Google colab untuk stable difussionnya.<br>
Linknya ada [di sini](https://colab.research.google.com/github/camenduru/stable-diffusion-webui-colab/blob/main/stable/stable_diffusion_1_5_webui_colab.ipynb)

alternative: [https://colab.research.google.com](https://colab.research.google.com/github/camenduru/stable-diffusion-webui-colab/blob/main/stable/stable_diffusion_1_5_webui_colab.ipynb)

# Apa itu Google colab?

Google Colab adalah sebuah platform pengembangan dan penelitian yang disediakan oleh Google. Ia memungkinkan pengguna untuk menulis, menjalankan, dan berbagi kode Python melalui browser web tanpa perlu melakukan instalasi atau pengaturan yang rumit.

Google colab ini punya limit cui, limitnya tergantung pemakaian dan akan di reset 1 hari kemudian.<br />
jika menggunakan google colab dan program yang dijalankan terlalu berat maka limit akan cepat habis dan akan memotong proses running programnya. Gitu cuiiii.

> [!TIP]
> **Sedikit tips dari saya:** <br>
> Kalian bisa gunakan 2 akun atau lebih, sebagai contoh misal akun A limit udh habis bisa ganti ke akun B yang limitnya masih fresh<br>
>Oiya cui jangan lupa untuk selalu mengecek halaman google colab, dikarenakan ada pop up captcha yang muncul untuk memastikan apakah kita bot atau bukan dan ini jangan sampai terlewawtkan, google colab akan memutus koneksi kita dari sana dan memotong program yang sedang kita jalankan dan memulai ulang.

Jika sudah masuk ke google colab nantinya kalian bakal di arahkan ke halaman baru seperti ini:
![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj_S_OUCpx-YmqNxNfA5yx0MrO91BFJXoU-koB_H24wI7co4JdOu6yMiWpozpRd3DDH0H9ayRv5vSNAD4tHQA2j5gcU3GPIbF7NdF0XnE7VIAljvq5drEb4tT7ycdVcGOCAZd6or3D6BD5TcvgS_eRIJqOjlL_2zocEglz8U_9zgtjnEd9bZy_3Fb0l_g/s1600-rw/g1.png)

Di sini hanya ada satu step aja jadi prosesny lumayan cepet kemungkinan hanya sekitaran 5-10 menit saja, dan jangan lupa untuk selalu buka tab ini karena kita nantinya dapat notifikasi apakah kita robot apa bukan jika itu terlewat nanti prosesnya akan mengulang kembali.

<div style="display: flex; justify-content:center; overflow-x: auto; white-space: nowrap;">
  <figure style="display: inline-block; text-align: center; margin-right: 10px;">
    <img alt="no image" class="c sz" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEin2xXz3ThsVuv_o2IJhl9-JzMk-opfbfa1n_GUf4H2MpvwFHVB-_YvHiVnm9XYMD7hnZ1xR4GVUAY9M9_ugxLHZGzsmlSgFnMIto4Ymj3RoKLfEBzzf7jf708-MwRtEpj1gBww5gDfirXw8cGkGpGOKQ54WhAN5lgPmdFV9Tqby2Z9YteBquOLiW7Upg/s1600-rw/g2.png" style="max-height: 200px;" />
    <figcaption>a. klik run.</figcaption>
  </figure>

  <figure style="display: inline-block; text-align: center; margin-right: 10px;">
    <img alt="no image" class="c sz" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjPQF8qeqSgxrYIg2mkEhv2Bz03UzP5NrLhPqxoQUL4fFcviyljOhuYwCHwGrhZ-fz3KRHTUxWAk7JB9KHgW-Qi_x-idgTtI3TzuoJgUQB8UT_Cutqi2CUEDW7eahdfOC-hGEkjPeG6Jcii3OL_A5qJIjMAOZCiJgqLHl4QHCpPEzzOQ6H3IaRN4lNptQ/s1600-rw/g3.png" style="max-height: 200px;" />
    <figcaption>b. Klik tetap jalankan.</figcaption>
  </figure>
</div>

dan tunggu beberapa saat sampai prosesnya sudah sampai tahap akhir, disitu kalian bisa lihat ada url untuk membuka Stable Diffusionnya kalian bisa klik url tersebut, maka programnya sudah siap digunakan.

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjfYn41FjD1NKahN1FAK3fVdZgMDjUD3T-XavPCThqHzKkGk4pKVICkv9ZzY1SLspXL4rRTiWf635kzzFo3FlqpgAhvd7YeUzt5CXxeo-0Cqsol34P7RYDwsJv66SrcrDw8R8TNm_ykT7TK5lq7Ql3hk8DS2GMQK9Gu_U0LABAuKs27BHFp69x_IMeYFg/s1600-rw/g4.png)

Setelah itu kalian klik link tersebut dan kalian akan di alihkan ke halaman Stable Diffusion:

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgfI-BD1U92quuEnJXDkw6Dr9dpOwW_rXc53sid8iTwCRP8uvj1NBilwG12Gd3XXeKva50HLrfRB0x43u3FD-09iwGle2CXGJvsD7Yww3bU7Rfbtx27EuIEEn3QRuZFBe6HGITT3F6_H4dMIXv5mmqbOxk_pN0peNZKcRYEOlp0nRiw3EKlJIvNuv5xGI0_/s1600-rw/stable_diffusion.png)

# Update 15/06/23

**Google collab anti disconnect** - Google colab kalian sering disconnect? Gw ada solusinya gw nemuin ini di channel [@Yoshia Kefasu](https://www.youtube.com/@yosiakefas) <br>
disini gk ada disconect sama sekali lancar total gak ada disconnect sama sekali.<br>
Sebelumnya kan sering disconnect yh, karena google udah membatasi beberapa sl,akhdl jadi sering diskonek

1. tinggal login aja ke akun google lalu masuk ke google collab [Stable Diffusion](https://colab.research.google.com/github/YKefasu/Vlad-SD-Google-Colab/blob/master/Vladmandic_SD_A1111.ipynb)<br>di situ ada peringatannya ada juga informasi penting yang harus kalian baca biar akun google kalian aman terhindar dari banned
2. lalu connect dulu pakai GPU <br>![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEglPP38qMZMaOygEoZHZfjYHs3Q_0leK8J72uPEMNYCDqyK7zOQabRhhb3R2jpmFLCpsK8KWIQgr8nEhDz8hLOif3Q3IxLicXIMtcu6xaipzCw24zLGI9MtdNReyW7ieBLTEW4P74MHWp2N72ssJboCqXNgnoFGEHCZReX1-3exRvsyxpI738jsRrMMX8o/s1600/VideoScreenshot--YouTube-GoogleColabStableDiffusionAntiDisconnect10Juli2023-0%E2%80%9926%E2%80%9D.png)
3. ikuti step yang ada di google colab
4. Enjoyy..

okh, sekian dulu pembahasan kali ini cukup singkat karena emag udah ada tutorialnya di youtube ngapain coba gw bikin ginian tapi gabut cuyy aseli awowkwk😅

<iframe width="100%" height="468" src="https://www.youtube.com/embed/xHApf9gX0PQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

dan itulah [cara menggunakan stable diffusion](http://eevelynxd.blogspot.com/2023/02/cara-menggunakan-stable-diffusion.html) di laptop / PC spek rendah, kalian juga bisa menggunakan program ini di terminal langsung dengan cara copas perintah yang ada di google colab tapi cara ini dibutuhkan spesifikasi laptop / PC gemink yang bisa menjalankan game Nier Automata dengan grafik full rata kanan.😁

sekian tutorial hari ini, cukup mudah bukan? gak ada yang gk bisa semua tergantung koneksi internet.

Selanjutnya kita akan membahas prompt untuk mengubah waifu menjadi nyata dengan stable diffusion.😱


<style>
     ::-webkit-scrollbar {
    width: 1px;
}
 
::-webkit-scrollbar-track { 
    background: transparent;    
}
 
::-webkit-scrollbar-thumb {
    background: transparent;
}
     
     
         .drK ::-webkit-scrollbar {
    width: 1px;
}
 
.drK ::-webkit-scrollbar-track { 
    background: transparent;    
}
 
.drK ::-webkit-scrollbar-thumb {
    background: transparent;
}
</style>