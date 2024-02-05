---
navigation:
  - function.mysql-set-charset.md: « mysql\_set\_charset
  - function.mysql-tablename.md: mysql\_tablename »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_stat
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_stat

(PHP 4 >= 4.3.0, PHP 5)

mysql\_stat — Повертає поточний статус сервера

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_stat()](mysqli.stat.md)
-   [PDO::getAttribute()](pdo.getattribute.md)с параметром`attribute`заданим як\*\*`PDO::ATTR_SERVER_INFO`\*\*

### Опис

```methodsynopsis
mysql_stat(resource $link_identifier = NULL): string
```

**mysql\_stat()** повертає статус сервера.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає рядок з даними аптайму, кількості потоків, запитів, кількістю відкритих таблиць та таблиць зі скинутим внутрішнім кешем (flush tables), а також кількість запитів на секунду. Щоб отримати повний список інших змінних, вам необхідно буде використовувати SQL-запит. `SHOW STATUS`. Якщо передано некоректний `link_identifier`, то буде повернутий **`null`**

### Приклади

**Пример #1 Пример использования**mysql\_stat()\*\*\*\*

```php
<?php
$link   = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$status = explode('  ', mysql_stat($link));
print_r($status);
?>
```

Висновок наведеного прикладу буде схожим на:

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

**Приклад #2 Альтернативний приклад використання **mysql\_stat()****

```php
<?php
$link   = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$result = mysql_query('SHOW STATUS', $link);
while ($row = mysql_fetch_assoc($result)) {
    echo $row['Variable_name'] . ' = ' . $row['Value'] . "\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [mysql\_get\_server\_info()](function.mysql-get-server-info.md) \- Повертає інформацію про сервер MySQL
-   [mysql\_list\_processes()](function.mysql-list-processes.md) \- Повертає список процесів MySQL
