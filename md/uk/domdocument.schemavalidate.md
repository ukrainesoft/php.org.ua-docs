---
navigation:
  - domdocument.savexml.md: '« DOMDocument::saveXML'
  - domdocument.schemavalidatesource.md: 'DOMDocument::schemaValidateSource »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::schemaValidate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Бітова маска прапори перевірки схеми Libxml. На даний момент підтримується лише одне значення [LIBXML\_SCHEMA\_CREATE](libxml.constants.md)Параметр доступен, начиная с Libxml 2.6.14.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [DOMDocument::schemaValidateSource()](domdocument.schemavalidatesource.md) \- Перевіряє дійсність документа, ґрунтуючись на схемі
-   [DOMDocument::relaxNGValidate()](domdocument.relaxngvalidate.md) \- Здійснює перевірку документа на правильність побудови за допомогою relaxNG
-   [DOMDocument::relaxNGValidateSource()](domdocument.relaxngvalidatesource.md) \- Перевіряє документ за допомогою relaxNG
-   [DOMDocument::validate()](domdocument.validate.md) \- Перевіряє документ на відповідність його DTD
