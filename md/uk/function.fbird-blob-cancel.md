---
navigation:
  - function.fbird-blob-add.md: « fbird\_blob\_add
  - function.fbird-blob-close.md: fbird\_blob\_close »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: fbird\_blob\_cancel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fbird\_blob\_cancel

(PHP 5, PHP 7 < 7.4.0)

fbird\_blob\_cancel — Скасовує створення BLOB

### Опис

```methodsynopsis
fbird_blob_cancel(resource $blob_handle): bool
```

Ця функція припиняє використання BLOB, якщо вона ще не була закрита [fbird\_blob\_close()](function.fbird-blob-close.md)

### Список параметрів

`blob_handle`

Дескриптор BLOB, відкритий за допомогою [fbird\_blob\_create()](function.fbird-blob-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fbird\_blob\_close()](function.fbird-blob-close.md) \- Псевдонім ibase\_blob\_close
-   [fbird\_blob\_create()](function.fbird-blob-create.md) \- Псевдонім ibase\_blob\_create
-   [fbird\_blob\_import()](function.fbird-blob-import.md) \- Псевдонім ibase\_blob\_import
