Повертає текст помилки останньої операції з MySQL

-   [« mysqlerrno](function.mysql-errno.html)
    
-   [mysqlescapestring »](function.mysql-escape-string.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає текст помилки останньої операції з MySQL
    

# mysqlerror

(PHP 4, PHP 5)

mysqlerror — Повертає текст помилки останньої операції з MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlierror()](mysqli.error.html)
-   [PDO::errorInfo()](pdo.errorinfo.html)

### Опис

```methodsynopsis
mysql_error(resource $link_identifier = NULL): string
```

Повертає текст помилки виконання останньої функції MySQL. Помилки роботи з MySQL більше не викликають повідомлень у PHP. Натомість використовуйте функцію **mysqlerror()**, щоб отримати повідомлення про помилку. Врахуйте, що функція повертає текст помилки лише останньої виконаної функції MySQL (за винятком **mysqlerror()** і [mysqlerrno()](function.mysql-errno.html)), тому переконайтеся, що ви викликаєте цю функцію до виклику наступної функції MySQL.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає текст помилки виконання останньої функції MySQL, або `''` (порожній рядок), якщо операцію виконано успішно.

### Приклади

**Приклад #1 Приклад використання **mysqlerror()****

```php
<?php
$link = mysql_connect("localhost", "mysql_user", "mysql_password");

mysql_select_db("nonexistentdb", $link);
echo mysql_errno($link) . ": " . mysql_error($link). "\n";

mysql_select_db("kossu", $link);
mysql_query("SELECT * FROM nonexistenttable", $link);
echo mysql_errno($link) . ": " . mysql_error($link) . "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
1049: Unknown database 'nonexistentdb'
1146: Table 'kossu.nonexistenttable' doesn't exist
```

### Дивіться також

-   [mysqlerrno()](function.mysql-errno.html) - Повертає чисельний код помилки виконання останньої операції з MySQL
-   [» Коды ошибок MySQL](http://dev.mysql.com/doc/mysql/en/error-handling.html)