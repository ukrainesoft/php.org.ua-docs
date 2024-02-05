---
navigation:
  - domdocument.relaxngvalidate.md: '« DOMDocument::relaxNGValidate'
  - domdocument.replacechildren.md: 'DOMDocument::replaceChildren »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::relaxNGValidateSource'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::relaxNGValidateSource

(PHP 5, PHP 7, PHP 8)

DOMDocument::relaxNGValidateSource — Перевіряє документ за допомогою relaxNG

### Опис

```methodsynopsis
public DOMDocument::relaxNGValidateSource(string $source): bool
```

Застосовує перевірку [» relaxNG](http://www.relaxng.org/)документа на соответствие заданному источнику RNG.

### Список параметрів

`source`

Рядок містить RNG-схему.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [DOMDocument::relaxNGValidate()](domdocument.relaxngvalidate.md) \- Здійснює перевірку документа на правильність побудови за допомогою relaxNG
-   [DOMDocument::schemaValidate()](domdocument.schemavalidate.md) \- Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.
-   [DOMDocument::schemaValidateSource()](domdocument.schemavalidatesource.md) \- Перевіряє дійсність документа, ґрунтуючись на схемі
-   [DOMDocument::validate()](domdocument.validate.md) \- Перевіряє документ на відповідність його DTD
