---
title: Mac (OSX) Kurulumu
isChild: true
---

## Mac (OSX) Kurulumu  {#mac_osx_kurulumu_title}

OSX ile birlikte PHP zaten kurulu halde gelir fakat PHP sürümü güncel ve kararlı sürümden biraz eski olabilir. Lion PHP 5.3.6 ile geliyor. Mountain Lion ise 5.3.10 ile.

OSX'de PHP'yi güncellemek için, bir dizi Mac [Paket Yöneticisi][mac-package-managers] ile paket edinebilirsiniz, [php-osx by Liip][php-osx-downloads] tavsiye edilir. 

Diğer bir seçenek ise PHP'yi [kendinizin derlemesidir][mac-compile], Bu durumda ise Xcode ya da Apple's Mac Developer Center üzerinden ["Command Line Tools for Xcode"][apple-developer] aracının kurulu olduğuna emin olun.

“Hepsi bir arada” olarak adlandırılabilecek, içerisinde PHP, Apache web sunucusu ve MySQL veritabanı sunucusu barındıran, bu servisleri kolay yönetmek için grafik kullanım arayüzü (GUI) bulunan [MAMP][mamp-downloads] uygulamasını da deneyebilirsiniz.

[mac-package-managers]: http://www.php.net/manual/tr/install.macosx.packages.php
[mac-compile]: http://www.php.net/manual/tr/install.macosx.compile.php
[xcode-gcc-substitution]: https://github.com/kennethreitz/osx-gcc-installer
[apple-developer]: https://developer.apple.com/downloads
[mamp-downloads]: http://www.mamp.info/en/downloads/index.html
[php-osx-downloads]: http://php-osx.liip.ch/
