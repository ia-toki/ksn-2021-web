---
layout: single-page-md
title: Peraturan KSN 2021 Bidang Informatika
key: rules
---

<div class="alert alert-primary" role="alert">
   <span class="pt-icon-standard pt-icon-info-sign sidebar-icon"></span>
   Pastikan untuk membaca juga <a href="/peraturan-daring.html">Peraturan Kompetisi Daring</a>.
</div>

Perbedaan dengan [Peraturan KSN Informatika 2020](https://ksn2020.toki.id/peraturan.html) ditandai <span style="color:red">warna merah</span>.

### A. Teknis Umum

1. KSN 2021 Bidang Informatika terdiri atas **1 hari uji coba** dan **2 hari kompetisi**.
2. Hasil pada hari uji coba **tidak** termasuk dalam penilaian.
3. Pada setiap hari kompetisi, terdapat **3 buah soal** yang diujikan selama **5 jam**.
4. Setiap peserta mendapatkan jatah sebanyak **50 kali pengumpulan** untuk setiap soal.
  <span style="color:red">Jatah ini bisa saja ditambahkan untuk beberapa soal tertentu</span>.
5. Bahasa pemrograman yang diperbolehkan adalah <span style="color:red">**C** dan **C++**</span>.
6. Selama kompetisi, peserta hanya dapat melihat nilainya sendiri.

<br>

### B. Tipe Soal

1. Terdapat **3 tipe soal** yang mungkin diujikan: **batch**, **interactive**, dan **output-only**. Mungkin saja terdapat tipe soal yang tidak diujikan.

2. Pada soal bertipe *batch*:
   1. Peserta membuat sebuah program yang membaca masukan kasus uji dari **stdin** dan mencetak jawaban ke **stdout**.
   2. Program harus mengeluarkan jawaban dalam batas waktu dan memori yang dinyatakan pada soal.
   3. Contoh soal: [Online Ojek, OSN 2018](https://tlx.toki.id/problems/osn-2018/1C).

3. Pada soal bertipe *interactive*:
   1. Peserta membuat sebuah program yang berinteraksi dengan program juri: program juri memberikan keluaran ke **stdout**, yang menjadi masukan **stdin** untuk program peserta, kemudian program peserta memberikan keluaran ke **stdout**, dan seterusnya, untuk mencapai tujuan tertentu yang dinyatakan pada soal.
   2. Program harus mengeluarkan jawaban dalam batas waktu dan memori yang dinyatakan pada soal.
   3. Contoh soal: [Detecting Gold, OSN 2019](https://tlx.toki.id/problems/osn-2019/2B).

4. Pada soal bertipe *output-only*:
   1. Peserta diberikan seluruh masukan dari kasus-kasus uji soal.
   2. Peserta menjawab dengan mengirimkan beberapa **berkas keluaran** yang sudah dikompres.
   3. Peserta **tidak harus** membuat program untuk menghasilkan berkas-berkas keluaran (boleh dikerjakan secara manual).
   4. Contoh soal: [OSN Excursion, OSN 2019](https://tlx.toki.id/problems/osn-2019/1C).

<br>

### C. Penilaian Soal

1. Terdapat **2 jenis penilaian**: **standar** dan **kreatif**. Soal dengan penilaian kreatif akan dinyatakan secara eksplisit pada soal.

1. Pada penilaian standar:
   1. Untuk soal bertipe *batch* dan *interactive*:
      1. Setiap soal terdiri atas **beberapa subsoal** dengan bobot nilai yang bervariasi.
      1. Setiap soal terdiri atas **beberapa kasus uji** yang dikelompokkan ke dalam **beberapa test group**.
      1. Setiap *test group* termasuk ke dalam satu atau lebih subsoal.
      1. Untuk mendapatkan nilai pada suatu subsoal, peserta harus menyelesaikan **seluruh test group** yang termasuk pada subsoal yang bersangkutan, _kecuali_ dinyatakan lain pada soal.
      1. Untuk menyelesaikan sebuah *test group*, peserta harus menyelesaikan **seluruh kasus uji** pada *test group* yang bersangkutan.
      1. Setiap soal mungkin memiliki beberapa **subsoal terbuka** yang isi kasus-kasus ujinya diberikan kepada peserta, sehingga memungkinkan dikerjakan secara manual.

   1. Untuk soal bertipe *output-only*:
      1. Setiap soal terdiri atas **beberapa kasus uji** dengan bobot nilai yang bervariasi.
      1. Untuk mendapatkan nilai pada suatu kasus uji, peserta harus menyelesaikan kasus uji tersebut.

1. Pada penilaian kreatif:
   1. Penilaian akan diberikan relatif terhadap hasil yang diperoleh solusi juri.
   1. Rumus penilaian bervariasi untuk setiap soal, dan akan dinyatakan secara eksplisit pada soal.

   1. Contoh soal:
      - *Batch*: [Membaca, OSN 2012](https://tlx.toki.id/problems/osn-2012/2D).
      - *Interactive*: [Mencari Bola, KSN 2020](https://tlx.toki.id/problems/ksn-2020/2C).
      - *Output-only*: [Pertahanan Negara, KSN 2020](https://tlx.toki.id/problems/ksn-2020/1A).

<br>

### D. Penilaian Peserta

1. Pada soal bertipe *batch* dan *interactive*:
   1. Pada penilaian kreatif, untuk setiap pengumpulan, nilai pada suatu subsoal adalah nilai minimum di antara seluruh kasus uji yang dicakup pada subsoal tersebut.
   1. Nilai akhir pada suatu subsoal adalah **nilai maksimum** subsoal tersebut di antara seluruh pengumpulan.
   1. Nilai peserta pada suatu soal merupakan jumlah nilai akhir seluruh subsoalnya.

   Sebagai contoh, jika pengumpulan pertama mendapatkan nilai 30 pada subsoal pertama dan nilai 0 pada subsoal kedua, dan pengumpulan kedua mendapatkan nilai 0 pada subsoal pertama dan nilai 40 pada subsoal kedua, maka nilai peserta pada soal ini adalah 70.
1. Pada soal bertipe *output-only*:
   1. Nilai akhir pada suatu kasus uji adalah **nilai maksimum** kasus uji tersebut di antara seluruh pengumpulan.
   1. Nilai peserta pada suatu soal merupakan jumlah nilai akhir seluruh kasus ujinya.
1. Total nilai peserta adalah total nilai yang didapatkan pada **seluruh soal** pada **seluruh hari kompetisi**.
1. Peserta akan diurutkan peringkat berdasarkan total nilai (semakin besar, semakin bagus).
1. Dua peserta yang memiliki total nilai yang **sama** akan mendapat peringkat yang **sama**.
1. Waktu pengumpulan **tidak berpengaruh** sama-sekali pada peringkat peserta.

<br>

### E. Sistem Grading

1. Sistem *grading* yang digunakan adalah [TLX](https://tlx.toki.id).
1. Besarnya berkas *source code* yang boleh dikumpulkan untuk setiap soal maksimum **300 KB**.

1. Untuk setiap kasus uji, balasan *grader* yang mungkin adalah:
   1. **AC** (Accepted): program berhasil menyelesaikan kasus uji dalam batas waktu dan memori.
   1. **WA** (Wrong Answer): program berhenti dalam batas waktu dan memori, namun menghasilkan keluaran yang salah.
   1. **RTE** (Runtime Error): program *crash* atas melebihi batas memori.
   1. **TLE** (Time Limit Exceeded): program melebihi batas waktu.
   1. Skipped: *grading* tidak dilakukan karena sudah ada kasus uji lain dalam *test group* yang sama yang tidak mendapatkan AC.

<br>

### F. Klarifikasi

1. Peserta dapat mengajukan klarifikasi selama kompetisi berlangsung.
1. Setiap klarifikasi yang berhubungan dengan soal hanya akan dijawab dengan salah satu dari balasan berikut:
   - "Ya"
   - "Tidak"
   - "Jawaban terdapat pada deskripsi soal" <br>
     Deskripsi soal telah mengandung informasi yang cukup. Peserta diimbau untuk membaca ulang soal dengan lebih teliti.
   - "Pertanyaan tidak valid" <br>
     Pertanyaan tidak bisa dijawab dengan jawaban Ya/Tidak. Peserta disarankan untuk mengulangi pertanyaannya.
   - "Tidak ada komentar" <br>
     Peserta menanyakan informasi yang tidak bisa diberikan jawabannya.
1. Jawaban dari klarifikasi bisa saja mempunyai informasi tambahan jika sekiranya diperlukan.

<br>

Peraturan pelaksanaan kompetisi secara daring lebih didetailkan di bagian <a href="/peraturan-daring.html">Peraturan Kompetisi Daring</a>.
