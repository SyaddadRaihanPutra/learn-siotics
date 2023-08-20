---
title: "Pembelajaran Variabel, Operator, Kondisional pada Arduino UNO"
description: "Lorem ipsum dolor sit amet"
pubDate: "Aug 15 2023"
heroImage: "/blog-placeholder-3.jpg"
---

<div class="container content">

### ✨ Apa itu Variabel?

Variabel adalah suatu wadah yang digunakan untuk menyimpan nilai atau data dalam program Arduino. Setiap variabel memiliki tipe data yang menentukan jenis data yang dapat disimpan di dalamnya.

---

### 📝 Deklarasi Variabel

Anda dapat mendeklarasikan variabel dengan menentukan tipe datanya, diikuti oleh nama variabel. Contoh:

    int nilaiSensor;
    float suhu;
    nilaiSensor = 100;
    suhu = 36.5;
    kondisiPB = HIGH;

---

### ✨ Apa Itu Operator?

Operator dalam bahasa pemrograman adalah simbol yang memberitahu compiler atau interpreter untuk melakukan operasi matematika

<style>
    .custom {
        border: 1px solid #000;
        
    }
</style>
<table class="custom">

<thead>

<tr>

<td>Operator</td>

<td>Deskripsi</td>

<td>Contoh</td>

</tr>

</thead>

<tbody>

<tr>

<td class="text-center">==</td>

<td>Memeriksa kesamaan nilai</td>

<td>if (nilai == 10)</td>

</tr>

<tr>

<td class="text-center">!=</td>

<td>Memeriksa ketidaksesuaian nilai</td>

<td>if (nilai != 5)</td>

</tr>

<tr>

<td class="text-center"><</td>

<td>Memeriksa nilai kurang dari</td>

<td>if (nilai < 20)</td>

</tr>

<tr>

<td class="text-center">></td>

<td>Memeriksa nilai lebih dari</td>

<td>if (nilai >= 50)</td>

</tr>

<tr>

<td class="text-center"><=</td>

<td>Memeriksa nilai kurang dari atau sama dengan</td>

<td>if (nilai <= 100)</td>

</tr>

<tr>

<td class="text-center">>=</td>

<td>Memeriksa nilai lebih dari atau sama dengan</td>

<td>if (nilai >= 30)</td>

</tr>

<tr>

<td class="text-center">!</td>

<td>Operator NOT logika</td>

<td>if (!kondisi)</td>

</tr>

<tr>

<td class="text-center">&&</td>

<td>Operator AND logika</td>

<td>if (kondisi1 && kondisi2)</td>

</tr>

<tr>

<td class="text-center">||</td>

<td>Operator OR logika</td>

<td>if (kondisi1 || kondisi2)</td>

</tr>

</tbody>

</table>

</div>

---

### ✨ Apa Itu Kondisional?

Kondisional adalah suatu pernyataan yang digunakan untuk mengeksekusi kode tertentu jika kondisi tertentu terpenuhi. Kondisional dapat digunakan untuk memeriksa nilai dari suatu variabel. Contoh:

<pre class="hljs" style="display: block; overflow-x: auto; padding: 0.5em; background: rgb(255, 255, 255); color: rgb(67, 79, 84);"> <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// Deklarasi variable</span>
            <span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> led = <span class="hljs-number" style="color: rgb(138, 123, 82);">13</span>;
            <span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> nilaiSensor = <span class="hljs-number" style="color: rgb(138, 123, 82);">0</span>;

            <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// void setup (hanya dijalankan sekali)</span>
            <span class="hljs-keyword" style="color: rgb(0, 151, 157);">void</span> <span class="hljs-built_in" style="color: rgb(211, 84, 0);">setup</span>() {
              <span class="hljs-built_in" style="color: rgb(211, 84, 0);">pinMode</span>(led, <span class="hljs-literal" style="color: rgb(211, 84, 0);">OUTPUT</span>);
              <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">/* Inisialisasi sensor dan konfigurasi 
                lainnya jika diperlukan */</span>
            }

            <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// function akan dijalankan berulang (looping)</span>
            <span class="hljs-keyword" style="color: rgb(0, 151, 157);">void</span> <span class="hljs-built_in" style="color: rgb(211, 84, 0);">loop</span>() {
              <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// Baca nilai sensor, misalnya:</span>
              <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// nilaiSensor = bacaNilaiSensor();</span> 

              <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// Kondisional</span>
              <span class="hljs-built_in" style="color: rgb(211, 84, 0);">if</span> (nilaiSensor > <span class="hljs-number" style="color: rgb(138, 123, 82);">100</span>) {
                <span class="hljs-built_in" style="color: rgb(211, 84, 0);">digitalWrite</span>(led, <span class="hljs-literal" style="color: rgb(211, 84, 0);">HIGH</span>);
              } <span class="hljs-built_in" style="color: rgb(211, 84, 0);">else</span> {
                <span class="hljs-built_in" style="color: rgb(211, 84, 0);">digitalWrite</span>(led, <span class="hljs-literal" style="color: rgb(211, 84, 0);">LOW</span>);
              }

            }
            </pre>

---

### 📑 Contoh Penggunaan Variabel dan Kondisional

