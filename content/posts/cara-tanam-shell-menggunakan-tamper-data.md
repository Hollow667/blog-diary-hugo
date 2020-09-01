---
title: 'Cara Tanam Shell menggunakan Tamper Data'
date: 2016-05-03T00:52:00.000-07:00
draft: false
aliases: [ "/2016/05/cara-tanam-shell-menggunakan-tamper-data.html" ]
tags : [Security]
---

Oke, pertama lu harus masuk ke web target. biasanya sih klo make tamper data poc nya: bypass admin > tamper data atau sqli > tamper data.  
  
ALAT TEMPUR :  
\- Download dulu addons Tamper Data untuk [mozilla](https://addons.mozilla.org/id/firefox/addon/tamper-data/) atau [chrome](https://chrome.google.com/webstore/detail/tamper-chrome-extension/hifhgpdkfodlpnlmlnmhchnkepplebkb)  
\- Shell backdoor yg sudah di rename menjadi .php.jpg/.php.png (menyesuaikan target)  
  
LANGKAH - LANGKAH :  
\- Gw asumsikan elu dah ada di dalem web target  
\- Cari tempat upload gambar (apa aja yg penting ada tulisan upload/unggah), biasanya di add photo, upload fav icon, dll.  

Dashboard

[![](https://3.bp.blogspot.com/-zVbc7VyFgYM/VyhKNH5pv4I/AAAAAAAAAeY/DZ8rWCiAbuwVbYuOdNg-A_oEZmvPER17ACLcB/s640/Screenshot_11.png)](https://3.bp.blogspot.com/-zVbc7VyFgYM/VyhKNH5pv4I/AAAAAAAAAeY/DZ8rWCiAbuwVbYuOdNg-A_oEZmvPER17ACLcB/s1600/Screenshot_11.png)

\- Klo nemu tempat uplot image/file, biasanya bisa. Tpi tdak mnutup kmungkinan gagal, jdi d coba dulu aja.  

[![](https://2.bp.blogspot.com/-9suQSJMKjGU/VyhMkJcpXWI/AAAAAAAAAek/JCKbArpIJvIGO50JB6-bmBNGe2wD1i5JwCLcB/s640/Screenshot_12.png)](https://2.bp.blogspot.com/-9suQSJMKjGU/VyhMkJcpXWI/AAAAAAAAAek/JCKbArpIJvIGO50JB6-bmBNGe2wD1i5JwCLcB/s1600/Screenshot_12.png)

\- Buka Tamper Datanya, klik Start Tamper  

[![](https://1.bp.blogspot.com/-L5spqmI0-IA/VyhObj2JWNI/AAAAAAAAAew/hZGz6sk9DIMq4UO7vbJ0NPEcqODw9v4eQCLcB/s640/Screenshot_13.png)](https://1.bp.blogspot.com/-L5spqmI0-IA/VyhObj2JWNI/AAAAAAAAAew/hZGz6sk9DIMq4UO7vbJ0NPEcqODw9v4eQCLcB/s1600/Screenshot_13.png)

\- Klik Choose File, lalu pilih shell mu  

[![](https://4.bp.blogspot.com/-Yl5_Jtu07Q8/VyhPRadHx8I/AAAAAAAAAe4/dNQx7oFYHWs2Somka-27UUHZCcJmZcUsQCLcB/s640/Screenshot_14.png)](https://4.bp.blogspot.com/-Yl5_Jtu07Q8/VyhPRadHx8I/AAAAAAAAAe4/dNQx7oFYHWs2Somka-27UUHZCcJmZcUsQCLcB/s1600/Screenshot_14.png)

\- Klik simpan lalu Tamper  

[![](https://4.bp.blogspot.com/-Rr8HCCVqflk/VyhTg64HSBI/AAAAAAAAAfY/Gg7DZVZGBu0BrGVQ6U5P9d_21aKh7oRFQCKgB/s640/Screenshot_15.png)](https://4.bp.blogspot.com/-Rr8HCCVqflk/VyhTg64HSBI/AAAAAAAAAfY/Gg7DZVZGBu0BrGVQ6U5P9d_21aKh7oRFQCKgB/s1600/Screenshot_15.png)

\- Nanti akan muncul popup, lihat di sbelah kanan, bagian POST\_DATA, pada box scrol ke bawah sampai ktemu nama file shellmu tadi, rename file tsb hilangin .png nya. lebih jealasnya lihat gambar  

[![](https://1.bp.blogspot.com/-W68J1raKxYg/VyhTgvwoDnI/AAAAAAAAAfY/GW4qu1nvTeo8gD68lJVXuehFNq9aKaAYACKgB/s640/Screenshot_16.png)](https://1.bp.blogspot.com/-W68J1raKxYg/VyhTgvwoDnI/AAAAAAAAAfY/GW4qu1nvTeo8gD68lJVXuehFNq9aKaAYACKgB/s1600/Screenshot_16.png)

\- Stelah oke, Klo muncun shell aksesnya brarti shell udah ke upload, jka gk nemu shell akses brarti udh kgak bsa lwat method tamper data ini.  

[![](https://1.bp.blogspot.com/-jXfSD1pnZzk/VyhThOUtthI/AAAAAAAAAfY/tpdw_KTf54Ibwd1y3At3kYtC03teOVdgwCKgB/s640/Screenshot_17.png)](https://1.bp.blogspot.com/-jXfSD1pnZzk/VyhThOUtthI/AAAAAAAAAfY/tpdw_KTf54Ibwd1y3At3kYtC03teOVdgwCKgB/s1600/Screenshot_17.png)

\- Tnggal copas ke address bar deh tuh..  

[![](https://3.bp.blogspot.com/-L6hELphmLJw/VyhThccJKgI/AAAAAAAAAfc/jsav0T_6pqYf_05x-qhWbyF_TXI_TG7eACKgB/s640/Screenshot_18.png)](https://3.bp.blogspot.com/-L6hELphmLJw/VyhThccJKgI/AAAAAAAAAfc/jsav0T_6pqYf_05x-qhWbyF_TXI_TG7eACKgB/s1600/Screenshot_18.png)

\- Terus upload shell kesayanganmu, yudh kalo udah sampe sini, trserah mau diapain.  

[![](https://2.bp.blogspot.com/-NRxB_gmNDg0/VyhTka439AI/AAAAAAAAAfc/EYwQ9jIvkg4i81eRbajUgL3RfFV8AT2SgCKgB/s640/Screenshot_19.png)](https://2.bp.blogspot.com/-NRxB_gmNDg0/VyhTka439AI/AAAAAAAAAfc/EYwQ9jIvkg4i81eRbajUgL3RfFV8AT2SgCKgB/s1600/Screenshot_19.png)

  
Semoga bermanfaat :)