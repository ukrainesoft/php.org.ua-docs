---
navigation:
  - function.fdf-close.html: « fdfclose
  - function.fdf-enum-values.html: fdfenumvalues »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfcreate
---
# fdfcreate

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfcreate — Створення нового документа FDF

### Опис

```methodsynopsis
fdf_create(): resource
```

Створює новий документ FDF.

Функція необхідна, якщо потрібно заповнити дані поля введення PDF.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дескриптор документа FDF або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Заповнення PDF-документу**

```php
<?php
$outfdf = fdf_create();
fdf_set_value($outfdf, "volume", $volume, 0);

fdf_set_file($outfdf, "http:/testfdf/resultlabel.pdf");
fdf_save($outfdf, "outtest.fdf");
fdf_close($outfdf);
Header("Content-type: application/vnd.fdf");
$fp = fopen("outtest.fdf", "r");
fpassthru($fp);
unlink("outtest.fdf");
?>
```

### Дивіться також

-   [fdfclose()](function.fdf-close.md) - Закриває FDF-документ
-   [fdfsave()](function.fdf-save.md) - Зберігає документ FDF
-   [fdfopen()](function.fdf-open.md) - Відкриває документ FDF
