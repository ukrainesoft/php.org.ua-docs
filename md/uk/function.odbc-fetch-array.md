---
navigation:
  - function.odbc-execute.html: « odbcexecute
  - function.odbc-fetch-into.html: odbcfetchinto »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcfetcharray
---
# odbcfetcharray

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

odbcfetcharray - Повертає рядок результату у вигляді асоціативного масиву

### Опис

```methodsynopsis
odbc_fetch_array(resource $statement, int $row = -1): array|false
```

Повертає асоціативний масив (array) із запиту ODBC.

### Список параметрів

`statement`

Ресурс результату з [odbcexec()](function.odbc-exec.html)

`row`

Необов'язковий параметр, який вказує номер рядка для повернення.

### Значення, що повертаються

Повертає масив, що відповідає рядку, що повертається, або **`false`** якщо рядків більше немає.

### Примітки

> **Зауваження**: Функція при компіляції з підтримкою DBMaker, IBM DB2 або UnixODBC.

### Дивіться також

-   [odbcfetchrow()](function.odbc-fetch-row.html) - Повертає рядок
-   [odbcfetchobject()](function.odbc-fetch-object.html) - Повертає рядок результату у вигляді об'єкту
-   [odbcnumrows()](function.odbc-num-rows.html) - Повертає кількість рядків у результаті
