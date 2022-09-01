---
navigation:
  - function.ibase-blob-open.html: « ibaseblobopen
  - function.ibase-commit-ret.html: ibasecommitret »
  - index.html: PHP Manual
  - ref.ibase.html: Функции Firebird/InterBase
title: ibaseclose
---
# ibaseclose

(PHP 5, PHP 7 < 7.4.0)

ibaseclose — Закриває з'єднання з базою даних InterBase

### Опис

```methodsynopsis
ibase_close(resource $connection_id = null): bool
```

Закриває посилання на базу даних InterBase, пов'язану з ідентифікатором з'єднання, отриманим за допомогою [ibaseconnect()](function.ibase-connect.html). Стандартна транзакція для посилання зафіксована, інші транзакції скасовані.

### Список параметрів

`connection_id`

Ідентифікатор посилання InterBase, отриманий за допомогою [ibaseconnect()](function.ibase-connect.html). Якщо не вказано, передбачається останнє відкрите посилання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseconnect()](function.ibase-connect.html) - Відкриває з'єднання з базою даних
-   [ibasepconnect()](function.ibase-pconnect.html) - Відкриває постійне з'єднання з базою даних InterBase
