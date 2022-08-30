Відкриває документ FDF

-   [« fdfopenstring](function.fdf-open-string.html)
    
-   [fdfremoveitem »](function.fdf-remove-item.html)
    
-   [PHP Manual](index.md)
    
-   [FDF](ref.fdf.md)
    
-   Відкриває документ FDF
    

# fdfopen

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfopen — Відкриває документ FDF

### Опис

```methodsynopsis
fdf_open(string $filename): resource
```

Відкриває файл із даними форми.

Ви також можете використовувати [fdfopenstring()](function.fdf-open-string.html) для обробки результатів POST-запиту PDF-форми.

### Список параметрів

`filename`

Шлях до файлу FDF. Файл повинен містити дані, повернені з форми PDF або створені за допомогою [fdfcreate()](function.fdf-create.html) і [fdfsave()](function.fdf-save.html)

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

-   [fdfopenstring()](function.fdf-open-string.html) - Читає FDF документ з рядка
-   [fdfclose()](function.fdf-close.html) - Закриває FDF-документ
-   [fdfcreate()](function.fdf-create.html) - Створює новий документ FDF
-   [fdfsave()](function.fdf-save.html) - Зберігає документ FDF