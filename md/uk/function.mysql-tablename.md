Повертає ім'я таблиці, що містить вказане поле

-   [« mysqlstat](function.mysql-stat.html)
    
-   [mysqlthreadid »](function.mysql-thread-id.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає ім'я таблиці, що містить вказане поле
    

# mysqltablename

(PHP 4, PHP 5)

mysqltablename — Повертає ім'я таблиці, яка містить вказане поле

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   SQL запит: `SHOW TABLES`

### Опис

```methodsynopsis
mysql_tablename(resource $result, int $i): string|false
```

Повертає ім'я таблиці з `result`

Ця функція застаріла. Замість неї рекомендується використання [mysqlquery()](function.mysql-query.html) із SQL-запитом `SHOW TABLES [FROM db_name] [LIKE 'pattern']`

### Список параметрів

`result`

Дескриптор результату типу resource, отриманий із виклику [mysqllisttables()](function.mysql-list-tables.html)

`i`

Цілочисельний індекс (номер ряду/таблиці)

### Значення, що повертаються

Ім'я таблиці у разі успішного виконання або **`false`** у разі виникнення помилки.

Використовуйте функцію **mysqltablename()** для роботи з результатом запиту або будь-яку іншу функцію, здатну це робити, наприклад, [mysqlfetcharray()](function.mysql-fetch-array.html)

### Приклади

**Приклад #1 Приклад використання **mysqltablename()****

```php
<?php
mysql_connect("localhost", "mysql_user", "mysql_password");
$result = mysql_list_tables("mydb");
$num_rows = mysql_num_rows($result);
for ($i = 0; $i < $num_rows; $i++) {
    echo "Table: ", mysql_tablename($result, $i), "\n";
}

mysql_free_result($result);
?>
```

### Примітки

> **Зауваження**
> 
> Для визначення кількості таблиць в результаті запиту можна використати функцію [mysqlnumrows()](function.mysql-num-rows.html)

### Дивіться також

-   [mysqllisttables()](function.mysql-list-tables.html) - Повертає список таблиць бази даних MySQL
-   [mysqlfieldtable()](function.mysql-field-table.html) - Повертає назву таблиці, до якої належить зазначене поле
-   [mysqlдбname()](function.mysql-db-name.html) - Повертає назву бази даних із виклику до mysqllistdbs