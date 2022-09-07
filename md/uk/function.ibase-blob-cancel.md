---
navigation:
  - function.ibase-blob-add.md: « ibaseblobadd
  - function.ibase-blob-close.md: ibaseblobclose »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaseblobcancel
---
# ibaseblobcancel

(PHP 5, PHP 7 < 7.4.0)

ibaseblobcancel — Скасує створення об'єкта BLOB

### Опис

```methodsynopsis
ibase_blob_cancel(resource $blob_handle): bool
```

Ця функція відкидає BLOB-об'єкт, якщо його ще не було закрито за допомогою [ibaseblobclose()](function.ibase-blob-close.md)

### Список параметрів

`blob_handle`

Дескриптор BLOB-об'єкта, відкритий за допомогою [ibaseblobcreate()](function.ibase-blob-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseblobclose()](function.ibase-blob-close.md) - Закриває BLOB-об'єкт
-   [ibaseblobcreate()](function.ibase-blob-create.md) - Створює новий BLOB-об'єкт для заповнення даними
-   [ibaseblobimport()](function.ibase-blob-import.md) - Створює BLOB-об'єкт, копіює файл і закриває його.
