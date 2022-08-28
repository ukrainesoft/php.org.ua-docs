Перевіряє дійсність документа, ґрунтуючись на схемі

-   [« DOMDocument::schemaValidate](domdocument.schemavalidate.html)
    
-   [DOMDocument::validate »](domdocument.validate.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Перевіряє дійсність документа, ґрунтуючись на схемі
    

# DOMDocument::schemaValidateSource

(PHP 5, PHP 7, PHP 8)

DOMDocument::schemaValidateSource — Перевіряє дійсність документа, ґрунтуючись на схемі

### Опис

```methodsynopsis
public DOMDocument::schemaValidateSource(string $source, int $flags = 0): bool
```

Перевіряє відповідність документа переданої через рядок схемою.

### Список параметрів

`source`

Рядок, що містить схему.

`flags`

Бітова маска прапори перевірки схеми Libxml. На даний момент підтримується лише одне значення [LIBXML\_SCHEMA\_CREATE](libxml.constants.html). Параметр доступний, починаючи з Libxml 2.6.14.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DOMDocument::schemaValidate()](domdocument.schemavalidate.html) - Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.
-   [DOMDocument::relaxNGValidate()](domdocument.relaxngvalidate.html) - Здійснює перевірку документа на правильність побудови за допомогою relaxNG
-   [DOMDocument::relaxNGValidateSource()](domdocument.relaxngvalidatesource.html) - Перевіряє документ за допомогою relaxNG
-   [DOMDocument::validate()](domdocument.validate.html) - Перевіряє документ на відповідність його DTD