Laporan Praktikum Selector, Cascade, dan Box Model
Nama  : Berlita Siburian
Nim   : 41426008
Prodi : DIV Teknologi Rekayasa Perangkat Lunak

//  AI USE STATEMENT //
saya menggunakan AI untuk membantu saya memahami maksud dari modul, untuk mengerti apa saja yang akan dikejakan, saya menggunakannya pada bagian class dan notice

// Link halaman saya //
file:///D:/Semester%201/Pengembangan%20Situs%20Web%201/Week%204/Praktikum/pswi-week-04/indexx.html?nama=lia&email=mahasiwa%40example&telepon=098767876&tiket=2&kode=009878&prodi=ti&mode=luring&Minat=HTML&Aksesibilitas=Aksesibilitas&catatan=goooo#


1. Persiapan Stylesheet
pada persiapan ini saya memgabungkan "<link rel="stylesheet" href="style.css">" week 1 dan week ke 3 pada satu folder week 4 sesi 2.
Jadi dalam program saya ini saya memakai "style.css" dimana sebelumnya saya sudah buat file cssnya, tapi tidak berjalan dengan baik, setelah saya periksa lagi ternyata letak kesalahannya ada pada "index.html" dimana saya tidak membuat "<link rel="stylesheet" href="style.css">". 
jadi saya dapat tarik kesimpulan bahwasannya jika ingin menjalankan fungsi css pada halaman web kita harus menulis link css nya pada index.html dulu

2.  Selector dan Class
jadi pada selector dan class ini saya memakai code yang sudah disediakan di modul yaitu :
"form.card { padding: 1rem; background: white; }
.notice { color: #175cd3; }"
saya memakai code diatas pada "style.css"

awalnya tidak ada perubahan sama sekali, tapi setelah saya baca kembali pada modul terdapat kalimat arahan untuk menambahkan class card pada "form" dan menembahkan class notice pada "paragraf(p)"
menjadi seperti ini
<p class="notice">,  <form action="/get" method="get" class="card">
(Tapi saya hanya melakukna ini pada uji coba, setelahnya saya kembalikan lagi halaman webnya kesemula karna menurut saya tampilannya lebih sederhana dan menarik yang semula)

hasilnya itu <p class="notice"> ini menjadi tulisan dalam paragraf nya berwarna  biru
sedangkan yang ini  <form action="/get" method="get" class="card"> membuat sebuah background lagi dalam sebuah background yang berwarna putih dan kalimat paragrafnya tidak ikut serta

3. Konflik Specificity
jadi pada code ini sudah jelas tertera bahwasannya akan diletakkan pada kelas mana 
".card p { color: purple; }
.notice { color: orange; }"
jadi ini ada dua kelas yang saya tambah pada bagian style.css tapi tidak perlu lagi ke index.html karna hanya menambahin saja. 
hasinya dari code tersebut adalah tulisan pada paragraf berubah menjadi warna orange, dan tulisan pada bacground menjadi ungu.

 Jelaskan mengapa .card p tetap lebih spesifik?
 jadi kelas card p lebih spesifik karna kelas ini langsung menempatkan sebuah elemennya pada P, yang dimana langsung pada pargraf tersebut, berbeda kalau dengan notice, karna itu keselurannya bukan spesifiknya seperti langsung pada <p>

4. ketika validatornya, aku ada mengalami kesalahan dan jadinya error. kesalahan ku itu karna membuat mainnya 2 " <main>", jadi aku menggantinya menjadi cuman satu dan hasilnya halaman webnya jadi gabung, ternyata main itu pemisahnya. 

5. setelah dari  <main> ada juga karna h1 ku dua, h1 sendri untuk judulnya tapi karna aku buatnya h1 ada dua jadinya harus kuganti satunya h2.

6. js ku tadinya tidak berfungsi dengan baik, tidak dapat membuat atau mengaktifkan ketika ditekan dan ternyata letak salahnya karna aku buat dalam sebuah folder "src=js/"main.js", sedangkan seharusnya src="main.js"hanya seperti ini saja.
