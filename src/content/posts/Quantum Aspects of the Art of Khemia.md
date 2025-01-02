---
title: Quantum Aspects of the Art of Khemia
published: 2022-06-02
description: 'Khaenri’ah was an underground realm, and its natural fauna were few indeed.'
image: 'https://gameranx.com/wp-content/uploads/2022/10/Genshin-Impact.jpg'
tags: ['Game']
category: 'Genshin Theory'
draft: false 
lang: 'id'
---

# Quantum Aspects of the Art of Khemia


## Bab 1.<br />Damage
<div style="text-align: center">Khaenri’ah was an underground realm, and its natural fauna were few indeed.
    As such, its alchemy focused more heavily on the creation of life. This art
    of creation was known as “The Art of Khemia“.

$\overline{\text{(Albedo)}}$    
</div>

Pada bab ini perhitungan damage untuk objek ∈ {Enemy, Character}<span style="font-size: xx-small;"><b><sup>1</sup></b></span>&nbsp; dijelaskan, mulai dengan damage dasar, beralih ke total damage, reaksi
  elemen dan beberapa tambahan informasi mengenai perhitungan damage tingkat
  lanjut dan lainnya disediakan.

### 1.1. Base Damage

<i>DMG</i><sub><i>Base</i></sub>&nbsp;damage dasar didefinisikan sebagai damage non-critical yang diberikan
  pada objek tanpa pertimbangan pertahanan objek, resistensi, segala bentuk
  pengurangan damage atau elemen reaksi.

Rumus damage dasar diberikan oleh
<b>
<div id="rumusatas">

$DMG_{\text{Base}} sf = sf \cdot \left( \underline{\text{ATK} \cdot \text{Mu l t}_{\text{Talent}}} \right)_{\text{DMG}_{\text{Skill}}} sf \cdot \left( 1 + DMG_{\text{Increase}} \right) sf + \sum_{k} DMG_{\text{Flat, k}} \cdot \left( 1 + DMG_{\text{Bonus}} \right)$
</b>
</div>

dimana definisi serangan&nbsp;<i>ATK</i>, talent multiplier&nbsp;<i>Mult</i><sub>Talent</sub>, peningkatan damage&nbsp;<i>DMG</i><sub>Increase</sub>,
  damage datar&nbsp;<i>DMG</i><sub>Flat&nbsp;</sub>dan bonus damage&nbsp;<i>DMG</i><sub>Bonus&nbsp;</sub>dapat ditemukan di bagian berikut. Meskipun beberapa
  karakter memiliki keterampilan yang berskala atribut selain serangan (misalnya
  pertahanan&nbsp;<i>DEF</i>, kesehatan&nbsp;<i>HP</i>), ini tidak mengubah
  garis besar umum rumus damage.

### 1.1.1. Attack

Dengan serangan dasar

<div style="text-align:center"><b><i><span style="font-size: medium;">ATK<sub>Base</sub> = ATK<sub>Character</sub> + ATK<sub>Weapon</sub></span></i></b></div>

dari sebuah karakter yang diberikan oleh jumlah dari nilai bawaan yang
  bergantung pada level karakter <i>ATK<sub>Character</sub> </i>dan stat utama
  senjata <i>ATK<sub>Weapon</sub> </i>nilai serangan total <i>ATK</i> dari
  sebuah karakter dapat dihitung dengan

<div style="text-align:center"><b>ATK = ATK<sub>Base</sub> * (1 + ATK%) + ATK<sub>Flat</sub> ⋅</b></div>

<i>ATK<sub>%</sub></i> adalah jumlah dari semua persentasi bonus serangan
yamg berkaitan dengan karakter dan <i>ATK<sub>Flat</sub></i> adalah jumlah
dari semua bonus serangan datar yang diterapkan pada karakter. Untuk musuh,
nilai total serangan dan nilai serangan (dan pertahanan) hanya bergantung
pada level dan tidak relavan untuk dibahas lebih lanjut dalam tesis ini.

### 1.1.2. Talent

Di bagian talent setiap karakter, pengganda talent
<i>Mult<sub>Talent</sub></i>, yang hanya bergantung pada tingkat talent yang sesuai, dapat ditemukan.
Meskipun dalam beberapa kasus pengganda ini dapat meningkat tergantung pada
jumlah tumpukan (ini hanya contoh)

<div style="text-align:center">

$ \text{Mult}_{\text{Talent}} = \text{Mult}_{\text{Talent.Base}} + \sum_{i=1}^n \text{Mult}_{\text{Stack,i}} + n \cdot \text{Mult}_{\text{stack}} $ </div>

dengan <i>n</i> adalah jumlah tumpukan yang diperoleh, dimana ketika
<i>Mult<sub>Stack,i</sub></i> adalah sebuah konstanta
<i>Mult<sub>Stack</sub></i>, maka hal ini menyederhanakan persamaan dan
<i>Mult<sub>Talent,Base</sub></i> adalah nilai dasar.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Contoh untuk stack adalah
<b>Lightfall Sword</b> (ledakan) Eula yang mendapatkan stack energi untuk
ledakan di akhir atau <b>Seni Rahasia Raiden: Musou Shinetsu</b>(burst)
mendapakan tumpukan tekad untuk meningkatkan serangan awal burst dan
    serangan normal selama burst.

<br>
<br>

