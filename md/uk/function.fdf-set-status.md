---
navigation:
  - function.fdf-set-opt.md: « fdf\_set\_opt
  - function.fdf-set-submit-form-action.md: fdf\_set\_submit\_form\_action »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_set\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_set\_status

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_set\_status — Встановлює значення ключа /STATUS

### Опис

```methodsynopsis
fdf_set_status(resource $fdf_document, string $status): bool
```

Устанавливает значение ключа`/STATUS`. Коли клієнт отримує FDF із встановленим статусом, він представляє значення у вікні попередження.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md)or[fdf\_open\_string()](function.fdf-open-string.md)

`status`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fdf\_get\_status()](function.fdf-get-status.md) \- Отримує значення ключа /STATUS
