---
navigation:
  - function.fdf-set-file.md: « fdfsetfile
  - function.fdf-set-javascript-action.md: fdfsetjavascriptaction »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsetflags
---
# fdfsetflags

(PHP 4> = 4.0.2, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetflags — Встановлює прапор поля

### Опис

```methodsynopsis
fdf_set_flags(    resource $fdf_document,    string $fieldname,    int $whichFlags,    int $newFlags): bool
```

Встановлює певні прапори поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) ор [fdfopenstring()](function.fdf-open-string.md)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`whichFlags`

`newFlags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfsetopt()](function.fdf-set-opt.md) - Встановлює параметри поля
