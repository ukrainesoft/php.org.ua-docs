---
navigation:
  - function.fdf-close.md: « fdf\_close
  - function.fdf-enum-values.md: fdf\_enum\_values »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_create

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_create — Створення нового документа FDF

### Опис

```methodsynopsis
fdf_create(): resource
```

Створює новий документ FDF.

Функція необхідна, якщо потрібно заповнити поля введення даних у PDF-файлі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дескриптор документа FDF або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Заповнення PDF-документу**

```php
<?php
$outfdf = fdf_create();
fdf_set_value($outfdf, "volume", $volume, 0);

fdf_set_file($outfdf, "http:/testfdf/resultlabel.pdf");
fdf_save($outfdf, "outtest.fdf");
fdf_close($outfdf);
Header("Content-type: application/vnd.fdf");
$fp = fopen("outtest.fdf", "r");
fpassthru($fp);
unlink("outtest.fdf");
?>
```

### Дивіться також

-   [fdf\_close()](function.fdf-close.md) \- Закриває FDF-документ
-   [fdf\_save()](function.fdf-save.md) \- Зберігає документ FDF
-   [fdf\_open()](function.fdf-open.md) \- Відкриває документ FDF
