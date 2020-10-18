# Jarkom_Modul1_Lapres_06

## Display Filter

### 1. Simpan webserver yang digunakan pada "testing.mekanis.me"!
```
http.host eq "testing.mekanis.me"
```
*kemudian buka Follow TCP Stream dengan cara klik kanan pada paket*

![1a](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%201.jpg)

*setelah itu akan terlihat servernya yaitu nginx*

![1b](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%201%20(2).jpg)

----

#### 2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

```
Pada kiri atas tab, klik File -> Export Object -> HTTP
```

*Masukkan nama file yang ingin di save (filtering), lalu **Save***

![2a](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%202.jpg)
![2b](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%202%20(2).jpg)

![2c](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%202%20(3).jpg)

----

#### 3. Cari username dan password ketika login di "ppid.dpr.go.id"!
```
http.request.method == POST
```
![3a](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%203.jpg)

----

#### 4. Temukan paket dari web-web yang menggunakan basic authentication method!

```
http.authbasic
```

![4](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%204.jpg)

----

#### 5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
```
http.host contains "aku.pengen.pw"
```

![5a](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%205.jpg)
![5b](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%205%20(2).jpg)
![5c](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%205%20(3).jpg)

----

#### 6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).

***Mencari file zip***

```
ftp-data
```

![6](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%206.jpg)

```
Klik kanan -> Follow -> TCP Stream -> Save data as Raw -> Jangan lupa tambahkan extension zip (.zip)
```

![6a](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%206%20(2).jpg)
![6b](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%206%20(3).jpg)

![6c](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%206%20(4).jpg)

![6d](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%206%20(5).jpg)

*File akan tersimpan sebagai **zip***

------

***Mencari password***

```
frame contains "zipkey.txt"
```

![6e](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%206%20(6).jpg)

```
Klik kanan -> Follow -> TCP Stream -> Save data as ASCII -> Ubah stream menjadi 23
```

![6f](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%206%20(7).jpg)

*File txt akan tersimpan dan berisi **password** dari file zip sebelumnya*

*Masukkan password, dan **open this.pdf** akan menampilkan seperti dibawah ini*

![6g](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%206%20(8).jpg)

![6h](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%206%20(9).jpg)

----

#### 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
```
frame contains "Yes.pdf"
```

![7](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%207.jpg)

*klik kanan, follow TCP Stream lalu save data menjadi Raw*

*extract zip lalu akan muncul file pdf seperti berikut*

![7b](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%207%20(2).jpg)

----

#### 8.Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
```
ftp.request.command eq "RETR"
```

![8](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%208.jpg)

![8a](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%208%20(2).jpg)

----

#### 9. Cari username dan password ketika login FTP pada localhost!
```
ftp.request.command == USER || ftp.request.command == PASS
```
![9](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%209.jpg)

----

#### 10. Cari file .pdf di wireshark lalu download dan buka file tersebut!

```
frame contains “application/pdf”
```
```
Klik kanan -> Follow -> TCP Stream -> Save data as Raw -> Jangan lupa tambahkan extension pdf (.pdf)
```

![10](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%2010.jpg)

![10a](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%2010%20(2).jpg)

![10a](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%2010%20(3).jpg)

*File akan tersimpan sebagai **pdf***

*Berikut tampilan saat file dibuka*

![10c](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%2010%20(4).jpg)

----

## Capture Filter

#### 11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
```
port 21
```

![11](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%2011.jpg)

```
Pilih *Adapter for loopback traffic capture* (Internet localhost)
```
```
buka cmd, ketik "*ftp (spasi) iplocalhost*"
```
```
masukkan user & password ftp (filezilla)
```
*Berikut tampilan packet-packet yang ditangkap wireshark*

![11a](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%2011%20(2).jpg)

----

#### 12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

```
src port 80
```
```
pilih wi-fi
```

![12](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%2012.jpg)

----

#### 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

```
dst port 433
```
```
pilih wi-fi
```

![13](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%2013.jpg)

----

#### 14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

*Mencari **ip** pc dahulu melalui terminal dengan cara :*

```
buka cmd, ketik ipconfig lalu enter. lihat ipv4, itulah ip kita.
```

*Capture di Wireshark*

```
src host 192.168.100.14
```

![14a](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%2014.jpg)

----

#### 15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!

```
dst host monta.if.its.ac.id
```
![15](https://github.com/davidbintang/Jarkom_Modul1_Lapres_B06/blob/main/SS%20JAWABAN/NO%2015.jpg)

----
