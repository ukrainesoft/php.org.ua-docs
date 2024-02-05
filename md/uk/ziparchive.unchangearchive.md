---
navigation:
  - ziparchive.unchangeall.md: '« ZipArchive::unchangeAll'
  - ziparchive.unchangeindex.md: 'ZipArchive::unchangeIndex »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::unchangeArchive'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::unchangeArchive

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::unchangeArchive — Повертає всі глобальні зміни, зроблені в архіві

### Опис

```methodsynopsis
public ZipArchive::unchangeArchive(): bool
```

Повертає всі глобальні зміни, зроблені у архіві. На даний момент лише скасовує зміни у коментарях до архіву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
