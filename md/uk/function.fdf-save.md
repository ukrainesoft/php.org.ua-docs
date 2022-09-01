---
navigation:
  - function.fdf-save-string.html: « fdfsavestring
  - function.fdf-set-ap.html: fdfsetap »
  - index.html: PHP Manual
  - ref.fdf.html: FDF
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

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) ор [fdfopenstring()](function.fdf-open-string.html)

`filename`

Якщо зазначено, FDF буде записаний у цей параметр. В іншому випадку функція запише FDF у вихідний потік PHP за промовчанням.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfclose()](function.fdf-close.html) - Закриває FDF-документ
-   [fdfcreate()](function.fdf-create.html) - Створює новий документ FDF
-   [fdfsavestring()](function.fdf-save-string.html) - Повертає документ FDF у вигляді рядка
