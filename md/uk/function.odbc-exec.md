---
navigation:
  - function.odbc-errormsg.md: « odbc\_errormsg
  - function.odbc-execute.md: odbc\_execute »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_exec
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_exec

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_exec — Виконує інструкцію SQL безпосередньо

### Опис

```methodsynopsis
odbc_exec(resource $odbc, string $query): resource|false
```

Надсилає інструкцію SQL на сервер бази даних.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

`query`

Інструкція SQL.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC, якщо команда SQL була успішно виконана, або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`flags`був видалений. |

### Дивіться також

-   [odbc\_prepare()](function.odbc-prepare.md) \- готує запит до виконання
-   [odbc\_execute()](function.odbc-execute.md) \- Виконує запит
