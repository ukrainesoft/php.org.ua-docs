Повертає ім'я елемента за його індексом

-   [« ZipArchive::getFromName](ziparchive.getfromname.html)
    
-   [ZipArchive::getStatusString »](ziparchive.getstatusstring.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Повертає ім'я елемента за його індексом
    

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

Якщо прапор встановлений у **`ZipArchive::FL_UNCHANGED`**, повертається оригінальне незмінене ім'я

### Значення, що повертаються

Повертає ім'я при успіху або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ZipArchive::getnameindex()****

```php
<?php
if ($zip->open('test.zip') == TRUE) {
 for ($i = 0; $i < $zip->numFiles; $i++) {
     $filename = $zip->getNameIndex($i);
     // ...
 }
}
?>
```