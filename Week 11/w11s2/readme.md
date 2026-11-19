Laporan JSON Lokal, Promise, dan Fetch

Nama  : Berlita Siburian
Nim   : 41426008
Prodi : DIV Teknologi Rekayasa Perangkat Lunak

AI USE STATEMENT
saya menggunakan AI sebagai alat bantu untuk memahami materi dan untuk mengidentifikasi kemungkinan kesalahan pada kode, serta memberikan saran perbaikan dan ide pengujian. Saya menggunakan bantuan tersebut untuk memahami cara kerja kode dan melanjutkan proyek dari praktikum sebelumnya

defer; untuk menunda sebuah eksekusi pernyataan, dimana js gak bisa dijalankan sebulum selesai.
supaya js nya ditunda dulu sebelum index htmlnya selesai di eksekusi 

GET membaca resource.
POST umumnya meminta pemrosesan atau penambahan data.
PUT/PATCH dan
DELETE terkait perubahan sesuai rancangan API.

JSON adalah format teks pertukaran data. Properti string memakai tanda kutip ganda. response.json mem-parsing badan respons dan juga menghasilkan Promise

Asynchronous (Async) di JavaScript adalah cara menjalankan suatu proses tanpa harus membuat program menunggu proses tersebut selesai untuk mengerjakan hal lainnya.

Asynchronous berguna untuk:
- Mengambil data dari server tanpa membuat halaman berhenti.
- Menunggu hasil dari API.
- Membaca file.
- Menjalankan proses yang membutuhkan waktu.
- Membuat website tetap bisa digunakan sambil menunggu proses selesai.

Try Catch Error adalah cara JavaScript mencoba menjalankan perintah dan menangani kesalahan jika terjadi masalah.

Kalau diterjemahkan satu per satu:
- Try = Coba atau mencoba.
- Catch = Tangkap atau menangkap.
- Error = Kesalahan.
(untuk mencegah crash, atau berhenti tiba tiba, melainkan memberi sebuah solusi)

fetch untuk mengambil data dari suatu alamat url
await untuk menunggu sebuah data.


await fetch() berarti JavaScript meminta data dari server dan menunggu sampai respons diterima sebelum melanjutkan ke baris berikutnya dalam fungsi async, ataupun untuk menunggu suatu proses asynchronous selesai sebelum melanjutkan ke perintah berikutnya di dalam fungsi tersebut.
harus ada waktu tunggu, contohnya saat mengambil data dari server
jadiii
const r = await fetch("./data/kegiatan.json");
adalah r nya sebagai data
if itu untuk memeriksa codenya, apakah benar atau tidak

(networ. tools)

Array.isArray(data) yaitu untum melihat jika datanya tidak dalam bentu array
agar data yang sebelunya disingkirkan dulu agar datanya ga terhapus ketika dibuat data yang baru dan agar tidak kepenuuhan

if (typeof k.judul !== "string")
Fungsinya adalah untuk memastikan bahwa judul kegiatan yang ada di dalam data harus berbentuk teks (String).

 document.createElement, artinya membuat elemen HTML baru menggunakan javascrip, dari const data 5 yang sudah berisi data, 

 jadi consol.log dan consol data itu setara posissinya karna dipisahkan oleh titik koma
 jadii:
- Posisi penulisan: setara (sama-sama berada di luar blok).
- Fungsi: berbeda (ada yang menyimpan data, ada yang menampilkan data).

catch(error) tidak perlu didefinisikan terlebih dahulu. Karena JavaScript sudah otomatis menyediakan variabel untuk menampung kesalahan ketika catch dijalankan. jadi catch itu juga adalah fungsi

Hasil Pengujian
No.| Pengujian                                | Hasil yang Diharapkan   	   | Hasil Pengamatan
1  | Menampilkan daftar peserta awal          | Nama peserta ditampilkan.      | Nama Rina dan Budi berhasil ditampilkan.
2  | Menambahkan peserta melalui formulir     |Peserta baru masuk ke daftar.   | Peserta berhasil ditambahkan melalui formulir.
3  | Mengisi nama menggunakan spasi saja      |Input ditolak.                  | Program menampilkan pesan "Nama harus diisi".
4  | Menekan tombol Hapus	                  |Peserta yang dipilih terhapus.  | Peserta berhasil dihapus dari daftar.
5  | Memperbarui tampilan setelah penghapusan |Daftar menampilkan data terbaru.|	Tampilan diperbarui melalui fungsi render().

1. Uji coba membuka file JSON
Pengujian ini dilakukan untuk memastikan file kegiatan.json sudah dibuat dengan benar dan bisa dibuka melalui browser. Setelah alamat file dibuka, muncul dua data kegiatan, yaitu HTML dengan kuota 20 dan CSS dengan kuota 0. Hal ini terjadi karena file JSON sudah tersimpan di folder yang benar sehingga dapat ditemukan dan dibaca oleh server.

2. Uji coba Fetch
Pengujian ini dilakukan untuk memastikan JavaScript dapat mengambil data dari file JSON menggunakan Fetch. Setelah tombol Muat kegiatan diklik, data HTML dan CSS berhasil diambil dan muncul di Console. Hal ini terjadi karena Fetch meminta data dari file JSON, kemudian await menunggu proses selesai dan r.json() mengubah data agar bisa dibaca oleh JavaScript.

3. Uji coba mengganti alamat menjadi hilang.json (404)
Pengujian ini dilakukan untuk mengetahui apa yang terjadi jika file yang diminta tidak ditemukan. Setelah alamat kegiatan.json diganti menjadi hilang.json, muncul kesalahan HTTP 404 karena file tersebut tidak tersedia di dalam folder. Hal ini terjadi karena server tidak menemukan file yang diminta sehingga program menangkap kesalahan tersebut melalui catch.


4. Uji coba data kosong
Pengujian ini dilakukan untuk mengetahui apa yang terjadi jika file JSON tidak memiliki isi data. Setelah isi JSON dihapus dan diganti dengan [], program menerima data kosong dan tidak menampilkan kegiatan apa pun.

5. Uji coba judul dengan markup HTML
Pengujian ini dilakukan untuk memastikan teks yang berisi kode HTML tidak dijalankan sebagai elemen HTML. Setelah judul diisi dengan markup seperti <p>HTML</p>, tulisan tersebut muncul sebagai teks biasa pada halaman website. Hal ini terjadi karena program menggunakan textContent untuk memasukkan teks tanpa menjalankannya sebagai kode HTML.