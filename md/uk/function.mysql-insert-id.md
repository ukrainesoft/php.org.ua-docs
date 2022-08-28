Повертає ідентифікатор, згенерований при останньому INSERT-запиті

-   [« mysql\_info](function.mysql-info.html)
    
-   [mysql\_list\_dbs »](function.mysql-list-dbs.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає ідентифікатор, згенерований при останньому INSERT-запиті
    

# mysqlinsertід

(PHP 4, PHP 5)

mysqlinsertid - Повертає ідентифікатор, згенерований при останньому INSERT-запиті

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_insert\_id()](mysqli.insert-id.html)
-   [PDO::lastInsertId()](pdo.lastinsertid.html)

### Опис

```methodsynopsis
mysql_insert_id(resource $link_identifier = NULL): int
```

Повертає ідентифікатор, згенерований колонкою з AUTOINCREMENT - останнім запитом (зазвичай INSERT).

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Ідентифікатор, згенерований колонкою з AUTOINCREMENT останнім запитом у разі успішного виконання, `0`якщо останній запит не генерує значення AUTOINCREMENT value, та **`false`**, якщо з'єднання MySQL не було встановлено.

### Приклади

**Приклад #1 Приклад використання **mysqlinsertid()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
mysql_select_db('mydb');

mysql_query("INSERT INTO mytable (product) values ('kossu')");
printf("Идентификатор последней вставленной записи %d\n", mysql_insert_id());
?>
```

### Примітки

**Застереження**

**mysqlinsertid()** конвертує повертається функцією MySQL C API тип значення функції `mysql_insert_id()` у тип `long` (званий int у PHP). Якщо ваша колонка AUTOINCREMENT має тип BIGINT (64 біта), то значення, яке повертається функцією в результаті перетворення може бути спотворене. Використовуйте замість цієї функції внутрішню MySQL-функцію LASTINSERTID() у SQL-запиті. Детальніше про максимальні значення цілих чисел дивіться в [разделе документации, посвящённом целым числам](language.types.integer.html)

> **Зауваження**
> 
> Так як **mysqlinsertid()** працює з останнім виконаним запитом, викликайте **mysqlinsertid()** відразу після запиту, що генерує нове значення.

> **Зауваження**
> 
> Значення у SQL функції MySQL `LAST_INSERT_ID()` завжди містить останній згенерований ID і не обнулюється між запитами.

### Дивіться також

-   [mysql\_query()](function.mysql-query.html) - Надсилає запит MySQL
-   [mysql\_info()](function.mysql-info.html) - Повертає інформацію про останній запит