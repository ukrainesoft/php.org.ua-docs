---
navigation:
  - function.ibase-backup.md: « ibase\_backup
  - function.ibase-blob-cancel.md: ibase\_blob\_cancel »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_blob\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_blob\_add

(PHP 5, PHP 7 < 7.4.0)

ibase\_blob\_add — Додає дані до новоствореного BLOB-об'єкта

### Опис

```methodsynopsis
ibase_blob_add(resource $blob_handle, string $data): void
```

**ibase\_blob\_add()** додає дані в BLOB-об'єкт, створений за допомогою [ibase\_blob\_create()](function.ibase-blob-create.md)

### Список параметрів

`blob_handle`

Дескриптор BLOB-об'єкта, відкритого за допомогою [ibase\_blob\_create()](function.ibase-blob-create.md)

`data`

Дані для додавання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [ibase\_blob\_cancel()](function.ibase-blob-cancel.md) \- Скасує створення BLOB-об'єкта
-   [ibase\_blob\_close()](function.ibase-blob-close.md) \- Закриває BLOB-об'єкт
-   [ibase\_blob\_create()](function.ibase-blob-create.md) \- Створює новий BLOB-об'єкт для заповнення даними
-   [ibase\_blob\_import()](function.ibase-blob-import.md) \- Створює BLOB-об'єкт, копіює файл і закриває його.
