Встановити метод стиснення запису, заданого на ім'я

-   [« ZipArchive::setCompressionIndex](ziparchive.setcompressionindex.md)
    
-   [ZipArchive::setEncryptionIndex »](ziparchive.setencryptionindex.md)
    
-   [PHP Manual](index.md)
    
-   [ZipArchive](class.ziparchive.md)
    
-   Встановити метод стиснення запису, заданого на ім'я
    

# ZipArchive::setCompressionName

(PHP 7, PHP 8, PECL zip >= 1.13.0)

ZipArchive::setCompressionName — Встановити метод стиснення запису, заданого на ім'я

### Опис

```methodsynopsis
public ZipArchive::setCompressionName(string $name, int $method, int $compflags = 0): bool
```

Встановлює метод стиснення запису заданого на ім'я.

### Список параметрів

`name`

Назва запису.

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
    $zip->setCompressionName('foo', ZipArchive::CM_STORE);
    $zip->setCompressionName('bar', ZipArchive::CM_DEFLATE);
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```

**Приклад #2 Додати файл та встановити метод стиснення**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip', ZipArchive::CREATE);
if ($res === TRUE) {
    $zip->addFile('foo.jpg', 'bar.jpg');
    $zip->setCompressionName('bar.jpg', ZipArchive::CM_XZ);
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```