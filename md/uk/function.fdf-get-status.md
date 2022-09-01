---
navigation:
  - function.fdf-get-opt.html: « fdfgetopt
  - function.fdf-get-value.html: fdfgetvalue »
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

Дескриптор FDF-документа, повернутий функціями [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) або [fdfopenstring()](function.fdf-open-string.html)

### Значення, що повертаються

Повертає значення ключа у вигляді рядка.

### Дивіться також

-   [fdfsetstatus()](function.fdf-set-status.html) - Встановлює значення ключа /STATUS
