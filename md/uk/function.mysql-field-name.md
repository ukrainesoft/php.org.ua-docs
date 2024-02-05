---
navigation:
  - function.mysql-field-len.md: « mysql\_field\_len
  - function.mysql-field-seek.md: mysql\_field\_seek »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_field\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_field\_name

(PHP 4, PHP 5)

mysql\_field\_name — Повертає назву вказаної колонки результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_fetch\_field\_direct()](mysqli-result.fetch-field-direct.md) \[name\]или\[orgname\]
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md) \[name\]

### Опис

```methodsynopsis
mysql_field_name(resource $result, int $field_offset): string|false
```

**mysql\_field\_name()** повертає назву колонки із зазначеним індексом.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

`field_offset`

Числовое смещение поля`field_offset` починається з . Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Назва поля за вказаним індексом у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**mysql\_field\_name()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
user_id
password
```

### Примітки

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_fieldname()**

### Дивіться також

-   [mysql\_field\_type()](function.mysql-field-type.md) \- Повертає тип вказаного поля із результату запиту
-   [mysql\_field\_len()](function.mysql-field-len.md) \- Повертає довжину вказаного поля
