---
title: 'Alasan Kenapa Website Pemerintah Mudah di Deface'
date: 2016-06-02T06:16:00.000-07:00
draft: false
aliases: [ "/2016/06/alasan-kenapa-website-pemerintah-mudah.html" ]
tags : [Knowledge]
---

[![](https://3.bp.blogspot.com/-NXitXvrcTWA/WD0mk7OuU1I/AAAAAAAABb0/N4vfO_oJW6cI5svwx-bezDSAcB4zaDNHwCLcB/s320/legobug.jpg)](https://3.bp.blogspot.com/-NXitXvrcTWA/WD0mk7OuU1I/AAAAAAAABb0/N4vfO_oJW6cI5svwx-bezDSAcB4zaDNHwCLcB/s1600/legobug.jpg)

  
Yo! seperti di judul. kali ini saya akan membahas kenapasih website pemerintah kita ini mudah di deface?  
Mari kita pelajari sedikit demi sedikit, kemungkinan hal ini akan berkembang menjadi lebih lebar lagi.  
  
Kita telaah dari sisi Defacer & Webmaster :  
  
**Defacer** setiap hari selalu mencari celah keamanan website agar bisa di deface, melakukan penelitian terhadap sourcecode yang ada, melihat update vulnerability dari website-website security yang ada di jagad raya. Berdiskusi di forum untuk menemukan dan memecahkan sesuatu yang tidak bisa dipecahkan. Hal inilah yang biasanya hampir tidak pernah dilakukan oleh Webmaster & Administrator. Defacer, bisa saja terdiri dari banyak orang yang berbeda-beda dan berasal dari lokasi mana saja di dunia ini, misalkan: Indonesia, Turki, Brazil, India, Tunisia, dsb. Oleh sebab itu bisa kita golongkan bahwa defacer merupakan sebuah kumpulan orang banyak.  
  
**Administrator / Webmaster** biasanya terdiri dari beberapa orang saja, bisa 1-3 orang saja. Administrator / Webmaster bertugas untuk mengatur dan mengurus website. Namun, entah kenapa kebanyakan webmaster & administrator website pemerintah Indonesia kebanyakan menggunakan layanan instant public (hosting, opensource cms, dsb), alangkah baiknya bila situs-situs pemerintah memiliki suatu badan tersendiri yang mengurusi hal ini (**dalam bayangan**).  
  
**Dari penjelasan di atas, terdapat beberapa kelebihan Defacer daripada Webmaster:**  
  
1\. Defacer unggul dalam jumlah, karena defacer bisa siapa saja di dunia ini.  
2\. Defacer bergerak setiap hari mengikuti perkembangan security.  
3\. Defacer mencoba dan melakukan research terdahap kelemahan-kelemahan di website setiap saat.  
  
Kita bisa melihat beberapa website pemerintah Indonesia yang di hack disini:  
[**http://zone-h.org/archive/filter=1/domain=go.id/fulltext=1/page=1**](http://adf.ly/313683/http://zone-h.org/archive/filter=1/domain=go.id/fulltext=1/page=1)  
  
**Ada beberapa alasan mengapa website pemerintah mudah di deface:**  
  
1\. **Penggunaan CMS yang free dan opensource tanpa adanya modification**. Sehingga keseluruhan konfigurasi menggunakan default konfigurasi, hal ini memudahkan para defacer untuk menemukan informasi file, directory, source, database, user, connection, dsb.  
2\. **Tidak updatenya source atau tidak menggunakan versi terakhir dari CMS**. Hal ini sangat rentan, karena security issue terus berkembang seiring masuknya laporan dan bugtrack terhadap source, kebanyakan hal inilah yang menjadi sebab website mudah dideface.  
3\. **Tidak pernah ada research yang mendalam dan detail mengenai CMS sebelum digunakan & di implementasikan**. Sehingga pemahaman dan pengetahuan dari webmaster hanya dari sisi administrasinya saja, tidak sampai ke level pemahaman sourcecode.  
4\. **Tidak adanya audit trail atau log yang memberikan informasi lengkap mengenai penambahan, pengurangan, perubahan yang terjadi di website baik source, file, directory, dsb**. Sehingga kesulitan untuk menemukan, memperbaiki dan menghapus backdoor yang sudah masuk di website.  
5\. **Jarang melakukan pengecekan terhadap security update, jarang mengunjungi dan mengikuti perkembangan yang ada di situs-situs security jagad maya**. Sehingga website sudah keduluan di deface oleh defacer sebelum dilakukan update dan patch oleh webmaster.  
6\. **Kurangnya security awareness dari masing-masing personel webmaster & administrator**. Sehingga kewaspadaan terhadap celah-celah keamanan cukup minim, kadangkala setelah website terinstall dibiarkan begitu saja. Kurangnya training dan kesadaran akan keamanan website seperti ini akan menjadikan website layaknya sebuah istana yang tak punya benteng.  
  

**Berikut screenshoot  Dari Zone-H.Org OpenSource CMS yang memiliki vulnerability**
-----------------------------------------------------------------------------------

  
**Vulnerability OpenSource CMS By Telematika.Co.Id**  
![](http://farm6.static.flickr.com/5029/5602690140_fb8caf7571_z.jpg "Software Telematika .Co.ID Vuln")  
**Vulnerability OpenSource CMS By Joomla.Org – Joomla 1.5**  
![](http://farm6.static.flickr.com/5310/5602105785_a6b58ddc90_z.jpg "Joomla 1.5 Vulnerability")  

### **Untuk teman-teman Webmaster / Administrator website pemerintah, ada beberapa saran yang mungkin bermanfaat untuk dapat di implementasikan:**

  
1\. **Wajib untuk mengikuti perkembangan source** dari source website yang digunakan, backuplah website dan database sebelum dilakukan update.  
2\. **Kebanyakan defacer telah memasang backdoor ketika telah berhasil melakukan deface website**, hal ini dimungkinkan agar dapat melakukan deface ulang terhadap website. **Wajib untuk memeriksa perubahan folder, file, database dan source terakhir dari website**.  
3\. **Pelajarilah lebih dalam mengenai dasar-dasar hacking dan antisipasinya (RFI, LFI, CSRF, SQL Injection, XSS, Exploit, Dsb)** karena artikel ini sudah banyak bertebaran di Internet. Semakin banyak tahu & mengerti tentang sebuah kelemahan website dari dasar-dasar hacking, maka akan semakin banyak tahu pula bagaimana cara mengatasinya.  
4\. **Sering-seringlah berdiskusi di forum dan milist yang berkaitan dengan perangkat serta aplikasi yang mensupport website anda**, baik dari sisi operating system, tempat hosting, bugtrack milist, developer milist, dsb. Hal ini bertujuan agar informasi vulnerability dapat dipatch lebih cepat sebelum defacer beraksi.  
5\. **Hardening website dan source wajib dilakukan**, misalkan jangan menggunakan “default configuration”, aturlah sedemikian rupa “configuration website” dengan memperhatikan: permission, access level, indexing, database connection, database configuration, password dan user management.  
6\. **Gunakanlah tambahan plugin / component yang tepat**, sehingga dapat meminimalisasi terjadinya kegiatan defacing dari thirdparty. Pastikan hasil review & ranking plugin bereputasi baik dan sudah di verified oleh penyedia CMS yang bersangkutan.  
7\. **Lakukanlah penetration testing terhadap website**, baik secara lokal maupun langsung di website. Banyak tools penetration testing yang bisa digunakan: Nexus, Acunetix, dsb. Tapi yang paling bagus dan lebih cepat adalah, copy source dan database website, Install di local computer, kemudian lakukanlah penetration testing. Updatelah website bila ditemukan vulnerability.  
8\. **Backdoor, baik (php, asp, perl, phyton) dikenali dengan baik oleh beberapa Antivirus**, ada bisa cleaning dengan melakukan scanning terhadap source website secara local. Apabila tidak dikenali, terpaksa anda harus mencari secara manual.  
  

### **Pada bagian ini, saya akan mencoba memberikan salah satu solusi apabila website sudah terlanjur dideface, silakan menggunakan langkah berikut:**

  
1\. **Download source & database yang ada di website untuk backup**. Hal ini untuk berjaga-jaga apabila langkah yang kita lakukan gagal, tetapi apabila konfigurasi & file benar dan lengkap dijamin 100% berhasil, terkecuali ada sesuatu yang terlewatkan.  
2\. **Download source CMS versi terbaru dari website penyedia CMS**, misalkan: **www.drupal.org, www.joomla.org, www.wordpress.org**, dsb.  
3\. **Lakukanlah perbaikan database secara lokal, berjaga-jaga apabila backdoor ada di database**. Biasanya didalam database ada access user tidak dikenal yang akses levelnya sama dengan Administrator.  
4\. **Install CMS yang tadi sudah di download di web hosting**. Kemudian lakukanlah konfigurasi: database, file permission, directory permission. **Jangan menggunakan default configuration**, modifikasilah konfigurasi-konfigurasi yang ada agar lebih powerfull.  
5\. **Kemudian instalasi component**: Themes, Plugin, Component, dsb. Gunakanlah yang paling update, atau source baru dari komponen yang akan di Install (**Fresh Install Component**).  
6\. **Kemudian update database**, dengan login ke Database Control Panel (phpMyAdmin, DB Admin, cPanel Database, dsb). Setelah anda melakukan login, maka importlah database.  
7\. **Gantilah username Administrator & Password menggunakan nama yang lebih Unik**, jangan menggunakan user (admin, administrator, adm1n, dsb) gunakanlah yang lebih powerful dan susah untuk di tebak untuk menghindari bruteforce, gunakanlah alias untuk menampilkan username administrator di web content.  
  
**Semoga sedikit sharing mengenai keamanan website ini berguna buat para sahabat-sahabat Webmaster & Administrator Website.**  
  
\*Dikutip dari berbagai sumber  
Semoga Bermanfaaat :)  
Keep save & secure..