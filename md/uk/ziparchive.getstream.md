---
navigation:
  - ziparchive.getstatusstring.html: '« ZipArchive::getStatusString'
  - ziparchive.getstreamindex.html: 'ZipArchive::getStreamIndex »'
  - index.html: PHP Manual
  - class.ziparchive.html: ZipArchive
title: 'ZipArchive::getStream'
---
# ZipArchive::getStream

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::getStream — Отримати дескриптор файлу елемента, визначений на ім'я елемента (лише для читання)

### Опис

```methodsynopsis
public ZipArchive::getStream(string $name): resource|false
```

Отримати дескриптор файлу, визначений на ім'я елемента. Наразі підтримуються лише операції читання.

### Список параметрів

`name`

Ім'я елемента, що використовується.

### Значення, що повертаються

Повертає файловий покажчик (ресурс) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Отримати вміст елемента за допомогою [fread()](function.fread.html) і зберегти його**

```php
<?php
$contents = '';
$z = new ZipArchive();
if ($z->open('test.zip')) {
    $fp = $z->getStream('test');
    if(!$fp) exit("ошибка\n");

    while (!feof($fp)) {
        $contents .= fread($fp, 2);
    }

    fclose($fp);
    file_put_contents('t',$contents);
    echo "готово.\n";
}
?>
```

**Приклад #2 Те саме, що й у попередньому прикладі, але використовуючи [fopen()](function.fopen.html) і через обгортку zip-потоку**

```php
<?php
$contents = '';
$fp = fopen('zip://' . dirname(__FILE__) . '/test.zip#test', 'r');
if (!$fp) {
    exit("Не получается открыть\n");
}
while (!feof($fp)) {
    $contents .= fread($fp, 2);
}
echo "$contents\n";
fclose($fp);
echo "Готово.\n";
?>
```

**Приклад #3 ZIP-потік та зображення можуть бути використані також у функції XML**

```php
<?php
$im = imagecreatefromgif('zip://' . dirname(__FILE__) . '/test_im.zip#pear_item.gif');
imagepng($im, 'a.png');
?>
```

### Дивіться також

-   [ZipArchive::getStreamIndex()](ziparchive.getstreamindex.html) - Отримує обробник файлу для запису, визначеного його індексом (тільки для читання)
-   [ZipArchive::getStreamName()](ziparchive.getstreamname.html) - Отримує обробник файлу для запису, визначеного його ім'ям (тільки для читання)
-   [Стислі потоки](wrappers.compression.html)
