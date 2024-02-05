---
navigation:
  - ziparchive.unchangearchive.md: '« ZipArchive::unchangeArchive'
  - ziparchive.unchangename.md: 'ZipArchive::unchangeName »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::unchangeIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::unchangeIndex

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::unchangeIndex — Скасує всі зміни у позиції із заданим індексом

### Опис

```methodsynopsis
public ZipArchive::unchangeIndex(int $index): bool
```

Скасує всі зміни у позиції із заданим індексом.

### Список параметрів

`index`

Індекс позиції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
