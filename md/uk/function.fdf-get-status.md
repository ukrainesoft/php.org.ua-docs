---
navigation:
  - function.fdf-get-opt.md: « fdfgetopt
  - function.fdf-get-value.md: fdfgetvalue »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfgetstatus
---
# fdfgetstatus

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfgetstatus — Отримує значення ключа /STATUS

### Опис

```methodsynopsis
fdf_get_status(resource $fdf_document): string
```

Отримує значення ключа `/STATUS`

### Список параметрів

`fdf_document`

Дескриптор FDF-документа, повернутий функціями [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) або [fdfopenstring()](function.fdf-open-string.md)

### Значення, що повертаються

Повертає значення ключа у вигляді рядка.

### Дивіться також

-   [fdfsetstatus()](function.fdf-set-status.md) - Встановлює значення ключа /STATUS
