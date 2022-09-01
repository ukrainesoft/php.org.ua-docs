---
navigation:
  - function.fdf-set-flags.html: « fdfsetflags
  - function.fdf-set-on-import-javascript.html: fdfsetвінimportjavascript »
  - index.html: PHP Manual
  - ref.fdf.html: FDF
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

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) ор [fdfopenstring()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`trigger`

`script`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfsetsubmitformaction()](function.fdf-set-submit-form-action.html) - Встановлює дію форми надсилання поля
