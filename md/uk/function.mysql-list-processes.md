---
navigation:
  - function.mysql-list-fields.md: « mysql\_list\_fields
  - function.mysql-list-tables.md: mysql\_list\_tables »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_list\_processes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_list\_processes

(PHP 4 >= 4.3.0, PHP 5)

mysql\_list\_processes — Повертає список процесів MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_thread\_id()](mysqli.thread-id.md)

### Опис

```methodsynopsis
mysql_list_processes(resource $link_identifier = NULL): resource|false
```

Повертає список поточних процесів на MySQL.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Дескриптор результату (resource) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysql\_list\_processes()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
1 localhost test Processlist 0
4 localhost mysql sleep 5
```

### Дивіться також

-   [mysql\_thread\_id()](function.mysql-thread-id.md) \- Повертає ідентифікатор потоку
-   [mysql\_stat()](function.mysql-stat.md) \- Повертає поточний статус сервера
