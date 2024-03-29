---
navigation:
  - domdocument.schemavalidate.md: '« DOMDocument::schemaValidate'
  - domdocument.validate.md: 'DOMDocument::validate »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::schemaValidateSource'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Бітова маска прапори перевірки схеми Libxml. На даний момент підтримується лише одне значення [LIBXML\_SCHEMA\_CREATE](libxml.constants.md)Параметр доступен, начиная с Libxml 2.6.14.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [DOMDocument::schemaValidate()](domdocument.schemavalidate.md) \- Перевіряє дійсність документа, ґрунтуючись на заданій схемі. Підтримується лише XML-схема 1.0.
-   [DOMDocument::relaxNGValidate()](domdocument.relaxngvalidate.md) \- Здійснює перевірку документа на правильність побудови за допомогою relaxNG
-   [DOMDocument::relaxNGValidateSource()](domdocument.relaxngvalidatesource.md) \- Перевіряє документ за допомогою relaxNG
-   [DOMDocument::validate()](domdocument.validate.md) \- Перевіряє документ на відповідність його DTD
