---
navigation:
  - ziparchive.extractto.md: '« ZipArchive::extractTo'
  - ziparchive.getarchiveflag.md: 'ZipArchive::getArchiveFlag »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::getArchiveComment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::getArchiveComment

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::getArchiveComment — Повертає коментар ZIP-архіву

### Опис

```methodsynopsis
public ZipArchive::getArchiveComment(int $flags = 0): string|false
```

Повертає коментар ZIP-архіву.

### Список параметрів

`flags`

Если флаг установлен в\*\*`ZipArchive::FL_UNCHANGED`\*\*, повертається оригінальний незмінений коментар

### Значення, що повертаються

Повертає коментар ZIP-архіву або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Вивести коментар архіву**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test_with_comment.zip');
if ($res === TRUE) {
    var_dump($zip->getArchiveComment());
    /* Или используя свойство */
    var_dump($zip->comment);
} else {
    echo 'Ошибка с кодом:' . $res;
}
?>
```
