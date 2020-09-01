---
title: 'Teknik menyembunyikan file (STEGANOGRAFI)'
date: 2016-03-28T00:43:00.000-07:00
draft: false
aliases: [ "/2016/03/teknik-menyembunyikan-file-steganografi.html" ]
tags : [Knowledge]
---

[![](https://indhoarief.files.wordpress.com/2011/03/123455.jpg)](https://indhoarief.files.wordpress.com/2011/03/123455.jpg)

  
**Steganografi** adalah seni dan ilmu menulis pesan tersembunyi atau menyembunyikan pesan dengan suatu cara sehingga selain si pengirim dan si penerima, tidak ada seorangpun yang mengetahui atau menyadari bahwa ada suatu pesan rahasia. Sebaliknya, kriptografi menyamarkan arti dari suatu pesan, tapi tidak menyembunyikan bahwa ada suatu pesan. Kata "steganografi" berasal dari bahasa Yunani _steganos_, yang artinya “tersembunyi atau terselubung”, dan _graphein_, “menulis”. Penjelasan selengkapnya [masuk sini](https://id.wikipedia.org/wiki/Steganografi).  
  
Oke gan, udah paham sama teknik steganografi? blum lengkap ya kya nya klo nggak di praktekkin :'v , ikuti step by step berikut :  

  

1.  Buat folder terserah agan, saya memberi nama folder steganografi dan saya letakkan di dekstop
2.  Masukkan 2 file yang nantinya kita buat untuk sampul (x.jpg) dan satunya file yang kita sembunyikan (ec.php), Buatlah file .rar dari 2 file tadi, biar lebih jelas lihat screenshot disamping.

[![](https://3.bp.blogspot.com/-8CJYxpB0bVI/VvjZt9ZXSaI/AAAAAAAAAbU/_kZzSbjU2NU1nk4d7YzF5FY9y-iNoFMvA/s640/Screenshot_31.png)](https://3.bp.blogspot.com/-8CJYxpB0bVI/VvjZt9ZXSaI/AAAAAAAAAbU/_kZzSbjU2NU1nk4d7YzF5FY9y-iNoFMvA/s1600/Screenshot_31.png)

4.  Setelah jadi, maka ada 3 file yaitu file ec.php , x.jpg , dan steganografi.rar
5.  Persiapan file sudah selesai, Sekarang buka command promt, tekan tombol Window + R, ketik cmd.
6.  Masuk ke direktori tempat kita membuat folder tadi, lihat screenshot di bawah.

[![](https://4.bp.blogspot.com/-IEB5C1bow64/VvjcDM2AsVI/AAAAAAAAAbg/HTilFkxP6iQRiiss7lhXGmRJzu5COYvJw/s640/Screenshot_32.png)](https://4.bp.blogspot.com/-IEB5C1bow64/VvjcDM2AsVI/AAAAAAAAAbg/HTilFkxP6iQRiiss7lhXGmRJzu5COYvJw/s1600/Screenshot_32.png)

8.  Sekarang saatnya kita satukan 2 file tadi, gimana caranya? ketik perintah berikut.

> copy /b x.jpg+steganografi.rar output.jpg

[![](https://4.bp.blogspot.com/-6mdez_H9dUc/Vvjej_WkOeI/AAAAAAAAAbs/SwCQmFmvzu0nJkwuOdxprsvlQlQ2uelTA/s640/Screenshot_33.png)](https://4.bp.blogspot.com/-6mdez_H9dUc/Vvjej_WkOeI/AAAAAAAAAbs/SwCQmFmvzu0nJkwuOdxprsvlQlQ2uelTA/s1600/Screenshot_33.png)

11.  Untuk melihatnya agan bsa buka dengan Winrar :D 

  
**PREVIEW**  
  

[![](https://4.bp.blogspot.com/-t0wntZf3XVg/Vvjf5vbEgPI/AAAAAAAAAb4/Bms8UNCRfr0cY3iLnZXZ7zslEJHM1LqPQ/s640/Screenshot_34.png)](https://4.bp.blogspot.com/-t0wntZf3XVg/Vvjf5vbEgPI/AAAAAAAAAb4/Bms8UNCRfr0cY3iLnZXZ7zslEJHM1LqPQ/s1600/Screenshot_34.png)

File bisa di klik 2 kali dan yang terbuka hanya gambarnya saja (gambar kiri), padahal di dalam gambar trsebut ada file tersembunyi (gambar kanan)

  
Semoga Bermanfaat :)