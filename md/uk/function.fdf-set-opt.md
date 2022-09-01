---
navigation:
  - function.fdf-set-on-import-javascript.html: « fdfsetвінimportjavascript
  - function.fdf-set-status.html: fdfsetstatus »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsetopt
---
# fdfsetopt

(PHP 4> = 4.0.2, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetopt — Встановлює параметри поля

### Опис

```methodsynopsis
fdf_set_opt(    resource $fdf_document,    string $fieldname,    int $element,    string $str1,    string $str2): bool
```

Встановлює параметри заданого поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) ор [fdfopenstring()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`element`

`str1`

`str2`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfsetflags()](function.fdf-set-flags.html) - Встановлює прапор поля
