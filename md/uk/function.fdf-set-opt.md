---
navigation:
  - function.fdf-set-on-import-javascript.md: « fdf\_set\_on\_import\_javascript
  - function.fdf-set-status.md: fdf\_set\_status »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_set\_opt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_set\_opt

(PHP 4 >= 4.0.2, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_set\_opt — Встановлює параметри поля

### Опис

```methodsynopsis
fdf_set_opt(    resource $fdf_document,    string $fieldname,    int $element,    string $str1,    string $str2): bool
```

Встановлює параметри заданого поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md)or[fdf\_open\_string()](function.fdf-open-string.md)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`element`

`str1`

`str2`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fdf\_set\_flags()](function.fdf-set-flags.md) \- Встановлює прапор поля
