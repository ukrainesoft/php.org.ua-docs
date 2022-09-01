---
navigation:
  - function.fdf-set-ap.html: « fdfsetап
  - function.fdf-set-file.html: fdfsetfile »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsetencoding
---
# fdfsetencoding

(PHP 4> = 4.0.7, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetencoding — Встановлює кодування символів FDF

### Опис

```methodsynopsis
fdf_set_encoding(resource $fdf_document, string $encoding): bool
```

Встановлює кодування символів для FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) ор [fdfopenstring()](function.fdf-open-string.md)

`encoding`

Назва кодування. Підтримуються такі значення: "`Shift-JIS`","`UHC`","`GBK`"і"`BigFive`".

Порожній рядок скидає кодування за умовчанням у схему `PDFDocEncoding/Unicode`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
