---
navigation:
  - domdocument.registernodeclass.md: '« DOMDocument::registerNodeClass'
  - domdocument.relaxngvalidatesource.md: 'DOMDocument::relaxNGValidateSource »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::relaxNGValidate'
---
# DOMDocument::relaxNGValidate

(PHP 5, PHP 7, PHP 8)

DOMDocument::relaxNGValidate — Здійснює перевірку документа на правильність побудови за допомогою relaxNG

### Опис

```methodsynopsis
public DOMDocument::relaxNGValidate(string $filename): bool
```

Виробляє [» relaxNG](http://www.relaxng.org/) перевірку документа, ґрунтуючись на заданій схемі RNG.

### Список параметрів

`filename`

Файл RNG.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DOMDocument::relaxNGValidateSource()](domdocument.relaxngvalidatesource.md) - Перевіряє документ за допомогою relaxNG
-   [DOMDocument::schemaValidate()](domdocument.schemavalidate.md) - Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.
-   [DOMDocument::schemaValidateSource()](domdocument.schemavalidatesource.md) - Перевіряє дійсність документа, ґрунтуючись на схемі
-   [DOMDocument::validate()](domdocument.validate.md) - Перевіряє документ на відповідність його DTD