$\overline{\phantom{xxxxxxxxxxxxxxxxxxxxxxx}}$<br>
<sup>1</sup>Dapat diperluas ke (beberapa) perisai, lihat bab [2](#ini-adalah-heading-3)


### 1.1.3. Damage Increase

Jenis damage <i>DMG<sub>Increase</sub></i> ini sangat jarang terjadi dan
  deskripsi dalam game menyebutkan sebagai peningkat skill<sup>2</sup> karakter
  tertentu, juga tidak berdasarkan atribut karakter, dan contohnya adalah:
<div>
  <ol style="text-align: left;">
    <li>
      <b>Tarian Api Niwabo Yoimiya:</b> "Selama waktu ini, panah yang ditembakan
      oleh Serangan Normal&nbsp; Yoimiya&nbsp; akan menjadi Blazing Arows, dan
      DMG mereka akan ditingkatkan dan di ubah menjadi pyro DMG." Pengganda 1 +
      <i>DMG<sub>Increase</sub></i> adalah Blazibg Arrows DMG yang disebutkan
      dalam talent tergantung pada level talent.
    </li>
    <br />
    <li>
      <b>Konstelasi ke-4 Xingqiu, Evilsoother:</b> "Sepanjang durasi Pedang
      Guhua: Raincutter, DMG yang diberikan oleh Guhua Sword: Fatal Rainscreen
      meningkat sebesar 50%." Oleh karena itu, 1 +
      <i>DMG<sub>Increase</sub></i> menghasilkan 1,5.
    </li>
  </ol>
  <br />
  <ol style="text-align: left;"></ol>
</div>

### 1.1.4. Flat Damage

Flat damage<sup>3</sup> Peningkatan <i>DMG<sub>Flat</sub></i> didasarkan pada
persentase tetap dari atribut karakter (misalnya <i>x%ATK, x%HP,</i>..),
biasanya dengan statistik normal dengan urutan besarnya O(102 hingga $ \infty $) dan
ditambahkan secara aditif ke damage skill. Misalnya, pasif level kenaikan ke-4
Zhongli memberinya, misalnya untuk serangan normal, peningkatan damage sebesar
1,39% dari HP maksimalnya. Rumus(<a href="#rumusatas">1.1</a>) akan berubah
menjadi

$DMG_(Base)=(ATK*Mu l t_(Ta l entsf" 1")+HP*Mu l t_(4thsf"
          Ascension"))*(1+DMG_(Bon us)).$

Contoh lainnya adalah Cinnabar Spindle, yang dilengkapi dengan Xingqiu (C4
  memberikan damage meningkatkan ke E-skill) itu akan meningkatkan skill damage
  elemennya sebagai berikut:

$ 
\begin{aligned}
\text{DMG}_{\text{Base}} = & \left( \text{ATK} \cdot \text{Mult}_{\text{Talent 2}} \cdot (1 + \text{DMG}_{\text{Increase, C4}}) + \text{DEF} \cdot \text{Mult}_{\text{Weapon, passive}} \right) \\
& \cdot (1 + \text{DMG}_{\text{Base}}) \cdot
\end{aligned}
$


### 1.1.5. Damage Bonus

Variabel <i>DMF<sub>Bonus</sub></i>&nbsp;dalam persamaan (<a href="#rumusatas">1.1</a>) adalah jumlah dari semua
  bonus damage. Ini selalu disebutkan dalam game dengan kata kunci "DMG" dan
  tidak dianggap sebagai peningkatan damage (lihat bagian [1.1.3](###-1.1.3.-Damage-Increase) ), peningkatan
  damage berdasarkan statistik&nbsp; karakter (lihat bagian [1.1.4](###-1.1.4.-Flat-Damage)).

<p style="text-indent: 30px;">Contohnya elemen-, physical-, elemental-burst-, skill-, <i>i</i>-hit- atau&nbsp;
  normal attack-, charged attack-, plunge-, semua DMG, <i>x%EM</i> dengan urutan
  besarnya <i>O</i>(1) dalam kisaran stat normal, senjata pasif dengan
    peningkatan DMG terhadap musuh yang terkena efek electro, hydro, pyro,..</p>

### 1.1.6. Critical Hit

Crit-rate$^{4}$ *CR* in $[0, 1]$ dari karakter adalah probabilitas terjadinya critical attack. Sebuah critical attack. Critical akan meningkat dengan nilai crit-damage *CD* in $[0, \infty[$ dari karakter tersebut menghasilkan
<div style="text-align:center">

$ \text{DMG}_{\text{Base, Crit}} = \text{DMG}_{\text{Base}} \times (1 + \text{CD}) $
</div>
<br>

$\overline{\phantom{xxxxxxxxxxxxxxxxxxxxxxx}}$<br>
<sup>2</sup>Karena peningkatan damage terkait dengan skill (secara eksplisit menyebutkan "nama" serang dalam deskripsi), talent tertentu, itu hanya mempengaruhi pengganda talent ini dan bukan bonus flat damage lainnya dari kenaikan level (misalnya Zhongli), Cinnabar Spindle, dll., (lihat bagian [1.1.4](###-1.1.4.-Flat-Damage)).<br>
<sup>3</sup>Bonus flat damage memiliki "bentuk" yang sama dengan damage skill dan secara teoritis juga dapat mengandung peningkatan damage.<br>
<sup>4</sup>Layar stat dalam game dapat menunjukkan nilai negatif atau lebih tinggi dari 100% untuk crit-rate dan variable <i>CR<sub>%</sub></i> yang lebih didefinisikan di sini masing-masing adalah 0% atau 100%

Rata-rata damage<sup>5</sup> kemudian diberikan oleh

<div style="text-align:center">

$ 
\begin{aligned}
\text{DMG}_{\text{Base}} &= \text{DMG}_{\text{Base}} \cdot (1 - \text{CR}) + \text{DMG}_{\text{Bonus}} \cdot \text{CR} \cdot (1 + \text{CD}) \\
&= \text{DMG}_{\text{Base}} \cdot (1 + \text{CR} \cdot \text{CD})
\end{aligned}
$
</div>

dengan crit-ratio$^{6}$ yang sempurna (setelah semua buff diterapkan dari setiap sumber)
<br>$CR:CD = 1:2$ untuk $CD\% \leq 200\%$

## 1.2. Total Damage

Total damage yang diterima karakter atau musuh tanpa mempertimbangkan reaksi elemen dapat diekspresikan dengan

<div style="text-align:center">

$ \text{DMG}_{\text{Total}} = \text{DMG}_{\text{Base}} \cdot \text{Mult}_{\text{DEF}} \cdot \text{Mult}_{\text{RES}} \cdot \text{Mult}_{\text{DMG\_Reduction}} $
</div>

di mana pengganda untuk defense, resistensi, dan pengurangan kerusakan dijlaskan dalam bagian berikut.

### 1.2.1. Defense

Analog dengan bagian [1.1.1](#-1.1.1-attack), pertahanan dasar $\text{DEF}_{\text{Base}}$ dan nilai pertahanan total $\text{DEF}$ dari sebuah karakter ditentukan oleh

<div style="text-align:center">

$ \text{DEF}_{\text{Base}} = \text{DEF}_{\text{Character}} $<br>
$ \text{DEF} = \text{DEF}_{\text{Base}} \cdot (1 + \text{DEF}\%) + \text{DEF}_{\text{Flat}} $
</div>

Disimpulkan bahwa pengganda pertahanan $\text{Mult}_{\text{DMG,DEF}}$ tergantung pada pertahanan pemain bertahan dan level penyerang. Oleh karena itu, untuk pertahanan musuh, tanpa pengurangan pertahanan, model polinomial dengan hanya level telah digunakan untuk analisis regresi dan menghasilkan

<div style="text-align:center">

$ \text{DEF}_{\text{Enemy}} = 5 \cdot \text{Level}_{\text{Enemy}} + 500 $
</div>

dan berdasarkan pertimbangan D-simetri ([3.1](#3.1)) pertahanan intrinsik $\tilde{\text{DEF}}_{\text{Object}}$ untuk setiap objek telah didefinikan

<div style="text-align:center">

$ \tilde{\text{DEF}}_{\text{Object}} = (1 - \text{DEF}_{\text{Reduction}}) \cdot (5 \cdot \text{Level}_{\text{Object}} + 500) $
</div>

di mana $ \text{DEF}_{\text{Reduction}} $ mempertimbangkan pengurangan pertahanan yang diterapkan pada objek $ \in \{ \text{Musuh}, \text{Karakter} \} $ yang sedang diserang (defender).

<p style="text-indent: 30px">Dengan menggunakan model fungsi rasional, pengurangan damage yang bergantung pada pertahanan pemain bertahan dan tingkat penyerang (yang dinyatakan melalui pertahanan intrinstik) telah disimpulkan menjadi</p>

<div style="text-align:center">

$ \text{DMG}_{\text{Reduction,DEF}} = \frac{\text{DEF}_{\text{Defender}}}{\text{DEF}_{\text{Defender}} + \tilde{\text{DEF}}_{\text{Attacker}}} $ </div>

$\overline{\phantom{xxxxxxxxxxxxxxxxxxxxxxx}}$<br>
<sup>5</sup> Damage rata-rata juga dapat dipengaruhi oleh buff kecepatan serangan, meskipun ini akan dihilangkan di sini, dan daripada integrasi waktu ke waktu diperlukan.  
<sup>6</sup> Untuk mencari nilai maksimum (extrema) dari damage rata-rata, rasio $f = CR \cdot CD$ dikenakan batasan $g = (2 - CR + CD) - CV = 0$ (dengan $CR \in [0, 1]$), dengan $CV$ adalah nilai critical, fungsi Lagrange $L = f - \lambda \cdot g$, dengan $\lambda$ adalah pengali Lagrange, harus dioptimalkan. Jadi, $\nabla L = \nabla f - \lambda \cdot \nabla g$ $ (CD, CR)^T - (2\lambda, \lambda)^T = 0 $, gaya $ CD = 2\lambda $ dan $ CR = \lambda $ untuk rasio optimal selama $CD \leq 2$.

Dengan ini pengganda pertahanan
<div style="text-align:center">

$ \text{Mult}_{\text{DEF}} = 1 - \text{DMG}_{\text{Reduction,DEF}} $</div>

dalam kasus karakter menyerang musuh, dapat disederhanakan menjadi

<div style="text-align:center">

$ \text{Mult}_{\text{DEF}} = \frac{\text{Level}_{\text{Character}} + 100}{\left( (1 - \text{DEF}_{\text{Ignore}}) \cdot (1 - \text{DEF}_{\text{Reduction}}) \cdot (\text{Level}_{\text{Enemy}} + 100) \right) + (\text{Level}_{\text{Character}} + 100)} $</div>

Dimana transformasi terakhir dari persamaan tersebut hanya berlaku ketika karakter menyerang musuh dan ini menunjukan bahwa pengali pertahanan hanya bergantung pada level karakter dan musuh.  
Selanjutnya, variabel $ \text{DEF}_{\text{Ignore}} $ ditambahkan, untuk mengenai serangan atau efek yang mengabaikan beberapa dari pertahanan musuh.  
<sup>7</sup>

<div style="display: flex; gap: 20px; justify-content: center; flex-wrap: wrap;">
  <div style="text-align: center; flex: 1; max-width: 100%; display: inline-block; margin: 10px;">
    <img alt="genshin impact" class="lazy" src="https://raw.githubusercontent.com/AlenaMiaw/Blogger-Post/b71448a1b78b4d8f0abe18b396d907c61a453238/svg/1%20Tidak%20ada%20pengurangan%20pertahanan.svg" style="max-width: 100%; height: auto;"/>
    <sup><b>a.</b> Tidak ada pengurangan pertahanan.</sup>
  </div>

  <div style="text-align: center; flex: 1; max-width: 100%; display: inline-block; margin: 10px;">
    <img alt="genshin impact" class="lazy" src="https://raw.githubusercontent.com/AlenaMiaw/Blogger-Post/b71448a1b78b4d8f0abe18b396d907c61a453238/svg/2%20Level%20karakter%2090.svg" style="max-width: 100%; height: auto;"/>
    <sup><b>b.</b> Level karakter 90.</sup>
  </div>
</div>

<b>Gambar 1.1.:</b> Pengganda pertahanan untuk level musuh yang berbeda sebagai fungsi dari level karakter dan pengurangan pertahanan.

<b><span style="color: #3d85c6;">Contoh 1.1</span> (Pengurangan Defense dengan Lisa):</b>

<div style="display: flex; gap: 20px; justify-content: center; flex-wrap: wrap;">
  <div style="text-align: center; flex: 1; max-width: 100%; display: inline-block; margin: 10px;">
    <img alt="Lighbox image without caption" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiDX2wniSXZJk1dPcvF8qYALLBhnmyzLIlnAEnUetWhGvf0JyzEMstRx1Pk_JDqWtS9_mqhBj6itzaZH-p9uIC_60S3AJQTwsUpqtsZrPLDeXI4MZHK6sKsTf1V7riIBdLE0IR45eC65xwQlPM35GTen62jdPILRw6who-l5KZV7xT-QCMxGQ5b09zo/s320/g1.png" style="max-width: 100%; height: auto;" />
    <b>a.</b> Tanpa pengurangan defense Lisa: 14147.
  </div>

  <div style="text-align: center; flex: 1; max-width: 100%; display: inline-block; margin: 10px;">
    <img alt="Lighbox image without caption" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi4zR8SxVSjnCas4c0MsWwxUn9RaoXK6qPaqMT9zK-TFV6TjOEpIrwlsLJzTbi3oWW0GYeKEzG6tp--IaaE2bzLqvZVQZ7IVV53sqiUI7gkjqmj4lA1JjQ7BYTYAH2cxDhZtNfQoK0nPOG_hUxJEpOCfvR3F3Euj_MAKrOxGxqWobCT4SQXJtcuqsNC/s320/g2.png" style="max-width: 100%; height: auto;" />
    <b>b.</b> Dengan pengurangan defense Lisa: 15303.
  </div>
</div>

<b>Gambar 1.2.:</b> Perbandingan damage untuk pengurangan defense dengan skill Q milik Lisa dan E milik Keqing.

$\overline{\phantom{xxxxxxxxxxxxxxxxxxxxxxx}}$<br>
<sup>7</sup> Mengurangi defense objek dan mengabaikan pertahanannya adalah sebuah perbedaan. Misalnya, Anda dapat mengurangi pertahanan sebesar $x\%$ dan mengabaikan $y\%$ dari defense yang dikurangi ini.

<i>Dalam contoh ini burst Lisa digunakan untuk mengurangi defense musuh, level Primo Geovishap</i> 93, <i>dengan</i> $DEF\left(\text{Reduction}\right) = 15\%$. <i>Karakter yang memberikan damage adalah Keqing level</i> 90 <i>dengan kemajuan E-nya</i>.<br />
<i>Dengan persamaan</i> (<a href="#rumus1.14">1.14</a>) <i>pengali defense tanpa pengurangan defense sebesar</i> 0.4961 <i>dan dengan perubahan menjadi</i> 0.5367. <i>Oleh karena itu peningkatan damage adalah</i> $\frac{0.5367}{0.4961} = 1.0818$, <i>dengan kata lain</i> 8.18%.

<i>Mengalikan damage pada gambar <a href="#1.2.a">1.2.a</a> dengan angka ini menghasilkan</i> 15.304, <i>yang mana, dengan mempertimbangkan pembulatan dalam game, setara dengan damage pada gambar <a href="#1.2.b">1.2.b</a> di sebelah kanan.</i>

<p style="text-indent: 30px;">Saat ini di versi 3.4 seseorang dapat maksimal. merobek-robek pertahanan sebesar 83% (Lisa, C4 Razor, C4 Ayaka, C2 Klee) dan mengabaikan 60% (C2 Raiden, C6 Yae) dari itu dan batas atas merobek-robek atau mengabaikan defense saat ini belum dapat dipastikan. Kita dapat melihat dari rumus (<a href="#rumus1.14">1.14</a>) atau pada gambar <a href="#1.1.a">1.1.a</a> bahwa, tanpa pengurangan defense, damage akan berkuran setengahnya ketika karakter dan musuh memiliki level yang sama.</p>

### 1.2.2. Resistance

Karakter atau musuh memiliki resistensi dasar yang berbeda $RES\left(\text{Base}\right)$ untuk setiap elemen dan physical damage. Ini dapat ditingkatkan atau dikurangi, di mana $RES\left(\text{Bonus}\right)$ didefinisikan sebagai jumlah dari pertama dan $RES\left(\text{Debuff}\right)$ yang terakhir. Pengganda resistensi bervariasi secara non-linear dengan total resistensi.
<div style="text-align:center">

**$RES = RES\left(\text{Base}\right) + RES\left(\text{Bonus}\right) - RES\left(\text{Debuff}\right)$** </div>

dan telah ditentukan oleh analisis regresi memiliki bentuk sebagai berikut

<div style="text-align:center">

$$
Mult_{\text{RES}}= 
\left\{
\begin{matrix}
1-\frac{(RES)}{2} & \text{for}\; RES \leq 0, \\
1-RES & \text{for}\; 0 \leq RES \leq 0.75, \\
\frac{1}{4 \cdot RES + 1} & \text{for}\; RES \geq 0.75.
\end{matrix}
\right.
$$

</div>

Dalam Kebanyakan kasus $RES_{\text{Base}, \%}$ musuh<sup>8</sup> lebih rendah dari 75%. Sebagai contoh, mari kita ambil $RES_{\text{Base}}$ = 10%, daripada reaksi pusaran Viridescent Venerer disebabkan ($RES_{\text{Debuff}, \%}$ = 40%) dari satu biasanya, dengan santai mengatakan bahwa resistensi akan berkurang menjadi nilai efektif $\frac{RES\%}{2} = -15\% $.  
Terakhir, perlu diingat bahwa resistensi musuh juga dapat dipengaruhi oleh efek seperti "Ley Line Disorder", "Elemental Nodes", "Elemental Armor of Fatui Skirmishers", dll.

<span style="color: #3d85c6;">**Contoh 1.2**</span> (Pengurangan Resistensi dengan Viridescent Vener (VV) Swirl):


<div style="display: flex; justify-content: center; align-items: center; text-align: center; gap: 20px;">
    <div>
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhcPpMtKMH1Uqp_DpCc7YZW0JaaKD57Sphm_QTDLPJI6YY5ZeLoxwPphX70hAuzJuzwSnbJmo5Bx7w7wvZbZYKRA_kKLKqTPoqXtVX3ramAOalpZFY8CpJibwoxI_eN9-xjAtFH5x4358uvhfsPFGwD1327S9cp-lH4rchdsSNe8D88m77QNNa-6XG0/s320/a%20Tanpa%20pengurangan%20VV%2014%20147.png" style="width: 100%; max-width: 480px; height: auto;" />
        <b>a.</b> Tanpa pengurangan VV 14147.
    </div>
  
<div>
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiZw0Ca53dXa4qazNhMWwZ6FH3wCkEl2eJw-Mq5_PeHUqC1SdYVpU0NVL1O6P83bE30eNB0bnCmTjlCh5ZHu7abVbUKhIfoUt9tamU5oNKqOo0CylCxMAISuVWgWxN78SHel11zZe71u8OFF38Qc7ZFBwkxJQxgr2Enb13BMSiBOB77oJvWlqvY9Yr3/s320/b.%20Dengan%20pengurangan%20VV%2018%20076.png" style="width: 100%; max-width: 480px; height: auto;" />
        <b>b.</b> Dengan pengurangan VV 18 076.
    </div>
</div>


**Gambar 1.3.:** Perbandingan damage untuk pengurangan resistensi dengan bonus artefak VV 4pc.

$\overline{\phantom{xxxxxxxxxxxxxxxxxxxxxxx}}$<br>
<sup>8</sup>Saat ini, pada versi 3.4, resistensi musuh yang diketahui dapat ditemukan di lampiran <a>B.1.</a>


*Sucrose, dilengkapi dengan set artefak VV 4*pc*, *digunakan untuk mengurangi resistensi elektro sebesar* 40% *dari musuh, (pyro) Primo Geovishap* $RES_{\text{Base},\%}$ = 10%. *Dengan persamaan* (<a href="#rumus1.16">1.16</a>) *resistensi pengali musuh berubah dari* 0,9 *menjadi* 1,15 *dan peningkatan total damage adalah* $\frac{1.15}{0.9} $ = 1.278, *dengan kata lain* 27,8%.


*Mengalikan damage pada gambar* <a href="#g3">1.3.a</a> *di sebelah kiri dengan angka ini akan menghasilkan* 18.077, *yaitu, dengan mempertimbangkan pembulatan dalam game, setara dengan damage pada gambar* <a href="#g4">1.3.b</a> *di sebelah kanan.*

![alt text](https://raw.githubusercontent.com/AlenaMiaw/Blogger-Post/b71448a1b78b4d8f0abe18b396d907c61a453238/svg/3%20Pengganda%20resistansi.svg)

**Gambar 1.4.:** Pengganda resistansi sebagai fungsi dari resistansi total.


### 1.2.3. Reduction

Pengganda terakhir untuk pengurangan damage sangat jarang terjadi, deskripsi dalam game menyebutkannya secara langsung sebagai pengurangan damage dari skill karakter tertentu dan diberikan oleh
<div style="text-align:center">

$\text{Mult}_{\text{DMG} \times \text{Reduction}} = 1 - \text{DMG}_{\text{Reduction}} $</div>

dimana beberapa kemampuan pengurangan damage ditambahkan bersama secara aditif. Contohnya adalah

<ol style="text-align: left;">
<li>
    Target milik Thunderbeast milik Beidou: "Mengurangi DMG yang diambil. (37% pada level bakat 13)"
</li>
<br />
<li>
    Pedang Guhua milik Xingqiu: "Ketika karakter mengambil DMG, Pedang Hujan akan hancur, mengurangi jumlah DMG yang diambil. 20% dari Bonus Hydro DMG Xingqiu akan dikonversi menjadi pengurangan DMG tambahan untuk Pedang Hujan."
</li>
<br />
<li>
    Konstelasi ke-6 Jean, Taring Singa, Pelindung Adil Mondstadt: "DMG yang masuk adalah menurun sebesar 35% di dalam Field yang diciptakan oleh Dandelion Breeze."
</li>
<br />
<li>
    Rasi bintang ke-4 Traveler (anemo) Cherising Breezes: "Mengurangi DMG yang diambil saat melemparkan Palm Vortex sebesar 10%."
</li>
</ol>

<span style="color: #3d85c6;">Contoh 1.3</span> (Pengurangan Damage dengan Beidou):</b> <i>Dalam contoh ini, pengurangan damage yang masuk ditunjukan dengan C6 Beidou, oleh karena itu hp tambahan perisai, berdasarkan 16% dari HP maksimal Beidou, harus dipertimbangkan.</i>

<div style="display: flex; justify-content: center; align-items: center; gap: 20px;">
    <div>
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjHlDR8MOdfBl3Vk5sQBdOJSVvpzj2EsZ-L0fZIM9CFo0zZ1uRwQsq8hqwcNeJjSvNwQFyhHtK-Qvy0Vc8Y36lsrcaR6BlKmpmOI5QIpponXbSBGl2YnujjBZbJ9RTHZ0g_llP1YO0jvIOSBUJsKiNqJFR_nsudl6AX2unzCx_aheHCNU_UYVCEqCrS/s320/a.png" style="width: 100%; max-width: 480px; height: auto;" />
        <b>a.</b> Tanpa pengurangan damage: 3440.
    </div>
  
<div>
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhvMPMaOL-Ssm1Dk4RKFHj3sPc-arWiCQ7VGrlpAwsL9t9tNFDQhEeZfuLrIs_DEs_1F73W5eNYsYT_2OYmJoho5UCJzXnr5yGYDRU-0oRnFuFJxrggGykvZFYZiKF8VpHSgn0XtTbQp6VDhWc0iuT_aA5BAhQWWDFO1mJge9YrB-dcPpxKpwlAGZxs/s320/b.png" style="width: 100%; max-width: 480px; height: auto;" />
        <sub><sup><b>b.</b> Dengan pengurangan damage pada serangan kedua: 1317 (+3 018 dari shield).</sup></sub>
    </div>
</div>

<b>Gambar 1.5.:</b> Perbandingan damage yang masuk untuk pengurangan damage dengan Beidou's Q.

<i>Dapat dilihat pada gambar <a href="#g5">1.5</a> bahwa HP maksimal Beidou adalah 18.860 dan oleh karena itu jumlah HP shieldnya menjadi 3.018. Level talent dari burst Beidou pada tes ini adalah 13, memberikan 37% reduksi damage.  
Pengali reduksi $\text{Mult}_{\text{DMG}\times\text{Reduction}}$ berubah dari 1 menjadi 0.63.</i>

<i>Tanpa reduksi apapun, damage yang masuk adalah 3.440 (sce fig. <a href="#g5">1.5.a</a>), mengalikan nilai ini dengan pengali pengurangan damage meghasilkan hanya 2.167 damage yang diterima perserangan. Dua serangan dengan pengurangan damage, setelah meghancurkan shield, menghasilkan 1.316 damage masuk yang diterima, yaitu, dengan mempertimbangkan pembulatan dalam game, setara dengan damage yang diterima pada gambar <a href="#g6">1.5.b</a> di sebelah kanan.</i>


## 1.3. Elemental Reactions

Ada dua jenis reaksi elemen: reaksi penguatan yang meningkatakn damage dari serangan yang memicu reaksi dan reaksi transformatif yang memberikan elemen tambahan damage tambahan ketika dipicu. Tinjauan singkat di bagian <a>3.1.</a>

Bonus elemen $EM_{\text{Bonus}}$ ditampilkan di layar status dalam game dan diberikan kira-kira sebesar

<div style="text-align:center">

$\text{EM}_{\text{Bonus},i} = k_{(i)} \cdot \frac{EM}{EM + c_{(i)}}$
</div>

dengan penguasaan elemen $EM$ dari karakter tersebut. Visualisasi pada gambar <a href="#g6">1.6</a> berfungsi untuk estimasi sederhana. Dua konstanta $C_{(i)}$ dan $K_{(i)}$ bergantung pada jenis reaksi dan tercantum dalam tabel <a href="#tab1.1">1.1.</a>

**Tabel 1.1.:** Parameter model regresi untuk bonus elemen $\text{EM}_\text{Bonus}$.

|      | Amplifying | Transformative | Crystallize |
| :--- | :--------: | :---------------: | ----------: | 
| $k_{(i)}$ | 2.78 | 16 | 4.44 |
| $C_{(i)}$ | 1 400 | 2 000 | 1 400 |

<p style="text-indent: 30px;">

Selain penguasaan elemen, bonus reaksi $Reaction_{\text{Bonus}}$, yang merupakan tambahan dari $EM_{\text{Bonus}}$, dapat meningkatkan lebih lanjut damage yang diberikan oleh reaksi elemen. Contohnya adalah</p>

<ul>
<li>Set artefak Crimson Witch of Flames (<b>CWoF</b>) 4pc: +15% untuk melt dan vaporize, +40 untuk burning dan overloade.</li>
<br />
<li>Set artefak Thundering Furry (TF) 4pc: +40% untuk overload, electro charge, dan superconduct.</li>
<br />
<li>Set artefak Viridescent Venere (VV) 4pc: +60% untuk swirl</li>
<br />
<li>Set artefak Retracing Bolide (RB) 2pc: +35% untuk crystallize.</li>
<br />
<li>Konstelasi pertama Mona Prophecy of Submersion: +15% untuk electro charge, vaporize dan
hydro swirl.</li>
</ul>


chart 4
    chart 4
    chart 4
    chart 4
    chart 4
    chart 4
    chart 4
    chart 4
    chart 4
    chart 4
    chart 4
    chart 4
    chart 4
    chart 4

<div style="text-align:center">

**Gambar 1.6.:** Bonus damage elemen sebagai fungsi dari penguasaan elemen.
</div>

### 1.3.1. Amplifying Reactions

Amplifying Reactions adalah melt dan vaporize. Melt adlah reaksi unsur yang dipicu oleh pyro pada target yang sudah terpengarug oleh cryo atau sebaliknya yang seringkali lebih secara akurat disebut reverse melt. Vaporize dipicu dengan menimbulkan hydro pada target yang sudah terkena pyro dan kebalikannya disebut reverse vaporize.

<p style="text-indent: 30px;">
Reaksi ini menambahkan pengganda ekstra pada damage dan bonus reaksi dari pemicu karakter. Ketika reaksi penguat terjadi, total damage yang diterima karakter atau musuh dapat diekspresikan dengan</p>

$$
DMG_{\text{Amplified}} = DMG_{\text{Total}} \cdot Mult_{\text{Amplified}}
$$

$$
Mult_{\text{Amplified}} = Mult_{\text{Reaction}} \cdot (1 + EM_{\text{Bonus,Amplified}} + Reaction_{\text{Bonus}})
$$

$$
Mult_{\text{Reaction}} =
\begin{cases}
2 & \text{for melt/vaporize,} \\
1.5 & \text{for reverse melt/vaporize.}
\end{cases}
$$

**Contoh 1.4** (Amplifying reaksi (Reverse melt) dengan HU Tao): *Hu Tao, dilengkapi dengan satu set artefak CWoF 4pc, digunakan untuk menyebabkan reverse melt reaksi, di mana Kokomi hanya digunakan untuk aplikasi hydro. Stat $EM$ Hu Tao berjumlah 65 (lihat gambar [1.7](#g7)), memberinya bonus elemental mastery dasar $EM_{\text{Bonus},\%}$ = 12,3%, menurut persamaan ([1.18](#rumus1.18)) dan tabel [1.1](#tab1.1). Dengan bonus reaksi 15% dari set CWoF 4pc, pengali reaksi reverse melt sebesar 1,5 dan persamaan ([1.20](#rumus1.20)) pengali amplifying adalah $Mult_{\text{Amplified}}$ = 1,91.*


<div style="display: flex; justify-content: center; align-items: center; gap: 20px;">
    <div>
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhYtAg1qVtFq2MpYuZDNocMhTVomFSdEHVsLHX4nkIbLq-_UK-sYjxeuGc4inRrsnzVe6mTGw1PwPEuCqzMiOeL4oSHgCv-lCezGlIJR6chYTvm3mh5_00g6IEdnNfUNMDHJkvmrPqr-97Kq07CQWApPAxfduIvzjyI3oQDTf8Y8AJEUIH0jzOUxnnR/s320/a1.png" style="width: 100%; max-width: 480px; height: auto;" />
        <b>a.</b> Tanpa reaksi 5 502.
    </div>
  
<div>
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiS2UHsJzYQ8x0-Y9Dl4phvzyCtRcVXVrOACsRP2EP0F1Vj4Ru6D5CtxWVxSZ7jlj0-wLi4hhNu93rKHBaTezcUwVS0f6wJYekqyTozkZM53_5O6wnbq8rFP5l_jIeQk16u3OQR9byTZSG5V7H-06HZsyIQE6uNESD1yaS0vYY33Id2PZ_3A82aR-nJ/s320/b1.png" style="width: 100%; max-width: 480px; height: auto;" />
        <b>b.</b> Dengan reverse vaporize 10513.
    </div>
</div>

<div style="text-align: center;">
    <b>Gambar 1.7.:</b> Perbandingan damage untuk reverse vaporize dengan serangan normal Hu Tao.
</div>

*Mengalikan damage di sebelah kiri gambar [1.7.a](g7) dengan angka ini akan menghasilkan 10.509, yaitu, dengan mempertimbangkan pembulatan dalam game, terutama untuk $EM$ ([64.5, 65.5) semuanya ditampilkan sebagai 65), setara dengan damage pada gambar [1.7.b](g8) sebelah kanan.*


### 1.3.2. Transformative Reactions

Reaksi transformatif adalah overload, shatter, electro-charge, superconduct, dan swril<sup>9</sup>. Ini hanya berskala dengan level karakter pemicu<sup>10</sup>, elemental mastery, bonus reaksi dan resistensi musuh (seperti biasa mereka tidak terpengaruh oleh statistik apa pun yang terkait dengan karakter menerapka elemen terlebih dahulu). Dengan kata lain, reaksi transformatif tidak memiliki skala karaker menyerang, tidak bisa critical, mengabaikan defense objek (oleh karena itu untuk musuh independen dari leve; di sana), tidak dapat dibuff dengan bonus damage , metode increase damage juga tidak dipengaruhi oleh reduction damage

$$
\begin{align*}
DMG_{\text{Transformative}} &= Mult_{\text{RES}}\;\cdot\; Mult_{\text{Transformative}} \\
Mult_{\text{Transformative}} &= Mult_{\text{Reaction}}\; \cdot \; Mult_{\text{Level}}\; \cdot \; (1+EM_{\text{Bonus,Transformative}}+Reaction_{\text{Bonus}}) \\
Mult_{\text{Reaction}} &= \left\{
\begin{matrix}
0.5 & \text{for superconduct} \\
0.6 & \text{for swirl} \\
1.2 & \text{for electro-charge} \\
1.5 & \text{for shatter} \\
2 & \text{for overload}
\end{matrix}
\right.
\end{align*}
$$

Pengali level untuk karakter tercantum dalam lampiran [B.2](#B.2), tetapi karena sebagian besar pemain memiliki karakter yang maksimal hingga titik tertentu, nilai $Mult_{\text{Level(80)}}$ = 1.077,4 dan $Mult_{\text{Level(90)}}$ = 1.446,9 atau gambar [1.8](#g1.8) seharusnya sudah cukup untuk sebagian besar pemain.


#### 1.3.2.1. Swirl-Induced Reaction Damage

Memicu swirl dengan beberapa musuh yang dipengaruhi oleh elemen yag bebeda akan menghasilkan tambahan memperkuat atau reaksi transformatif yang dipicu karena transfer elemen di antara

$\overline{\phantom{xxxxxxxxxxxxxxxxxxxxxxx}}$<br>
<sup>9</sup>Reaksi "burning" akan dihilangkan di sini. Selanjutnya, kumpulan artefak Ocean-Hued Clam (OHC) adalah dihitung dengan cara yang sama seperti yang dinyatakan dalam deskripsi artefak, meskipun "pengali reaksi" adalah 1 dan tidak terengaruh oleh pengali level, maupun bonus elemen atau reaksi. Damage dari gelembung masih dapat ditingkatkan dengan meningkatkan status bonus healing dan healing yang masuk dari karakter dan mengurangi rsistensi musuh.<br /><sup>10</sup>Ofc reaksi ini juga bisa terjadi sebaliknya dan akan meningkatkan skala level dan resistensi musuh dari karakter tersebut.


chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5
    chart 5

<div style="text-align:center">

**Gambar 1.8.:** Pengganda untuk reaksi transformatif sebagai fungsi dari level karakter.</div>

musuh. Reaksi yang disebut swirl-induced ini berperilaku dan berskala persis sama dengan reaksi transformatif, di mana untuk memperkuat reaksi, produk dari swirl dan amplifying multiplier digunakan:

$DMG_{\text{Swirl-Induced}} = Mult_{\text{RES,2nd Enemy}} \cdot \left( \text{Mult}_{\text{Transformative}}, \left( \text{Mult}_{\text{Transformative,Swirl}} \cdot \text{Mult}_{\text{Amplified}} \right) \right)$


Dalam kedua kasus tersebut, pengganda level didasarkan pada karakter yang memicu swirl.


### 1.3.3. Crystallize

Reaksi unsur yang dipicu dengan menimbulkan geo pada target yang sudah terpengaruh oleh pyro, hydro, cryo atau electro disebut crystallize<sup>11</sup>. Reaksi ini tidak menimbulkan damage, melainkan menghasilkan pecahan elemen yang sesuai yang dapat diambil untuk mendapatkan shield elemen (lebih lanjut lihat bagian <a>2.1</a>)

## 1.4. Attack Speed

Attack speed<sup>12</sup> (ATK SPD) mengubah kecepatan serangan karakter. Ini meningkatkan rata-rata dan keseluruhan dps dengan cara multiplicative di samping bonus berbasis damage lainnya dan beberapa buff speed atk menumpuk secara aditif<sup>13</sup>.

<p style="text-indent: 30px;">
Karena perhitungan sangat bergantung pada tim yang digunakan, artikel ini tidak akan membahas lebih jauh hal itu, sebagai contoh kita dapat mengambil Eula, di mana peningkatan atk speed menyebabkan lebih benyak kemungkinan tumpukan (burst) dan oleh karena itu rata-rata damage dan tangkapan layar yang lebih tiggi.</p>

$\overline{\phantom{xxxxxxxxxxxxxxxxxxxxxxx}}$<br>
<sup>11</sup>Cara reverse juga dapat dilakukan tetapi geo aplikasi memiliki waktu peluruhan yang sangat rendah dan tidak bertahan lama, yang membuatnya hampir tidak mungkin untuk memicu dengan cara ini.<br />
<sup>12</sup>Movement speed tidak meningkatkan attack speed dan sebaliknya.<br />
<sup>13</sup>Menganalisis jumlah frame dengan buff yang berbeda mengarah mengarah pada kesimpulan bahwa mungkin ada yang umum atau untuk setiap karakter memilik batas individu (tergantung pada fisika karakter) sekitar (63 ± 15)%. . . Lebih banyak buff atk speed tinggi diperlukan untuk membuat pernyataan yang lebih baik.

## 1.5. Other types of damages

### 1.5.1. True Damage

True damage memberikan damage sebagai persentase tetap dari stat objek, misalnya HP, atau nilai tetap sambil mengabaikan semua (de)buff (juga bypass shield) yang diterapakan pada suatu objek. Contohnya adalah:

- Fall damage terjadi ketika sebuah objek menghantam tanah (atau misalnya dinding) dengan kecepatan tertentu dan memberikan persentase dari *HP* maksimal mereka sebagai physical damage (karena itu adalah damage yang sebenarnya tidak terpengaruh oleh peningkatan physical damage, atau physical resistance). Persentasenya tergantung pada posisi suatu objek berada dan berskala dengan kecepatan, yang tidak perlu berhubungan langsung ke ketinggian.

- Sheer Cold dan Blazing Heat memberikan damage dengan $1\%HP_{\text{max}}$ + 150 per detik. Contoh dengan 15 kHP, dibutuhkan 50 detik untuk menghabiskan semua HP.

- Damage yang sebenarnya sebagai Gangguan Ley Line eksplisit (misalnya di spiral Abyss, event, . . .) memberikan damage tetap tergantung pada level objek.

### 1.5.2. Proc Damage

Proc mengacu pada pasif senjata, kemampuan, dan senjata sebagainya yang memberikan contoh fisik yang terpisah damage saat dipicu dan dipengaruhi oleh bonus damage fisik karakter, defense dan physical resistance musuh dapat melakukan crit. Perhitungannya secara harfiah sama dengan sumber damage normal lainnya, di mana talent multiplier dalam persamaan (<a href="#rumus1.2">1.1</a>) akan diganti dengan persentase proc (mis, 125% damage physical ATK R1 Skyward Harp), meskipun damage tersebut bukan bagian dari salah satu dari tiga jenis gerakan dan damage standar.

<p style="text-indent: 30px;">Contohnya adalah Aquila-Favonia, Prototype Archaic, Eye of Perception, The Viridescent Hunt, Crescent Pike, Anemo Traveler’s Slitting Wind (A1), . . . .</p>


### 1.5.3. Environmental Damage

Damage lingkungan berasal dari sumber-sumber lingkungan, contohnya adalah:

- Burning grass, air yang dialiri listrik, dll. memberikan damage elemen, tergantung pada dunia tingkat dunia dan resistance elemen objek.

- Mist Flowers, Electro Crystals, dll. memberikan damage elemen yang dikurangi oleh defense objek (oleh karena itu jelas bahwa bahaya lingkungan seperti itu memang tersembunyi tingkat) dan resistensi.

- Reaksi elemen transformatif yang dipicu oleh lingkungan menyebabkan damage yang berskala dengan tingkat dunia.

- Damage yang diberikan oleh aura tergantung pada aura dan level domain/dunia. Itu mengabaikan pertahanan, tetapi tidak untuk resistensi elemen atau shield.

## 1.6. Complex Examples

### 1.6.1. Raiden

Pada bagian ini, pertama-tama, damage burst awal (dan serangan charge selama Q-nya) dari Raiden C2 harus dihitung. Karakter (dan musuh), artefak, dan senjata berikut ini digunakan (hanya informasi yang diperlukan yang ditampilkan)

1. C2 Raiden: Emblem 4pc, R1 Engulfing Lightning, level 90, level talent Q: 10 (maks. tumpukan). Tingkat talent E: 9.

2. C3 Bennet: 4pc Nobless, Aquillia Favonius, level 90, Q talent level: 10, Digunakan: $(191+674) \cdot \left( \frac{100.8\% + 20\%}{100\%} \right) = 1045$ atk buff.


3. C6 Sucrose: 4pc VV, Usage: 20% electro damage buff and 40% electro shred.

4. C6 Beidou: Usage: 15% electro shred.

5. (pyro) Geovishap: Level 93, 10% base electro resistance

Tentu saja secara teoritis seseorang dapat meningkatkan damage lebih lanjut dengan karakter senjata lain dan seterusnya. Hanya untuk mereka yang tertarik, kami akan menyebukan damage dengan R5 Thrilling Tales of Dragon Slayers (TToDS) pada Sucrose, R5 wolf's Gravestone (WG) pada Beidou dengan hp musuh dan C6 Sara dengan buff atk maksimal.


<p style="text-indent: 30px;">Bagian pertama terdiri dari menghitung statistik Raiden setelah menerapkan setiap buff yang disebutkan di atas:</p>


$$
\begin{align*}
 ER &= ER_{\text{Character}} + ER_{\text{Weapon,Q-passive}} + ER_{\text{Artefacts}} \\
   &= 132\%\ + 55.1\%\ + 30\%\ + 90.6\%\ = 307.7\%, \\
 ATK_{\text{Base}} &= ATK_{\text{Character}} + ATK_{\text{Weapon}} = 945, \\
 ATK &= ATK_{\text{Base}}\; \cdot \; \left(1 + \frac{29.2\%}{100\%} + \frac{ER-100\%}{100\%} \cdot \frac{28\%}{100\%} + \frac{20\%}{100\%} \right) \\
     &\quad + ATK_{\text{Artefacts, Flat}} + ATK_{\text{Bennet,buff}} \\
     &= 945 \cdot \left(1 + \frac{29.2\%}{100\%} + \frac{ER - 100\%}{100\%} \cdot \frac{28\%}{100\%} + \frac{20\%}{100\%} \right) + 375 + 1045 = 3379, \\
 CD_{\text{\%}} &= CD_{\text{Base,\%}} + CD_{\text{Artefact,\%}} = 50\% + 103.4\% = 153.4\%.
\end{align*}
$$

<br>
Selanjutnya pengganda bonus talent dan damage<sup>14</sup>:
<br><br>



<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">
  <mtable displaystyle="true" columnalign="right left" columnspacing="0em" rowspacing="3pt">
    <mtr>
      <mtd>
        <mi>M</mi>
        <mi>u</mi>
        <mi>l</mi>
        <msub>
          <mi>t</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Q-Talent,Initial</mtext>
          </mrow>
        </msub>
      </mtd>
      <mtd>
        <mi></mi>
        <mo>=</mo>
        <mi>M</mi>
        <mi>u</mi>
        <mi>l</mi>
        <msub>
          <mi>t</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Q-Talent,Initial</mtext>
          </mrow>
        </msub>
        <mo>+</mo>
        <msub>
          <mi>n</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Resolve stacks</mtext>
          </mrow>
        </msub>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mo>&#x22C5;</mo>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mi>M</mi>
        <mi>u</mi>
        <mi>l</mi>
        <msub>
          <mi>t</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Q-Talent,Initial bonus</mtext>
          </mrow>
        </msub>
      </mtd>
    </mtr>
    <mtr>
      <mtd></mtd>
      <mtd>
        <mi></mi>
        <mo>=</mo>
        <mn>721</mn>
        <mtext>%</mtext>
        <mo>+</mo>
        <mn>60</mn>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mo>&#x22C5;</mo>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mn>7</mn>
        <mtext>%</mtext>
        <mo>=</mo>
        <mn>1141</mn>
        <mtext>%</mtext>
        <mo>,</mo>
      </mtd>
    </mtr>
    <mtr>
      <mtd>
        <mi>M</mi>
        <mi>u</mi>
        <mi>l</mi>
        <msub>
          <mi>t</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Q-Talent,Charge 1.Hit</mtext>
          </mrow>
        </msub>
      </mtd>
      <mtd>
        <mi></mi>
        <mo>=</mo>
        <mi>M</mi>
        <mi>u</mi>
        <mi>l</mi>
        <msub>
          <mi>t</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Q-Talent,Charge 1.Hit</mtext>
          </mrow>
        </msub>
        <mo>+</mo>
        <msub>
          <mi>n</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Resolve stacks</mtext>
          </mrow>
        </msub>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mo>&#x22C5;</mo>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mi>M</mi>
        <mi>u</mi>
        <mi>l</mi>
        <msub>
          <mi>t</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Q-Talent,DMG bonus</mtext>
          </mrow>
        </msub>
      </mtd>
    </mtr>
    <mtr>
      <mtd></mtd>
      <mtd>
        <mi></mi>
        <mo>=</mo>
        <mn>109.9</mn>
        <mtext>%</mtext>
        <mo>+</mo>
        <mn>60</mn>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mo>&#x22C5;</mo>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mn>1.31</mn>
        <mtext>%</mtext>
        <mo>=</mo>
        <mn>188.6</mn>
        <mtext>%</mtext>
        <mo>,</mo>
      </mtd>
    </mtr>
    <mtr>
      <mtd>
        <mi>M</mi>
        <mi>u</mi>
        <mi>l</mi>
        <msub>
          <mi>t</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Q-Talent,Charge 2.Hit</mtext>
          </mrow>
        </msub>
      </mtd>
      <mtd>
        <mi></mi>
        <mo>=</mo>
        <mi>M</mi>
        <mi>u</mi>
        <mi>l</mi>
        <msub>
          <mi>t</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Q-Talent,Charge 2.Hit</mtext>
          </mrow>
        </msub>
        <mo>+</mo>
        <msub>
          <mi>n</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Resolve stacks</mtext>
          </mrow>
        </msub>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mo>&#x22C5;</mo>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mi>M</mi>
        <mi>u</mi>
        <mi>l</mi>
        <msub>
          <mi>t</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Q-Talent,DMG bonus</mtext>
          </mrow>
        </msub>
      </mtd>
    </mtr>
    <mtr>
      <mtd></mtd>
      <mtd>
        <mi></mi>
        <mo>=</mo>
        <mn>132.7</mn>
        <mtext>%</mtext>
        <mo>+</mo>
        <mn>60</mn>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mo>&#x22C5;</mo>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mn>1.31</mn>
        <mtext>%</mtext>
        <mo>=</mo>
        <mn>211.6</mn>
        <mtext>%</mtext>
      </mtd>
    </mtr>
    <mtr>
      <mtd>
        <mi>D</mi>
        <mi>M</mi>
        <msub>
          <mi>G</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Bonus,%</mtext>
          </mrow>
        </msub>
      </mtd>
      <mtd>
        <mi></mi>
        <mo>=</mo>
        <mi>D</mi>
        <mi>M</mi>
        <msub>
          <mi>G</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Artefacts,%</mtext>
          </mrow>
        </msub>
        <mo>+</mo>
        <mi>D</mi>
        <mi>M</mi>
        <msub>
          <mi>G</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Talent,passive,%</mtext>
          </mrow>
        </msub>
      </mtd>
    </mtr>
    <mtr>
      <mtd></mtd>
      <mtd>
        <mi></mi>
        <mo>+</mo>
        <mi>D</mi>
        <mi>M</mi>
        <msub>
          <mi>G</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>E-Talent,Bonus,%</mtext>
          </mrow>
        </msub>
        <mo>+</mo>
        <mi>D</mi>
        <mi>M</mi>
        <msub>
          <mi>G</mi>
          <mrow data-mjx-texclass="ORD">
            <mtext>Sucrose,%</mtext>
          </mrow>
        </msub>
      </mtd>
    </mtr>
    <mtr>
      <mtd></mtd>
      <mtd>
        <mi></mi>
        <mo>=</mo>
        <mn>46.6</mn>
        <mtext>%</mtext>
        <mo>+</mo>
        <mfrac>
          <mrow>
            <mi>E</mi>
            <mi>R</mi>
            <mo>&#x2212;</mo>
            <mn>100</mn>
            <mtext>%</mtext>
          </mrow>
          <mrow>
            <mn>100</mn>
            <mtext>%</mtext>
          </mrow>
        </mfrac>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mo>&#x22C5;</mo>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mn>0.4</mn>
        <mtext>%</mtext>
        <mo>+</mo>
        <mfrac>
          <mrow>
            <mi>E</mi>
            <mi>R</mi>
          </mrow>
          <mrow>
            <mn>100</mn>
            <mtext>%</mtext>
          </mrow>
        </mfrac>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mo>&#x22C5;</mo>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mn>25</mn>
        <mtext>%</mtext>
        <mo>+</mo>
        <mn>90</mn>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mo>&#x22C5;</mo>
        <mstyle scriptlevel="0">
          <mspace width="0.278em"></mspace>
        </mstyle>
        <mn>0.3</mn>
        <mtext>%</mtext>
        <mo>+</mo>
        <mn>20</mn>
        <mtext>%</mtext>
      </mtd>
    </mtr>
    <mtr>
      <mtd></mtd>
      <mtd>
        <mi></mi>
        <mo>=</mo>
        <mn>251.68</mn>
        <mtext>%</mtext>
        <mo>.</mo>
      </mtd>
    </mtr>
  </mtable>
</math>


Dengan persamaan (<a href="rumus1.2">1.1</a>), hal ini menghasilkan damage dasar sebesar

$$
DMG_{\text{Base,Initial}} = 135.6\ \text{k}, \quad DMG_{\text{Base,Charge 1.Hit}} = 22.4\ \text{k}, \quad DMG_{\text{Base,Charge 2.Hit}} = 25.1\ \text{k}
$$

Terakhir, perhitungan total damage menurut bab <a>1.2</a>:

<i>RES<sub>%</sub> = RES<sub>Base,%</sub> - RES<sub>Debuff,VV,%</sub> - RES<sub>Debuff,Beidou,%</sub></i>


$\overline{\phantom{xxxxxxxxxxxxxxxxxxxxxxx}}$<br>
<sup>14</sup>Untuk akurasi yang lebih tinggi, seseorang dapat mengambil nilai exacter, alih-alih nilai yang ditampilkan di dalam game, dari misalnya <a target="_blank" href="https://genshin.honeyhunterworld.com/">https://genshin.honeyhunterworld.com/</a>.


$$
\begin{align*}
 & = 10\text{\%} - 40\text{\%} - 15\text{\%} = -45\text{\%}, \\
 Mult_{\text{RES}} &= 1 - \left( \frac{RES_{\text{\%}}}{2 \cdot 100\text{\%}} \right) = 1 - \left( \frac{-45\text{\%}}{2 \cdot 100\text{\%}} \right) = 1.225, \\
 Mult_{\text{DEF}} &= \frac{Level_{\text{Character}} + 100}{(1 - DEF_{\text{Ignore,C2-Raiden}}) \cdot (Level_{\text{Enemy}} + 100) + Level_{\text{Character}} + 100} \\
 &= \frac{190}{(1 - 0.6) \cdot (93 + 100) + 90 + 100} = 0.711,
\end{align*}
$$

$$
\begin{align*}
 DMG_{\text{Total,Crit,Initial}} &= DMG_{\text{Base}} \cdot Mult_{\text{RES}} \cdot Mult_{\text{DEF}} \cdot \left(1 - \frac{CD_{\text{\%}}}{100\text{\%}} \right) \\
 &= 135.7\text{k} \cdot 1.225 \cdot 0.711 \cdot \left( 1 + \frac{153.4\text{\%}}{100\text{\%}} \right) = 299\text{k}, \\
 DMG_{\text{Total,Crit,Charge 1.Hit}} &= 49.4\text{k}, \\
 DMG_{\text{Total,Crit,Charge 2.Hit}} &= 55.4\text{k}.
\end{align*}
$$


Angka-angka ini setara dengan damage pada gambar <a href="#g9">1.9</a>, dengan mempertimbangkan pembulatan dalam game. Untuk referensi, Raiden di C0 akan menghasilkan 209 k dengan tebasan burst awal dalam pengaturan ini.<br />Melengkapi Beidou dengan R5 WG dan Sucrose dengan R5 TToDS, serangan awal akan meningkat menjadi 406,5 k, di mana mengganti Beidou dengan C6 Sara dengan buff serangan maksimal akan menghasilkan 475,8 k.

<p style="text-indent: 30px;">Langkah berikutnya adalah menemukan statistik optimal untuk pengaturan dan senjata ini. Oleh karena itu
kita harus menjaga crit-damage konstan, karena jika tidak maka akan selalu mengarah ke tak terhingga di sana, dan menggunakan serangan dan energy recharge sebagai variabel. Mulai dari 0% ATK%/ER artefak persentase bonus<sup>15</sup> dapat dilihat pada gambar <a href="#g10">1.10</a> bahwa ER memiliki nilai yang sedikit lebih tinggi dalam hal damage (dan juga dalam hal mendapakan energi untuk tim). Dengan kata lain: Hingga 300% ER (termasuk senjata pasif selama burst), lebih baik mendapatkan ER daripada ATK% (statistik utama dan sub) pada artefak untuk R1 Engulfing. Selanjutnya setelah mencapai 300% ER, seseorang dapat bertanya pada diri sendiri apakah bonus damage elemen atau attack goblet akan lebih baik.Jawabannya adalah damage elemen tetapi hanya sekitar 4% di sini, oleh karena itu lebih baik menggunakan yang memiliki statistik crit yang lebih tinggi.</p>

<p style="text-indent: 30px;">Terakhir, perlu diingat bahwa penyeimbangan stat sangat bergantung pada tim dan senjata yang digunakan. Sebagai contoh jika Bennet (atau penyangga serangan serupa) tidak digunakan, maka sebaiknya gunakan ER sands dan goblet ATK%, atau jika Kazuha digunakan sebagai pengganti C6 Sucrose, goblet attack akan menjadi nilai yang sama dengan damageelectro setelah mencapai 300% ER dan seterusnya.</p>

<div style="text-align: center;">    
<img alt="genshin impact" class="lazy full" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiSbM6chkjuyDJTQxaWoILpLby6owm86zW76uc2IV3hYuHjsD3H0aiHsYgsG7o85YlvHAubvIp4A4HG-_5k_qIciwMXxrpsibf3-PWcl-HZNq5gXcsT1PHKk4A5NoyvEQnerjyz1up8g5NPUSDO16NA45TgnIu-RwJrazTXTgraPalofVXiUjDekmFP/s600/raiden.png" />
    <b>a.</b> Statistik Raiden tanpa bentuk buff apa pun.
</div>


$\overline{\phantom{xxxxxxxxxxxxxxxxxxxxxxx}}$<br>
<sup>15</sup>Perlu diingat bahwa 5,8% ATK% dan 6,5% ER memiliki nilai yang sama.

<div style="display: flex; justify-content: center; align-items: center; gap: 20px;">
    <div style="text-align:center">
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhGURAPmpL2mZCX9NoUh79cEaaQP4cVihEi0hqELSCeX5w6OBnzPy9Bc-VnCcmJbKbRWXsMjQqS8doGr4kLk7V1ISTZG8G6IEnivp1jjpG5PF2zVRTFLb62rQGTL9BMXi9z-UjPYrFJWTk-EGACKkwP0rjkUAImb1ui4KZPo9A9F8Ws1dyVmOeGz7Cy/s1600/a1.1.png" style="width: 100%; max-width: 480px; height: auto;" />
        <b>a.</b> Pukulan burst awal: 299.484.
    </div>
  
<div>
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiu5Z1da7-EIjCh_V5RHapOjib5tKwVrOs5gpg3hJtXcq34-Y7PqcWJQRDyQgLB3ChzjxAhHX88-GAtY-pFcGccXSCaCc4r8yNGvs5zWYPQwhKqIOZIZRLfM0vSJnT53hLkq3iPnimQDPYDCLCi6pQi3jwbpGU5xRACbjmjgJODK7N9hJsp18R1ENP9/s400/Untitled.png" style="width: 100%; max-width: 480px; height: auto;" />
        <sup><b>b.</b> Charge attack 1.hit: 49 416, 2.hit: 55 389.</sup>
    </div>
</div>

**Gambar 1.9.:** Statistik dan damage dari C2 Raiden dengan R1 Engulfing dengan buff tim penuh seperti yang disebutkan di awal bagian <a>1.6.1</a>.


chart 6
      chart 6
      chart 6
      chart 6
      chart 6
      chart 6
      chart 6
      chart 6
      chart 6
      chart 6
      chart 6
      chart 6
      chart 6
      chart 6
      chart 6


<b>Gambar 1.10.:</b> damage total sebagai fungsi dari ER dan ATK% gulungan artefak (stat utama pasir dan substat) untuk R1 Engulfing dengan tim ini (Bennet). Hal pertama yang perlu diperhatikan adalah naik hingga sekitar 270% ER (total), seseorang mendapatkan lebih banyak damage daripada dengan statistik attack, setelah itu hampir secara linear hingga 300% ER dan 12% ATK% dan pada saat itu ATK% meningkatkan damage lebih banyak dari ER (Alasan: bonus set artefak Emblem 4pc).


### 1.6.2. Sucrose

Pada bagian ini, damage akibat swirl dan swirl-induced dari Sucrose, yang dilengkapi dengan VV-set 4pc; statistik yang ditunjukkan pada gambar <a href="#g11">1.11.a</a>, harus dihitung. Musuh Ruin Guards dengan basis 10% resistance.

Dengan persamaan (<a>1.22</a>) dan rumus yang tercantum dalam bagian <a href="#rumus1.3">1.3</a>, damage akibat sewirl adalah sebesar:

$$
\begin{align*}
 RES_{\text{\%}} &= RES_{\text{Base,\%}} - RES_{\text{Debuff,VV,\%}} = 10\text{\%} - 40\text{\%} = -30\text{\%}, \\
 Mult_{\text{RES}} &= 1 - \left( \frac{RES_{\text{\%}}}{2 \cdot 100\text{\%}} \right) = \left( \frac{-30\text{\%}}{2 \cdot 100\text{\%}} \right) = 1.15, \\
 EM_{\text{Bonus,Transformative}} &= 16 \cdot \frac{869}{869 + 2000} = 4.846, \\
 Mult_{\text{Transformative,Swirl}} &= Mult_{\text{Swirl}} \cdot Mult_{\text{Level(90)}} \\
 &\quad \cdot (1 + EM_{\text{Bonus,transformative}} + Reaction_{\text{Bonus,VV}}) \\
 &= 0.6 \cdot 1,446.0 \cdot (1 + 4.846 + 0.6) + 5,596, \\
 DMG_{\text{Swirl}} &= Mult_{\text{RES}} \cdot Mult_{\text{Transformative,Swirl}} = 6,436 \pm 3.
\end{align*}
$$


Analog dengan persamaan (<a>1.25</a>), overload yang diinduksi oleh swirl dan (reverse-)melt damage dapat dihitung, di mana beberapa perhitungan resistensi sepele, dll. Dilewati dan diasumsikan bahwa hanya ada dua musuh dalam contoh ini. Ingatlah bahwa hanya resistensi dari elemen yang ada pada musuh sebelum swirl dipicu akan berkurang, misalnya swirl yang diinduksi damage yang berlebihan dianggap sebagai damage pyro dan hanya musuh yang diinfus dengan pyro sebelumnya swirl yang terjadi akan membuat resistensi pyro berkurang dan karena menerima lebih banyak damage daripada musuh yang diinfus electro sebelumnya.


$$
\begin{align*}
Mult_{\text{Transformative,Overload}} &= Mult_{\text{Overload}} \cdot Mult_{\text{Level(90)}} \cdot (1 + EM_{\text{Bonus,Transformative}}) \\
&= 2 \cdot 1,446.9 \cdot (1 + 4.846) = 16,918, \\
DMG_{\frac{\text{Swirl-Induced Overload,}}{\text{electro-infused enemy}}} &= Mult_{\frac{\text{RES(pyro),}}{\text{electro-infused enemy}}} \cdot Mult_{\text{Transformative,Overload}} \\
&= 0.9 \cdot 16,918 = 15,226 \pm 6, \\
EM_{\text{Bonus,Amplified}} &= 2.78 \cdot \frac{869}{869 + 1,400} = 1.065, \\
Mult_{\text{Amplified,Melt}} &= Mult_{\text{Melt}} \cdot (1 + EM_{\text{Bonus,Amplified}}) \\
&= 2 \cdot (1 + 1.065) = 4.129, \\
Mult_{\text{Amplified,Reverse-Melt}} &= Mult_{\text{Reverse-Melt}} \cdot (1 + EM_{\text{Bonus,Amplified}}) \\
&= 1.5 \cdot (1 + 1.065) = 3.097, \\
DMG_{\text{Swirl-Induced Melt}} &= Mult_{\frac{\text{RES(pyro),}}{\text{cryo-infused enemy}}} \cdot Mult_{\text{Transformative,Swirl}} \cdot Mult_{\text{Amplified,Melt}} \\
&= 0.9 \cdot 5,596 \cdot 4.129 = 20,798 \pm 11, \\
DMG_{\text{Swirl-Induced Reverse-Melt}} &= Mult_{\frac{\text{RES(cryo),}}{\text{pyro-infused enemy}}} \cdot Mult_{\text{Transformative,Swirl}} \cdot Mult_{\text{Amplified,Reverse-Melt}} \\
&= 0.9 \cdot 5,596 \cdot 3.097 = 15,599 \pm 8.
\end{align*}
$$


Angka-angka ini setara dengan damage pada gambar <a href="#g11">1.11</a>, dengan mempertimbangkan pembulatan dalam game. Satu dapat dengan jelas melihat bahwa mengurangi resistensi yang sesuai sangat memperkuat yang disebabkan oleh swirl-induced damage, itulah mengapa terutama taser comps diterima dengan sangat baik, karena hydro dan elektro tetap ada pada semua musuh pada saat yang sama dan reaksi swirl (4pc VV-set) mengurangi kedua resistensi oleh karena itu, saat memberikan hydro-swirl, electro-swirl, dan electro-charge damage yang diinduksi swirl.

<div id="g9" style="text-align: center;">    
    <img alt="genshin impact" class="lazy full" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiioqXi8mdYXRiptejrfNo7HeEmDQdTKyh04Spao_GwszizGYX1zAfWtVjvsguGaWItuaSDtTkEzkFLDVN3E6DA52Bxyq1otXu-8cFZ4APcxet38xvTJDVCgiLX-U_sT9DfYqmnrLCOAPNeb9WWShDxnhalmIVGyNjAqQsW3xxqywi7VTnTT6FwY0mM/s1600/q.png" />
     <b>a.</b> Statistik Sucrose tanpa bentuk buff apa pun.
  </div>


<div style="display: flex; justify-content: flex-start; gap: 20px; overflow-x: auto; white-space: nowrap;">
    <div style="text-align: center; flex-shrink: 0;">
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiUEAgORDxnqLB13lyKjhaeg2OHRlh8dR7p15M8qe7gCnsKERM6hjOjpYFZezqOkkD-Hlm5KrPPciIgz9rklcYDHwGEaRHLdoJOesBXWbrzqJlcTuB9XztBHHn8502Kz3qoRrB_Mh7-2FrmR9Qb93XyIlfCthWD2XZk9TfjthtFtpe4DFYc-pGsR-qK/s1600/w.png" style="width: 300px; height: auto;" />
        <b>b.</b> Damage akibat swirl (piro): 6 433.
    </div>

<div style="flex-shrink: 0;">
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjzSMnqUoHOueh6CFCQIeHhEJSsZ-lMCC9Gx49BGcbBkV-Ff4AmSTYJjsUptV_dfbarntziJHFlWGhyhwn_f_uPcrL6HMi-ecEb_seF8o5WgDqnlrTc7lnplLlDeMWNOWuznA0HEWMCX-wZ7T-g5QCN2l3__jUjCY4cADpdz9ddnsEaFfXVWozvwZiH/s1600/e.png" style="width: 300px; height: auto;" />
        <b>c.</b> Damage yang disebabkan oleh swirl<br />overload damage<br />pyro-infused enemy: 19.449,<br />electro-infused enemy: 15.221.
    </div>

<div style="text-align: center; flex-shrink: 0;">
        <img alt="genshin impact" class="lazy" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi0klInWKPYOnQ1nHzsqRPLvmZ0n7Sda4BIr6cTCXX7nwYamj7rPQpA0_7ZVBIQw4fEUGHsArMidNAshmeXxUOwUNE0QuCH0nqd6tUsVUMdYsaxjnD_1WbLcrnUc_RQwrv1FFFx3AysJUGcSQ_yjWsxDJ_oFL9y9N-7OEOPsvqTdUvB1M73fDMh65OA/s1600/r.png" style="width: 300px; height: auto;" />
        <b>d.</b> Swirl-induced<br />melt damage: 20 789,<br />reverse-melt damage: 15 592.
    </div>
</div>

<b>Gambar 1.11.:</b> Statistik uji damage Sucrose dan swirl(-induced), tanpa mengurangi resistensi yang sesuai sebelumnya – first swirl reaction –, terhadap Ruin Guards.

## 1.6.3. Albedo

To be continued. . .


## 1.6.4. Ayaka

To be continued. . .


## 1.6.5. Mona

To be continued. . .


## 1.6.6. Shenhe

To be continued. . .


## 1.6.7. Hu Tao

To be continued. . .


## 1.6.8. Dual Carry Team

To be continued. . .


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