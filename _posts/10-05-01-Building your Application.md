---
title: Uygulamanızı Build Etmek ve Deploy Etmek
isChild: true
---

## Uygulamanızı Build Etmek ve Deploy Etmek {#uygulamanızı_build_etmek_ve_deploy_etmek_title}

Eğer dosyalarınızı güncellemeden önce kendinizi elle (manually) veritabanı şemasını güncellerken veya 
testlerinizi elle (manually) çalıştırıyor buluyorsanız, iki kere düşünün! 

Uygulamanızın yeni versiyonunu deploy etmek için elle (manually) yapmanız gerekecek her ekstra işlem ile büyük hatalar
yapma ihtimaliniz artacaktır. İster basit bir güncellemeyle uğraşırken, ister kapsamlı bir yapı kuruyorken ve hatta sürekli
entegrasyon stratejisiyle uğraşıyorken [build otomasyonu](http://en.wikipedia.org/wiki/Build_automation) arkadaşınızdır.

Otomatikleştirmek isteyeceğiniz bazı işlemler:

* Bağımlılık yönetimi
* Dosyalarınızın (assets) derleme, sıkıştırma (minification) işlemleri
* Test çalıştırma
* Dökümantasyon oluşturma
* Paketleme
* Deployment


### Otomasyon Araçlarını Hazırlamak

Otomasyon araçları, yazılım deployment larının yaygın görevlerini idare eden betik koleksiyonu olarak tanımlanabilir.
Build araçları yazılımınızın bir parçası değildir, sadece yazılımınızla dışarıdan çalışır.

Bazıları PHP, bazıları farklı dillerde olmak üzere build otomasyonunda size yardımcı olabilecek bir çok açık kaynak 
araç bulunmaktadır. Eğer belirli bir iş için daha uygunlarsa PHP ile yazılmış olmamaları sizi durdurmasın.
İşte bir kaç örnek:

[Phing](http://www.phing.info/) PHP dünyasında otomatik deployment a başlamak için en kolay yoldur. Phing ile basit 
bir XML dosyasından paketleme, deployment ve ya test işlemlerini kontrol edebilirsiniz. Phing ([Apache Ant](http://ant.apache.org/) 
tabanlıdır) bir web apliasyonunu yüklemek ve ya güncellemek için genellikle ihtiyaç duyulabilecek geniş çaplı işlemleri
hizmetinize sunar ve PHP de yazılmış özel işlemler ile geliştirilebilir.

[Capistrano](https://github.com/capistrano/capistrano/wiki) is a system for *intermediate-to-advanced programmers* to 
execute commands in a structured, repeatable way on one or more remote machines. It is pre-configured for deploying 
Ruby on Rails applications, however people are **successfully deploying PHP systems** with it. Successful use of 
Capistrano depends on a working knowledge of Ruby and Rake.

Dave Gardner's blog post [PHP Deployment with Capistrano](http://www.davegardner.me.uk/blog/2012/02/13/php-deployment-with-capistrano/) 
is a good starting point for PHP developers interested in Capistrano.

[Chef](http://www.opscode.com/chef/) is more than a deployment framework, it is a very powerful Ruby based system 
integration framework that doesn't just deploy your app but can build your whole server environment or virtual boxes.

Chef resources for PHP developers:

* [Three part blog series about deploying a LAMP application with Chef, Vagrant, and EC2](http://www.jasongrimes.org/2012/06/managing-lamp-environments-with-chef-vagrant-and-ec2-1-of-3/)
* [Chef Cookbook which installs and configures PHP 5.3 and the PEAR package management system](https://github.com/opscode-cookbooks/php)

Further reading:

* [Automate your project with Apache Ant](http://net.tutsplus.com/tutorials/other/automate-your-projects-with-apache-ant/)
* [Maven](http://maven.apache.org/), a build framework based on Ant and [how to use it with PHP](http://www.php-maven.org/)

### Continuous Integration

> Continuous Integration is a software development practice where members of a team integrate their work frequently, 
> usually each person integrates at least daily — leading to multiple integrations per day. Many teams find that this 
> approach leads to significantly reduced integration problems and allows a team to develop cohesive software more 
> rapidly.

*-- Martin Fowler*

There are different ways to implement continuous integration for PHP. Recently [Travis CI](https://travis-ci.org/) has 
done a great job of making continuous integration a reality even for small projects. Travis CI is a hosted continuous 
integration service for the open source community. It is integrated with GitHub and offers first class support for many 
languages including PHP.

Further reading:

* [Continuous Integration with Jenkins](http://jenkins-ci.org/)
* [Continuous Integration with PHPCI](http://www.phptesting.org/)
* [Continuous Integration with Teamcity](http://www.jetbrains.com/teamcity/)
