---
title: Composer ve Packagist
isChild: true
---

## Composer ve Packagist {#composer_ve_packagist_title}

Composer PHP için **muhteşem** bir bağımlılık yönetimi aracıdır. Bağımlılık yönetimini bir kaç basit komut ile `composer.json` dosyası içerisinde yazıyoruz, Composer projenizin ihtiyaçlarını otomatik olarak indiriyor ve kurulumunu gerçekleştiriyor.

Composer ile uyumlu şimdiden projenizde kullanmanız için bir çok PHP kütüphanesi bulunmakta. Bu paketler Composer'ın resmi deposu olan [Packagist][1]'da listelenmetedir.

### Composer Nasıl Kurulur

Yerel (önerilmemesine rağmen içinde bulunduğunuzu dizin için) ya da genel (örneğin: /usr/local/bin) kullanım için Composer'ı kurabilirsiniz. Yerel olarak kurmak için aşağıdaki örneğe bakınız:

    curl -s https://getcomposer.org/installer | php

Bu komut `composer.phar` (bir PHP ikili arşivi) dosyası indirecek. Bu dosyayı `php` kullanarak çalıştırabilir ve projenizin ihtiyaçlarını yönetebilirsiniz. <strong>Not:</strong> Kodu çevirici bir kaynağa indirdi iseniz öncelikle çevrim içi kod okuyunuz.

### Composer Nasıl Kurulur (elle)

Composer'i elle kurmak biraz üst seviye bir tekniktir. Ancak geliştiricinin etkileşimli kurulum yerine bu yöntemi kullanması için bir kaç sebep vardır. Etkilşimli kurulum aşağıdaki PHP kurulumlarını denetler:

 - PHP'nin yeterli bir sürümü kontrol edilir
 - `.phar` dosyası düzgün çalıştırılır.
 - Dizin izinleri kontrol edilir.
 - Sorunlu uzantılar yüklenmez.
 - Belirli `php.ini` ayarları ayarlanır. 

Bu kurulum adımlarının hiçbiri olmadan yapılan elle kurulumda, sizin için bir değerinin olup olmadığına karar vermelisiniz. Aşağıdaki komutlar ile elle kuruluma başlayalım : 

    curl -s https://getcomposer.org/composer.phar -o $HOME/local/bin/composer
    chmod +x $HOME/local/bin/composer

`$HOME/local/bin` dizini (ya da sizin seçeceğiniz bir dizin) sizin `$PATH` değişkeninizin içerisinde olmalı. Bu `composer` komutunu kullanılabilir yapacaktır. 

Dökümantasyonda karşılaştığımız `php composer.phar install` komutunu aşağıdaki gibi kullanabilirsiniz : 

    composer install

### Bağımlıklıkları Nasıl Tanımlar ve Kurarız

Composer proje bağımlılığını `composer.json` isimli bir dosya ile sağlar. Bu dosyayı elle ya da Composer vasıtasıyla güncelleyebilirsiniz. `php composer.phar require` komutu projenize bağımlılığı ekler ve daha önce oluşturmamış iseniz `composer.json` dosyanızı oluşturur. Aşağıda bir örnek yapalım ve projemize [Twig][2]'i ekleyelim. Aşağıdaki komutu projenizin ana dizininde çalıştırın. 

	php composer.phar require twig/twig:~1.8

`php composer.phar init` komutu sana tam bir `composer.json` dosyası oluşturmak için rehber olabilir. Herhangi bir şekilde `composer.json` dosyanızı oluşturduktan sonra aşağıdaki komutu kullanarak Composer ile bağımlılıklarınızı `vendor/` dizini altına indirebilir ve yükleyebilirsiniz. 

    php composer.phar install

Daha sonra aşağıdaki satırları uygulamanızın ana PHP dosyasına ekleyiniz; bunları nasıl yapacağınız size zaten Composer'daki projelerde bildirilecek.

{% highlight php %}
<?php
require 'vendor/autoload.php';
{% endhighlight %}

Şimdi projenize eklediğiniz kütüphaneleri kullanabilirsiniz ve bunlar projenizde talep dahilinde otomatik yükleniyor (autoloaded) olacak.

### Bağımlılıkları Güncellemek

Composer, `php composer.phar install` komutunu ilk çalıştırdığınızda `composer.lock` adında bir dosya oluşturur ve bu dosyada her paketin o anki versiyonunu tutar. Projenizi başka geliştiricilerle paylaştığınızda, `composer.lock` dosyanızı da paylaşırsanız, geliştiriciler `php composer.phar install` komutunu uyguladıklarında sizinle aynı versiyondaki paketlere sahip olurlar. Bağımlılıkları (Dependencies) güncellemek için, `php composer.phar update` komutunu çalıştırabilirsiniz.

This is most useful when you define your version requirements flexibly. For instance a version requirement of ~1.8  means "anything newer than 1.8.0, but less than 2.0.x-dev". You can also use the `*` wildcard as in `1.8.*`. Now Composer's `php composer.phar update` command will upgrade all your dependencies to the newest version that fits the restrictions you define.

### Checking your dependencies for security issues

The [Security Advisories Checker][3] is a web service and a command-line tool, both will examine your `composer.lock` file and tell you if you need to update any of your dependencies.

* [Learn about Composer][4]


[1]: http://packagist.org/
[2]: http://twig.sensiolabs.org
[3]: https://security.sensiolabs.org/ 
[4]: http://getcomposer.org/doc/00-intro.md
