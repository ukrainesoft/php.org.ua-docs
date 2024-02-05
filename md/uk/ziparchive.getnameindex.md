---
navigation:
  - ziparchive.getfromname.md: '« ZipArchive::getFromName'
  - ziparchive.getstatusstring.md: 'ZipArchive::getStatusString »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::getNameIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::getNameIndex

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.5.0)

ZipArchive::getNameIndex — Повертає ім'я елемента за його індексом

### Опис

```methodsynopsis
public ZipArchive::getNameIndex(int $index, int $flags = 0): string|false
```

Повертає ім'я елемента за його індексом.

### Список параметрів

`index`

Індекс елемент.

`flags`

Если флаг установлен в\*\*`ZipArchive::FL_UNCHANGED`\*\*, повертається оригінальне незмінене ім'я

### Значення, що повертаються

Возвращает имя при успехе или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** ZipArchive::getnameindex()\*\*\*\*

```php
<?php
if ($zip->open('test.zip') == TRUE) {
 for ($i = 0; $i < $zip->numFiles; $i++) {
     $filename = $zip->getNameIndex($i);
     // ...
 }
}
?>
```
