---
navigation:
  - function.odbc-fetch-into.md: « odbcfetchinto
  - function.odbc-fetch-row.md: odbcfetchrow »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcfetchobject
---
# odbcfetchobject

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

odbcfetchobject — Повертає рядок результату як об'єкт

### Опис

```methodsynopsis
odbc_fetch_object(resource $statement, int $row = -1): stdClass|false
```

Повертає об'єкт (object) із запиту ODBC.

### Список параметрів

`statement`

Ресурс результату з [odbcexec()](function.odbc-exec.md)

`row`

Необов'язковий параметр, який вказує номер рядка для повернення.

### Значення, що повертаються

Повертає об'єкт, що відповідає рядку, що повертається, або **`false`** якщо рядків більше немає.

### Примітки

> **Зауваження**: Функція при компіляції з підтримкою DBMaker, IBM DB2 або UnixODBC.

### Дивіться також

-   [odbcfetchrow()](function.odbc-fetch-row.md) - Повертає рядок
-   [odbcfetcharray()](function.odbc-fetch-array.md) - Повертає рядок результату у вигляді асоціативного масиву
-   [odbcnumrows()](function.odbc-num-rows.md) - Повертає кількість рядків у результаті
