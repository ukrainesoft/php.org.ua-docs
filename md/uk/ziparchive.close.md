---
navigation:
  - ziparchive.clearerror.md: '« ZipArchive::clearError'
  - ziparchive.count.md: 'ZipArchive::count »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::close

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::close — Закриває активний архів (відкритий або знову створений)

### Опис

```methodsynopsis
public ZipArchive::close(): bool
```

Закриває відкритий або створений архів та зберігає зміни. Метод автоматично викликається наприкінці виконання сценарію.

Якщо архів не містить файлів, файл за замовчуванням повністю видаляється (порожній архів не записується) відповідно до значення глобального прапора **`[ZipArchive::AFL_CREATE_OR_KEEP_FILE_FOR_EMPTY_ARCHIVE](zip.constants.md#ziparchive.constants.afl-create-or-keep-file-for-empty-archive)`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ZipArchive::setArchiveFlag()](ziparchive.setarchiveflag.md) \- Встановлює глобальний прапор ZIP-архіву
