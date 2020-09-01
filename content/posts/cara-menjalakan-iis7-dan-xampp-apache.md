---
title: 'Cara Menjalakan IIS7 dan XAMPP (Apache) di Windows'
date: 2016-08-13T20:38:00.000-07:00
draft: false
aliases: [ "/2016/08/cara-menjalakan-iis7-dan-xampp-apache.html" ]
tags : [Knowledge]
---

[![](https://1.bp.blogspot.com/--TBvCST2JBs/V6_e_CKE1iI/AAAAAAAAA9Q/fyCW52dvTvQEXGui8KPGlqSsZNCBLxBTQCLcB/s400/iis7xamp.png)](https://1.bp.blogspot.com/--TBvCST2JBs/V6_e_CKE1iI/AAAAAAAAA9Q/fyCW52dvTvQEXGui8KPGlqSsZNCBLxBTQCLcB/s1600/iis7xamp.png)

  
Setelah sekian lama nggak ngepost, mumpung ada wktu jdi dbikin tutorial ini, hehe  
Buat para developer pasti pgen tau kan sensasi mnjalankan 2 web server dalam satu machine,  
Untuk mmbantu jga yg mau belajar bikin project, riset riset, experimen :v  
Nah pada tutorial ini gw mo share cara setting nya,  
Pada intinya kita hanya butuh merubah portnya saja biar ngga' tabrakan bos,  
Oke ya, lngsung ke tutor nya :  
  
**A. Setting Port Xampp**  
**1.** Lu hrus tau dlu direktori xampp nya :v . direktori default xampp ada di c:\\xampp\\  
**2.** Sekarang masuk ke \\xampp\\apache\\conf  
**3.** Biar aman, backup dlu file "httpd.conf". Krn file ini yg kita konfigurasi  
**4.** Rename terserah lu, klo gw jadi gini "httpd.conf.bak"  
**5.** Buka file httpd.conf dgn text editor, make notepad / notepad++ terserah  
**6.** Cari text :  
_a._ Listen 80  
(Defaultnya ada di line 47)  
ganti menjadi Listen 8080  
_b._ ServerName localhost:80  
(Defaultnya ada di line 181)  
ganti menjadi ServerName localhost:8080  
**7.** Selanjutnya masuk ke \\xampp\\apache\\conf\\extra  
**8.** Buka file httpd-ssl.conf (bisa di backup dlu, bwat jaga")  
**9.** Cari text:  
_a._ Listen 443  
Ubah ke 449  
_b._ <VirtualHost \_default\_:443>  
Ubah ke <VirtualHost \_default\_:449>  
_c._ ServerName www.example.com:443 / ServerName localhost:449  
NOTE:  Knpa ada dua? Krn di versi xampp berbeda", ada dua kmungkinan, jadi coba satu".  
Ubah ke ServerName www.example.com:449 / ServerName localhost:449  
**10.** Setting selesai, silahkan di jalankan lgi xampp nya. Start dlu di XAMPP Control Panel nya, lalu akses ke _http://127.0.0.1:8080/_ atau _http://localhost:8080/_  
**11.** Doc root ada di \\xampp\\htdocs  
  

Belum Terinstall XAMPP ? Masuk [sini](https://www.apachefriends.org/download.html) stah

  
**B. Setting Port IIS 7**  
**1.** Tidak perlu di setting portnya  
**2.** IIS jga tidak perlu di Start dlu sperti halnya xampp, karena iis otomatis running saat windows jalan  
**3.** Untuk aksesnya, lngsung ketik: _localhost_  
**4.** Doc root ada di C:\\inetpub\\wwwroot  
  

Belum Terinstall IIS 7 ? Masuk [sini](http://www.yuzac0der.id/2016/05/menjalankan-web-server-iis-windows-10.html) ster

  
Semoga bermanfaat ^.^