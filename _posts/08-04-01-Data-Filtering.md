---
title: Veri Süzme
isChild: true
---

## Veri Süzme {#veri_suzme_title}

Yabancı bir girdiye kesinlikle güvenmeyin. Yabancı girdiden gelen veriyi kesinlikle temizleyin ve onaylayın (validate). 
`filter_var` ve `filter_input` fonksiyonları metni temizler ve onaylar (validate). (e-posta adresi vs.)

Yabancı girdi herşey olabilir: `$_GET` ve `$_POST` ile gelen veriler, bazı `$_SERVER` değerlerinde ve 
`fopen('php://input', 'r')` aracılığıyla gelen HTTP isteklerinde gibi. Yabancı girdiler sadece kullanıcı form verileri ile 
sınırlandırılmamalı. Dosya yükleme ve indirmeler, oturum verileri, çerez verileri ve sisteminiz dışından aldığınız web 
servislerinden gelen verilerde yabancı girdidir. 

Yabancı veriler saklanabilir, birleştirilebilir ve daha sonra erişilebilir, ancak o halen yabancı bir girdidir. 
Her işleminizde çıktı verdiğinizde, birleştirmenizde veya kodunuzun içine kattığınızda kendinize "Veri güvenli mi?" sorusunu 
tekrar tekrar sorun. 

Veri amacına göre farklı şekillerde süzülebilir. Örneğin, Süzgeçten geçirilmemiş bir yabancı girdi, HTMl içerisinde 
kullanılabilir ve bir javascript kodunu çalıştırabilir. Bu `Cross-Site Scripting (XSS)` olarak bilinir ve çok tehlikeli 
bir ataktır. Bunu önlemenin bir yolu vardır. Kullanıcı tarafından oluşturulan bütün girdilerdeki HTML kodlarını 
`strip_tags` fonksiyonu ile silmektir veya `htmlentities`, `htmlspecialchars` fonksiyonları ile HTML özel karakterleri kaçış 
karakterleri ile değiştirmektir.

Diğer bir örnek komut satırına parametre göndermektir. Bu genellikle tehlikelidir. Ancak kullanılacaksa `escapeshellarg` 
fonskiyonu ile parametreleri temizleyebilirsiniz. 

Son bir örnek ise, yabancı girdiyi dosya sisteminde bir dosyayı load etmek için kullandığımızı düşünelim. Burada bir açık oluşabilir. 
Burada "/", "../", [null bytes][6], veya diğer karakterleri girdiden gelen dosya adından silmeniz gerekebilir. Aksi durumda gizli, 
özel veya hassas dosyalara ulaşılabilir. 

* [Veri Süzme hakkında][1]
* [`filter_var` hakkında][4]
* [`filter_input` hakkında][5]
* [null byte ile başa çıkma hakkında][6]

### Sterilize Etmek (Sanitization)

Sterilize etmek kural dışı ve güvenli olmayan karakterlerin yabancı girdilerden silinmesi demektir.

Örneğin, yabancı girdileri HTML içerisine ya da SQL sorgusuna göndermeden önce sterilize etmelisiniz. 
Eğer parametreleri gönderirken [PDO](#veritabanlari) kullanırsanız, o sizin için girdileri sterilize edecektir. 

Bazen HTML sayfalarında sadece bazı güvenli tagların kullanılması gerekmektedir. Bu çoğu zaman çok zor bir iştir. 
Bunu önlemek için Markdown veya BBCode gibi kısıtlı biçimlendiriciler kullanılır. Bu nedenle [HTML Purifier][html-purifier]
gibi kütüphaneler mevcuttur. 

[Sterilize Etme Filtreleri][2]

### Doğrulama

Doğrulama yabancı girdiler için ön bir eleme sağlar. Örneğin, bir kayıt işlemi sırasında bir e-posta adresini, 
bir telefonu ya da yaşı doğrulamak isteyebilirsiniz. 


[Doğrulama Süzgeçleri][3]

[1]: http://www.php.net/manual/tr/book.filter.php
[2]: http://www.php.net/manual/tr/filter.filters.sanitize.php
[3]: http://www.php.net/manual/tr/filter.filters.validate.php
[4]: http://php.net/manual/tr/function.filter-var.php
[5]: http://www.php.net/manual/tr/function.filter-input.php
[6]: http://php.net/manual/tr/security.filesystem.nullbytes.php
[html-purifier]: http://htmlpurifier.org/
