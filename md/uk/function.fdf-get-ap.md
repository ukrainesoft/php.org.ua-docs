---
navigation:
  - function.fdf-error.md: « fdf\_error
  - function.fdf-get-attachment.md: fdf\_get\_attachment »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_get\_ap
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_get\_ap

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_get\_ap — Отримує вигляд поля

### Опис

```methodsynopsis
fdf_get_ap(    resource $fdf_document,    string $field,    int $face,    string $filename): bool
```

Набуває вигляду `field` (тобто значення ключа /AP) та зберігає його у файлі.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

`field`

`face`

Можливі значення: **`FDFNormalAP`** **`FDFRolloverAP`** і **`FDFDownAP`**

`filename`

Зовнішній вигляд буде збережено у цьому параметрі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
