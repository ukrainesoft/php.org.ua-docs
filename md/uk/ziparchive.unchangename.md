---
navigation:
  - ziparchive.unchangeindex.md: '« ZipArchive::unchangeIndex'
  - ref.zip.md: Опції Zip »
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::unchangeName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::unchangeName

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.5.0)

ZipArchive::unchangeName — Скасує всі зміни у позиції із заданим ім'ям

### Опис

```methodsynopsis
public ZipArchive::unchangeName(string $name): bool
```

Скасує всі зміни у позиції із заданим ім'ям.

### Список параметрів

`name`

Назва позиції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
