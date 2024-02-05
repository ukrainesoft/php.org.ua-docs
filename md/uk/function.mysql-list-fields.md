---
navigation:
  - function.mysql-list-dbs.md: « mysql\_list\_dbs
  - function.mysql-list-processes.md: mysql\_list\_processes »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_list\_fields
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_list\_fields

(PHP 4, PHP 5)

mysql\_list\_fields — Повертає список колонок таблиці

**Увага**

Ця функція оголошена застарілою в PHP 5.4.0, і, разом з [модулем MySQL](book.mysql.md)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Так же смотрите раздел[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   SQL запит:`SHOW COLUMNS FROM sometable`

### Опис

```methodsynopsis
mysql_list_fields(string $database_name, string $table_name, resource $link_identifier = NULL): resource
```

Повертає інформацію про таблицю із переданим ім'ям.

Ця функція застаріла. Замість неї рекомендується використовувати [mysql\_query()](function.mysql-query.md) із SQL-запитом `SHOW COLUMNS FROM table [LIKE 'name']`

### Список параметрів

`database_name`

Ім'я опитуваної бази даних.

`table_name`

Ім'я таблиці, що опитується.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Дескриптор результату (resource) у разі успішного виконання, або \*\*`false`\*\*в случае возникновения ошибки.

Результат, що повертається, може бути оброблений за допомогою наступних функцій: [mysql\_field\_flags()](function.mysql-field-flags.md) [mysql\_field\_len()](function.mysql-field-len.md) [mysql\_field\_name()](function.mysql-field-name.md) і [mysql\_field\_type()](function.mysql-field-type.md)

### Приклади

**Приклад #1 Приклад використання** mysql\_list\_fields()\*\*\*\*

```php
<?php
$result = mysql_query("SHOW COLUMNS FROM sometable");
if (!$result) {
    echo 'Ошибка при выполнении запроса: ' . mysql_error();
    exit;
}
if (mysql_num_rows($result) > 0) {
    while ($row = mysql_fetch_assoc($result)) {
        print_r($row);
    }
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [Field] => id
    [Type] => int(7)
    [Null] =>
    [Key] => PRI
    [Default] =>
    [Extra] => auto_increment
)
Array
(
    [Field] => email
    [Type] => varchar(100)
    [Null] =>
    [Key] =>
    [Default] =>
    [Extra] =>
)
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_listfields()**

### Дивіться також

-   [mysql\_field\_flags()](function.mysql-field-flags.md) \- Повертає прапори, пов'язані із зазначеним полем результату запиту
-   [mysql\_info()](function.mysql-info.md) \- Повертає інформацію про останній запит
