Laporan Praktikum CSS Grid dan Class yang Dapat Dipakai Ulang

Nama  : Berlita Siburian
Nim   : 41426008
Prodi : DIV Teknologi Rekayasa Perangkat Lunak

Branch, Merge, dan Code Review adalah istilah penting dalam pengembangan perangkat lunak (software development) yang menggunakan sistem kontrol versi seperti Git.

1. Branch (Percabang)
• Pengertian: Salinan atau "cabang" terpisah dari kode utama (main atau master).
• Fungsi: Memungkinkan developer menulis kode, memperbaiki bug, atau membuat fitur baru tanpa mengganggu atau merusak kode utama yang sedang berjalan.
• Analogi: Seperti membuat draft atau fotokopi dokumen asli agar Anda bisa mencorat-coret dan bereksperimen tanpa merusak dokumen aslinya.

2. Merge (Penggabungan)
• Pengertian: Proses menyatukan kembali perubahan dari satu branch ke branch utama (atau branch lain).
• Fungsi: Memasukkan fitur atau perbaikan yang sudah selesai dikerjakan di branch terpisah agar resmi menjadi bagian dari aplikasi utama.
• Cara kerja: Biasanya didahului dengan Pull Request (permintaan izin untuk menggabungkan kode).

3. Code Review (Tinjauan Kode)
• Pengertian: Proses di mana kode yang Anda tulis diperiksa dan dibaca oleh rekan developer lain (misalnya senior atau tim) sebelum digabungkan.
• Fungsi:
	• Menemukan bug atau kesalahan logika lebih awal.
	• Memastikan kode sesuai dengan standar tim (best practices).
	• Menjaga keamanan dan performa aplikasi.
	• Menjadi sarana belajar bersama antar anggota tim.

Perintah Git	                  |Pengertian dan fungsi
git init	                      |Membuat repository Git baru di folder yang sedang digunakan jika belum menjadi repository.
git status	                      |Memeriksa kondisi file, seperti perubahan yang belum di-commit dan branch yang sedang aktif.
git branch	                      |Menampilkan daftar branch lokal yang tersedia.
git switch -c                     |fitur-petunjuk	Membuat branch baru bernama fitur-petunjuk sekaligus berpindah ke branch tersebut.
git diff	                      |Menampilkan perbedaan perubahan isi file sebelum perubahan disimpan sebagai commit.
git diff main...fitur-petunjuk	  |Membandingkan perubahan branch fitur-petunjuk dengan titik awal bersama branch main.
git add .	                      |Memasukkan perubahan file di folder saat ini dan subfoldernya ke staging area untuk dipersiapkan menjadi commit.
git commit -m "pesan"	          |Menyimpan perubahan yang sudah masuk staging area sebagai sebuah commit.
git switch main	                  |Berpindah ke branch main yang sudah ada.
git merge fitur-petunjuk	      |Menggabungkan perubahan dari branch fitur-petunjuk ke branch yang sedang aktif.
git log --oneline --max-count=5	  |Menampilkan maksimal lima riwayat commit terakhir dengan tampilan satu baris per commit.
git rm --cached -f	              |Mengeluarkan file atau entri dari indeks Git tanpa menghapus file kerja biasa; -f memaksa pengeluaran jika diperlukan. Pemakaiannya harus hati-hati, terutama pada submodule.
git push	                      |Mengirim commit lokal ke repository jarak jauh, misalnya GitHub.
git reset --hard	              |Memindahkan posisi HEAD dan membuang perubahan pada file yang dilacak sesuai target reset. Berbahaya karena perubahan yang belum disimpan dapat hilang.

aku bingung tentang perbedaan dari git branch dan git switch
git branch	                                                  |git switch
Melihat atau mengelola daftar branch	                      |Berpindah ke branch lain.
Tidak berpindah branch jika hanya dijalankan tanpa argumen	  |Mengubah branch aktif.

card internaal dan gap
ketika aku menambahakan
.card { display: flex; flex-direction: column; gap: .5rem; } 
hasilnya ada jarak antara h2 dengan p karna gap kan artinya jarak
.card h2, .card p { margin: 0; }
membuat sebuah paragraf dalam sebuah kartu, kalau card.a nya disatukan  buat semua jadinya dia nyatu ga ada bedanya antara kaliamt "kegiatan", "kontak"

Teks di tengah	                                        |text-align: center;
Area main di tengah halaman                         	| margin-inline: auto;
Elemen di tengah secara horizontal dengan Flexbox   	| justify-content: center;
Elemen di tengah secara vertikal dengan Flexbox     	|align-items: center;
Elemen di tengah horizontal dan vertikal dengan Grid	|place-items: center;

Tujuan dari pembelajaran
Membuat beberapa halaman HTML dan menghubungkannya dengan navigasi.
Menggunakan elemen HTML semantik seperti header, nav, main, section, article, address, dan footer.
Mengatur tampilan halaman dengan CSS, termasuk Grid dan Flexbox.
Membuat formulir dengan label dan validasi dasar HTML.
Menambahkan interaksi sederhana menggunakan JavaScript.
Memeriksa tampilan halaman dan memperbaiki kesalahan saat proses pengerjaan.

Informasi Halaman Website
- Tentang (index.html): menampilkan profil singkat, tujuan pembelajaran, informasi kontak, dan jam layanan.
- Kegiatan (kegiatan.html): menampilkan kartu kegiatan dan tabel jadwal kegiatan.
- Daftar/Kontak (daftar.html): menampilkan gambar gedung dan formulir yang berisi nama, email, nomor telepon, jumlah tiket, kode peserta, program studi, mode kehadiran, minat topik, dan catatan.

