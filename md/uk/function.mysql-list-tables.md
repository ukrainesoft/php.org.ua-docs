Повертає список таблиць бази даних MySQL

-   [« mysql\_list\_processes](function.mysql-list-processes.html)
    
-   [mysql\_num\_fields »](function.mysql-num-fields.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає список таблиць бази даних MySQL
    

# mysqllisttables

(PHP 4, PHP 5)

mysqllisttables — Повертає список таблиць бази даних MySQL

**Увага**

Ця функція оголошена застарілою в PHP 4.3.0, і, разом з [модулем MySQL](book.mysql.html)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Також дивіться розділ [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   SQL запит: `SHOW TABLES FROM dbname`

### Опис

```methodsynopsis
mysql_list_tables(string $database, resource $link_identifier = NULL): resource|false
```

Повертає список імен таблиць бази даних MySQL.

Ця функція застаріла. Замість неї рекомендується використовувати [mysql\_query()](function.mysql-query.html) із запитом `SHOW TABLES [FROM db_name] [LIKE 'pattern']`

### Список параметрів

`database`

Ім'я бази даних

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Дескриптор результату (resource) у разі успішного виконання або **`false`** у разі виникнення помилки.

Використовуйте функцію [mysql\_tablename()](function.mysql-tablename.html) для роботи з результатом запиту або будь-яку іншу функцію, здатну це робити, наприклад, [mysql\_fetch\_array()](function.mysql-fetch-array.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція позначена застарілою. |

### Приклади

**Приклад #1 Приклад використання **mysqllisttables()****

```php
<?php
$dbname = 'mysql_dbname';

if (!mysql_connect('mysql_host', 'mysql_user', 'mysql_password')) {
    echo 'Ошибка подключения к mysql';
    exit;
}

$sql = "SHOW TABLES FROM $dbname";
$result = mysql_query($sql);

if (!$result) {
    echo "Ошибка базы, не удалось получить список таблиц\n";
    echo 'Ошибка MySQL: ' . mysql_error();
    exit;
}

while ($row = mysql_fetch_row($result)) {
    echo "Таблица: {$row[0]}\n";
}

mysql_free_result($result);
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqllisttables()**

### Дивіться також

-   [mysql\_list\_dbs()](function.mysql-list-dbs.html) - Повертає список баз даних, доступних на сервері
-   [mysql\_tablename()](function.mysql-tablename.html) - Повертає ім'я таблиці, що містить вказане поле