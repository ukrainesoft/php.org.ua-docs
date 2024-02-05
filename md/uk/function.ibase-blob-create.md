---
navigation:
  - function.ibase-blob-close.md: « ibase\_blob\_close
  - function.ibase-blob-echo.md: ibase\_blob\_echo »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_blob\_create
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_blob\_create

(PHP 5, PHP 7 < 7.4.0)

ibase\_blob\_create — Створює новий BLOB-об'єкт для заповнення даними

### Опис

```methodsynopsis
ibase_blob_create(resource $link_identifier = null): resource|false
```

**ibase\_blob\_create()** створює новий BLOB-об'єкт заповнення даними.

### Список параметрів

`link_identifier`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

### Значення, що повертаються

Повертає дескриптор BLOB-об'єкта для подальшого використання з [ibase\_blob\_add()](function.ibase-blob-add.md)или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_blob\_add()](function.ibase-blob-add.md) \- Додає дані до новоствореного BLOB-об'єкту
-   [ibase\_blob\_cancel()](function.ibase-blob-cancel.md) \- Скасує створення BLOB-об'єкта
-   [ibase\_blob\_close()](function.ibase-blob-close.md) \- Закриває BLOB-об'єкт
-   [ibase\_blob\_import()](function.ibase-blob-import.md) \- Створює BLOB-об'єкт, копіює файл і закриває його.
