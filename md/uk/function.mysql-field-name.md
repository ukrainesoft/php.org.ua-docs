Повертає назву вказаної колонки результату запиту

-   [« mysql\_field\_len](function.mysql-field-len.html)
    
-   [mysql\_field\_seek »](function.mysql-field-seek.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає назву вказаної колонки результату запиту
    

# mysqlfieldname

(PHP 4, PHP 5)

mysqlfieldname — Повертає назву вказаної колонки результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_fetch\_field\_direct()](mysqli-result.fetch-field-direct.html) name або orgname
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.html) name

### Опис

```methodsynopsis
mysql_field_name(resource $result, int $field_offset): string|false
```

**mysqlfieldname()** повертає назву колонки із зазначеним індексом.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.html)

`field_offset`

Числове усунення поля . `field_offset` починається з `0`. Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Назва поля за вказаним індексом у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlfieldname()****

```php
<?php
/* Таблица пользователей состоит из трёх колонок:
 *   user_id
 *   username
 *   password.
 */
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения с MySQL: ' . mysql_error());
}
$dbname = 'mydb';
$db_selected = mysql_select_db($dbname, $link);
if (!$db_selected) {
    die("Не удалось выбрать базу $dbname: " . mysql_error());
}
$res = mysql_query('select * from users', $link);

echo mysql_field_name($res, 0) . "\n";
echo mysql_field_name($res, 2);
?>
```

Результат виконання цього прикладу:

```
user_id
password
```

### Примітки

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlfieldname()**

### Дивіться також

-   [mysql\_field\_type()](function.mysql-field-type.html) - Повертає тип вказаного поля із результату запиту
-   [mysql\_field\_len()](function.mysql-field-len.html) - Повертає довжину вказаного поля