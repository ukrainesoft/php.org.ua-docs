---
navigation:
  - function.fdf-get-encoding.md: « fdfgetencoding
  - function.fdf-get-flags.md: fdfgetflags »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfgetfile
---
# fdfgetfile

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfgetfile — Отримує значення ключа /F

### Опис

```methodsynopsis
fdf_get_file(resource $fdf_document): string
```

Отримує значення ключа `/F`

### Список параметрів

`fdf_document`

Дескриптор FDF-документа, повернутий функціями [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) або [fdfopenstring()](function.fdf-open-string.md)

### Значення, що повертаються

Повертає значення ключа у вигляді рядка.

### Дивіться також

-   [fdfsetfile()](function.fdf-set-file.md) - Встановлює PDF-документ для відображення даних FDF
