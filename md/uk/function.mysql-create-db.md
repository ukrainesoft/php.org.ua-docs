---
navigation:
  - function.mysql-connect.md: « mysql\_connect
  - function.mysql-data-seek.md: mysql\_data\_seek »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_create\_db
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_create\_db

(PHP 4, PHP 5)

mysql\_create\_db — Створює базу даних MySQL

**Увага**

Ця функція оголошена застарілою в PHP 4.3.0, і, разом з [модулем MySQL](book.mysql.md)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Так же смотрите раздел[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_query()](mysqli.query.md)
-   [PDO::query()](pdo.query.md)

### Опис

```methodsynopsis
mysql_create_db(string $database_name, resource $link_identifier = NULL): bool
```

**mysql\_create\_db()** намагається створити базу даних на сервері, з яким асоційовано переданий дескриптор з'єднання.

### Список параметрів

`database_name`

Ім'я бази даних, що створюється.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад створення бази даних MySQL**

Функция**mysql\_create\_db()** не рекомендується використовувати. Переважно використовувати [mysql\_query()](function.mysql-query.md) із SQL-запитом створення бази даних `CREATE DATABASE`

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}

$sql = 'CREATE DATABASE my_db';
if (mysql_query($sql, $link)) {
    echo "База my_db успешно создана\n";
} else {
    echo 'Ошибка при создании базы данных: ' . mysql_error() . "\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
База my_db успешно создана
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_createdb()**

> **Зауваження** :
> 
> Ця функція не буде доступна, якщо модуль MySQL був скомпільований клієнтською бібліотекою MySQL версії 4.x.

### Дивіться також

-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
-   [mysql\_select\_db()](function.mysql-select-db.md) \- Вибирає базу даних MySQL
