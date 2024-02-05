---
navigation:
  - function.ibase-blob-cancel.md: « ibase\_blob\_cancel
  - function.ibase-blob-create.md: ibase\_blob\_create »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_blob\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_blob\_close

(PHP 5, PHP 7 < 7.4.0)

ibase\_blob\_close — Закриває BLOB-об'єкт

### Опис

```methodsynopsis
ibase_blob_close(resource $blob_handle): mixed
```

Ця функція закриває BLOB-об'єкт, відкритий для читання за допомогою [ibase\_blob\_open()](function.ibase-blob-open.md) або [ibase\_blob\_create()](function.ibase-blob-create.md)

### Список параметрів

`blob_handle`

BLOB-об'єкт, відкритий за допомогою [ibase\_blob\_create()](function.ibase-blob-create.md) або [ibase\_blob\_open()](function.ibase-blob-open.md)

### Значення, що повертаються

Якщо BLOB-об'єкт читався, функція повертає **`true`** у разі успішного виконання, якщо BLOB записувався, функція повертає рядок, що містить ідентифікатор BLOB-об'єкта, призначений їй базою даних. У разі невдачі функція повертає **`false`**

### Дивіться також

-   [ibase\_blob\_cancel()](function.ibase-blob-cancel.md) \- Скасує створення BLOB-об'єкта
-   [ibase\_blob\_open()](function.ibase-blob-open.md) \- Відкриває BLOB-об'єкт для вилучення частин даних
