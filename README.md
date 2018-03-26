#	Kendali-via-Telegram

Kendali adalah Alat Administrasi Jarak Jauh khusus target Windows dan dikendalikan melalui Telegram (Python 2.7) untuk Python 3+ belum

###	Kenapa yang lain?

-	Alat Administrasi Jarak Jauh saat ini di pasar menghadapi 2 masalah utama:

	-	Kurangnya enkripsi.
	-	Memerlukan penerusan port untuk mengontrol dari ratusan mil.

-	Kendali ini mengatasi kedua masalah ini dengan menggunakan API bot Telegram.

	-	Sepenuhnya dienkripsi. Data yang dipertukarkan tidak dapat dimata-matai menggunakan alat MITM.
	-	Aplikasi messenger Telegram menyediakan cara sederhana untuk berkomunikasi dengan target tanpa mengkonfigurasi port maju sebelum tangan pada target.

##	Fitur:
-	Keylogger dengan log judul windows disertakan
-	Dapatkan versi PC Windows target, prosesor dan banyak lagi
-	Dapatkan informasi alamat IP PC target dan perkiraan lokasi di peta
-	Hapus, Pindahkan file
-	Tampilkan direktori saat ini
-	Ubah direktori saat ini
-	Daftar direktori saat ini atau yang ditentukan
-	Download file apa pun dari target
-	Upload file lokal ke target. Kirim gambar Anda, pdf, exe atau apapun fileke bot Telegram
-	Mulai otomatis memainkan video dalam layar penuh dan tidak ada kontrol untuk video youtube pada target
-	Ambil Screeshot/Tangkapan Layar
-	Jalankan file apa pun
-	Akses ke mikrofon
-	Mulai HTTP Proxy Server
-	Bekukan/freeze keyboard target
-	Bikin Jadwal tugas untuk dijalankan pada waktu yang ditentukan
-	Encode / Decode semua file lokal
-	Ping ke Target
-	Perbarui .exe
-	Perintah untuk menghancurkan Kendali/penghancuran diri terhadap Kendali untuk menghindari pendeteksian.
-	Ubah wallpaper dari file atau url
-	Jalankan python 2.7 di mana saja
-	Jalankan cmd shell
-	Pemanggilan login / kata sandi Chrome
-	Tampilkan tabel ARP
-	Dapatkan proses dan layanan aktif
-	Komputer Shutdown / Reboot
-	Tampilkan Cache DNS
-	[SEDANG BERLANGSUNG] Browser (IE, Firefox, ~~Chrome~~) pengambilan cookie
-	[SEDANG BERLANGSUNG] Pengambilan kata sandi
-	[SEDANG BERLANGSUNG] Pantau lalu lintas web (secara grafis?)
-	[SEDANG BERLANGSUNG] Skrip fine-tuning (yaitu: jika aplikasi x dibuka y dieksekusi)
-	[SEDANG BERLANGSUNG] Bekukan/Freeze mouse target
-	[SEDANG BERLANGSUNG] Capture clipboard (Teks, Gambar)
-	[SEDANG BERLANGSUNG] Sembunyikan ikon desktop
-	[SEDANG BERLANGSUNG] Ambil foto dari webcam (jika terpasang)
-	[SEDANG BERLANGSUNG] Kompresi audio

& Selebihnya datang segera!

##	Tangkapan layar:

<img src="http://i.imgur.com/I5nzrbz.jpg"/>

##	Instalasi & Penggunaan:
-	Klon repositori ini.
-	Buka Telegram anda, bisa melalui Smarphone atau Desktop 
-	Buat BOT Telegram dengan mengunjungi `BotFather`.
-	Salin token yang didapat dan gantilah di awal skrip.
-	Menginstal dependensi: `pip install -r requirements.txt`.
-	Instal `pyHook` 64-bit atau 32-bit tergantung pada sistem Anda.
-	Untuk 64-bit- `pip install pyHook-1.5.1-cp27-cp27m-win_amd64.whl`.
-	Untuk 32-bit- `pip install pyHook-1.5.1-cp27-cp27m-win32.whl`.
-	Jalankan script: `python RATAttack.py`.
-	Buka bot Anda di telegram dan kirim beberapa perintah ke bot untuk mengujinya.
-	Untuk membatasi bot sehingga hanya merespons Anda, catat `chat_id` dari konsol Anda dan ganti dalam skrip dan komentari pada baris `return True`. Jangan khawatir, Anda akan tahu kapan Anda membaca komentar di skrip.
<img src="http://i.imgur.com/XKARtrp.png">