fitur yang saya gunakan 
- Navigasi antarhalaman Tentang, Kegiatan, dan Daftar.
- Kartu kegiatan dengan gambar.
- Tabel jadwal kegiatan.
- Formulir dengan atribut validasi bawaan HTML, seperti required, min, max, dan pattern.
- Tombol Tampilkan salam yang menampilkan pesan melalui JavaScript.
- Tampilan yang diatur menggunakan CSS, termasuk Grid, Flexbox, dan media query

Membuat container
mengganti dari class cards ke catalog (.catalog), kemudia saya juga mengganti kelas pada index.html dan menghapus flex pada containernya.
yang dimana hasilnya membuat satu ruang kosong untuk sata kolom lagi.

Grid adaptif
menambahkan beberapa elemen pada class catalog, dan menambahkan repeat 
" repeat(auto-fit, minmax(min(100%, 15rem), 1fr)); " dan hasilnya ada tambah satu kolom 

Branch, Merge, dan Code Review adalah istilah penting dalam pengembangan perangkat lunak (software development) yang menggunakan sistem kontrol versi seperti Git.

1. Branch (Percabang)
• Pengertian: Salinan atau "cabang" terpisah dari kode utama (main atau master).
• Fungsi: Memungkinkan developer menulis kode, memperbaiki bug, atau membuat fitur baru tanpa mengganggu atau merusak kode utama yang sedang berjalan.
• Analogi: Seperti membuat draft atau fotokopi dokumen asli agar Anda bisa mencorat-coret dan bereksperimen tanpa merusak dokumen aslinya.

2. Merge (Penggabungan)
• Pengertian: Proses menyatukan kembali perubahan dari satu branch ke branch utama (atau branch lain).
• Fungsi: Memasukkan fitur atau perbaikan yang sudah selesai dikerjakan di branch terpisah agar resmi menjadi bagian dari aplikasi utama.
• Cara kerja: Biasanya didahului dengan Pull Request (permintaan izin untuk menggabungkan kode).

3. Code Review (Tinjauan Kode)
• Pengertian: Proses di mana kode yang Anda tulis diperiksa dan dibaca oleh rekan developer lain (misalnya senior atau tim) sebelum digabungkan.
• Fungsi:
	• Menemukan bug atau kesalahan logika lebih awal.
	• Memastikan kode sesuai dengan standar tim (best practices).
	• Menjaga keamanan dan performa aplikasi.
	• Menjadi sarana belajar bersama antar anggota tim.

card internaal dan gap
ketika aku menambahakan
.card { display: flex; flex-direction: column; gap: .5rem; } 
hasilnya ada jarak antara h2 dengan p karna gap kan artinya jarak
.card h2, .card p { margin: 0; }
membuat sebuah paragraf dalam sebuah kartu, kalau card.a nya disatukan  buat semua jadinya dia nyatu ga ada bedanya antara kaliamt "kegiatan", "kontak"

Kasus         |Harapan 
320px         |Tidak overflow
Satu card     |Card tetap terbaca 
Lima card     |Auto-placement benar Urutan Tab    |Sama dengan alur DOM

Latihan Mandiri Terarah
1. Mengulangi contoh terarah
Saya mengulangi pembuatan halaman HTML secara mandiri tapi karna saya agak kesusahan dalam pembuatannya saya jadi melihat pekerjaan teman. Saya membuat halaman Tentang, Kegiatan, dan Kontak dengan menggunakan tag HTML semantik seperti header, nav, main, section, article, address, dan footer.

2. Menambahkan data panjang, kosong, atau invalid
Saya mencoba memeriksa beberapa kondisi pada kode HTML, seperti teks yang panjang, gambar yang tidak ditemukan, dan kesalahan penulisan tag. Saya juga memeriksa tautan navigasi dan alamat email untuk memastikan penggunaannya sesuai.

3. Menuliskan prediksi sebelum eksperimen
Sebelum menjalankan halaman di browser, saya memperkirakan bahwa halaman akan menampilkan judul, menu navigasi, gambar, tabel kegiatan, dan informasi kontak. Saya juga memperkirakan bahwa gambar tidak akan muncul jika nama atau lokasi file salah.

4. Memperbaiki hasil gagal dan melakukan pengujian ulang
Setelah menjalankan halaman di browser, saya memeriksa hasilnya dan memperbaiki kesalahan yang ditemukan. Contohnya, saya memperbaiki penulisan atribut tabel dan tag HTML yang tidak sesuai. Setelah itu, saya menjalankan kembali halaman untuk memastikan perbaikannya berhasil.

5. Meminta teman memeriksa alasan teknis
Saya meminta teman untuk memeriksa salah satu alasan teknis dalam kode, yaitu penggunaan tag HTML semantik. Pemeriksaan ini bertujuan untuk memastikan bahwa setiap tag digunakan sesuai fungsinya, bukan hanya agar tampilan halaman terlihat bagus.

Berdasarkan hasil eksperimen yang sudah saya lakukan ketika saya mengubah salah satu id section (<section id="kegiatan">) kalimat kegiatan tersebut tidak bisa berfungsi dengan benar, seperti sebelumnya sebelum diubah.
Pada tangkapan layar validator sesudah dan sebelum, sebenarnya code saya tidak ada yang salah tapi saya ingin melihat apa yang terjadi ketika ada salah satu yang error, makanya saya menambahkan "r" pada kata(<header>), dan ternyata hasil uji coba saya itu, ketika saya menambahkan huruf "r" terjadi error disertakan tempat erorrnya berada dimana