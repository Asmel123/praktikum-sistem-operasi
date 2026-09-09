# praktikum-sistem-operasi
Tugas CLI LINUX
Tahap 1 Navigasi & Informasi Direktori
1 pwd (Print Working Directory)
Menampilkan jalur atau lokasi direktori lengkap di mana kamu berada saat ini

2 ls (List)
Menampilkan daftar file dan folder yang ada di direktori aktif saat ini

3 ls -l (Long List)
Menampilkan daftar file atau folder dalam format rinci seperti hak akses, jumlah link, nama pemilik, ukuran file, dan tanggal dibuat

4 ls -a (List All)
Menampilkan seluruh file dan folder termasuk file tersembunyi yang diawali dengan tanda titik

5 mkdir -p /home/asmel/praktikum_asmel (Make Directory)
Membuat folder baru bernama praktikum_asmel sekaligus folder induknya jika belum ada

6 cd /home/asmel/praktikum_asmel (Change Directory)
Pindah lokasi kerja terminal ke folder praktikum_asmel

7 cd ..
Berpindah atau naik satu tingkat ke folder di atas direktori saat ini

8 cd ~
Berpindah secara instan langsung ke direktori home milik user kamu /home/asmel

Tahap 2 Manajemen File & Folder
9 cd ~/praktikum_asmel
Pindah langsung ke folder praktikum di direktori home

10 mkdir modul_asmel
Membuat folder baru bernama modul_asmel di dalam direktori aktif

11 mkdir -p tugas_asmel/bab1/laporan
Membuat struktur folder bertingkat secara instan dari tugas_asmel hingga sub-folder laporan

12 touch catatan_asmel.txt
Membuat sebuah file teks baru yang masih kosong bernama catatan_asmel.txt

13 cp catatan_asmel.txt backup_asmel.txt (Copy)
Menyalin file catatan_asmel.txt menjadi file baru bernama backup_asmel.txt

14 cp -r modul_asmel backup_modul
Menyalin folder modul_asmel beserta seluruh isinya secara rekursif ke folder backup_modul

15 mv backup_asmel.txt catatan_lama.txt (Move)
Memindahkan file atau mengganti nama file dari backup_asmel.txt menjadi catatan_lama.txt

16 rm catatan_lama.txt (Remove)
Menghapus file catatan_lama.txt dari sistem secara permanen

17 rm -r backup_modul
Menghapus folder backup_modul beserta seluruh isi file di dalamnya secara rekursif

18 rmdir modul_asmel (Remove Directory)
Menghapus direktori modul_asmel khusus untuk folder yang sudah kosong

19 ln -s catatan_asmel.txt shortcut_catatan (Link Symbolic)
Membuat file tautan atau pintasan shortcut bernama shortcut_catatan yang mengarah ke file asli catatan_asmel.txt

Tahap 3 Membaca & Edit Isi File
20 nano catatan_asmel.txt
Membuka aplikasi text editor Nano di dalam terminal untuk mengetik atau mengedit isi file catatan_asmel.txt

21 cat catatan_asmel.txt (Concatenate)
Mencetak dan menampilkan seluruh isi teks di dalam file catatan_asmel.txt ke layar terminal

22 less /var/log/syslog
Membuka file teks yang panjang atau besar halaman demi halaman agar mudah dibaca

23 head -n 10 /etc/passwd
Menampilkan 10 baris pertama dari bagian atas file /etc/passwd

24 tail -n 10 /etc/passwd
Menampilkan 10 baris terakhir dari bagian bawah file /etc/passwd

25 tail -f /var/log/syslog (Follow)
Memantau perubahan atau baris baru pada file log sistem secara real-time

26 vim catatan_asmel.txt
Membuka editor teks canggih Vim untuk mengedit file catatan_asmel.txt

27 grep "asmel" catatan_asmel.txt
Mencari dan memfilter baris yang mengandung kata "asmel" di dalam file catatan_asmel.txt

28 wc catatan_asmel.txt (Word Count)
Menghitung jumlah baris, kata, dan ukuran karakter atau byte di dalam file catatan_asmel.txt

Tahap 4 Hak Akses & Pengguna (User Management)
29 whoami
Menampilkan nama akun pengguna yang sedang aktif dan digunakan saat ini (asmel)

