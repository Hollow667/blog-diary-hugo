---
title: 'Trik Menyembunyikan Source Code file HTML'
date: 2017-01-03T20:33:00.002-08:00
draft: false
aliases: [ "/2017/01/trik-menyembunyikan-source-code-file-html.html" ]
tags : [Knowledge]
---

[![](https://4.bp.blogspot.com/-8-ItSks9ABk/WGx1S1gQrNI/AAAAAAAABqQ/9jKK4ELffTAiW6ygSxlSusW60LiceJ8MwCLcB/s640/1_008.jpg)](https://4.bp.blogspot.com/-8-ItSks9ABk/WGx1S1gQrNI/AAAAAAAABqQ/9jKK4ELffTAiW6ygSxlSusW60LiceJ8MwCLcB/s1600/1_008.jpg)

  
Holaa para pengunjung setia lasttrick 😁  
kali ini gw mo ngebagiin cara meng-encrypt source code html, ya sebenarnya jga buat apa html di encrypt :v beberapa orang memang ada yang kurang suka kalo script nya di edit / di modifikasi tanpa se-izin si pembuat, nah cara ini bisa di lakukan untuk mengecoh script kiddie saat melakukan aksinya 😆 karena kebanyakan pasti pada bingung dimana mana ini tag htmlnya? hhh  
  
Caranya begini:  
**1**. Kunjungi [situs ini](http://ouo.io/xES0QE)  
**2**. Siapkan kode html kalian, copas ke box yang di sediakan, lalu klik "_Obfuscate!_"  

**Screenshot**

[![](https://3.bp.blogspot.com/-5n9Jc9EdUGo/WGx1SeRD7RI/AAAAAAAABqY/q8v99ovozU0XGofgZVsmfI74BxjU95XEACEw/s640/1_006.jpg)](https://3.bp.blogspot.com/-5n9Jc9EdUGo/WGx1SeRD7RI/AAAAAAAABqY/q8v99ovozU0XGofgZVsmfI74BxjU95XEACEw/s1600/1_006.jpg)

**3**. Setelah itu akan muncul pop-up download file, simpan saja file javascript (.js) nya  
**4**. Upload ke hosting kalian jika make javascript external, dan jangan lupa tambahkan tag ini :  
  

> \[<script language="Javascript" src="sitemu.com/path/hasil-script-tadi.js"></script>\]

  
**5**. Jika make internal tinggal selipin code hasil enkripan ke :  
  

> \[<html><head><script type="text/javascript">Script di dalam file javascript yang di download tadi taruh disini</script>\]

  
**6**. Save, dan lihat hasilnya 😎  
  

**Coba juga [cara ini](http://blog.yuzaway.com/2016/05/cara-encrypt-file-html-ke-javascript.html) gan !**

  
Sekian dulu tutorial hari ini,  
Semoga Bermanfaat :)