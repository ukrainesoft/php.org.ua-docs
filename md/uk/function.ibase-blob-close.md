---
navigation:
  - function.ibase-blob-cancel.html: « ibaseblobcancel
  - function.ibase-blob-create.html: ibaseblobcreate »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaseblobclose
---
# ibaseblobclose

(PHP 5, PHP 7 < 7.4.0)

ibaseblobclose — Закриває BLOB-об'єкт

### Опис

```methodsynopsis
ibase_blob_close(resource $blob_handle): mixed
```

Ця функція закриває BLOB-об'єкт, відкритий для читання за допомогою [ibaseblobopen()](function.ibase-blob-open.html) або [ibaseblobcreate()](function.ibase-blob-create.md)

### Список параметрів

`blob_handle`

BLOB-об'єкт, відкритий за допомогою [ibaseblobcreate()](function.ibase-blob-create.html) або [ibaseblobopen()](function.ibase-blob-open.md)

### Значення, що повертаються

Якщо BLOB-об'єкт читався, функція повертає **`true`** у разі успішного виконання, якщо BLOB записувався, функція повертає рядок, що містить ідентифікатор BLOB-об'єкта, призначений їй базою даних. У разі невдачі функція повертає **`false`**

### Дивіться також

-   [ibaseblobcancel()](function.ibase-blob-cancel.md) - Скасує створення BLOB-об'єкта
-   [ibaseblobopen()](function.ibase-blob-open.md) - Відкриває BLOB-об'єкт для вилучення частин даних
