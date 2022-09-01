---
navigation:
  - ziparchive.getarchivecomment.html: '« ZipArchive::getArchiveComment'
  - ziparchive.getcommentname.html: 'ZipArchive::getCommentName »'
  - index.html: PHP Manual
  - class.ziparchive.html: ZipArchive
title: 'ZipArchive::getCommentIndex'
---
# ZipArchive::getCommentIndex

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.4.0)

ZipArchive::getCommentIndex — Повертає коментар елемента, використовуючи його індекс

### Опис

```methodsynopsis
public ZipArchive::getCommentIndex(int $index, int $flags = 0): string|false
```

Повертає коментар елемента, використовуючи його індекс.

### Список параметрів

`index`

Індекс запису.

`flags`

Якщо прапор встановлений у **`ZipArchive::FL_UNCHANGED`**, повертається оригінальний незмінений коментар

### Значення, що повертаються

Повертає коментар при успіху або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Вивести коментар елемента**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test1.zip');
if ($res === TRUE) {
    var_dump($zip->getCommentIndex(1));
} else {
    echo 'Ошибка с кодом:' . $res;
}
?>
```
