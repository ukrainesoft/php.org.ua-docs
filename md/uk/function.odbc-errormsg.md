---
navigation:
  - function.odbc-error.md: « odbcerror
  - function.odbc-exec.md: odbcexec »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcerrormsg
---
# odbcerrormsg

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

odbcerrormsg — Повертає останнє повідомлення про помилку

### Опис

```methodsynopsis
odbc_errormsg(?resource $odbc = null): string
```

Повертає рядок, що містить останнє повідомлення про помилку ODBC або порожній рядок, якщо помилок не виникло.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, див. [odbcconnect()](function.odbc-connect.md)

### Значення, що повертаються

Якщо вказано параметр `odbc`, повертається останній стан цієї сполуки, інакше повертається останній стан будь-якої сполуки.

Ця функція повертає осмислене значення лише тоді, коли останній запит ODBC завершився невдало (тобто функція [odbcexec()](function.odbc-exec.md) повернула **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `odbc` тепер допускає значення null. |

### Дивіться також

-   [odbcerror()](function.odbc-error.md) - Повертає останній код помилки
-   [odbcexec()](function.odbc-exec.md) - Виконує інструкцію SQL безпосередньо
