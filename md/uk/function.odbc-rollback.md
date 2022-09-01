---
navigation:
  - function.odbc-result.html: « odbcresult
  - function.odbc-setoption.html: odbcsetoption »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcrollback
---
# odbcrollback

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcrollback - Відкочує транзакцію

### Опис

```methodsynopsis
odbc_rollback(resource $odbc): bool
```

Відкочує всі незавершені операції у з'єднанні.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, див. [odbcconnect()](function.odbc-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
