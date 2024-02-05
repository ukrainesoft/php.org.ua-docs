---
navigation:
  - function.odbc-result.md: « odbc\_result
  - function.odbc-setoption.md: odbc\_setoption »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_rollback
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_rollback

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_rollback - Відкочує транзакцію

### Опис

```methodsynopsis
odbc_rollback(resource $odbc): bool
```

Відкочує всі незавершені операції у з'єднанні.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
