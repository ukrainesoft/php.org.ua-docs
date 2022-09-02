---
navigation:
  - function.mysql-result.md: « mysqlresult
  - function.mysql-set-charset.md: mysqlsetcharset »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlselectдб
---
# mysqlselectдб

(PHP 4, PHP 5)

mysqlselectdb - Вибирає базу даних MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqliselectdb()](mysqli.select-db.md)
-   [PDO::construct()](pdo.construct.md) (розділ про dsn)

### Опис

```methodsynopsis
mysql_select_db(string $database_name, resource $link_identifier = NULL): bool
```

Вибирає для роботи вказану базу даних на сервері, на який посилається переданий дескриптор з'єднання. Кожен наступний виклик функції [mysqlquery()](function.mysql-query.md) буде працювати з обраною базою даних.

### Список параметрів

`database_name`

Ім'я бази даних, що вибирається.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlselectdb()****

```php
<?php

$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Не удалось соединиться : ' . mysql_error());
}

// выбираем foo в качестве текущей базы данных
$db_selected = mysql_select_db('foo', $link);
if (!$db_selected) {
    die ('Не удалось выбрать базу foo: ' . mysql_error());
}
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlselectdb()**

### Дивіться також

-   [mysqlconnect()](function.mysql-connect.md) - Відкриває з'єднання із сервером MySQL
-   [mysqlpconnect()](function.mysql-pconnect.md) - Встановлює постійне з'єднання із сервером MySQL
-   [mysqlquery()](function.mysql-query.md) - Надсилає запит MySQL
