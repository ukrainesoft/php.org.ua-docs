---
navigation:
  - ziparchive.getcommentindex.md: '« ZipArchive::getCommentIndex'
  - ziparchive.getexternalattributesindex.md: 'ZipArchive::getExternalAttributesIndex »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::getCommentName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::getCommentName

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.4.0)

ZipArchive::getCommentName — Повертає коментар елемента, використовуючи його ім'я

### Опис

```methodsynopsis
public ZipArchive::getCommentName(string $name, int $flags = 0): string|false
```

Повертає коментар елемента, використовуючи його ім'я.

### Список параметрів

`name`

Ім'я елемент.

`flags`

Если флаг установлен в\*\*`ZipArchive::FL_UNCHANGED`\*\*, повертається оригінальний незмінений коментар

### Значення, що повертаються

Повертає коментар при успіху або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Вивести коментар елемента**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test1.zip');
if ($res === TRUE) {
    var_dump($zip->getCommentName('test/entry1.txt'));
} else {
    echo 'Ошибка с кодом:' . $res;
}
?>
```
