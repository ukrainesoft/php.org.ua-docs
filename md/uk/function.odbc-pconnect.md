---
navigation:
  - function.odbc-num-rows.md: « odbc\_num\_rows
  - function.odbc-prepare.md: odbc\_prepare »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_pconnect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_pconnect

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_pconnect — Відкриває постійне з'єднання з базою даних

### Опис

```methodsynopsis
odbc_pconnect(    string $dsn,    string $user,    string $password,    int $cursor_option = SQL_CUR_USE_DRIVER): resource|false
```

Відкриває постійне з'єднання з базою даних.

Функция очень похожа на[odbc\_connect()](function.odbc-connect.md), крім того, що з'єднання насправді не закривається після завершення роботи скрипта. Наступні запити на з'єднання з тією самою комбінацією `dsn` `user`и`password` (за допомогою [odbc\_connect()](function.odbc-connect.md)и**odbc\_pconnect()**) можуть повторно використовувати постійне з'єднання.

### Список параметрів

Для більш детальної інформації варто звернутись до опису [odbc\_connect()](function.odbc-connect.md)

### Значення, що повертаються

Повертає з'єднання ODBC або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження**: Постійні з'єднання не діють, якщо PHP використовується як CGI.

### Дивіться також

-   [odbc\_connect()](function.odbc-connect.md) \- З'єднує із джерелом даних
-   [Постійні з'єднання з базами даних](features.persistent-connections.md)
