Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.

-   [« DOMDocument::saveXML](domdocument.savexml.html)
    
-   [DOMDocument::schemaValidateSource »](domdocument.schemavalidatesource.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.
    

# DOMDocument::schemaValidate

(PHP 5, PHP 7, PHP 8)

DOMDocument::schemaValidate — Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.

### Опис

```methodsynopsis
public DOMDocument::schemaValidate(string $filename, int $flags = 0): bool
```

Перевіряє документ на дійсність, ґрунтуючись на файлі схеми.

### Список параметрів

`filename`

Шлях до файлу із схемою.

`flags`

Бітова маска прапори перевірки схеми Libxml. На даний момент підтримується лише одне значення [LIBXML\_SCHEMA\_CREATE](libxml.constants.html). Параметр доступний, починаючи з Libxml 2.6.14.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DOMDocument::schemaValidateSource()](domdocument.schemavalidatesource.html) - Перевіряє дійсність документа, ґрунтуючись на схемі
-   [DOMDocument::relaxNGValidate()](domdocument.relaxngvalidate.html) - Здійснює перевірку документа на правильність побудови за допомогою relaxNG
-   [DOMDocument::relaxNGValidateSource()](domdocument.relaxngvalidatesource.html) - Перевіряє документ за допомогою relaxNG
-   [DOMDocument::validate()](domdocument.validate.html) - Перевіряє документ на відповідність його DTD