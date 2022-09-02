---
navigation:
  - function.fdf-set-value.md: « fdfsetvalue
  - book.gnupg.md: GnuPG »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsetversion
---
# fdfsetversion

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetversion — Встановлює номер версії для файлу FDF

### Опис

```methodsynopsis
fdf_set_version(resource $fdf_document, string $version): bool
```

Встановлює `version` FDF для цього документа.

Деякі функції, які підтримує модуль, доступні лише в нових версіях FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) ор [fdfopenstring()](function.fdf-open-string.md)

`version`

Номер версії. Для поточного набору інструментів FDF 5.0 це може бути `1.2` `1.3` або `1.4`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfgetversion()](function.fdf-get-version.md) - Отримує номер версії для FDF API або файлу
