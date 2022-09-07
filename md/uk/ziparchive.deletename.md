---
navigation:
  - ziparchive.deleteindex.md: '« ZipArchive::deleteIndex'
  - ziparchive.extractto.md: 'ZipArchive::extractTo »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::deleteName'
---
# ZipArchive::deleteName

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.5.0)

ZipArchive::deleteName — Видаляє елемент в архіві за допомогою його імені.

### Опис

```methodsynopsis
public ZipArchive::deleteName(string $name): bool
```

Видаляє елемент (файл або каталог) в архіві за допомогою його імені.

### Список параметрів

`name`

Ім'я елемента видалення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Видалити файл та каталог із архіву, використовуючи імена**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test1.zip') === TRUE) {
    $zip->deleteName('testfromfile.php');
    $zip->deleteName('testDir/');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```