30 sudo ls /root (SuperUser DO)
Menjalankan perintah ls /root menggunakan hak akses tertinggi atau administrator root

31 chmod 755 catatan_asmel.txt (Change Mode)
Mengubah izin atau hak akses file catatan_asmel.txt menjadi read write execute untuk owner serta read execute untuk group dan others

32 sudo chown asmel:asmel catatan_asmel.txt (Change Owner)
Mengubah hak kepemilikan file catatan_asmel.txt menjadi milik user asmel dan grup asmel

33 sudo adduser user_praktikum
Menambahkan pengguna baru bernama user_praktikum ke dalam sistem Ubuntu

34 passwd
Mengubah kata sandi atau password dari akun user yang sedang aktif

35 sudo deluser user_praktikum
Menghapus akun pengguna user_praktikum dari sistem

Tahap 5 Manajemen Sistem & Sumber Daya
36 top
Menampilkan daftar proses sistem yang berjalan serta penggunaan RAM dan CPU secara dinamis atau real-time

37 htop
Menampilkan manajemen proses sistem dengan tampilan grafik visual yang interaktif

38 ps aux (Process Status)
Menampilkan daftar seluruh proses aplikasi yang sedang berjalan di sistem beserta nomor PID-nya

39 df -h (Disk Free)
Menampilkan sisa ruang penyimpanan pada harddisk dalam format yang mudah dibaca manusia seperti MB atau GB

40 du -sh ~/praktikum_asmel (Disk Usage)
Menghitung total ukuran file atau folder praktikum_asmel secara ringkas

41 free -m
Menampilkan kapasitas penggunaan memori RAM terpakai, kosong, dan cache dalam satuan Megabyte

42 kill 1234
Menghentikan atau mematikan proses aplikasi tertentu berdasarkan ID Prosesnya (PID)

43 killall firefox
Mematikan seluruh proses aplikasi sekaligus berdasarkan nama aplikasinya

Tahap 6 Jaringan & Konektivitas
44 ping -c 4 google.com
Mengirim 4 paket data tes ke server google.com untuk menguji koneksi internet

45 ip a (IP Address)
Menampilkan informasi kartu jaringan dan alamat IP milik komputer kamu

46 ifconfig (Interface Configuration)
Perintah klasik untuk memeriksa status dan konfigurasi antarmuka jaringan

47 netstat -tuln
Menampilkan daftar port jaringan yang sedang aktif atau terbuka di komputer

48 curl [https://ifconfig.me](https://ifconfig.me)
Mengambil atau menampilkan data dari suatu situs web langsung di dalam terminal

49 wget [https://releases.ubuntu.com/robots.txt](https://releases.ubuntu.com/robots.txt) -O ~/praktikum_asmel/robots_download.txt
Mengunduh file dari internet dan menyimpannya langsung dengan nama robots_download.txt

50 ssh asmel@192.168.1.100 (Secure Shell)
Mengakses dan mengendalikan komputer atau server jarak jauh secara aman melalui alamat IP-nya

Tahap 7 Paket & Pembaruan Aplikasi
51 sudo apt update
Memperbarui indeks atau daftar katalog aplikasi terbaru dari repositori resmi Ubuntu

52 sudo apt upgrade -y
Memperbarui seluruh aplikasi yang sudah terinstal di Ubuntu ke versi paling baru

53 sudo apt install tree -y
Mengunduh dan memasang aplikasi baru bernama tree ke dalam sistem secara otomatis

54 tree ~/praktikum_asmel
Menampilkan struktur cabang direktori dan file dalam bentuk diagram pohon visual

55 sudo apt remove tree -y
Menghapus atau mencopot aplikasi tree yang terinstal dari sistem

56 sudo apt autoremove -y
Membersihkan dan menghapus file paket bekas atau dependensi yang sudah tidak digunakan lagi

Tahap 8 Utilitas & Kebersihan Terminal
57 history
Mencetak dan menampilkan daftar seluruh perintah terminal yang pernah diketik dari awal sampai akhir

58 clear
Membersihkan seluruh riwayat teks di layar terminal agar tampilan kembali bersih dan rapi
