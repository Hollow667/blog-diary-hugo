---
title: 'Cara menjalankan file .php di cmd'
date: 2016-05-11T08:32:00.000-07:00
draft: false
aliases: [ "/2016/05/cara-menjalankan-file-php-di-cmd.html" ]
tags : [Knowledge]
---

[![](https://1.bp.blogspot.com/-48WV--UdCgM/VyiUxucVFNI/AAAAAAAAAf4/f04kQoG21vEqtIODM21Dc8aatqJTVJGyACLcB/s200/cmd.png)](https://1.bp.blogspot.com/-48WV--UdCgM/VyiUxucVFNI/AAAAAAAAAf4/f04kQoG21vEqtIODM21Dc8aatqJTVJGyACLcB/s1600/cmd.png)

\[UPDATED 8:48 AM 5/20/2016\]  
  
Langsung aja ya, pertama install dulu webservernya, kali ini menggunakan iis, krna biar tdak ribet" kyak xampp/lamp/dll, kita harus masuk ke php module di dir xampp. Klo mke xampp jga hrus d aktifkan dlu kan lwat control panelnya bwat buka webserver, dll. Ribeet!  
IIS ini lngsng jalan wktu windows di nyalakan..  
Jika blum terinstall IIS ikutin step-stepnya [DISINI](http://yuzanotes.blogspot.co.id/2016/05/menjalankan-web-server-iis-windows-10.html)  
  

**LANGKAH LANGKAH**

  
\*Harus terinstall IIS, jika belum baca lagi dari atas  
1\. Download dulu Web Platform Installer [disini](http://www.iis.net/learn/install/web-platform-installer/web-platform-installer-direct-downloads)  
2\. Buka iis manager, scroll kebawah ke bagian Management, nah disitu ada Web Platform Installer, klik kanan > Open feature. Lebih jelasnya lihat gambar dibawah  

[![](https://4.bp.blogspot.com/-V9vVmctgiJY/Vz5o4BoQ96I/AAAAAAAAAmo/TB3PB8dYmD8oBw4zOfrnp2aEXmJaAwHUACLcB/s640/wpi.png)](https://4.bp.blogspot.com/-V9vVmctgiJY/Vz5o4BoQ96I/AAAAAAAAAmo/TB3PB8dYmD8oBw4zOfrnp2aEXmJaAwHUACLcB/s1600/wpi.png)

3\. Tulis di search "php" pilih php versi 5.3.28 (serah lu mo pilih versi brapa) klik Add, lalu Install. Lihat gambar lebih jelasnya (gmbar di bawah sudah ter install jdi udah Installed :v pas belum di install lupa ga' d ss)  

[![](https://3.bp.blogspot.com/-H1kKscr2WBk/Vz5o-T_Z-yI/AAAAAAAAAms/5SdPFGlYDIAZYSDA4PKOMcppEQWObnu9ACKgB/s640/Screenshot_49.png)](https://3.bp.blogspot.com/-H1kKscr2WBk/Vz5o-T_Z-yI/AAAAAAAAAms/5SdPFGlYDIAZYSDA4PKOMcppEQWObnu9ACKgB/s1600/Screenshot_49.png)

4\. Setelah di klik install mncul popup, pilih "I accept"  

5\. ikutin intruksi yg kluar d layar smpe selesai, gampang kok ini  
6\. Langkah terakhir, kita tambahkan path environment variable  
7\. Buka Control Panel > pilih System and Security > pilih tab Advanced > klik tombol "Environment Variables". Pada kolom **System Variables** cari variable _Path_, pilih lalu tekan tombol _edit_. Tambahkan 'C:\\Program Files (x86)\\PHP\\v5.6' di akhir value-nya, terserah sih mao di taruh mana yg penting masuk. Lebih jelasnya lihat ss dibawah  

[![](https://1.bp.blogspot.com/-aIqHqvKx6Ss/Vz5sJ7T8dOI/AAAAAAAAAm8/aqePuXvfPuwMGlO5DKvoDJQ1-dq7_mCugCLcB/s640/Screenshot_50.png)](https://1.bp.blogspot.com/-aIqHqvKx6Ss/Vz5sJ7T8dOI/AAAAAAAAAm8/aqePuXvfPuwMGlO5DKvoDJQ1-dq7_mCugCLcB/s1600/Screenshot_50.png)

8\. Klik OK, lalu restart pc,lepi lu.  
9\. Selesai.. Semoga Bermanfaat :)