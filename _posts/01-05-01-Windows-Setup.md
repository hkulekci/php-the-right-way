---
title: Windows Kurulumu
isChild: true
---

## Windows Kurulumu {#windows_kurulumu_title}

PHP'nin Windows üzerinde kurulumu ile ilgili çeşitli yollar bulunmaktadır. ".msi" kurulum paketi olarak [indirebilirsiniz][php-downloads]. Bu kurulum dosyası PHP 5.3.0 dan sonra desteklememektedir.

PH'yi öğrenmek ve kendi makinenizde geliştirme yapmak için PHP 5.4 ile birlikte gelen dahili sunucuyu kullanabilirsiniz. Ayarlar konusunda endişelenmenize gerek kalmaz. [Web Platform Installer][wpi], 
[Zend Server CE][zsce], [XAMPP][xampp] ve [WAMP][wamp] gibi herşey içinde bir araç kullanırsanız bu sizin için Windows geliştirme ortamının kurulması ve çalıştırılması için hız katacaktır. Eğer Windows üzerinde geliştirirken Linux üzerinde yayınlıyorsanız, bu araçlar (üretim) yayınlama aşamasından biraz farklı sonuçlar doğurabilir, bu konuda dikkatli olun.

Eğer geliştirme ortamınız Windows iken Windows üzerinde yayınlayacaksanız, IIS7 daha kararlı ve performanslı olacaktır. PHP'yi ayarlamak ve yönetmek için [phpmanager][phpmanager] (IIS7 için GUI eklentisi) kullanabilirsiniz. IIS7 FastCGI desteği ile birlikte gelmektedir. Sadece işleyici olarak PHP'yi tanımlamanız gerekir. Destek ve ek kaynaklar için [dedicated area on iis.net][php-iis] adresini kullanabilirsiniz.

[php-downloads]: http://windows.php.net
[phpmanager]: http://phpmanager.codeplex.com/
[wpi]: http://www.microsoft.com/web/downloads/platform.aspx
[zsce]: http://www.zend.com/en/products/server-ce/
[xampp]: http://www.apachefriends.org/en/xampp.html
[wamp]: http://www.wampserver.com/
[php-iis]: http://php.iis.net/
