---
navigation:
  - function.fdf-save-string.md: « fdfsavestring
  - function.fdf-set-ap.md: fdfsetap »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfsave
---
# fdfsave

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfsave — Зберігає документ FDF

### Опис

```methodsynopsis
fdf_save(resource $fdf_document, string $filename = ?): bool
```

Зберігає документ FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) ор [fdfopenstring()](function.fdf-open-string.md)

`filename`

Якщо зазначено, FDF буде записаний у цей параметр. В іншому випадку функція запише FDF у вихідний потік PHP за промовчанням.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfclose()](function.fdf-close.md) - Закриває FDF-документ
-   [fdfcreate()](function.fdf-create.md) - Створює новий документ FDF
-   [fdfsavestring()](function.fdf-save-string.md) - Повертає документ FDF у вигляді рядка
