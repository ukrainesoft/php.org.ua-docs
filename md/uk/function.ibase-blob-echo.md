---
navigation:
  - function.ibase-blob-create.md: « ibase\_blob\_create
  - function.ibase-blob-get.md: ibase\_blob\_get »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_blob\_echo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_blob\_echo

(PHP 5, PHP 7 < 7.4.0)

ibase\_blob\_echo — Виводить вміст BLOB-об'єкта у браузер

### Опис

```methodsynopsis
ibase_blob_echo(string $blob_id): bool
```

```methodsynopsis
ibase_blob_echo(resource $link_identifier, string $blob_id): bool
```

Функція відкриває BLOB-об'єкт для читання та надсилає його вміст на стандартний висновок (у більшості випадків – браузер).

### Список параметрів

`link_identifier`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

`blob_id`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_blob\_open()](function.ibase-blob-open.md) \- Відкриває BLOB-об'єкт для вилучення частин даних
-   [ibase\_blob\_close()](function.ibase-blob-close.md) \- Закриває BLOB-об'єкт
-   [ibase\_blob\_get()](function.ibase-blob-get.md) \- Отримує кількість байтів від відкритого BLOB-об'єкта
