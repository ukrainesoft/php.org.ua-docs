---
navigation:
  - function.ibase-backup.md: « ibasebackup
  - function.ibase-blob-cancel.md: ibaseblobcancel »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaseblobadd
---
# ibaseblobadd

(PHP 5, PHP 7 < 7.4.0)

ibaseblobadd — Додає дані до новоствореного BLOB-об'єкта

### Опис

```methodsynopsis
ibase_blob_add(resource $blob_handle, string $data): void
```

**ibaseblobadd()** додає дані в BLOB-об'єкт, створений за допомогою [ibaseblobcreate()](function.ibase-blob-create.md)

### Список параметрів

`blob_handle`

Дескриптор BLOB-об'єкта, відкритого за допомогою [ibaseblobcreate()](function.ibase-blob-create.md)

`data`

Дані для додавання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [ibaseblobcancel()](function.ibase-blob-cancel.md) - Скасує створення BLOB-об'єкта
-   [ibaseblobclose()](function.ibase-blob-close.md) - Закриває BLOB-об'єкт
-   [ibaseblobcreate()](function.ibase-blob-create.md) - Створює новий BLOB-об'єкт для заповнення даними
-   [ibaseblobimport()](function.ibase-blob-import.md) - Створює BLOB-об'єкт, копіює файл і закриває його.
