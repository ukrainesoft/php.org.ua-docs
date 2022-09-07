---
navigation:
  - function.fdf-set-opt.md: « fdfsetopt
  - function.fdf-set-submit-form-action.md: fdfsetsubmitformaction »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsetstatus
---
# fdfsetstatus

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfsetstatus — Встановлює значення ключа /STATUS

### Опис

```methodsynopsis
fdf_set_status(resource $fdf_document, string $status): bool
```

Встановлює значення ключа `/STATUS`. Коли клієнт отримує FDF із встановленим статусом, він представляє значення у вікні попередження.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) ор [fdfopenstring()](function.fdf-open-string.md)

`status`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfgetstatus()](function.fdf-get-status.md) - Отримує значення ключа /STATUS
