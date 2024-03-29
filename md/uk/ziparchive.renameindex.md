---
navigation:
  - ziparchive.registerprogresscallback.md: '« ZipArchive::registerProgressCallback'
  - ziparchive.renamename.md: 'ZipArchive::renameName »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::renameIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::renameIndex

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.5.0)

ZipArchive::renameIndex — Перейменовує елемент за його індексом

### Опис

```methodsynopsis
public ZipArchive::renameIndex(int $index, string $new_name): bool
```

Перейменовує елемент за його індексом.

### Список параметрів

`index`

Індекс елемента для перейменування.

`new_name`

Нове ім'я

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Перейменування одного елемента**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip');
if ($res === TRUE) {
    $zip->renameIndex(2,'newname.txt');
    $zip->close();
} else {
    echo 'ошибка с кодом:' . $res;
}
?>
```
