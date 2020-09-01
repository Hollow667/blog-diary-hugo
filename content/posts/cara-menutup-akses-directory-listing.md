---
title: 'Cara Menutup Akses Directory Listing'
date: 2016-12-31T08:58:00.001-08:00
draft: false
aliases: [ "/2016/12/cara-menutup-akses-directory-listing.html" ]
tags : [Knowledge]
---

[![](https://1.bp.blogspot.com/-_C3oRumylQ0/WGfesACFFVI/AAAAAAAABoA/mfbNqMDnZ0kBlC0AKg7rejCJXmHXqcelACLcB/s640/Selection_002.jpg)](https://1.bp.blogspot.com/-_C3oRumylQ0/WGfesACFFVI/AAAAAAAABoA/mfbNqMDnZ0kBlC0AKg7rejCJXmHXqcelACLcB/s1600/Selection_002.jpg)

  
\*Sorry text di gambar typo hhh  
Haloo kawan,  
yo! kali ini gw mo ngebahas directory listing, pasti sudah tidak asing lagi kan kalo sudah lihat gambar diatas, pada dasarnya jika tidak ada file index.html/.php di suatu web maka akan terlihat jelas isi-isi file di dalamnya, nah kali ini gw kasih trik menutupi suatu directory tanpa harus membuat file index  
  
Ok langsung ke langkahnya saja kawan:  
  
**1**. Kita perlu membuat file .htaccess  
NOTE: Secara default file dengan awalan . (dot) akan dibaca sebagai hidden file, so kita perlu mensetting sedikit seperti ini langkahnya, buka CPanel/Panel lain > masuk File Manager > lihat bagian kanan atas, klik SETTING > Centang "Show Hidden Files (dotfiles)"  

_Screenshot_

[![](https://2.bp.blogspot.com/-YjCx1fALG2Q/WGfhGnjkKWI/AAAAAAAABoI/hrldJZt8fhcbv7zzT3ghbZPK0SkpUOCSgCLcB/s640/Selection_003.jpg)](https://2.bp.blogspot.com/-YjCx1fALG2Q/WGfhGnjkKWI/AAAAAAAABoI/hrldJZt8fhcbv7zzT3ghbZPK0SkpUOCSgCLcB/s1600/Selection_003.jpg)

**2**. Buat file baru dengan nama .htaccess  
**3**. Buka dan edit file .htacess nya, lalu masukkan code dibawah  

> \[RewriteEngine on  
> RewriteCond %{REQUEST\_FILENAME} !-f  
> RewriteCond %{REQUEST\_FILENAME} !-d  
> RewriteRule . index.php  
> Options All -Indexes\]

**4**. Kemudian save, dan lihat hasilnya akan nampak seperti gambar dibawah  

[![](https://2.bp.blogspot.com/-t3B9oT76z4o/WGfikEOD5xI/AAAAAAAABoQ/hBK4xO6xUH46UgnKSS3g08nVwyrb54xygCLcB/s640/Selection_004.jpg)](https://2.bp.blogspot.com/-t3B9oT76z4o/WGfikEOD5xI/AAAAAAAABoQ/hBK4xO6xUH46UgnKSS3g08nVwyrb54xygCLcB/s1600/Selection_004.jpg)

  
Sekian dulu tutor hari ini, oh iya ini sekaligus artikel penutup di tahun 2016, semoga di 2017 nanti semuanya yang kita lakukan akan bermanfaat buat semua orang, dan tentunya akan menjadi yang lebih baik dari hari sekarang, keep share 😇  
  
Semoga bermanfaat,  
HAPPY NEW YEAR 2017  
^\_^