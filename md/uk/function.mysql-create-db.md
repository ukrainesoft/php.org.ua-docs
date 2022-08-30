Створює базу даних MySQL

-   [« mysqlconnect](function.mysql-connect.html)
    
-   [mysqldataseek »](function.mysql-data-seek.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Створює базу даних MySQL
    

# mysqlcreateдб

(PHP 4, PHP 5)

mysqlcreatedb — Створює базу даних MySQL

**Увага**

Ця функція оголошена застарілою в PHP 4.3.0, і, разом з [модулем MySQL](book.mysql.html)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Також дивіться розділ [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqliquery()](mysqli.query.html)
-   [PDO::query()](pdo.query.html)

### Опис

```methodsynopsis
mysql_create_db(string $database_name, resource $link_identifier = NULL): bool
```

**mysqlcreatedb()** намагається створити базу даних на сервері, з яким асоційовано переданий дескриптор з'єднання.

### Список параметрів

`database_name`

Ім'я бази даних, що створюється.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад створення бази даних MySQL**

Функція **mysqlcreatedb()** не рекомендується використовувати. Переважно використовувати [mysqlquery()](function.mysql-query.html) із SQL-запитом створення бази даних `CREATE DATABASE`

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}

$sql = 'CREATE DATABASE my_db';
if (mysql_query($sql, $link)) {
    echo "База my_db успешно создана\n";
} else {
    echo 'Ошибка при создании базы данных: ' . mysql_error() . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
База my_db успешно создана
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlcreatedb()**

> **Зауваження**
> 
> Ця функція не буде доступна, якщо модуль MySQL був скомпільований клієнтською бібліотекою MySQL версії 4.x.

### Дивіться також

-   [mysqlquery()](function.mysql-query.html) - Надсилає запит MySQL
-   [mysqlselectdb()](function.mysql-select-db.html) - Вибирає базу даних MySQL