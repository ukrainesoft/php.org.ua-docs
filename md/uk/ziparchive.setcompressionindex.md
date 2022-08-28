Встановити метод стиснення запису, заданого його індексом

-   [« ZipArchive::setCommentName](ziparchive.setcommentname.html)
    
-   [ZipArchive::setCompressionName »](ziparchive.setcompressionname.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Встановити метод стиснення запису, заданого його індексом
    

# ZipArchive::setCompressionIndex

(PHP 7, PHP 8, PECL zip >= 1.13.0)

ZipArchive::setCompressionIndex — Встановити метод стиснення запису, заданого його індексом

### Опис

```methodsynopsis
public ZipArchive::setCompressionIndex(int $index, int $method, int $compflags = 0): bool
```

Встановлює метод стиснення запису, заданого його індексом.

### Список параметрів

`index`

Індекс запису.

`method`

Метод стиснення, одна з констант **`ZipArchive::CM_*`**

`compflags`

Рівень стиску.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Додати до архіву файли з різними методами стиснення**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip', ZipArchive::CREATE);
if ($res === TRUE) {
    $zip->addFromString('foo', 'Некоторый текст');
    $zip->addFromString('bar', 'Некоторый другой текст');
    $zip->setCompressionIndex(0, ZipArchive::CM_STORE);
    $zip->setCompressionIndex(1, ZipArchive::CM_DEFLATE);
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```