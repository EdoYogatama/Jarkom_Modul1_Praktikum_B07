# Jarkom_Modul1_Praktikum_B07

#### 1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
Display filter dengan syntax
```
http.host == testing.mekanis.me
```
![img](no1.png)

lalu follow TCP stream dan lihat webservernya. Webserver : nginx/1.14.0(ubuntu)
![img](no1.1.png)

#### 2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
Export HTTP, setelah itu mencari nama image yang akan dicari pada text filter. Lalu save object gambar
![img](21.png)
![img](Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg)
#### 3. Cari username dan password ketika login di "ppid.dpr.go.id"!
Display filter dengan syntax
```
http.host == "ppkl.dpr.go.id" && http.request.method == POST
```
Username : 10pemuda
password : guncangdunia
![img](no3.png)

#### 4. Temukan paket dari web-web yang menggunakan basic authentication method!
Display Filter dengan syntax
```
http.authorization contains Basic
```
![img](4.png)
#### 5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
Display filter dengan syntax
```
http.host == "aku.pengen.pw"
```
![img](no5.png)

dapatkan username dan password pada Authorization
username : kakakgamtenk
password : hartatahtabermuda
lalu masuk ke web tersebut dan masukan username dan passwordnya. Kemudian lakukan instruksi didalamnya (isi urutan konfigurasi kabel T568B)
![img](no5.1.png)

#### 6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
Ctrl + f, cari paket list dengan "Answer.zip" dan "zipkey.txt". Cari yang baris dengan kolom protocolnya "FTP-Data". setelah itu Klik kanan, follow -> TCP Stream. Ubah dari ASCII ke Raw. Save as dengan nama dan ekstensi yang sesuai dengan file yang akan disave

![img](61.png)![img](62.png)![img](63.png)![img](64.png)![img](65.png)![img](66.png)
#### 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"
Cari menggunakan find dengan filter hex code dan masukan kode hex dari "Yes.pdf" yaitu 59 65 73 2e 70 64 66
![img](no7.png)

follow TCP stream dan save file zip tersebut dan buka

![img](no7.1.png)

#### 8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
Display Filter dengan syntax
```
ftp.request.command == RETR
```
![img](8.png)
#### 9. Cari username dan password ketika login FTP pada localhost!
Display filter dengan syntax
```
http.request.command == USER || http.request.command == PASS
```
![img](no9.png)

#### 10. Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46"
Lakukan find dengan kode hex 25 50 44 46

![img](no10.png)

follow TCP stream dan save file pdf tersebut

![img](no10.1.png)
#### 11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
Capture filter dengan syntax
```
port 21
```
![img](no11.png)
![img](no11.1.png)
#### 12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
mengcapture packet dari port 80, maka source nya ada pada port 80
```
src port 80
```
![img](12.png)
#### 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
Capture filter dengan syntax
```
dst port 443
```
![img](no13.png)
![img](no13.1.png)
#### 14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
Mencari Informasi IP Address pada PC, jika di windows melihat di Network Properties. Setelah itu Capture filter dengan syntax
```
src net 192.168.1.9
```
![img](14.png)
#### 15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
Capture filter dengan syntax
```
dst host monta.if.its.ac.id
```
![img](no15.png)
![img](no15.1.png)
