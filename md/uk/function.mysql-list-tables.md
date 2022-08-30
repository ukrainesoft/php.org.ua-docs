Повертає список таблиць бази даних MySQL

-   [« mysqllistprocesses](function.mysql-list-processes.html)
    
-   [mysqlnumfields »](function.mysql-num-fields.html)
    
-   [PHP Manual](index.md)
    
-   [MySQL](ref.mysql.md)
    
-   Повертає список таблиць бази даних MySQL
    

# mysqllisttables

(PHP 4, PHP 5)

mysqllisttables — Повертає список таблиць бази даних MySQL

**Увага**

Ця функція оголошена застарілою в PHP 4.3.0, і, разом з [модулем MySQL](book.mysql.md)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.html). Також дивіться розділ [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   SQL запит: `SHOW TABLES FROM dbname`

### Опис

```methodsynopsis
mysql_list_tables(string $database, resource $link_identifier = NULL): resource|false
```

Повертає список імен таблиць бази даних MySQL.

Ця функція застаріла. Замість неї рекомендується використовувати [mysqlquery()](function.mysql-query.html) із запитом `SHOW TABLES [FROM db_name] [LIKE 'pattern']`

### Список параметрів

`database`

Ім'я бази даних

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Дескриптор результату (resource) у разі успішного виконання або **`false`** у разі виникнення помилки.

Використовуйте функцію [mysqltablename()](function.mysql-tablename.html) для роботи з результатом запиту або будь-яку іншу функцію, здатну це робити, наприклад, [mysqlfetcharray()](function.mysql-fetch-array.html)

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

-   [mysqllistdbs()](function.mysql-list-dbs.html) - Повертає список баз даних, доступних на сервері
-   [mysqltablename()](function.mysql-tablename.html) - Повертає ім'я таблиці, що містить вказане поле