<pre class="hljs" style="
          display: block;
          overflow-x: auto;
          padding: 0.5em;
          background: rgb(255, 255, 255);
          color: rgb(67, 79, 84);
        "> <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// Deklarasi variable led</span>
        <span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> led = <span class="hljs-number" style="color: rgb(138, 123, 82);">13</span>;
        <span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> led2 = <span class="hljs-number" style="color: rgb(138, 123, 82);">12</span>;
        <span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> led3 = <span class="hljs-number" style="color: rgb(138, 123, 82);">11</span>;
        <span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> led4 = <span class="hljs-number" style="color: rgb(138, 123, 82);">10</span>;
        <span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> led5 = <span class="hljs-number" style="color: rgb(138, 123, 82);">9</span>;
        <span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> led6 = <span class="hljs-number" style="color: rgb(138, 123, 82);">8</span>;

        <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// void setup (hanya dijalankan sekali)</span>
        <span class="hljs-keyword" style="color: rgb(0, 151, 157);">void</span> <span class="hljs-built_in" style="color: rgb(211, 84, 0);">setup</span>() {
          <span class="hljs-built_in" style="color: rgb(211, 84, 0);">pinMode</span>(led, <span class="hljs-literal" style="color: rgb(211, 84, 0);">OUTPUT</span>);
          <span class="hljs-built_in" style="color: rgb(211, 84, 0);">pinMode</span>(led2, <span class="hljs-literal" style="color: rgb(211, 84, 0);">OUTPUT</span>);
          <span class="hljs-built_in" style="color: rgb(211, 84, 0);">pinMode</span>(led3, <span class="hljs-literal" style="color: rgb(211, 84, 0);">OUTPUT</span>);
          <span class="hljs-built_in" style="color: rgb(211, 84, 0);">pinMode</span>(led4, <span class="hljs-literal" style="color: rgb(211, 84, 0);">OUTPUT</span>);
          <span class="hljs-built_in" style="color: rgb(211, 84, 0);">pinMode</span>(led5, <span class="hljs-literal" style="color: rgb(211, 84, 0);">OUTPUT</span>);
          <span class="hljs-built_in" style="color: rgb(211, 84, 0);">pinMode</span>(led6, <span class="hljs-literal" style="color: rgb(211, 84, 0);">OUTPUT</span>);
        }

        <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">/* Custom function lowhigh() x,y,t akan digantikan 
        dengan parameter yang diberikan pada void loop()*/</span>
        <span class="hljs-keyword" style="color: rgb(0, 151, 157);">void</span> lowhigh(<span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> x, <span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> y, <span class="hljs-keyword" style="color: rgb(0, 151, 157);">int</span> t){
          <span class="hljs-built_in" style="color: rgb(211, 84, 0);">digitalWrite</span>(x, <span class="hljs-literal" style="color: rgb(211, 84, 0);">HIGH</span>);
          <span class="hljs-built_in" style="color: rgb(211, 84, 0);">digitalWrite</span>(y, <span class="hljs-literal" style="color: rgb(211, 84, 0);">LOW</span>);	
          <span class="hljs-built_in" style="color: rgb(211, 84, 0);">delay</span>(t);  
        }

        <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// function akan dijalankan berulang (looping)</span>
        <span class="hljs-keyword" style="color: rgb(0, 151, 157);">void</span> <span class="hljs-built_in" style="color: rgb(211, 84, 0);">loop</span>() {
          <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// LED bergerak maju</span>
          lowhigh(led, led2, <span class="hljs-number" style="color: rgb(138, 123, 82);">250</span>);
          lowhigh(led2, led3, <span class="hljs-number" style="color: rgb(138, 123, 82);">250</span>);
          lowhigh(led3, led4, <span class="hljs-number" style="color: rgb(138, 123, 82);">250</span>);
          lowhigh(led4, led5, <span class="hljs-number" style="color: rgb(138, 123, 82);">250</span>);
          lowhigh(led5, led6, <span class="hljs-number" style="color: rgb(138, 123, 82);">250</span>);

          <span class="hljs-comment" style="color: rgba(149, 165, 166, 0.8);">// LED bergerak mundur</span>
          lowhigh(led6, led5, <span class="hljs-number" style="color: rgb(138, 123, 82);">250</span>);
          lowhigh(led5, led4, <span class="hljs-number" style="color: rgb(138, 123, 82);">250</span>);
          lowhigh(led4, led3, <span class="hljs-number" style="color: rgb(138, 123, 82);">250</span>);
          lowhigh(led3, led2, <span class="hljs-number" style="color: rgb(138, 123, 82);">250</span>);
          lowhigh(led2, led, <span class="hljs-number" style="color: rgb(138, 123, 82);">250</span>);
        }
        </pre>

---

### 🚧 Ayo Praktik!

<iframe class="rounded-3" width="100%" height="720" src="https://www.tinkercad.com/embed/f35GXHyr2NI?editbtn=1" frameborder="0" marginwidth="0" marginheight="0" scrolling="no"></iframe>

<footer class="text-center my-3"><span>© 2023 | SIOTICS

<small>Divisi Perangkat Lunak</small>

</span></footer>

</div>
