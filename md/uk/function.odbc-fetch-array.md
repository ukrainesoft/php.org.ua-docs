---
navigation:
  - function.odbc-execute.md: « odbc\_execute
  - function.odbc-fetch-into.md: odbc\_fetch\_into »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_fetch\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_fetch\_array

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

odbc\_fetch\_array - Повертає рядок результату у вигляді асоціативного масиву

### Опис

```methodsynopsis
odbc_fetch_array(resource $statement, int $row = -1): array|false
```

Повертає асоціативний масив (array) із запиту ODBC.

### Список параметрів

`statement`

Ресурс результата из[odbc\_exec()](function.odbc-exec.md)

`row`

Необов'язковий параметр, який вказує номер рядка для повернення.

### Значення, що повертаються

Повертає масив, що відповідає рядку, що повертається, або **`false`** якщо рядків більше немає.

### Примітки

> **Зауваження**: Функція при компіляції з підтримкою DBMaker, IBM DB2 або UnixODBC.

### Дивіться також

-   [odbc\_fetch\_row()](function.odbc-fetch-row.md) \- Повертає рядок
-   [odbc\_fetch\_object()](function.odbc-fetch-object.md) \- Повертає рядок результату у вигляді об'єкту
-   [odbc\_num\_rows()](function.odbc-num-rows.md) \- Повертає кількість рядків у результаті
