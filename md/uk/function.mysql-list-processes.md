Повертає список процесів MySQL

-   [« mysqllistfields](function.mysql-list-fields.html)
    
-   [mysqllisttables »](function.mysql-list-tables.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає список процесів MySQL
    

# mysqllistprocesses

(PHP 4> = 4.3.0, PHP 5)

mysqllistprocesses — Повертає список процесів MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlithreadid()](mysqli.thread-id.html)

### Опис

```methodsynopsis
mysql_list_processes(resource $link_identifier = NULL): resource|false
```

Повертає перелік поточних процесів на сервері MySQL.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Дескриптор результату (resource) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqllistprocesses()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');

$result = mysql_list_processes($link);
while ($row = mysql_fetch_assoc($result)){
    printf("%s %s %s %s %s\n", $row["Id"], $row["Host"], $row["db"],
        $row["Command"], $row["Time"]);
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

-   [mysqlthreadid()](function.mysql-thread-id.html) - Повертає ідентифікатор потоку
-   [mysqlstat()](function.mysql-stat.html) - Повертає поточний статус сервера