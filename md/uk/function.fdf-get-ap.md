---
navigation:
  - function.fdf-error.md: « fdferror
  - function.fdf-get-attachment.md: fdfgetattachment »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfgetап
---
# fdfgetап

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfgetap — Отримує вигляд поля

### Опис

```methodsynopsis
fdf_get_ap(    resource $fdf_document,    string $field,    int $face,    string $filename): bool
```

Набуває вигляду `field` (тобто значення ключа /AP) та зберігає його у файлі.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) або [fdfopenstring()](function.fdf-open-string.md)

`field`

`face`

Можливі значення: **`FDFNormalAP`** **`FDFRolloverAP`** і **`FDFDownAP`**

`filename`

Зовнішній вигляд буде збережено у цьому параметрі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
