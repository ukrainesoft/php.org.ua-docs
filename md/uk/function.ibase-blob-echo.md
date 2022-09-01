---
navigation:
  - function.ibase-blob-create.html: « ibaseblobcreate
  - function.ibase-blob-get.html: ibaseblobget »
  - index.html: PHP Manual
  - ref.ibase.html: Функции Firebird/InterBase
title: ibaseblobecho
---
# ibaseblobecho

(PHP 5, PHP 7 < 7.4.0)

ibaseblobecho — Виводить вміст BLOB-об'єкта у браузер

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseblobopen()](function.ibase-blob-open.html) - Відкриває BLOB-об'єкт для вилучення частин даних
-   [ibaseblobclose()](function.ibase-blob-close.html) - Закриває BLOB-об'єкт
-   [ibaseblobget()](function.ibase-blob-get.html) - Отримує кількість байтів від відкритого BLOB-об'єкта
