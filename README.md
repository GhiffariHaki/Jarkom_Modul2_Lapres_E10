# Jarkom_Modul2_Lapres_E10
- Ardy Wahyu Setiawan 05111840000050
- Mochamad Haikal Ghiffari 05111840000095

### 1.	Membuat semerue10.pw pada UML Malang
-	nano /etc/bind/named.conf.local
-	mkdir /etc/bind/jarkom
-	cp /etc/bind/db.local /etc/bind/jarkom/semerue10.pw
-	nano /etc/bind/jarkom/semerue10.pw
-	service bind9 restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98974540-981ee780-2547-11eb-81cb-3a71345766a3.png)
![image](https://user-images.githubusercontent.com/57068224/98974546-9a814180-2547-11eb-8097-76aac5d3316b.png)
![image](https://user-images.githubusercontent.com/57068224/98974550-9c4b0500-2547-11eb-8bb1-8dad25be85f2.png)

### 2.	Membuat alias CNAME pada semerue10.pw pada UML Malang
-	nano /etc/bind/jarkom/semerue10.pw
-	service bind9 restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98974556-9ead5f00-2547-11eb-8bbe-de9fd949fc9c.png)
![image](https://user-images.githubusercontent.com/57068224/98974621-b258c580-2547-11eb-87b7-c8e3a99b959c.png)

### 3.	Membuat subdomain www.penanjakan yang mengarah ke IP PROBOLINGGO
-	nano /etc/bind/jarkom/semerue10.pw
-	service bind9 restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98974657-bedd1e00-2547-11eb-8508-fdb807557179.png)
![image](https://user-images.githubusercontent.com/57068224/98974664-c13f7800-2547-11eb-8099-08e0344ace44.png)

### 4.	Membuat Reverse domain untuk domain utama
-	nano /etc/bind/named.conf.local
-	cp /etc/bind/db.local /etc/bind/jarkom/71.151.10.in-addr.arpa
-	nano /etc/bind/jarkom/71.151.10.in-addr.arpa
-	service bind9 restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98974703-cbfa0d00-2547-11eb-96aa-83242e34ab0c.png)
![image](https://user-images.githubusercontent.com/57068224/98974712-cdc3d080-2547-11eb-8172-1905f0be245c.png)
![image](https://user-images.githubusercontent.com/57068224/98974720-cf8d9400-2547-11eb-883a-9e7103bc2f7d.png)

### 5.	Membuat Slave pada UML MOJOKERTO
-	nano /etc/bind/named.conf.local pada MALANG
-	service bind9 restart pada MALANG
-	nano /etc/bind/named.conf.local pada MOJOKERTO
-	service bind9 restart pada MOJOKERTO

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98974802-e6cc8180-2547-11eb-9603-b07171d75b4d.png)
![image](https://user-images.githubusercontent.com/57068224/98974812-e8964500-2547-11eb-9578-7722838147fb.png)

### 6.	Membuat Delegasi yang pada MOJOKERTO yang mengarah ke PROBOLINGGO
-	nano /etc/bind/jarkom/semerue10.pw pada MALANG
-	nano /etc/bind/named.conf.options
-	allow-query{ any; };
-	nano /etc/bind/named.conf.local
-	service bind9 restart
-	nano /etc/bind/named.conf.options pada MOJOKERTO
-	allow-query{any;};
-	nano /etc/bind/named.conf.local
-	mkdir /etc/bind/delegasi
-	cp /etc/bind/db.local /etc/bind/delegasi/gunung.semerue10.pw
-	nano /etc/bind/delegasi/gunung.semerue10.pw
-	service bind9 restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98974832-efbd5300-2547-11eb-8e1d-c70ff2e4eedd.png)
![image](https://user-images.githubusercontent.com/57068224/98974837-f21fad00-2547-11eb-92d6-f66c965ecb30.png)
![image](https://user-images.githubusercontent.com/57068224/98974847-f51a9d80-2547-11eb-92c3-a7ce50c1a953.png)
![image](https://user-images.githubusercontent.com/57068224/98974852-f64bca80-2547-11eb-9941-e99ec62e6a00.png)
![image](https://user-images.githubusercontent.com/57068224/98974859-f8ae2480-2547-11eb-8c5b-7013bf6c805f.png)

### 7.	Membuat subdomain naik.gunung.semerue10.pw yang mengarah ke PROBOLINGGO
-	nano /etc/bind/delegasi/gunung.semerue10.pw
-	service bind9 restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98974939-0cf22180-2548-11eb-9698-5602f3423ae0.png)
![image](https://user-images.githubusercontent.com/57068224/98974951-0f547b80-2548-11eb-97b1-4c618aa05be4.png)

### 8.	Mengatur webserver semerue10.pw
-	wget 10.151.36.202/semeru.pw.zip pada /var/www/ di PROBOLINGGO
-	extract pada folder semerue10.pw
-	copy 000default menjadi semerue10.pw.conf
-	tambahkan ServerName dan ServerAlias
-	ubah DocumentRoot menjadi /var/www/semerue10.pw
-	a2ensite semerue10.pw.conf
-	apache restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98974992-21361e80-2548-11eb-99b4-f41bbcae3a18.png)
![image](https://user-images.githubusercontent.com/57068224/98975004-24310f00-2548-11eb-853f-a8269ccda209.png)


### 9.	Awalnya web dapat diakses menggunakan alamat http://semeruyyy.pw/index.php/home. Karena dirasa alamat urlnya kurang bagus, maka (9) diaktifkan mod rewrite agar urlnya menjadi http://semeruyyy.pw/home.
-	Nano /var/www/semerue10.pw/.htaccsess
-	A2enmod rewrite
-	Apache restart
-	RewriteEngine On = untuk flag bahwa menggunakan module rewrite
-	RewriteCond %{REQUEST_FILENAME} !-d = aturan tidak akan jalan ketika yang diakses adalah directory (d)
-	RewriteRule ^([^\.]+)$ $1.php [NC,L] = $1 adalah parameter input yang akan dicari oleh webserver
-	Edit semerue10.pw.conf pada PROBOLINGGO
-	Apache restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98975123-504c9000-2548-11eb-915b-d1d24db496a4.png)
![image](https://user-images.githubusercontent.com/57068224/98975133-52165380-2548-11eb-9cbf-e012e670cf8f.png)
![image](https://user-images.githubusercontent.com/57068224/98975141-53e01700-2548-11eb-95d8-0a9a3bc41aca.png)

### 10.	Web http://penanjakan.semeruyyy.pw akan digunakan untuk menyimpan assets file yang memiliki DocumentRoot pada /var/www/penanjakan.semeruyyy.pw
-	Edit penanjakan.semerue10.pw.conf pada PROBOLINGGO

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98975150-56db0780-2548-11eb-863e-6f2d5a222505.png)
![image](https://user-images.githubusercontent.com/57068224/98975156-593d6180-2548-11eb-9461-e8b55ebc3103.png)

### 11.	Pada folder /public dibolehkan directory listing namun untuk folder yang berada di dalamnya tidak dibolehkan.
-	Edit penanjakan.semerue10.pw.conf pada PROBOLINGGO
-	Tambahkan +Indexes pada public
-	Tambahkan -Indexes pada seluruh folder yang ada di public
-	Apache restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98975208-69edd780-2548-11eb-9930-b4d7df368dad.png)
![image](https://user-images.githubusercontent.com/57068224/98975215-6c503180-2548-11eb-84a8-0b6b6ec50fb4.png)

### 12.	Untuk mengatasi HTTP Error code 404, disediakan file 404.html pada folder /errors untuk mengganti error default 404 dari Apache.
-	Tambahkan error document pada penanjakan.semerue10.pw.conf
-	Apache restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98975225-6f4b2200-2548-11eb-8007-df8e3c5a99e6.png)
![image](https://user-images.githubusercontent.com/57068224/98975242-72461280-2548-11eb-9ad0-8c39baa5281a.png)

### 13.	Untuk mengakses file assets javascript awalnya harus menggunakan url http://penanjakan.semeruyyy.pw/public/javascripts. Karena terlalu panjang maka dibuatkan konfigurasi virtual host agar ketika mengakses file assets menjadi http://penanjakan.semeruyyy.pw/js.
-	Tambahkan Alias "/js" "/var/www/penanjakan.semerue10.pw/public/javascripts" pada penanjakan.semerue10.pw.conf
-	+Indexes pada folder javascripts

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98975313-88ec6980-2548-11eb-8af0-8d8fca90ac0a.png)
![image](https://user-images.githubusercontent.com/57068224/98975320-8b4ec380-2548-11eb-8702-06a9b7c527e7.png)
![image](https://user-images.githubusercontent.com/57068224/98975331-8db11d80-2548-11eb-822d-b34321fa97fb.png)

### 14.	Untuk web http://gunung.semeruyyy.pw belum dapat dikonfigurasi pada web server karena menunggu pengerjaan website selesai. (14) sedangkan web http://naik.gunung.semeruyyy.pw sudah bisa diakses hanya dengan menggunakan port 8888. DocumentRoot web berada pada /var/www/naik.gunung.semeruyyy.pw.
-	Membuat naik.gunung.semerue10.pw.conf pada PROBOLINGGO
-	Ubah port menjadi 8888
-	Tambahkan listen 8888 pada file ports pada folder apache2

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98975343-91dd3b00-2548-11eb-8153-3ddb178a4072.png)
![image](https://user-images.githubusercontent.com/57068224/98975352-93a6fe80-2548-11eb-9a14-b9c4217b5508.png)
![image](https://user-images.githubusercontent.com/57068224/98975359-96095880-2548-11eb-8d0b-2f35913dfbc4.png)


### 15.	Dikarenakan web http://naik.gunung.semeruyyy.pw bersifat private (15) Bibah meminta kamu membuat web http://naik.gunung.semeruyyy.pw agar diberi autentikasi password dengan username “semeru” dan password “kuynaikgunung” supaya aman dan tidak sembarang orang bisa mengaksesnya.
-	htpasswd -c /etc/apache2/.htpasswd semeru
-	masukkan password kuynaikgunung
-	edit naik.gunung.semerue10.pw.conf
-	apache restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98975428-ae797300-2548-11eb-938f-1a006b573daf.png)
![image](https://user-images.githubusercontent.com/57068224/98975436-b0433680-2548-11eb-8df4-d76849c66237.png)

### 16.	Karena dirasa kurang profesional, maka setiap Bibah mengunjungi IP PROBOLINGGO akan dialihkan secara otomatis ke http://semeruyyy.pw.
-	Edit 000-default.conf
-	Ubah DocumentRoot menjadi menuju ke semerue10.pw
-	Apache restart

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98975448-b46f5400-2548-11eb-81dd-456a3887c51c.png)
![image](https://user-images.githubusercontent.com/57068224/98975456-b6391780-2548-11eb-97b3-30b7fe015a06.png)

### 17.	Karena pengunjung pada /var/www/penanjakan.semeruyyy.pw/public/images sangat banyak maka semua request gambar yang memiliki substring “semeru” akan diarahkan menuju semeru.jpg.

Gambar :

![image](https://user-images.githubusercontent.com/57068224/98975466-b89b7180-2548-11eb-8c21-10b4246ef9aa.png)
![image](https://user-images.githubusercontent.com/57068224/98975473-bafdcb80-2548-11eb-928d-a6cf8c91e6b3.png)
