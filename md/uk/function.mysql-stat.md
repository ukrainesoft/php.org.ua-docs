- [«mysql_set_charset](function.mysql-set-charset.md)
- [mysql_tablename »](function.mysql-tablename.md)

- [PHP Manual](index.md)
- [MySQL](ref.mysql.md)
- Повертає поточний статус сервера

# mysql_stat

(PHP 4 = 4.3.0, PHP 5)

mysql_stat — Повертає поточний статус сервера

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений до PHP 7.0.0.
Використовуйте замість нього [MySQLi](book.mysqli.md) або
[PDO_MySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

- [mysqli_stat()](mysqli.stat.md)
- [PDO::getAttribute(PDO::ATTR_SERVER_INFO)](pdo.getattribute.md)

### Опис

**mysql_stat**(resource `$link_identifier` = NULL): string

**mysql_stat()** повертає поточний статус сервера.

### Список параметрів

`link_identifier`
З'єднання MySQL. Якщо ідентифікатор з'єднання не було вказано,
використовується останнє з'єднання, відкрите
[mysql_connect()](function.mysql-connect.md). Якщо таке з'єднання не
було знайдено, функція спробує створити таке, якби
[mysql_connect()](function.mysql-connect.md) була викликана без
параметрів. Якщо з'єднання не було знайдено і не змогло бути створено,
генерується помилка рівня **`E_WARNING`**.

### Значення, що повертаються

Повертає рядок з даними аптайму, кількості потоків, запитів,
кількістю відкритих таблиць та таблиць зі скинутим внутрішнім кешем
(flush tables), а також кількість запитів за секунду. Для отримання
повного списку інших змінних вам необхідно буде використати
SQL-запит `SHOW STATUS`. Якщо передано некоректний `link_identifier`,
то буде повернено **`null`**.

### Приклади

**Приклад #1 Приклад використання **mysql_stat()****

` <?php$link   = mysql_connect('localhost', 'mysql_user', 'mysql_password');$status = explode('  ', mysql_stat($link));print_r($status);?> `

Результатом виконання цього прикладу буде щось подібне:

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

**Приклад #2 Альтернативний приклад використання **mysql_stat()****

` <?php$link   = mysql_connect('localhost', 'mysql_user', 'mysql_password');$result = mysql_query('SHOW STATUS', $link);while ($row = mysql_fetch_    row['Variable_name'] . ' = ' . $row['Value'] . "
";}?> `

Результатом виконання цього прикладу буде щось подібне:

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

### Дивіться також

- [mysql_get_server_info()](function.mysql-get-server-info.md) -
Повертає інформацію про сервер MySQL
- [mysql_list_processes()](function.mysql-list-processes.md) -
Повертає список процесів MySQL
