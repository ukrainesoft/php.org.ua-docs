---
navigation:
  - function.odbc-do.md: « odbcдо
  - function.odbc-errormsg.md: odbcerrormsg »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcerror
---
# odbcerror

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

odbcerror — Повертає останній код помилки

### Опис

```methodsynopsis
odbc_error(?resource $odbc = null): string
```

Повертає шестизначний стан ODBC або порожній рядок, якщо помилок не виникло.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbcconnect()](function.odbc-connect.md)

### Значення, що повертаються

Якщо вказано параметр `odbc`, повертається останній стан цієї сполуки, інакше повертається останній стан будь-якої сполуки.

Ця функція повертає осмислене значення лише тоді, коли останній запит ODBC завершився невдало (тобто функція [odbcexec()](function.odbc-exec.md) повернула **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `odbc` тепер допускає значення null. |

### Дивіться також

-   [odbcerrormsg()](function.odbc-errormsg.md) - Повертає останнє повідомлення про помилку
-   [odbcexec()](function.odbc-exec.md) - Виконує інструкцію SQL безпосередньо
