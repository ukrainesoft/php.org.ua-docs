- [« ZipArchive::getFromName](ziparchive.getfromname.md)
- [ZipArchive::getStatusString »](ziparchive.getstatusstring.md)

- [PHP Manual](index.md)
- [ZipArchive](class.ziparchive.md)
- Повертає ім'я елемента за його індексом

# ZipArchive::getNameIndex

(PHP 5 \>= 5.2.0, PHP 7, PHP 8, PECL zip \>= 1.5.0)

ZipArchive::getNameIndex — Повертає ім'я елемента за його індексом

### Опис

public **ZipArchive::getNameIndex**(int `$index`, int `$flags` = 0):
string\|false

Повертає ім'я елемента за його індексом.

### Список параметрів

`index`
Індекс елемент.

`flags`
Якщо прапор встановлений у **`ZipArchive::FL_UNCHANGED`**, повертається
оригінальне незмінене ім'я.

### Значення, що повертаються

Повертає ім'я за успіху або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ZipArchive::getnameindex()****

` <?phpif ($zip->open('test.zip') == TRUE) { for ($i = 0; $i < $zip->numFiles; $i++) {     $filename = $zip ($i); // ... }}?> `
