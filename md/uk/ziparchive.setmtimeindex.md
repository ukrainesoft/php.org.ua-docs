Встановити час модифікації файлу за його індексом

-   [« ZipArchive::setExternalAttributesName](ziparchive.setexternalattributesname.html)
    
-   [ZipArchive::setMtimeName »](ziparchive.setmtimename.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Встановити час модифікації файлу за його індексом
    

# ZipArchive::setMtimeIndex

(PHP >= 8.0.0, PECL zip >= 1.16.0)

ZipArchive::setMtimeIndex — Встановити час модифікації файлу за його індексом

### Опис

```methodsynopsis
public ZipArchive::setMtimeIndex(int $index, int $timestamp, int $flags = 0): bool
```

Встановити час модифікації файлу за його індексом.

### Список параметрів

`index`

Індекс.

`timestamp`

Час модифікації (тимчасова мітка unix) файлу.

`flags`

Необов'язкові прапори. В даний момент не використовуються.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

Приклад створення ZIP-архіву test.zip, додавання до нього файлу test.txt та встановлення часу модифікації для нього.

**Приклад #1 Архівування файлу**

```php
<?php
$zip = new ZipArchive();
if ($zip->open('test.zip', ZipArchive::CREATE) === TRUE) {
    $zip->addFile('text.txt');
    $zip->setMtimeIndex(0, mktime(0,0,0,12,25,2019));
    $zip->close();
    echo "Ok\n";
} else {
    echo "KO\n";
}
?>
```

### Примітки

> **Зауваження**
> 
> Ця функція доступна лише в тому випадку, якщо збірка здійснювалася з libzip ≥ 1.0.0.

### Дивіться також

-   [ZipArchive::setMtimeName()](ziparchive.setmtimename.html) - Встановити час модифікації файлу на його ім'я