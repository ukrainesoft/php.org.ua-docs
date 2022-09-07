---
navigation:
  - function.fdf-open-string.md: « fdfopenstring
  - function.fdf-remove-item.md: fdfremoveitem »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfopen
---
# fdfopen

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfopen — Відкриває документ FDF

### Опис

```methodsynopsis
fdf_open(string $filename): resource
```

Відкриває файл із даними форми.

Ви також можете використовувати [fdfopenstring()](function.fdf-open-string.md) для обробки результатів POST-запиту PDF-форми.

### Список параметрів

`filename`

Шлях до файлу FDF. Файл повинен містити дані, повернені з форми PDF або створені за допомогою [fdfcreate()](function.fdf-create.md) і [fdfsave()](function.fdf-save.md)

### Значення, що повертаються

Повертає дескриптор документа FDF або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Доступ до даних форми**

```php
<?php
// Сохранение данных FDF во временный файл
$fdffp = fopen("test.fdf", "w");
fwrite($fdffp, $HTTP_FDF_DATA, strlen($HTTP_FDF_DATA));
fclose($fdffp);

// Открытие временного файла и получение данных
$fdf = fdf_open("test.fdf");
/* ... */
fdf_close($fdf);
?>
```

### Дивіться також

-   [fdfopenstring()](function.fdf-open-string.md) - Читає FDF документ з рядка
-   [fdfclose()](function.fdf-close.md) - Закриває FDF-документ
-   [fdfcreate()](function.fdf-create.md) - Створює новий документ FDF
-   [fdfsave()](function.fdf-save.md) - Зберігає документ FDF
