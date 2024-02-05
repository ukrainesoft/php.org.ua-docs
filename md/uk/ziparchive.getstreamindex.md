---
navigation:
  - ziparchive.getstream.md: '« ZipArchive::getStream'
  - ziparchive.getstreamname.md: 'ZipArchive::getStreamName »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::getStreamIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::getStreamIndex

(PHP 8 >= 8.2.0, PECL zip >= 1.20.0)

ZipArchive::getStreamIndex — Отримує обробник файлу для запису, визначеного його індексом (тільки для читання)

### Опис

```methodsynopsis
public ZipArchive::getStreamIndex(int $index, int $flags = 0): resource|false
```

Отримує обробник файлу для запису, визначеного його індексом. На даний момент метод підтримує лише операції читання.

### Список параметрів

`index`

Індекс запису.

`flags`

Если в flags установлена константа\*\*`ZipArchive::FL_UNCHANGED`\*\*повертається вихідний незмінений потік.

### Значення, що повертаються

У разі успішного виконання повертає покажчик на файл (ресурс) або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Отримання та збереження вмісту запису за допомогою [fread()](function.fread.md)**

```php
<?php
$contents = '';
$z = new ZipArchive();
if ($z->open('test.zip')) {
    $fp = $z->getStreamIndex(1, ZipArchive::FL_UNCHANGED);
    if(!$fp) die($z->getStatusString());

    echo stream_get_contents($fp);

    fclose($fp);
}
?>
```

### Дивіться також

-   [ZipArchive::getStreamName()](ziparchive.getstreamname.md) \- Отримує обробник файлу для запису, визначеного його ім'ям (тільки для читання)
