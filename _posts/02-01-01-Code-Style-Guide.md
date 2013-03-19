---
title: Kodlama Stili Rehberi
---

# Kodlama Stili Rehberi {#kodlama_stili_rehberi_title}

PHP topluluğu geniş ve çeşitlidir, sayısız kütüphane, framework ve bileşenlerden oluşur. Bunlardan birkaçını seçip herhangi bir projede kullanmak PHP geliştiricileri için doğaldır. PHP kodlarında genel bir stile uymak, farklı ve çeşitli kütüphaneleri kullanmak ve karşılaştırmak açısından geliştiriciler için önemlidir. PHP kodunun genel kod stiline olabildiğince uyması gerekiyor ki geliştiriciler kolaylıkla farklı kütüphaneleri karıştırıp eşleştirebilsinler.

[Framework Interop Group][fig] (daha önce 'PHP Standards Group' olarak bilinen) çeşitli kodlama standartları önerilerinde bulunmuş ve [PSR-0][psr0], [PSR-1][psr1] ve [PSR-2][psr2] olarak bilinen standartları kabul etmiştir. Kabul edilmiş olan bu standartlar Drupal, Zend, Symfony, CakePHP, phpBB, AWS SDK, FuelPHP ve Lithium gibi büyük projelerde kullanılmaya başlanmıştır. Bunları kendi projelerinizde kullanabilirsiniz veya kendi kodlama stilinizi ve standartlarınız ile devam edebilirsiniz.

Diğer geliştiricilerin yazdığınız kodu daha kolay okuyup anlamaları ve üzerinden çalışabilmeleri için bu standartlardan bir veya daha fazlasına uygun kod yazmalısınız, bunlar PSR'nin standartları ya da PEAR veya Zend'in standartları olabilir. Üçüncü partiler tarafından hazırlanmış kodlarla çalışırken birçok bileşenden oluşan uygulamalar birbiri ile daha uyumlu olabilir.

* [PSR-0 hakkında][psr0]
* [PSR-1 hakkında][psr1]
* [PSR-2 hakkında][psr2]
* ["PEAR Coding Standards" hakkında][pear-cs]
* ["Zend Coding Standards" hakkında][zend-cs] 

[PHP_CodeSniffer][phpcs] kullanarak yazdığınız kodları bu standartlardan herhangi birine karşı kodunuzu kontrole etmek için kullanabilirsiniz [Sublime Text 2][st-cs] gibi bir editör eklentisi ile gerçek zamanlı geribildirimler alabilirsiniz.
Fabien Potencier tarafından hazırlanan [PHP Coding Standards Fixer][phpcsfixer] uygulamasını kullanarak kodlarınızın bu standartlara uygun olarak otomatik düzeltilmesini sağlayabilirsiniz.

İngilizce dili kod içinde bulunan değişken, sabit, fonksiyon, yordam gibi semboller ve yapılara ait isimlendirmelerde tercih edilir. Yorumlar için ise şu anda ve gelecekte kodlar üzerinde uğraşacak kişilerin anlayabileceği bir dil tercih edilebilir (Örneğin; proje ekibinde yabancı veya Türkçe bilmeyen bir eleman varsa Türkçe yerine İngilizce tercih etmeniz daha uygun olur).


[fig]: http://www.php-fig.org/
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr1]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[psr2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[psr3]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-3-logger-interface.md
[pear-cs]: http://pear.php.net/manual/en/standards.php
[zend-cs]: http://framework.zend.com/wiki/display/ZFDEV2/Coding+Standards
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[st-cs]: https://github.com/benmatselby/sublime-phpcs
[phpcsfixer]: http://cs.sensiolabs.org/

