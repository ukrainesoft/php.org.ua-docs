---
navigation:
  - function.mysql-list-processes.md: « mysql\_list\_processes
  - function.mysql-num-fields.md: mysql\_num\_fields »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_list\_tables
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_list\_tables

(PHP 4, PHP 5)

mysql\_list\_tables — Повертає список таблиць бази даних MySQL

**Увага**

Ця функція оголошена застарілою в PHP 4.3.0, і, разом з [модулем MySQL](book.mysql.md)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Так же смотрите раздел[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   SQL запит:`SHOW TABLES FROM dbname`

### Опис

```methodsynopsis
mysql_list_tables(string $database, resource $link_identifier = NULL): resource|false
```

Повертає список імен таблиць бази даних MySQL.

Ця функція застаріла. Замість неї рекомендується використовувати [mysql\_query()](function.mysql-query.md) із запитом `SHOW TABLES [FROM db_name] [LIKE 'pattern']`

### Список параметрів

`database`

Ім'я бази даних

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Дескриптор результату (resource) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

Используйте функцию[mysql\_tablename()](function.mysql-tablename.md) для роботи з результатом запиту або будь-яку іншу функцію, здатну це робити, наприклад, [mysql\_fetch\_array()](function.mysql-fetch-array.md)

### список змін

| Версия | Опис |
| --- | --- |
| 4.3.7 | Функція позначена застарілою. |

### Приклади

**Приклад #1 Приклад використання** mysql\_list\_tables()\*\*\*\*

```php
<?php
$dbname = 'mysql_dbname';

if (!mysql_connect('mysql_host', 'mysql_user', 'mysql_password')) {
    echo 'Ошибка подключения к mysql';
    exit;
}

$sql = "SHOW TABLES FROM $dbname";
$result = mysql_query($sql);

if (!$result) {
    echo "Ошибка базы, не удалось получить список таблиц\n";
    echo 'Ошибка MySQL: ' . mysql_error();
    exit;
}

while ($row = mysql_fetch_row($result)) {
    echo "Таблица: {$row[0]}\n";
}

mysql_free_result($result);
?>
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_listtables()**

### Дивіться також

-   [mysql\_list\_dbs()](function.mysql-list-dbs.md) \- Повертає список баз даних, доступних на сервері
-   [mysql\_tablename()](function.mysql-tablename.md) \- Повертає ім'я таблиці, що містить вказане поле
