---
title: 'Cara setting force download files dengan .htaccess'
date: 2016-03-27T07:17:00.000-07:00
draft: false
aliases: [ "/2016/03/cara-setting-force-download-files.html" ]
tags : [Knowledge]
---

[![](https://4.bp.blogspot.com/-MGqiClcjoJQ/VvfoqOe8R8I/AAAAAAAAAa0/Ku0ishQSIkY1hzij8rNDVfz0Sl10sxyTQ/s640/Screenshot_30.png)](https://4.bp.blogspot.com/-MGqiClcjoJQ/VvfoqOe8R8I/AAAAAAAAAa0/Ku0ishQSIkY1hzij8rNDVfz0Sl10sxyTQ/s1600/Screenshot_30.png)

gak mao bnyak cincong. lngsung aja ya :'v  

1.  buat file .htaccess di direktori yang agan inginkan
2.  isikan sperti ini.

> ```
> AddType application/octet-stream .csv  
> AddType application/octet-stream .xls  
> AddType application/octet-stream .doc  
> AddType application/octet-stream .avi  
> AddType application/octet-stream .mpg  
> AddType application/octet-stream .mov  
> AddType application/octet-stream .pdf
> ```

4.  Save, kmudian coba sperti gmbar di atas. file akan ke download otomatis tnpa ke buka d browser.

  
**NOTE :**  
untuk `AddType application/octet-stream` `.ekstensinya **; bisa di sesuaikan dengan file yg d inginkan, jika pada gmbar di atas agan bisa menambahkan ini di baris paling bawah**` `AddType application/octet-stream .php.`