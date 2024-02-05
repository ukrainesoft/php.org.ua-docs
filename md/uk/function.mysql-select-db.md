---
navigation:
  - function.mysql-result.md: « mysql\_result
  - function.mysql-set-charset.md: mysql\_set\_charset »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_select\_db
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_select\_db

(PHP 4, PHP 5)

mysql\_select\_db - Вибирає базу даних MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_select\_db()](mysqli.select-db.md)
-   [PDO::\_\_construct()](pdo.construct.md)(розділ про dsn)

### Опис

```methodsynopsis
mysql_select_db(string $database_name, resource $link_identifier = NULL): bool
```

Вибирає для роботи вказану базу даних на сервері, на який посилається переданий дескриптор з'єднання. Кожен наступний виклик функції [mysql\_query()](function.mysql-query.md) буде працювати з обраною базою даних.

### Список параметрів

`database_name`

Ім'я бази даних, що вибирається.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysql\_select\_db()\*\*\*\*

```php
<?php

$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Не удалось соединиться : ' . mysql_error());
}

// выбираем foo в качестве текущей базы данных
$db_selected = mysql_select_db('foo', $link);
if (!$db_selected) {
    die ('Не удалось выбрать базу foo: ' . mysql_error());
}
?>
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_selectdb()**

### Дивіться також

-   [mysql\_connect()](function.mysql-connect.md) \- Відкриває з'єднання із сервером MySQL
-   [mysql\_pconnect()](function.mysql-pconnect.md) \- Встановлює постійне з'єднання із сервером MySQL
-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
