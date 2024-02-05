---
navigation:
  - function.fdf-set-ap.md: « fdf\_set\_ap
  - function.fdf-set-file.md: fdf\_set\_file »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_set\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_set\_encoding

(PHP 4 >= 4.0.7, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_set\_encoding — Встановлює кодування символів FDF

### Опис

```methodsynopsis
fdf_set_encoding(resource $fdf_document, string $encoding): bool
```

Встановлює кодування символів для FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md)or[fdf\_open\_string()](function.fdf-open-string.md)

`encoding`

Назва кодування. Підтримуються такі значення: "`Shift-JIS`", "`UHC`", "`GBK`"і"`BigFive`".

Порожній рядок скидає кодування за умовчанням у схему `PDFDocEncoding/Unicode`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
