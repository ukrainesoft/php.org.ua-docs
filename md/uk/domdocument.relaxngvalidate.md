Здійснює перевірку документа на правильність побудови за допомогою relaxNG

-   [« DOMDocument::registerNodeClass](domdocument.registernodeclass.html)
    
-   [DOMDocument::relaxNGValidateSource »](domdocument.relaxngvalidatesource.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Здійснює перевірку документа на правильність побудови за допомогою relaxNG
    

# DOMDocument::relaxNGValidate

(PHP 5, PHP 7, PHP 8)

DOMDocument::relaxNGValidate — Здійснює перевірку документа на правильність побудови за допомогою relaxNG

### Опис

```methodsynopsis
public DOMDocument::relaxNGValidate(string $filename): bool
```

Виробляє [» relaxNG](http://www.relaxng.org/) перевірку документа, ґрунтуючись на заданій схемі RNG.

### Список параметрів

`filename`

Файл RNG.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DOMDocument::relaxNGValidateSource()](domdocument.relaxngvalidatesource.html) - Перевіряє документ за допомогою relaxNG
-   [DOMDocument::schemaValidate()](domdocument.schemavalidate.html) - Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.
-   [DOMDocument::schemaValidateSource()](domdocument.schemavalidatesource.html) - Перевіряє дійсність документа, ґрунтуючись на схемі
-   [DOMDocument::validate()](domdocument.validate.html) - Перевіряє документ на відповідність його DTD