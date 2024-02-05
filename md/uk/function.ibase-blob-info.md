---
navigation:
  - function.ibase-blob-import.md: « ibase\_blob\_import
  - function.ibase-blob-open.md: ibase\_blob\_open »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_blob\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_blob\_info

(PHP 5, PHP 7 < 7.4.0)

ibase\_blob\_info — Повертає довжину BLOB-об'єкта та іншу корисну інформацію

### Опис

```methodsynopsis
ibase_blob_info(resource $link_identifier, string $blob_id): array
```

```methodsynopsis
ibase_blob_info(string $blob_id): array
```

Повертає довжину BLOB-об'єкта та іншу корисну інформацію.

### Список параметрів

`link_identifier`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

`blob_id`

Ідентифікатор об'єкта BLOB.

### Значення, що повертаються

Повертає масив, що містить інформацію про BLOB-об'єкт. Повертана інформація складається з довжини BLOB-об'єкта, кількості сегментів, що містяться в ньому, розміру найбільшого сегмента і того, чи є він BLOB-потоком або сегментованим BLOB-об'єктом.
