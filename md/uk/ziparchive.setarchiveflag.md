---
navigation:
  - ziparchive.setarchivecomment.md: '« ZipArchive::setArchiveComment'
  - ziparchive.setcommentindex.md: 'ZipArchive::setCommentIndex »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::setArchiveFlag'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::setArchiveFlag

(PHP >= 8.3.0, PECL zip >= 1.22.0)

ZipArchive::setArchiveFlag — Встановлює глобальний прапор ZIP-архіву

### Опис

```methodsynopsis
public ZipArchive::setArchiveFlag(int $flag, int $value): bool
```

Встановлює глобальний прапор ZIP-архіву.

### Список параметрів

`flag`

Глобальний прапор, який необхідно змінити, з констант `AFL_*` :

-   **`[ZipArchive::AFL_WANT_TORRENTZIP](zip.constants.md#ziparchive.constants.afl-want-torrentzip)`**
    
-   **`[ZipArchive::AFL_CREATE_OR_KEEP_FILE_FOR_EMPTY_ARCHIVE](zip.constants.md#ziparchive.constants.afl-create-or-keep-file-for-empty-archive)`**
    

`value`

Нове значення прапора.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Створення архіву torrentzip**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip', ZipArchive::CREATE);
if ($res === TRUE) {
    $zip->setArchiveFlag(ZipArchive::AFL_WANT_TORRENTZIP, 1);
    $zip->addFromString('test.txt', 'содержимое файла');
    $zip->close();
    echo 'Успешное выполнение';
} else {
    echo 'Ошибка';
}
?>
```

### Дивіться також

-   [ZipArchive::getArchiveFlag()](ziparchive.getarchiveflag.md) \- Повертає значення глобального прапора ZIP-архіву
