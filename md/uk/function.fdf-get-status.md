---
navigation:
  - function.fdf-get-opt.md: « fdf\_get\_opt
  - function.fdf-get-value.md: fdf\_get\_value »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_get\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_get\_status

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_get\_status — Отримує значення ключа /STATUS

### Опис

```methodsynopsis
fdf_get_status(resource $fdf_document): string
```

Получает значение ключа`/STATUS`

### Список параметрів

`fdf_document`

Дескриптор FDF-документа, повернутий функціями [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

### Значення, що повертаються

Повертає значення ключа у вигляді рядка.

### Дивіться також

-   [fdf\_set\_status()](function.fdf-set-status.md) \- Встановлює значення ключа /STATUS
