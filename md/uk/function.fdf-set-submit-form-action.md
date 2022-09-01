---
navigation:
  - function.fdf-set-status.html: « fdfsetstatus
  - function.fdf-set-target-frame.html: fdfsettargetframe »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsetsubmitformaction
---
# fdfsetsubmitformaction

(PHP 4> = 4.0.2, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetsubmitformaction — Встановлює дію форми надсилання поля

### Опис

```methodsynopsis
fdf_set_submit_form_action(    resource $fdf_document,    string $fieldname,    int $trigger,    string $script,    int $flags): bool
```

Встановлює дію форми надсилання для заданого поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) або [fdfopenstring()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`trigger`

`script`

`flags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfsetjavascriptaction()](function.fdf-set-javascript-action.html) - Встановлює дію JavaScript для поля
