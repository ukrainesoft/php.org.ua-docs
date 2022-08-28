Повертає назву бази даних із виклику до mysqllistdbs

-   [« mysql\_data\_seek](function.mysql-data-seek.html)
    
-   [mysql\_db\_query »](function.mysql-db-query.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає назву бази даних із виклику до mysqllistdbs
    

# mysqlдбname

(PHP 4, PHP 5)

mysqlдбname — Повертає назву бази даних із виклику до [mysql\_list\_dbs()](function.mysql-list-dbs.html)

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   Запит: `SELECT DATABASE()`

### Опис

```methodsynopsis
mysql_db_name(resource $result, int $row, mixed $field = NULL): string
```

Повертає назву бази даних із виклику до [mysql\_list\_dbs()](function.mysql-list-dbs.html)

### Список параметрів

`result`

Дескриптор результату, отриманий із виклику [mysql\_list\_dbs()](function.mysql-list-dbs.html)

`row`

Індекс у результаті.

`field`

Ім'я поля.

### Значення, що повертаються

Повертає назву бази даних у разі успішного виконання, або **`false`** у разі помилки. У разі повернення **`false`** використовуйте [mysql\_error()](function.mysql-error.html) визначення природи помилок.

### Приклади

**Приклад #1 Приклад використання **mysqlдбname()****

```php
<?php
error_reporting(E_ALL);

$link = mysql_connect('dbhost', 'username', 'password');
$db_list = mysql_list_dbs($link);

$i = 0;
$cnt = mysql_num_rows($db_list);
while ($i < $cnt) {
    echo mysql_db_name($db_list, $i) . "\n";
    $i++;
}
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqldbname()**

### Дивіться також

-   [mysql\_list\_dbs()](function.mysql-list-dbs.html) - Повертає список баз даних, доступних на сервері
-   [mysql\_tablename()](function.mysql-tablename.html) - Повертає ім'я таблиці, що містить вказане поле