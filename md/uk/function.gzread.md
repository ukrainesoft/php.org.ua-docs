Бінарне читання gz-файлу

-   [« gzputs](function.gzputs.md)
    
-   [gzrewind »](function.gzrewind.md)
    
-   [PHP Manual](index.md)
    
-   [Функции Zlib](ref.zlib.md)
    
-   Бінарне читання gz-файлу
    

# gzread

(PHP 4, PHP 5, PHP 7, PHP 8)

gzread — Бінарне читання gz-файлу

### Опис

```methodsynopsis
gzread(resource $stream, int $length): string|false
```

**gzread()** читає (розпаковуючи) до `length` байт із gz-файлу з переданого покажчика gz-файлу. Читання закінчується при досягненні максимального розміру `length` розпакованих даних або кінця файлу (EOF)

### Список параметрів

`stream`

Вказівник на gz-файл, повернутий після його успішного відкриття функцією [gzopen()](function.gzopen.md)

`length`

Кількість байт (після розпакування), які слід прочитати.

### Значення, що повертаються

Прочитані дані або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі виникнення помилки повертається **`false`**; раніше, повертався `0` |

### Приклади

**Приклад #1 Приклад використання **gzread()****

```php
<?php
// поместить содержимое gz-файла в строку
$filename = "/usr/local/something.txt.gz";
$zd = gzopen($filename, "r");
$contents = gzread($zd, 10000);
gzclose($zd);
?>
```

### Дивіться також

-   [gzwrite()](function.gzwrite.md) - Бінарний запис у gz-файл
-   [gzopen()](function.gzopen.md) - Відкрити gz-файл
-   [gzgets()](function.gzgets.md) - Отримати рядок із покажчика файлу
-   [gzgetss()](function.gzgetss.md) - Повертає рядок із покажчика gz-файлу та видалити HTML-теги
-   [gzfile()](function.gzfile.md) - Зчитує весь gz-файл у масив
-   [gzpassthru()](function.gzpassthru.md) - Виведення всіх даних з покажчика gz-файлу.