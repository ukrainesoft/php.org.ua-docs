---
navigation:
  - function.mysql-set-charset.md: « mysqlsetcharset
  - function.mysql-tablename.md: mysqltablename »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlстати
---
# mysqlстати

(PHP 4> = 4.3.0, PHP 5)

mysqlstat — Повертає поточний статус сервера

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlistat()](mysqli.stat.md)
-   [PDO::getAttribute(PDO::ATTRSERVERINFO)](pdo.getattribute.md)

### Опис

```methodsynopsis
mysql_stat(resource $link_identifier = NULL): string
```

**mysqlстати()** повертає статус сервера.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

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

-   [mysqlgetserverinfo()](function.mysql-get-server-info.md) - Повертає інформацію про сервер MySQL
-   [mysqllistprocesses()](function.mysql-list-processes.md) - Повертає список процесів MySQL
