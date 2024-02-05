---
navigation:
  - function.mysql-db-name.md: « mysql\_db\_name
  - function.mysql-drop-db.md: mysql\_drop\_db »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_db\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_db\_query

(PHP 4, PHP 5)

mysql\_db\_query — Переключається на вказану базу даних та надсилає запит

**Увага**

Ця функція оголошена застарілою в PHP 5.3.0, і, разом з [модулем MySQL](book.mysql.md)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Так же смотрите раздел[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_select\_db()](mysqli.select-db.md)then the query
-   [PDO::\_\_construct()](pdo.construct.md)

### Опис

```methodsynopsis
mysql_db_query(string $database, string $query, resource $link_identifier = NULL): resource|bool
```

**mysql\_db\_query()** вибирає базу даних та виконує запит до неї.

### Список параметрів

`database`

Ім'я бази даних, яку відбудеться переключення.

`query`

Запит MySQL.

Дані у запиті мають бути [коректно проекрановано](function.mysql-real-escape-string.md)

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Возвращает ресурс результата запроса к MySQL или\*\*`false`\*\* у разі виникнення помилки. Функція також повертає **`true`** \*\*`false`\*\*для`INSERT` `UPDATE` `DELETE` запитів для індикації успіху/провалу.

### Приклади

**Приклад #1 Приклад використання альтернативи **mysql\_db\_query()****

```php
<?php

if (!$link = mysql_connect('mysql_host', 'mysql_user', 'mysql_password')) {
    echo 'Не удалось подключиться к mysql';
    exit;
}

if (!mysql_select_db('mysql_dbname', $link)) {
    echo 'Не удалось выбрать базу данных';
    exit;
}

$sql    = 'SELECT foo FROM bar WHERE id = 42';
$result = mysql_query($sql, $link);

if (!$result) {
    echo "Ошибка DB, запрос не удался\n";
    echo 'MySQL Error: ' . mysql_error();
    exit;
}

while ($row = mysql_fetch_assoc($result)) {
    echo $row['foo'];
}

mysql_free_result($result);

?>
```

### Примітки

> **Зауваження** :
> 
> Врахуйте, що ця функція **НЕ** перемикає з'єднання назад до попередньої бази даних. Іншими словами, ви не можете використовувати цю функцію, щоб *тимчасово* перейти на іншу базу даних і виконати запит. Перейти назад вам доведеться вручну. Вкрай рекомендується використовувати синтаксис `database.table` у SQL-запитах чи функцію [mysql\_select\_db()](function.mysql-select-db.md)замість використання цієї функції.

### Дивіться також

-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
-   [mysql\_select\_db()](function.mysql-select-db.md) \- Вибирає базу даних MySQL
