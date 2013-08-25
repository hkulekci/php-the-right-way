---
title: İsim Uzayları (Namespaces)
isChild: true
---

## İsim Uzayları (Namespaces) {#isim_uzaylari_namespaces_title}

Daha öncede bahsedildiği üzere, PHP topluluğu bir sürü geliştiriciden oluşmaktadır. Bu nedenle bazı durumlarda bir kaç farklı kütüphane aynı isimde kullanılmış olabilir. İki kütüphane aynı isim uzayında olduğunda çakışırlar ve bu da soruna neden olur.

_İsim uzayları_ bu sorunu çözer. PHP referans kılavuzunda da açıklandığı gibi, isim uzayları işletim sistemlerindeki klasörler ile karşılaştırılabilir; aynı isimdeki iki dosya fakrlı dizinlerde bulunabilir. Aynı şekilde, aynı isimdeki iki sınıf farklı isim uzaylarında bulunabilir. Bu kadar basit. 

Diğer geliştiricilerin geliştirdiği kütüphaneler ile çakışma korkusu olmadan geliştirme yapabilmeniz adına isim uzaylarını kullanmak sizin için iyi olabilir.

[PSR-0][psr0] isim uzayları konusuna değinilmiştir ve birbiri ile uyumlu (plug-and-play code) standart dosya, sınıf ve isim uzayı düzeni kurmayı amaçlamaktadır.

* [İsim Uzayları hakkında][namespaces]
* [PSR-0 hakkında][psr0]

[namespaces]: http://php.net/manual/tr/language.namespaces.php
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
