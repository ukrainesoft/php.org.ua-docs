---
navigation:
  - ziparchive.getarchivecomment.md: '« ZipArchive::getArchiveComment'
  - ziparchive.getcommentindex.md: 'ZipArchive::getCommentIndex »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::getArchiveFlag'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::getArchiveFlag

(PHP >= 8.3.0, PECL zip >= 1.22.0)

ZipArchive::getArchiveFlag — Повертає значення глобального прапора ZIP-архіву

### Опис

```methodsynopsis
public ZipArchive::getArchiveFlag(int $flag = 0, int $flags = 0): int
```

Повертає значення глобального прапора ZIP-архіву.

### Список параметрів

`flag`

Глобальний прапор для вилучення, з констант `AFL_*` :

-   **`[ZipArchive::AFL_RDONLY](zip.constants.md#ziparchive.constants.afl-rdonly)`**
    
-   **`[ZipArchive::AFL_IS_TORRENTZIP](zip.constants.md#ziparchive.constants.afl-is-torrentzip)`**
    
-   **`[ZipArchive::AFL_WANT_TORRENTZIP](zip.constants.md#ziparchive.constants.afl-want-torrentzip)`**
    
-   **`[ZipArchive::AFL_CREATE_OR_KEEP_FILE_FOR_EMPTY_ARCHIVE](zip.constants.md#ziparchive.constants.afl-create-or-keep-file-for-empty-archive)`**
    

`flags`

Якщо значення flags дорівнює **`ZipArchive::FL_UNCHANGED`**, Повертається вихідний незмінений прапор.

### Значення, що повертаються

Повертає 1, якщо прапор встановлений для архіву, 0 якщо ні, і -1 у разі виникнення помилки.

### Приклади

**Приклад #1 Перевірка, чи є архів форматом torrentzip**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip');
if ($res === TRUE) {
    var_dump($zip->getArchiveFlag(ZipArchive::AFL_IS_TORRENTZIP));
} else {
    echo 'failed, code:' . $res;
}
?>
```

### Дивіться також

-   [ZipArchive::setArchiveFlag()](ziparchive.setarchiveflag.md) \- Встановлює глобальний прапор ZIP-архіву
