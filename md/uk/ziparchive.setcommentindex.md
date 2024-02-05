---
navigation:
  - ziparchive.setarchiveflag.md: '« ZipArchive::setArchiveFlag'
  - ziparchive.setcommentname.md: 'ZipArchive::setCommentName »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::setCommentIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::setCommentIndex

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.4.0)

ZipArchive::setCommentIndex — Встановлює коментар до елемента за його індексом

### Опис

```methodsynopsis
public ZipArchive::setCommentIndex(int $index, string $comment): bool
```

Встановлює коментар до елемента за його індексом.

### Список параметрів

`index`

Індекс елемент.

`comment`

Зміст коментаря.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Відкриває архів та встановлює коментар до елемента**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip');
if ($res === TRUE) {
    $zip->setCommentIndex(2, 'новая запись комментария');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```
