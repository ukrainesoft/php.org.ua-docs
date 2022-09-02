---
navigation:
  - function.fdf-set-flags.md: « fdfsetflags
  - function.fdf-set-on-import-javascript.md: fdfsetвінimportjavascript »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsetjavascriptaction
---
# fdfsetjavascriptaction

(PHP 4> = 4.0.2, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetjavascriptaction — Встановлює дію javascript для поля

### Опис

```methodsynopsis
fdf_set_javascript_action(    resource $fdf_document,    string $fieldname,    int $trigger,    string $script): bool
```

Встановлює дію JavaScript для заданого поля

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) ор [fdfopenstring()](function.fdf-open-string.md)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`trigger`

`script`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfsetsubmitformaction()](function.fdf-set-submit-form-action.md) - Встановлює дію форми надсилання поля
