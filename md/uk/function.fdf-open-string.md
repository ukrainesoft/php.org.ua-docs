---
navigation:
  - function.fdf-next-field-name.md: « fdfnextfieldname
  - function.fdf-open.md: fdfopen »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfopenstring
---
# fdfopenstring

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfopenstring — Читає документ FDF з рядка

### Опис

```methodsynopsis
fdf_open_string(string $fdf_data): resource
```

Зчитує дані форми з рядка.

Ви можете використовувати **fdfopenstring()** разом із $HTTPFDFDATA для обробки введення форми FDF від віддаленого клієнта.

### Список параметрів

`fdf_data`

Дані, повернуті з PDF форми або створені за допомогою [fdfcreate()](function.fdf-create.md) і [fdfsavestring()](function.fdf-save-string.md)

### Значення, що повертаються

Повертає дескриптор FDF документа або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Доступ до даних форми**

```php
<?php
$fdf = fdf_open_string($HTTP_FDF_DATA);
/* ... */
fdf_close($fdf);
?>
```

### Дивіться також

-   [fdfopen()](function.fdf-open.md) - Відкриває документ FDF
-   [fdfclose()](function.fdf-close.md) - Закриває FDF-документ
-   [fdfcreate()](function.fdf-create.md) - Створює новий документ FDF
-   [fdfsavestring()](function.fdf-save-string.md) - Повертає документ FDF у вигляді рядка
