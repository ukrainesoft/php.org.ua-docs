---
navigation:
  - function.mysql-info.md: « mysql\_info
  - function.mysql-list-dbs.md: mysql\_list\_dbs »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_insert\_id
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_insert\_id

(PHP 4, PHP 5)

mysql\_insert\_id - Повертає ідентифікатор, згенерований при останньому INSERT-запиті

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_insert\_id()](mysqli.insert-id.md)
-   [PDO::lastInsertId()](pdo.lastinsertid.md)

### Опис

```methodsynopsis
mysql_insert_id(resource $link_identifier = NULL): int
```

Повертає ідентифікатор, згенерований колонкою з AUTO\_INCREMENT - останнім запитом (зазвичай INSERT).

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Ідентифікатор, згенерований колонкою з AUTO\_INCREMENT останнім запитом у разі успішного виконання, якщо останній запит не генерує значення AUTO\_INCREMENT value, и\*\*`false`\*\*якщо з'єднання MySQL не було встановлено.

### Приклади

**Приклад #1 Приклад використання** mysql\_insert\_id()\*\*\*\*

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
mysql_select_db('mydb');

mysql_query("INSERT INTO mytable (product) values ('kossu')");
printf("Идентификатор последней вставленной записи %d\n", mysql_insert_id());
?>
```

### Примітки

**Застереження**

**mysql\_insert\_id()** конвертує повертається функцією MySQL C API тип значення функції `mysql_insert_id()` у тип `long` (званий int у PHP). Якщо ваша колонка AUTO\_INCREMENT має тип BIGINT (64 біта), то значення, яке повертається функцією в результаті перетворення може бути спотворене. Використовуйте замість цієї функції внутрішню MySQL-функцію LAST\_INSERT\_ID() у SQL-запиті. Детальніше про максимальні значення цілих чисел дивіться в [розділ документації, присвячений цілим числам](language.types.integer.md)

> **Зауваження** :
> 
> Так как**mysql\_insert\_id()** працює з останнім виконаним запитом, викликайте \*\*mysql\_insert\_id()\*\*сразу же после запроса, генерирующего новое значение.

> **Зауваження** :
> 
> Значение в SQL функции MySQL`LAST_INSERT_ID()` завжди містить останній згенерований ID і не обнулюється між запитами.

### Дивіться також

-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
-   [mysql\_info()](function.mysql-info.md) \- Повертає інформацію про останній запит