- Folder bernama `RATAttack` akan dibuat di direktori kerja Anda yang berisi `keylogs.txt` dan file apa pun yang Anda upload ke bot.

###	Perintah:
Saat menggunakan perintah di bawah ini; gunakan (Slash) "/" sebagai awalan. Sebagai contoh: /pc_info.

```
/arp 			- menampilkan tabel arp
/capture_pc 		- tangkapan layar PC
/cmd_exec 		- jalankan perintah shell
/cp 			- menyalin file
/cd 			- ubah direktori saat ini
/delete 		- hapus file / folder
/download 		- unduh file dari target
/decode_all 		- decode SEMUA file lokal yang dikodekan
/dns 			- menampilkan Cache DNS
/encode_all 		- menyandikan SEMUA file lokal
/freeze_keyboard 	- aktifkan pembekuan keyboard
/unfreeze_keyboard 	- menonaktifkan pembekuan keyboard
/get_chrome 		- Dapatkan login / kata sandi Google Chrome
/listen 		- rekam mikrofon
/ip_info 		- via ipinfo.io
/keylogs 		- dapatkan keylogs
/ls 			- daftar isi direktori saat ini atau yang ditentukan
/msg_box 		- menampilkan kotak pesan dengan teks
/mv 			- memindahkan file
/pc_info 		- Informasi PC
/ping 			- pastikan target sudah habis
/play 			- memainkan video youtube
/proxy 			- membuka server proxy
/pwd 			- tampilkan direktori saat ini
/python_exec 		- menafsirkan python
/reboot 		- reboot komputer
/run 			- jalankan file
/schedule 		- jadwalkan perintah untuk dijalankan pada waktu tertentu
/self_destruct 		- hancurkan semua jejak
/shutdown 		- komputer shutdown
/task list 		- menampilkan layanan dan proses yang sedang berjalan
/to 			- pilih target dengan nama itu
/update 		- perbarui dieksekusi
/wallpaper 		- ubah wallpaper
```
Anda dapat menyalin di atas untuk memperbarui daftar perintah Anda melalui `BotFather` sehingga Anda tidak perlu mengetiknya secara manual.

##	Kompilasi:
###	Cara Mengompilasi:
####	Antara:
Ganti path Anda di `compile.bat` dan `Run.bat` (menjalankan ini benar-benar akan menjalankan eksekusi)
####	Atau:
-	Jalankan `pyinstaller --onefile --noconsole C:\path\to\RATAttack.py`. 
-	Anda juga bisa menambahkan `--icon=<path\to\icon.ico>` untuk menggunakan ikon kustom apa pun.

	Setelah berhasil dikompilasi, cari file .exe di dalam C:\Python27\Scripts\dist\.
	Anda dapat mengubah nama dari .exe apa pun yang Anda inginkan.
	AWAS! Jika Anda menjalankan compiled .exe, script akan menyembunyikan dirinya dan menginfeksi PC Anda untuk dijalankan saat startup. Anda dapat kembali ke normal dengan menggunakan /self_destructopsi atau secara manual menghapus C:\Users\Username\AppData\Roaming\Portaldirektori dan C:\Users\Username\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\portal.lnk(meskipun saya merekomendasikan untuk menghapusnya secara manual untuk sementara waktu).

###	Memodifikasi Pengaturan:
-	Anda juga dapat memodifikasi nama .exefile tersembunyi dan lokasi & nama folder tempat tersembunyi .exeakan menyembunyikan dirinya. Untuk melakukan ini; memodifikasi compiled_namedan hide_foldermasing - masing.
-	Tetapkan id obrolan Anda yang dikenal ke awal RATAttack.py

##	Catatan:
Saat ini hanya Python2 yang didukung. Dukungan Python3 akan ditambahkan segera!

##	Penolakan:
Alat ini seharusnya hanya digunakan pada sistem yang resmi. Setiap penggunaan tanpa izin dari alat ini tanpa izin eksplisit adalah ilegal.
