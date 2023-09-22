# Laporan Resmi Praktikum Modul 1 Jarkom Kelompok D20

## Anggota Kelompok
NRP | Nama |
--- | --- | 
5025201041 | Khairuddin Nasty |
5025211187 | Altriska Izzati Khairunnisa Hermawan |

## Soal 1
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.
a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?
b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?
c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
### Penyelesaian
### Bukti Flag

## Soal 2
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
### Penyelesaian
- Klik kanan pada paket dengan source yang digunakan portal praktikum Jaringan Komputer
- Klik “follow” -> “HTTP Stream”
- Bisa dilihat server yang digunakan adalah `gunicorn`
![soal2](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/0c9199fe-05ef-4fb9-b9c8-625b0bd5272b)
### Bukti Flag
![soal2flag](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/b46a5b10-7367-48b9-92ca-bf461c562a91)


## Soal 3
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
b. Protokol layer transport apa yang digunakan?
Penyelesaian
### Bukti Flag

## Soal 4
Berapa nilai checksum yang didapat dari header pada paket nomor 130?
### Penyelesaian
- Buka paket 130 dan buka UDP 
- Dapat dilihat bahwa checksum dari paket 130 adalah `0x18e5`
![soal4](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/732acb25-fa4b-44db-916a-b4d5ec9f97eb)
### Bukti Flag
![soal4flag](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/2eba7f3f-c6d0-4796-a0c7-76a47afe856e)

## Soal 5
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.
a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
b. Port berapakah pada server yang digunakan untuk service SMTP?
c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?
### Penyelesaian
Sebelum memulai pengerjaan kita harus mencari nc untuk menjawab soal ini dengan melakukan beberapa tahap:
- Filter file dengan “SMTP” 
- Di antara paket ditemukan sebuah pesan di Line-based text data berisi password file zip yang harus di-decode menggunakan Base64 (paket 22)
- Setelah file zip dibuka ditemukan file .txt berisi nc untuk submit jawaban
### a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
- Buka “Statistics” dan klik “Capture File Properties”, scroll dan temukan packet yang ter-capture
- Banyak paket yang didapat adalah `60`
![soal5_1](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/f709640c-618f-4cea-9aa7-7185d7ae83d9)
### b. Port berapakah pada server yang digunakan untuk service SMTP?
- Klik paket dengan protokol “SMTP” dan bisa dilihat destination port yang digunakan
- Port yang digunakan adalah `25`
![soal5_2](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/06549850-7d3c-410d-b44b-3f9a1c27b745)
### c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?
- Di antara semua alamat IP, yang merupakan public IP adalah `74.53.140.153`
### Bukti Flag
![soal5flag](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/b4bb16fa-b1cf-4e3d-9ba1-6d6fe9bb55ad)

## Soal 6
Seorang anak bernama Udin Berteman dengan Slamet yang merupakan seorang penggemar film detektif. sebagai Teman yang baik, Ia selalu mengajak slamet untuk bermain valorant bersama. suatu malam, Terjadi sebuah hal yang tak terduga. ketika Udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.
Hint :
- Sepertinya ada yang salah dengan penulisan tersebut secara KBBI. Ada sesuatu yang Besar di depan mata.
- Jenis cipher merupakan substitusi a1z26 Cipher
- Rentang Huruf yang digunakan Huruf A-R, 1-18 dengan Jawaban 6 Huruf.
- SOURCE ADDRESS ADALAH KUNCI SEMUANYA.
### Penyelesaian
- Source address paket 7812 adalah 104.18.14.101
  ![soal6_1](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/61efaac2-1929-4adb-8720-5bac17877dc2)
- Hint-hint yang sudah diberikan menunjukkan bahwa source address paket 7812 harus disubstitusi a1z26 cipher dan didapatkan string seperti berikut
![soal6](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/fbb72225-8f07-4015-ae1a-932121967dda)
- Didapatkan jawaban yaitu `JDRNJA`
### Bukti Flag
![soal6flag](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/ac7583ed-5d73-4225-b78b-79c219337a5a)

## Soal 7
Berapa jumlah packet yang menuju IP 184.87.193.88?
### Penyelesaian
### Bukti Flag

## Soal 8
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)
### Penyelesaian
- Kueri yang digunakan adalah `tcp.dstport == 80 || udp.dstport == 80`
![soal8](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/650defa7-df06-49f7-a01a-69eaf8f367e0)
### Bukti Flag
![soal8flag](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/20c604f1-5d98-4c9b-9a44-cd8254068997)

## Soal 9
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!
### Penyelesaian
### Bukti Flag

## Soal 10
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet
### Penyelesaian
- Filter dengan “telnet” maka akan ditampilkan paket-paket dengan protocol TELNET
- Scroll paket-paket ke bawah dan dapat ditemukan dari paket 81 didapat hint bahwa kredensial yang digunakan adalah `dhafian:kesayangannyak0k0`
![soal10](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/ee8a71f9-c545-4e52-bec8-b7152cba9a57)
### Bukti Flag
![soal10flag](https://github.com/altriskaa/Jarkom-Modul-1-D20-2023/assets/114663340/4cf6c001-bd22-41a7-8b84-22b52bf0c6f9)
