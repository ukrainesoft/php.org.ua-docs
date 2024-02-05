---
navigation:
  - function.ibase-blob-info.md: « ibase\_blob\_info
  - function.ibase-close.md: ibase\_close »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_blob\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_blob\_open

(PHP 5, PHP 7 < 7.4.0)

ibase\_blob\_open — Відкриває BLOB-об'єкт для вилучення частин даних

### Опис

```methodsynopsis
ibase_blob_open(resource $link_identifier, string $blob_id): resource|false
```

```methodsynopsis
ibase_blob_open(string $blob_id): resource|false
```

Відкриває існуючий об'єкт BLOB для читання.

### Список параметрів

`link_identifier`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

`blob_id`

Ідентифікатор об'єкта BLOB.

### Значення, що повертаються

Повертає дескриптор BLOB-об'єкта для подальшого використання за допомогою [ibase\_blob\_get()](function.ibase-blob-get.md)или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_blob\_close()](function.ibase-blob-close.md) \- Закриває BLOB-об'єкт
-   [ibase\_blob\_echo()](function.ibase-blob-echo.md) \- Виводить вміст BLOB-об'єкта у браузер
-   [ibase\_blob\_get()](function.ibase-blob-get.md) \- Отримує кількість байтів від відкритого BLOB-об'єкта
