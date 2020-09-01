---
title: 'Web Shell Detector'
date: 2016-08-20T06:49:00.000-07:00
draft: false
aliases: [ "/2016/08/web-shell-detector.html" ]
tags : [Source Code]
---

[![](https://3.bp.blogspot.com/-9lxmQUz9_3k/V7hXlQro2EI/AAAAAAAABAk/TN3fNVBdZGQpbwyeUZtmHX34PLeUv-kswCLcB/s640/Screenshot_30.png)](https://3.bp.blogspot.com/-9lxmQUz9_3k/V7hXlQro2EI/AAAAAAAABAk/TN3fNVBdZGQpbwyeUZtmHX34PLeUv-kswCLcB/s1600/Screenshot_30.png)

  
Pasti gak asing lagi di telinga. Nama "backdoor" udah seperti makanan sehari-hari buat para developer web, programmer web, dan yg biasa nongkrong di underground network :3  
Nah pada tutorial kali ini, gw mau share script yang berguna banget buat developer dan programmer web atau yang lagi belajar web sekuriti eeiits, mksudnya security. Bukan satpam loh ya -\_-  
Script ini berfungsi untuk menscan file-file (yang di curigai sebagai suspicious/shell) termasuk file yang di dalam folder, sampai ke akar" nya.  
Pasti penasaran dong gmna cara kerjanya script ini.  
  
Script ini dibuat oleh orang asal Israel dengan codename Maxim,  
Dibuat 2 tahun yang lalu,  
Dia membuat project-project dan salah satunya Web Shell Detector ini,  
Jika Ingin lihat projectnya bisa ke [Github](https://github.com/emposha/)  
Oke lanjut ke cara penggunaannya ya, begini :  
  
**1**. Copas script dibawah, simpan dengan nama shelldetect.php  
  
  
**2**. Copas script dibawah, simpan dengan nama shelldetect.db  
  
  
**3\.** Simpan dalam 1 folder  
**4**. Jalankan dengan memanggil name file. Contoh site.com/shelldetect.php atau bisa juga dijalankan di server local / localhost  
  
**NOTE** :  
2 File di atas harus di simpan satu folder, lebih baik jika disimpan dan dijalankan di /public\_html/  
  
**Screenshot :**  
  

JIKA TIDAK DITEMUKAN FILE MENCURIGAKAN

[![](https://3.bp.blogspot.com/-oTg4Vmfzvxc/V7hdR2t8kyI/AAAAAAAABA0/LlCvmLD9d1MTIpx5ROdluot2l3rKhA1tACEw/s640/Screenshot_31.png)](https://3.bp.blogspot.com/-oTg4Vmfzvxc/V7hdR2t8kyI/AAAAAAAABA0/LlCvmLD9d1MTIpx5ROdluot2l3rKhA1tACEw/s1600/Screenshot_31.png)

  

JIKA DITEMUKAN FILE YANG MENCURIGAKAN

[![](https://3.bp.blogspot.com/-_Rjd1pQFWEY/V7hdR7q0_8I/AAAAAAAABA4/ggZRMHAHgzQgnZBm1tkllHeKgola6zbPwCEw/s640/Screenshot_33.png)](https://3.bp.blogspot.com/-_Rjd1pQFWEY/V7hdR7q0_8I/AAAAAAAABA4/ggZRMHAHgzQgnZBm1tkllHeKgola6zbPwCEw/s1600/Screenshot_33.png)

[![](https://1.bp.blogspot.com/--voPDo0aDx0/V7hdR5LklrI/AAAAAAAABA8/rugfJ1zJrSceLKxtVLWBB3JfjPyoA_hXACEw/s640/Screenshot_34.png)](https://1.bp.blogspot.com/--voPDo0aDx0/V7hdR5LklrI/AAAAAAAABA8/rugfJ1zJrSceLKxtVLWBB3JfjPyoA_hXACEw/s1600/Screenshot_34.png)

  

Semoga Bermanfaat :D