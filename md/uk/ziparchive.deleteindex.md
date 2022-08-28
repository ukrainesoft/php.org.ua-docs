Видаляє елемент в архіві, використовуючи його індекс

-   [« ZipArchive::count](ziparchive.count.html)
    
-   [ZipArchive::deleteName »](ziparchive.deletename.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Видаляє елемент в архіві, використовуючи його індекс
    

# ZipArchive::deleteIndex

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.5.0)

ZipArchive::deleteIndex — Видаляє елемент в архіві за допомогою його індексу.

### Опис

```methodsynopsis
public ZipArchive::deleteIndex(int $index): bool
```

Видаляє елемент (файл або каталог) в архіві за допомогою його індексу.

### Список параметрів

`index`

Індекс елемент видалення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Видалити файл із архіву, використовуючи його індекс**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test.zip') === TRUE) {
    $zip->deleteIndex(2);
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```