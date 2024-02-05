---
navigation:
  - function.fdf-set-file.md: « fdf\_set\_file
  - function.fdf-set-javascript-action.md: fdf\_set\_javascript\_action »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_set\_flags
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_set\_flags

(PHP 4 >= 4.0.2, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_set\_flags — Встановлює прапор поля

### Опис

```methodsynopsis
fdf_set_flags(    resource $fdf_document,    string $fieldname,    int $whichFlags,    int $newFlags): bool
```

Встановлює певні прапори поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md)or[fdf\_open\_string()](function.fdf-open-string.md)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`whichFlags`

`newFlags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fdf\_set\_opt()](function.fdf-set-opt.md) \- Встановлює параметри поля
