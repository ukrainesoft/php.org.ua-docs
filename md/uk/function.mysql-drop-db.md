---
navigation:
  - function.mysql-db-query.md: « mysql\_db\_query
  - function.mysql-errno.md: mysql\_errno »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_drop\_db
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_drop\_db

(PHP 4, PHP 5)

mysql\_drop\_db — Знищує базу даних MySQL

**Увага**

Ця функція оголошена застарілою в PHP 4.3.0, і, разом з [модулем MySQL](book.mysql.md)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Так же смотрите раздел[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   Виконати запит`DROP DATABASE`

### Опис

```methodsynopsis
mysql_drop_db(string $database_name, resource $link_identifier = NULL): bool
```

**mysql\_drop\_db()** намагається знищити базу даних на сервері, на який посилається переданий дескриптор з'єднання. Ця функція застаріла, використовуйте замість неї [mysql\_query()](function.mysql-query.md) із запитом `DROP DATABASE`

### Список параметрів

`database_name`

Ім'я бази даних, що видаляється.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Альтернативний приклад використання **mysql\_drop\_db()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Не удалось подключиться к базе данных: ' . mysql_error());
}

$sql = 'DROP DATABASE my_db';
if (mysql_query($sql, $link)) {
    echo "База данных my_db была успешно удалена\n";
} else {
    echo 'Ошибка при удалении базы данных: ' . mysql_error() . "\n";
}
?>
```

### Примітки

**Увага**

Ця функція недоступна, якщо модуль був скомпілюваний із клієнтською бібліотекою MySQL версії 4.x.

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_dropdb()**

### Дивіться також

-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
