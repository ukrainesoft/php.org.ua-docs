---
navigation:
  - function.fdf-add-template.md: « fdfaddtemplate
  - function.fdf-create.md: fdfcreate »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfclose
---
# fdfclose

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfclose - Закриває FDF-документ

### Опис

```methodsynopsis
fdf_close(resource $fdf_document): void
```

Закриває документ FDF.

### Список параметрів

`fdf_document`

Дескриптор FDF-документа, повернутий функціями [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) або [fdfopenstring()](function.fdf-open-string.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [fdfopen()](function.fdf-open.md) - Відкриває документ FDF
