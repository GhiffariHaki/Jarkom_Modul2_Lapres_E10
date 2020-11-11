# Jarkom_Modul2_Lapres_E10
- Ardy Wahyu Setiawan 05111840000050
- Mochamad Haikal Ghiffari 05111840000095

### 1.	Membuat semerue10.pw pada UML Malang
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98778956-b42a6800-2425-11eb-9ca4-4eb28577f122.png)
![image](https://user-images.githubusercontent.com/57068224/98778995-be4c6680-2425-11eb-86e7-62c8aa9a3731.png)

### 2.	Membuat alias CNAME pada semerue10.pw pada UML Malang
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98779069-db813500-2425-11eb-81a6-9dab02a1bc99.png)
![image](https://user-images.githubusercontent.com/57068224/98779146-feabe480-2425-11eb-9860-94b28a86f000.png)

### 3.	Membuat subdomain www.penanjakan yang mengarah ke IP PROBOLINGGO
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98779198-15523b80-2426-11eb-8ba0-b7b017e1fddd.png)
![image](https://user-images.githubusercontent.com/57068224/98779230-23a05780-2426-11eb-89c2-122aa264bbb9.png)

### 4.	Membuat Reverse domain untuk domain utama
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98779278-34e96400-2426-11eb-8e4a-c90374534f74.png)
![image](https://user-images.githubusercontent.com/57068224/98779304-3ca90880-2426-11eb-91b3-0e770b4b9619.png)

### 5.	Membuat Slave pada UML MOJOKERTO
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98779349-564a5000-2426-11eb-9aa1-5ae23e077c12.png)
![image](https://user-images.githubusercontent.com/57068224/98779354-58141380-2426-11eb-8578-2a2e1b007b82.png)

### 6.	Membuat Delegasi yang pada MOJOKERTO yang mengarah ke PROBOLINGGO
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98779479-842f9480-2426-11eb-94fd-956933df77dd.png)
![image](https://user-images.githubusercontent.com/57068224/98779483-85f95800-2426-11eb-8fa3-5dc61859d70d.png)
![image](https://user-images.githubusercontent.com/57068224/98779494-88f44880-2426-11eb-82bc-a6d07803525e.png)
![image](https://user-images.githubusercontent.com/57068224/98779501-8c87cf80-2426-11eb-89c1-337059d2e590.png)
![image](https://user-images.githubusercontent.com/57068224/98779505-8db8fc80-2426-11eb-848f-c4cb635cd315.png)

### 7.	Membuat subdomain naik.gunung.semerue10.pw yang mengarah ke PROBOLINGGO
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98779548-a1fcf980-2426-11eb-9943-c1e31dcf9d56.png)
![image](https://user-images.githubusercontent.com/57068224/98779562-a9bc9e00-2426-11eb-9cba-194d611052a0.png)

### 8.	Mengatur webserver semerue10.pw
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98779641-c8bb3000-2426-11eb-9ac9-35fa4c41fdbc.png)
![image](https://user-images.githubusercontent.com/57068224/98779647-ca84f380-2426-11eb-8e94-82f83389cfb4.png)

### 9.	Awalnya web dapat diakses menggunakan alamat http://semeruyyy.pw/index.php/home. Karena dirasa alamat urlnya kurang bagus, maka (9) diaktifkan mod rewrite agar urlnya menjadi http://semeruyyy.pw/home.
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98779949-fef8af80-2426-11eb-9f47-d7fdaa95e7a3.png)
![image](https://user-images.githubusercontent.com/57068224/98779966-01f3a000-2427-11eb-8b9c-4b92cfc8974d.png)

### 10.	Web http://penanjakan.semeruyyy.pw akan digunakan untuk menyimpan assets file yang memiliki DocumentRoot pada /var/www/penanjakan.semeruyyy.pw
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98780250-1899f700-2427-11eb-9184-1527a709bbe0.png)
![image](https://user-images.githubusercontent.com/57068224/98780256-1a63ba80-2427-11eb-8643-d73c97b23c09.png)

### 11.	Pada folder /public dibolehkan directory listing namun untuk folder yang berada di dalamnya tidak dibolehkan.
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98780319-294a6d00-2427-11eb-99b1-54393fde2d03.png)
![image](https://user-images.githubusercontent.com/57068224/98780328-2b143080-2427-11eb-8828-45c5946ed0f6.png)

### 12.	Untuk mengatasi HTTP Error code 404, disediakan file 404.html pada folder /errors untuk mengganti error default 404 dari Apache.
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98780404-4a12c280-2427-11eb-9cfa-721864a24bfa.png)
![image](https://user-images.githubusercontent.com/57068224/98780415-4bdc8600-2427-11eb-9fcd-befdefb29dd9.png)

### 13.	Untuk mengakses file assets javascript awalnya harus menggunakan url http://penanjakan.semeruyyy.pw/public/javascripts. Karena terlalu panjang maka dibuatkan konfigurasi virtual host agar ketika mengakses file assets menjadi http://penanjakan.semeruyyy.pw/js.
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98780454-5b5bcf00-2427-11eb-8a07-bf43c2f61b58.png)
![image](https://user-images.githubusercontent.com/57068224/98780459-5d259280-2427-11eb-98af-21a0de06319e.png)
![image](https://user-images.githubusercontent.com/57068224/98780502-6d3d7200-2427-11eb-8cdc-a6b412e09369.png)

### 14.	Untuk web http://gunung.semeruyyy.pw belum dapat dikonfigurasi pada web server karena menunggu pengerjaan website selesai. (14) sedangkan web http://naik.gunung.semeruyyy.pw sudah bisa diakses hanya dengan menggunakan port 8888. DocumentRoot web berada pada /var/www/naik.gunung.semeruyyy.pw.
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98780600-9e1da700-2427-11eb-8279-95b253f57b6b.png)
![image](https://user-images.githubusercontent.com/57068224/98780605-a1b12e00-2427-11eb-8431-92f73f9a98fe.png)

### 15.	Dikarenakan web http://naik.gunung.semeruyyy.pw bersifat private (15) Bibah meminta kamu membuat web http://naik.gunung.semeruyyy.pw agar diberi autentikasi password dengan username “semeru” dan password “kuynaikgunung” supaya aman dan tidak sembarang orang bisa mengaksesnya.
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98780660-b8f01b80-2427-11eb-8d99-6047b4a95ed3.png)
![image](https://user-images.githubusercontent.com/57068224/98780671-bb527580-2427-11eb-8453-7c5d79c44a67.png)

### 16.	Karena dirasa kurang profesional, maka setiap Bibah mengunjungi IP PROBOLINGGO akan dialihkan secara otomatis ke http://semeruyyy.pw.
Gambar :

![image](https://user-images.githubusercontent.com/57068224/98780755-d9b87100-2427-11eb-8c94-b7b7e574af0b.png)
![image](https://user-images.githubusercontent.com/57068224/98780760-db823480-2427-11eb-800e-9c5356cca74e.png)

### 17.	Karena pengunjung pada /var/www/penanjakan.semeruyyy.pw/public/images sangat banyak maka semua request gambar yang memiliki substring “semeru” akan diarahkan menuju semeru.jpg.
