---
navigation:
  - ziparchive.setexternalattributesindex.md: '« ZipArchive::setExternalAttributesIndex'
  - ziparchive.setmtimeindex.md: 'ZipArchive::setMtimeIndex »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::setExternalAttributesName'
---
# ZipArchive::setExternalAttributesName

(PHP 5 >= 5.6.0, PHP 7, PHP 8, PECL zip >= 1.12.4)

ZipArchive::setExternalAttributesName — Встановлення зовнішніх атрибутів запису, заданого на ім'я

### Опис

```methodsynopsis
public ZipArchive::setExternalAttributesName(    string $name,    int $opsys,    int $attr,    int $flags = 0): bool
```

Встановлення зовнішніх атрибутів запису, заданого на ім'я.

### Список параметрів

`name`

Назва запису.

`opsys`

Код операційної системи визначається однією з констант ZipArchive::OPSYS

`attr`

Зовнішні атрибути. Значення залежить від операційної системи.

`flags`

Необов'язкові прапори. Нині немає.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

У цьому прикладі відкривається файл архіву ZIP test.zip і до нього додається файл test.txt із правами Unix у вигляді зовнішніх атрибутів.

**Приклад #1 Стиснення файлу з його правами Unix**

```php
<?php
$zip = new ZipArchive();
$stat = stat($filename='test.txt');
if (is_array($stat) && $zip->open('test.zip', ZipArchive::CREATE) === TRUE) {
    $zip->addFile($filename);
    $zip->setExternalAttributesName($filename, ZipArchive::OPSYS_UNIX, $stat['mode'] << 16);
    $zip->close();
    echo "готово\n";
} else {
    echo "ошибка\n";
}
?>
```
