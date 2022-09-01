---
navigation:
  - function.fdf-save.html: « fdfsave
  - function.fdf-set-encoding.html: fdfsetencoding »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsetап
---
# fdfsetап

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfsetap — Встановлює зовнішній вигляд поля

### Опис

```methodsynopsis
fdf_set_ap(    resource $fdf_document,    string $field_name,    int $face,    string $filename,    int $page_number): bool
```

Встановлює зовнішній вигляд поля (тобто значення ключа `/AP`

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) ор [fdfopenstring()](function.fdf-open-string.html)

`field_name`

`face`

Допустимі значення: **`FDFNormalAP`** **`FDFRolloverAP`** і **`FDFDownAP`**

`filename`

`page_number`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
