---
navigation:
  - ziparchive.setexternalattributesname.md: '« ZipArchive::setExternalAttributesName'
  - ziparchive.setmtimename.md: 'ZipArchive::setMtimeName »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::setMtimeIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

Приклад створення ZIP-архіву test.zip, додавання до нього файлу test.txt та встановлення часу модифікації для нього.

**Приклад #1 Архівування файлу**

```php
<?php
$zip = new ZipArchive();
if ($zip->open('test.zip', ZipArchive::CREATE) === TRUE) {
    $zip->addFile('text.txt');
    $zip->setMtimeIndex(0, mktime(0,0,0,12,25,2019));
    $zip->close();
    echo "Ok\n";
} else {
    echo "KO\n";
}
?>
```

### Примітки

> **Зауваження** :
> 
> Ця функція доступна лише в тому випадку, якщо збірка здійснювалася з libzip ≥ 1.0.0.

### Дивіться також

-   [ZipArchive::setMtimeName()](ziparchive.setmtimename.md) \- Встановити час модифікації файлу на його ім'я
