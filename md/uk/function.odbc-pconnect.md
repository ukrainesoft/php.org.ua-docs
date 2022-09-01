---
navigation:
  - function.odbc-num-rows.html: « odbcnumrows
  - function.odbc-prepare.html: odbcprepare »
  - index.md: PHP Manual
  - ref.uodbc.md: Функции ODBC
title: odbcpconnect
---
# odbcpconnect

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcpconnect — Відкриває постійне з'єднання з базою даних

### Опис

```methodsynopsis
odbc_pconnect(    string $dsn,    string $user,    string $password,    int $cursor_option = SQL_CUR_USE_DRIVER): resource|false
```

Відкриває постійне з'єднання з базою даних.

Функція дуже схожа на [odbcconnect()](function.odbc-connect.html), крім того, що з'єднання насправді не закривається після завершення роботи скрипта. Наступні запити на з'єднання з тією самою комбінацією `dsn` `user` і `password` (за допомогою [odbcconnect()](function.odbc-connect.md) і **odbcpconnect()**) можуть повторно використовувати постійне з'єднання.

### Список параметрів

Для більш детальної інформації варто звернутись до опису [odbcconnect()](function.odbc-connect.md)

### Значення, що повертаються

Повертає з'єднання ODBC або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**: Постійні з'єднання не діють, якщо PHP використовується як CGI.

### Дивіться також

-   [odbcconnect()](function.odbc-connect.md) - З'єднує із джерелом даних
-   [Постійні з'єднання з базами даних](features.persistent-connections.md)
