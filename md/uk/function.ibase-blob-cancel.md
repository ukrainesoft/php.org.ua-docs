---
navigation:
  - function.ibase-blob-add.md: « ibase\_blob\_add
  - function.ibase-blob-close.md: ibase\_blob\_close »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_blob\_cancel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_blob\_cancel

(PHP 5, PHP 7 < 7.4.0)

ibase\_blob\_cancel — Скасує створення об'єкта BLOB

### Опис

```methodsynopsis
ibase_blob_cancel(resource $blob_handle): bool
```

Ця функція відкидає BLOB-об'єкт, якщо його ще не було закрито за допомогою [ibase\_blob\_close()](function.ibase-blob-close.md)

### Список параметрів

`blob_handle`

Дескриптор BLOB-об'єкта, відкритий за допомогою [ibase\_blob\_create()](function.ibase-blob-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_blob\_close()](function.ibase-blob-close.md) \- Закриває BLOB-об'єкт
-   [ibase\_blob\_create()](function.ibase-blob-create.md) \- Створює новий BLOB-об'єкт для заповнення даними
-   [ibase\_blob\_import()](function.ibase-blob-import.md) \- Створює BLOB-об'єкт, копіює файл і закриває його.
