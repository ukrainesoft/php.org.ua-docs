---
navigation:
  - function.ibase-blob-close.md: « ibaseblobclose
  - function.ibase-blob-echo.md: ibaseblobecho »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaseblobcreate
---
# ibaseblobcreate

(PHP 5, PHP 7 < 7.4.0)

ibaseblobcreate — Створює новий BLOB-об'єкт для заповнення даними

### Опис

```methodsynopsis
ibase_blob_create(resource $link_identifier = null): resource|false
```

**ibaseblobcreate()** створює новий BLOB-об'єкт заповнення даними.

### Список параметрів

`link_identifier`

Ідентифікатор посилання на InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

### Значення, що повертаються

Повертає дескриптор BLOB-об'єкта для подальшого використання з [ibaseblobadd()](function.ibase-blob-add.md) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseblobadd()](function.ibase-blob-add.md) - Додає дані до новоствореного BLOB-об'єкту
-   [ibaseblobcancel()](function.ibase-blob-cancel.md) - Скасує створення BLOB-об'єкта
-   [ibaseblobclose()](function.ibase-blob-close.md) - Закриває BLOB-об'єкт
-   [ibaseblobimport()](function.ibase-blob-import.md) - Створює BLOB-об'єкт, копіює файл і закриває його.
