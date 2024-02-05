---
navigation:
  - function.fdf-set-status.md: « fdf\_set\_status
  - function.fdf-set-target-frame.md: fdf\_set\_target\_frame »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_set\_submit\_form\_action
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_set\_submit\_form\_action

(PHP 4 >= 4.0.2, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_set\_submit\_form\_action — Встановлює дію форми надсилання поля

### Опис

```methodsynopsis
fdf_set_submit_form_action(    resource $fdf_document,    string $fieldname,    int $trigger,    string $script,    int $flags): bool
```

Встановлює дію форми надсилання для заданого поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`trigger`

`script`

`flags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fdf\_set\_javascript\_action()](function.fdf-set-javascript-action.md) \- Встановлює дію JavaScript для поля
