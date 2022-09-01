---
navigation:
  - function.fbird-blob-add.html: « fbirdblobadd
  - function.fbird-blob-close.html: fbirdblobclose »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: fbirdblobcancel
---
# fbirdblobcancel

(PHP 5, PHP 7 < 7.4.0)

fbirdblobcancel — Скасовує створення BLOB

### Опис

```methodsynopsis
fbird_blob_cancel(resource $blob_handle): bool
```

Ця функція припиняє використання BLOB, якщо вона ще не була закрита [fbirdblobclose()](function.fbird-blob-close.md)

### Список параметрів

`blob_handle`

Дескриптор BLOB, відкритий за допомогою [fbirdblobcreate()](function.fbird-blob-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fbirdblobclose()](function.fbird-blob-close.md) - Псевдонім ibaseblobclose
-   [fbirdblobcreate()](function.fbird-blob-create.md) - Псевдонім ibaseblobcreate
-   [fbirdblobimport()](function.fbird-blob-import.md) - Псевдонім ibaseblobimport
