Відкриває документ FDF

-   [« fdf\_open\_string](function.fdf-open-string.html)
    
-   [fdf\_remove\_item »](function.fdf-remove-item.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Відкриває документ FDF
    

# fdfopen

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfopen — Відкриває документ FDF

### Опис

```methodsynopsis
fdf_open(string $filename): resource
```

Відкриває файл із даними форми.

Ви також можете використовувати [fdf\_open\_string()](function.fdf-open-string.html) для обробки результатів POST-запиту PDF-форми.

### Список параметрів

`filename`

Шлях до файлу FDF. Файл повинен містити дані, повернені з форми PDF або створені за допомогою [fdf\_create()](function.fdf-create.html) і [fdf\_save()](function.fdf-save.html)

### Значення, що повертаються

Повертає дескриптор документа FDF або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Доступ до даних форми**

```php
<?php
// Сохранение данных FDF во временный файл
$fdffp = fopen("test.fdf", "w");
fwrite($fdffp, $HTTP_FDF_DATA, strlen($HTTP_FDF_DATA));
fclose($fdffp);

// Открытие временного файла и получение данных
$fdf = fdf_open("test.fdf");
/* ... */
fdf_close($fdf);
?>
```

### Дивіться також

-   [fdf\_open\_string()](function.fdf-open-string.html) - Читає FDF документ з рядка
-   [fdf\_close()](function.fdf-close.html) - Закриває FDF-документ
-   [fdf\_create()](function.fdf-create.html) - Створює новий документ FDF
-   [fdf\_save()](function.fdf-save.html) - Зберігає документ FDF