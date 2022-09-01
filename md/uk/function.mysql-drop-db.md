---
navigation:
  - function.mysql-db-query.html: « mysqlдбquery
  - function.mysql-errno.html: mysqlerrno »
  - index.html: PHP Manual
  - ref.mysql.html: MySQL
title: mysqldropдб
---
# mysqldropдб

(PHP 4, PHP 5)

mysqldropdb — Знищує базу даних MySQL

**Увага**

Ця функція оголошена застарілою в PHP 4.3.0, і, разом з [модулем MySQL](book.mysql.html)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Також дивіться розділ [MySQL: вибір API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   Виконати запит `DROP DATABASE`

### Опис

```methodsynopsis
mysql_drop_db(string $database_name, resource $link_identifier = NULL): bool
```

**mysqldropdb()** намагається знищити базу даних на сервері, на який посилається переданий дескриптор з'єднання. Ця функція застаріла, використовуйте замість неї [mysqlquery()](function.mysql-query.html) із запитом `DROP DATABASE`

### Список параметрів

`database_name`

Ім'я бази даних, що видаляється.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Альтернативний приклад використання **mysqldropdb()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Не удалось подключиться к базе данных: ' . mysql_error());
}

$sql = 'DROP DATABASE my_db';
if (mysql_query($sql, $link)) {
    echo "База данных my_db была успешно удалена\n";
} else {
    echo 'Ошибка при удалении базы данных: ' . mysql_error() . "\n";
}
?>
```

### Примітки

**Увага**

Ця функція недоступна, якщо модуль був скомпілюваний із клієнтською бібліотекою MySQL версії 4.x.

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqldropdb()**

### Дивіться також

-   [mysqlquery()](function.mysql-query.html) - Надсилає запит MySQL
