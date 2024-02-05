---
navigation:
  - function.odbc-do.md: « odbc\_do
  - function.odbc-errormsg.md: odbc\_errormsg »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_error

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

odbc\_error — Повертає останній код помилки

### Опис

```methodsynopsis
odbc_error(?resource $odbc = null): string
```

Повернення шестизначного стану ODBC або порожній рядок, якщо помилок не виникло.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

### Значення, що повертаються

Если указан параметр`odbc`, повертається останній стан цієї сполуки, інакше повертається останній стан будь-якої сполуки.

Ця функція повертає осмислене значення лише тоді, коли останній запит ODBC завершився невдало (тобто функція [odbc\_exec()](function.odbc-exec.md) повернула **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `odbc` тепер допускає значення null. |

### Дивіться також

-   [odbc\_errormsg()](function.odbc-errormsg.md) \- Повертає останнє повідомлення про помилку
-   [odbc\_exec()](function.odbc-exec.md) \- Виконує інструкцію SQL безпосередньо
