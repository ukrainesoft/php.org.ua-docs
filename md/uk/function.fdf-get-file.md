---
navigation:
  - function.fdf-get-encoding.md: « fdf\_get\_encoding
  - function.fdf-get-flags.md: fdf\_get\_flags »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_get\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_get\_file

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_get\_file — Отримує значення ключа /F

### Опис

```methodsynopsis
fdf_get_file(resource $fdf_document): string
```

Получает значение ключа`/F`

### Список параметрів

`fdf_document`

Дескриптор FDF-документа, повернутий функціями [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

### Значення, що повертаються

Повертає значення ключа у вигляді рядка.

### Дивіться також

-   [fdf\_set\_file()](function.fdf-set-file.md) \- Встановлює PDF-документ для відображення даних FDF
