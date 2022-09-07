---
navigation:
  - function.mysql-field-len.md: « mysqlfieldlen
  - function.mysql-field-seek.md: mysqlfieldseek »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlfieldname
---
# mysqlfieldname

(PHP 4, PHP 5)

mysqlfieldname — Повертає назву вказаної колонки результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlifetchfielddirect()](mysqli-result.fetch-field-direct.md) name або orgname
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md) name

### Опис

```methodsynopsis
mysql_field_name(resource $result, int $field_offset): string|false
```

**mysqlfieldname()** повертає назву колонки із зазначеним індексом.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.md)

`field_offset`

Числове усунення поля . `field_offset` починається з `0`. Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Назва поля за вказаним індексом у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlfieldname()****

```php
<?php
/* Таблица пользователей состоит из трёх колонок:
 *   user_id
 *   username
 *   password.
 */
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения с MySQL: ' . mysql_error());
}
$dbname = 'mydb';
$db_selected = mysql_select_db($dbname, $link);
if (!$db_selected) {
    die("Не удалось выбрать базу $dbname: " . mysql_error());
}
$res = mysql_query('select * from users', $link);

echo mysql_field_name($res, 0) . "\n";
echo mysql_field_name($res, 2);
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

-   [mysqlfieldtype()](function.mysql-field-type.md) - Повертає тип вказаного поля із результату запиту
-   [mysqlfieldlen()](function.mysql-field-len.md) - Повертає довжину вказаного поля
