Повертає поточний статус сервера

-   [« mysql\_set\_charset](function.mysql-set-charset.html)
    
-   [mysql\_tablename »](function.mysql-tablename.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає поточний статус сервера
    

# mysqlстати

(PHP 4> = 4.3.0, PHP 5)

mysqlstat — Повертає поточний статус сервера

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_stat()](mysqli.stat.html)
-   [PDO::getAttribute(PDO::ATTR\_SERVER\_INFO)](pdo.getattribute.html)

### Опис

```methodsynopsis
mysql_stat(resource $link_identifier = NULL): string
```

**mysqlстати()** повертає статус сервера.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає рядок з даними аптайму, кількості потоків, запитів, кількістю відкритих таблиць та таблиць зі скинутим внутрішнім кешем (flush tables), а також кількість запитів на секунду. Для отримання повного списку інших змінних вам необхідно використовувати SQL-запит `SHOW STATUS`. Якщо передано некоректний `link_identifier`, то буде повернутий **`null`**

### Приклади

**Приклад #1 Приклад використання **mysqlстати()****

```php
<?php
$link   = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$status = explode('  ', mysql_stat($link));
print_r($status);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => Uptime: 5380
    [1] => Threads: 2
    [2] => Questions: 1321299
    [3] => Slow queries: 0
    [4] => Opens: 26
    [5] => Flush tables: 1
    [6] => Open tables: 17
    [7] => Queries per second avg: 245.595
)
```

**Приклад #2 Альтернативний приклад використання **mysqlстати()****

```php
<?php
$link   = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$result = mysql_query('SHOW STATUS', $link);
while ($row = mysql_fetch_assoc($result)) {
    echo $row['Variable_name'] . ' = ' . $row['Value'] . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
back_log = 50
basedir = /usr/local/
bdb_cache_size = 8388600
bdb_log_buffer_size = 32768
bdb_home = /var/db/mysql/
bdb_max_lock = 10000
bdb_logdir =
bdb_shared_data = OFF
bdb_tmpdir = /var/tmp/
...
```

### Дивіться також

-   [mysql\_get\_server\_info()](function.mysql-get-server-info.html) - Повертає інформацію про сервер MySQL
-   [mysql\_list\_processes()](function.mysql-list-processes.html) - Повертає список процесів MySQL