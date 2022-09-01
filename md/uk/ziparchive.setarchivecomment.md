---
navigation:
  - ziparchive.replacefile.md: '« ZipArchive::replaceFile'
  - ziparchive.setcommentindex.md: 'ZipArchive::setCommentIndex »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::setArchiveComment'
---
# ZipArchive::setArchiveComment

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.4.0)

ZipArchive::setArchiveComment — Встановлює коментар до ZIP-архіву

### Опис

```methodsynopsis
public ZipArchive::setArchiveComment(string $comment): bool
```

Встановлює коментар до ZIP-архіву.

### Список параметрів

`comment`

Зміст коментаря.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Створення архіву та встановлення коментарів**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip', ZipArchive::CREATE);
if ($res === TRUE) {
    $zip->addFromString('test.txt', 'содержимое файла');
    $zip->setArchiveComment('новый комментарий архива');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```
