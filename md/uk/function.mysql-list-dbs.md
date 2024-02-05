---
navigation:
  - function.mysql-insert-id.md: « mysql\_insert\_id
  - function.mysql-list-fields.md: mysql\_list\_fields »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_list\_dbs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_list\_dbs

(PHP 4, PHP 5)

mysql\_list\_dbs — Повертає список баз даних, доступних на сервері

**Увага**

Ця функція оголошена застарілою в PHP 5.4.0, і, разом з [модулем MySQL](book.mysql.md)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Так же смотрите раздел[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   SQL запит:`SHOW DATABASES`

### Опис

```methodsynopsis
mysql_list_dbs(resource $link_identifier = NULL): resource
```

Повертає покажчик на результат, що містить список баз даних, доступних на вказаному сервері.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає resource результату у разі успішного виконання, або \*\*`false`\*\*в случае возникновения ошибки. Используйте функцию[mysql\_tablename()](function.mysql-tablename.md), щоб отримати дані з результату, або будь-яку іншу функцію, що працює з результатами запитів, наприклад [mysql\_fetch\_array()](function.mysql-fetch-array.md)

### Приклади

**Приклад #1 Приклад використання** mysql\_list\_dbs()\*\*\*\*

```php
<?php
// Без использования mysql_list_dbs()
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$res = mysql_query("SHOW DATABASES");

while ($row = mysql_fetch_assoc($res)) {
    echo $row['Database'] . "\n";
}

// Устарело, начиная с PHP 5.4.0
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$db_list = mysql_list_dbs($link);

while ($row = mysql_fetch_object($db_list)) {
     echo $row->Database . "\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
database1
database2
database3
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_listdbs()**

### Дивіться також

-   [mysql\_db\_name()](function.mysql-db-name.md) \- Повертає назву бази даних із виклику до mysql\_list\_dbs
-   [mysql\_select\_db()](function.mysql-select-db.md) \- Вибирає базу даних MySQL
