# Jarkom-Modul-1-C15-2021

### Anggota Kelompok
1. Gerald Elroy Van Ryan 05111940000187
2. Gian Ega              05111940000214
3. Riza Dwi Andhika      05111940000149

## Soal 1

```
Sebutkan webserver yang digunakan pada "ichimarumaru.tech"! 
```

**Filter** : http.host == "ichimarumaru.tech"

**Cara pengerjaan** :
Masukkan filter di atas pada wireshark, lalu pilih salah satu paket yang muncul. Setelah itu, ***follow TCP Stream*** pada paketnya untuk mendapatkan webserver yang digunakan.

**Screenshot** :
1. Hasil paket yang didapat dari filter
![image](https://user-images.githubusercontent.com/64303057/134768737-4aab9525-cc55-4a5f-b06d-6741a1787b20.png)
2. Hasil ***follow TCP Stream*** pada salah satu paket
![image](https://user-images.githubusercontent.com/64303057/134768756-b81005fd-7929-46c3-9028-e1ece7190b62.png)

**Kendala yang dialami** :
Sempat bingung karena tidak ada hasil paket yang didapatkan. Ternyata, ada kesalahan syntax pada filter karena hanya memakai satu sama dengan '='. Yang benar adalah '=='.


## Soal 2

```
Temukan paket dari web-web yang menggunakan basic authentication method!
```

**Filter** : http.authbasic

**Cara pengerjaan** :
Masukkan filter di atas pada wireshark, maka akan muncul paket-paket yang sesuai

**Screenshot** :
1. Hasil paket yang didapat dari filter
![image](https://user-images.githubusercontent.com/64303057/134768808-b9c49f06-50fa-4449-8070-cce317292ab6.png)

**Kendala yang dialami** :
Tidak ada.

## Soal 3

```
 Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!
```

**Filter** : http.host == "basic.ichimarumaru.tech"

**Cara pengerjaan** :
Masukkan filter di atas pada wireshark, maka akan muncul paket-paket yang sesuai. Carilah paket yang memiliki *Credentials* pada bagian Hypertext Transfer Protocol. Di sana akan tertulis **usename & passwordnya**.

Username : kuncimenujulautan

Password : tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN

**Screenshot** :
1. Username & password yang didapat dari salah satu paket
![image](https://user-images.githubusercontent.com/64303057/134768994-72da469e-fdd0-4f42-b282-28ebd3310155.png)
2. Tampilan depan website setelah berhasil login
![image](https://user-images.githubusercontent.com/64303057/134769025-a3f03a51-bdf3-4f1d-93b6-a5204a8db455.png)

**Jawaban pada pertanyaan di website** :

Urutan ke 1 : Putih Hijau TD+ (data kirim+)

Urutan ke 2 : Hijau TD- (data kirim-)

Urutan ke 3 : Putih Orange RD+ (data terima +)

Urutan ke 4 : Biru NC (tidak dipakai)

Urutan ke 5 : Putih Biru NC (tidak dipakai)

Urutan ke 6 : Orange RD- (data terima -)

Urutan ke 7 : Putih Coklat NC (tidak dipakai)

Urutan ke 8 : Coklat NC (tidak dipakai)

**Kendala yang dialami** :
Awalnya tidak mendapatkan jawaban, karena tidak menemukan username & password saat ***follow TCP Stream***. Ternyata, jawaban ditemukan dari bagian Hypertext Transfer Protocol paket.

## Soal 4

```
Temukan paket mysql yang mengandung perintah query select!
```

**Filter** : mysql.query matches select

**Cara pengerjaan** :
Masukkan filter di atas pada wireshark, maka akan muncul paket-paket yang sesuai dengan filter

**Screenshot** :
1. Hasil paket yang didapat dari filter
![image](https://user-images.githubusercontent.com/64303057/134769225-95bcf801-13f3-4d0a-b482-0de7ef26a347.png)

**Kendala yang dialami** :
TIdak ada.

## Soal 5

```
Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya!

Username dan password bisa didapat dari query insert pada table users dari file .pcap!
```

**Filter** : mysql.query matches insert

**Cara pengerjaan** :
Masukkan filter di atas pada wireshark, maka akan muncul paket yang sesuai pada filter. 
Lakukan ***follow TCP Stream*** untuk mendapatkan **username & password** untuk dimasukkan ke dalam website.

Username : akakanomi

Password : pemisah4lautan

**Screenshot** :
1. Hasil paket yang didapat dari filter
![image](https://user-images.githubusercontent.com/64303057/134769325-7a3c86c3-6fce-45f9-91b4-4941bf633db7.png)
2. Hasil ***follow TCP Stream*** untuk dapatkan username & password
![image](https://user-images.githubusercontent.com/64303057/134769345-81363913-ad56-49b5-a9f1-94439f01779b.png)
3. Tampilan depan website setelah masukkan berhasil login
![image](https://user-images.githubusercontent.com/64303057/134769373-9663ada0-5b3a-4c23-ba51-1e7596b0652b.png)

**Jawaban pada pertanyaan di website** :

Urutan ke 1 : Putih Orange RD+ (data terima+)

Urutan ke 2 : Orange RD- (data terima-)

Urutan ke 3 : Putih Hijau TD+ (data kirim +)

Urutan ke 4 : Biru NC (tidak dipakai)

Urutan ke 5 : Putih Biru NC (tidak dipakai)

Urutan ke 6 : Hijau TD- (data kirim -)

Urutan ke 7 : Putih Coklat NC (tidak dipakai)

Urutan ke 8 : Coklat NC (tidak dipakai)

**Kendala yang dialami** :
Tidak ada. 

## Soal 6
```
Cari username dan password ketika melakukan login ke FTP Server
```

**Filter : ftp.request.command == USER || ftp.request.command == PASS**
**Cara pengerjaan :**
1. Gunakan filter
2. Kemudian follow tcp stream paket yang ada 


Screenshot:

![image](https://user-images.githubusercontent.com/90212308/134769441-23facb32-c505-40bb-a8d1-a316eb990db6.png)
![image](https://user-images.githubusercontent.com/90212308/134769468-b1cebc74-9a07-450b-af0b-33bcbba29d52.png)

**Kendala :**
Tidak ada.

## Soal 7
```
Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")
```

**Filter : frame contains Real.pdf**
**Cara pengerjaan :**
1. Gunakan filter
2. Kemudian follow tcp stream paket yang ada 
3. Pilih RAW pada ```show data as```
4. Pilih Save as dan save dengan exstensi pdf


Screenshot:
![image](https://user-images.githubusercontent.com/90212308/134769498-ed70feb6-31ef-4b1e-89ec-cabd6eb62f00.png)
![image](https://user-images.githubusercontent.com/90212308/134769535-307e2278-185a-47b8-83cc-14f971c83c52.png)
![image](https://user-images.githubusercontent.com/90212308/134769555-cd4c91f1-27cd-4e7c-9344-7099a6a7a9d3.png)

**Kendala :**
Tidak ada.

## Soal 8
```
Cari paket yang menunjukan pengambilan file dari FTP tersebut!
```

**Filter : ftp.request.command == RETR**
***ralat STOR***
**Cara pengerjaan :**
1. Gunakan filter
2. Paket akan terdisplay

Screenshot :

![image](https://user-images.githubusercontent.com/90212308/134769654-378501df-63f2-491e-9aa0-0068cb0a9731.png)
![image](https://user-images.githubusercontent.com/90212308/134769674-3c0e8416-db69-4554-93f2-d2f5c5887906.png)

**Kendala :**
Hasil filter tidak ada, ralat.

## Soal 9
```
Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!

```

**Filter : ftp-data.command contains "secret.zip"**
**Cara pengerjaan :**
1. Gunakan filter
2. Kemudian follow tcp stream paket yang ada 
3. Pilih RAW pada ```show data as```
4. Pilih Save as dan save dengan exstensi zip


Screenshot :

![image](https://user-images.githubusercontent.com/90212308/134769749-4be9167c-1809-4779-af18-a3267db2635d.png)
![image](https://user-images.githubusercontent.com/90212308/134769762-97955293-b70b-4a17-b834-fb77a1d194dd.png)
![image](https://user-images.githubusercontent.com/90212308/134769768-a12041cc-fb1f-45fe-8d9f-fdda4ea3b6ef.png)

**Kendala :**
Terkendala ketika mendownload file secret zip.

## Soal 10
```
Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!
```

**Filter : ftp-data.command contains "history.txt"**
**Cara pengerjaan :**
1. Gunakan filter
2. Kemudian follow tcp stream paket yang ada 
3. Pada stream tersebut terdapat hint berupa ```bukanapaapa.txt```
4. Filter dengan format yang sama namun rubah ```history.txt``` menjadi ```bukanapaapa.txt```

Screenshot :

![image](https://user-images.githubusercontent.com/90212308/134769809-85768113-7db2-4264-8004-f4957edf66d4.png)
![image](https://user-images.githubusercontent.com/90212308/134769811-dba08646-c29f-4c59-90cc-6eae2c36aed3.png)

**Filter : ftp-data.command contains "bukanapaapa.txt"**
1. Gunakan filter
2. Kemudian follow tcp stream paket yang ada
3. Pada Stream tersebut terdapat password untuk membuka zip pada nomor 9


Screenshot : 
![image](https://user-images.githubusercontent.com/90212308/134769886-3235c42e-d899-4071-836f-f6c8f421ad80.png)
![image](https://user-images.githubusercontent.com/90212308/134769901-0b24107a-d21b-4f84-b0f8-274b3916720f.png)

**Kendala :**
Terkendala ketika mencari hint untuk membuka file nomor 9.

## Soal 11

```
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
```

**Filter capture: src port 80**

Screenshot:
![](./img/11.png)

## Soal 12

```
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

```

**Filter capture: port 21**

Screenshot:
![](./img/12.png)

## Soal 13

```
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
```

Filter display: **tcp**.dstport == 443 || udp.dstport == 443

Screenshot:
![](./img/13.png)

## Soal 14

```
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!
```

Filter capture: dst host kemenag.go.id

Screenshot:
![](./img/14.png)

## Soal 15

```
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
```

IP komputer pribadi saat itu adalah **192.168.100.5**
Filter capture: src host 192.168.100.5

Screenshot:
![](./img/15.png)
