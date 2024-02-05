---
navigation:
  - function.odbc-fetch-into.md: « odbc\_fetch\_into
  - function.odbc-fetch-row.md: odbc\_fetch\_row »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_fetch\_object
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_fetch\_object

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

odbc\_fetch\_object — Повертає рядок результату як об'єкт

### Опис

```methodsynopsis
odbc_fetch_object(resource $statement, int $row = -1): stdClass|false
```

Повертає об'єкт (object) із запиту ODBC.

### Список параметрів

`statement`

Ресурс результата из[odbc\_exec()](function.odbc-exec.md)

`row`

Необов'язковий параметр, який вказує номер рядка для повернення.

### Значення, що повертаються

Повертає об'єкт, що відповідає рядку, що повертається, або **`false`** якщо рядків більше немає.

### Примітки

> **Зауваження**: Функція при компіляції з підтримкою DBMaker, IBM DB2 або UnixODBC.

### Дивіться також

-   [odbc\_fetch\_row()](function.odbc-fetch-row.md) \- Повертає рядок
-   [odbc\_fetch\_array()](function.odbc-fetch-array.md) \- Повертає рядок результату у вигляді асоціативного масиву
-   [odbc\_num\_rows()](function.odbc-num-rows.md) \- Повертає кількість рядків у результаті
