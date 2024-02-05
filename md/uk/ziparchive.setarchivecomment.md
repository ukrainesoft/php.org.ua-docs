---
navigation:
  - ziparchive.replacefile.md: '« ZipArchive::replaceFile'
  - ziparchive.setarchiveflag.md: 'ZipArchive::setArchiveFlag »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::setArchiveComment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Створення архіву та встановлення коментарів**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip', ZipArchive::CREATE);
if ($res === TRUE) {
    $zip->addFromString('test.txt', 'содержимое файла');
    $zip->setArchiveComment('новый комментарий архива');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```
