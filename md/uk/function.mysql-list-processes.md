---
navigation:
  - function.mysql-list-fields.md: « mysqllistfields
  - function.mysql-list-tables.md: mysqllisttables »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqllistprocesses
---
# mysqllistprocesses

(PHP 4> = 4.3.0, PHP 5)

mysqllistprocesses — Повертає список процесів MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlithreadid()](mysqli.thread-id.md)

### Опис

```methodsynopsis
mysql_list_processes(resource $link_identifier = NULL): resource|false
```

Повертає перелік поточних процесів на сервері MySQL.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Дескриптор результату (resource) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqllistprocesses()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');

$result = mysql_list_processes($link);
while ($row = mysql_fetch_assoc($result)){
    printf("%s %s %s %s %s\n", $row["Id"], $row["Host"], $row["db"],
        $row["Command"], $row["Time"]);
}
mysql_free_result($result);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
1 localhost test Processlist 0
4 localhost mysql sleep 5
```

### Дивіться також

-   [mysqlthreadid()](function.mysql-thread-id.md) - Повертає ідентифікатор потоку
-   [mysqlstat()](function.mysql-stat.md) - Повертає поточний статус сервера
