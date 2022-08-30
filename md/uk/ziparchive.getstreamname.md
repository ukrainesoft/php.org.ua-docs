Отримує обробник файлу для запису, визначеного його ім'ям (тільки для читання)

-   [« ZipArchive::getStreamIndex](ziparchive.getstreamindex.html)
    
-   [ZipArchive::isCompressionMethodSupported »](ziparchive.iscompressionmethoddupported.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Отримує обробник файлу для запису, визначеного його ім'ям (тільки для читання)
    

# ZipArchive::getStreamName

(PHP 8 >= 8.2.0, PECL zip >= 1.20.0)

ZipArchive::getStreamName — Отримує обробник файлу для запису, визначеного його ім'ям (тільки для читання)

### Опис

```methodsynopsis
public ZipArchive::getStreamName(string $name, int $flags = 0): resource|false
```

Отримує обробник файлу для запису, визначеного його ім'ям. На даний момент метод підтримує лише операції читання.

### Список параметрів

`name`

Ім'я запису для використання.

`flags`

Якщо у flags встановлена ​​константа \*\*`ZipArchive::FL_UNCHANGED`\*\*повертається вихідний незмінений потік.

### Значення, що повертаються

У разі успішного виконання повертає покажчик на файл (ресурс) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Отримання та збереження вмісту запису за допомогою [fread()](function.fread.html)**

```php
<?php
$contents = '';
$z = new ZipArchive();
if ($z->open('test.zip')) {
    $fp = $z->getStreamName('test', ZipArchive::FL_UNCHANGED);
    if(!$fp) die($z->getStatusString());

    echo stream_get_contents($fp);

    fclose($fp);
}
?>
```

### Дивіться також

-   [ZipArchive::getStreamIndex()](ziparchive.getstreamindex.html) - Отримує обробник файлу для запису, визначеного його індексом (тільки для читання)