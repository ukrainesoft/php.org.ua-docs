---
navigation:
  - function.odbc-errormsg.html: « odbcerrormsg
  - function.odbc-execute.html: odbcexecute »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcexec
---
# odbcexec

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcexec — Виконує інструкцію SQL безпосередньо

### Опис

```methodsynopsis
odbc_exec(resource $odbc, string $query): resource|false
```

Надсилає інструкцію SQL на сервер бази даних.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, див. [odbcconnect()](function.odbc-connect.html)

`query`

Інструкція SQL.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC, якщо команда SQL була успішно виконана, або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `flags` був видалений. |

### Дивіться також

-   [odbcprepare()](function.odbc-prepare.html) - готує запит до виконання
-   [odbcexecute()](function.odbc-execute.html) - Виконує запит
