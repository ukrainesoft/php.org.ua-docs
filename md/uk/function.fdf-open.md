---
navigation:
  - function.fdf-open-string.md: « fdf\_open\_string
  - function.fdf-remove-item.md: fdf\_remove\_item »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_open

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_open — Відкриває документ FDF

### Опис

```methodsynopsis
fdf_open(string $filename): resource
```

Відкриває файл із даними форми.

Ви також можете використовувати [fdf\_open\_string()](function.fdf-open-string.md) для обробки результатів POST-запиту PDF-форми.

### Список параметрів

`filename`

Шлях до файлу FDF. Файл повинен містити дані, повернені з форми PDF або створені за допомогою [fdf\_create()](function.fdf-create.md) і [fdf\_save()](function.fdf-save.md)

### Значення, що повертаються

Повертає дескриптор документа FDF або \*\*`false`\*\*в случае возникновения ошибки.

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

-   [fdf\_open\_string()](function.fdf-open-string.md) \- Читає FDF документ з рядка
-   [fdf\_close()](function.fdf-close.md) \- Закриває FDF-документ
-   [fdf\_create()](function.fdf-create.md) \- Створює новий документ FDF
-   [fdf\_save()](function.fdf-save.md) \- Зберігає документ FDF
