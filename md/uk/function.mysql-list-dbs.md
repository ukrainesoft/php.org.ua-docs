Повертає список баз даних, доступних на сервері

-   [« mysql\_insert\_id](function.mysql-insert-id.html)
    
-   [mysql\_list\_fields »](function.mysql-list-fields.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає список баз даних, доступних на сервері
    

# mysqllistdbs

(PHP 4, PHP 5)

mysqllistdbs — Повертає список баз даних, доступних на сервері

**Увага**

Ця функція оголошена застарілою в PHP 5.4.0, і, разом з [модулем MySQL](book.mysql.html)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Також дивіться розділ [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   SQL запит: `SHOW DATABASES`

### Опис

```methodsynopsis
mysql_list_dbs(resource $link_identifier = NULL): resource
```

Повертає покажчик на результат, що містить список баз даних, доступних на вказаному сервері.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає resource результату у разі успішного виконання, або **`false`** у разі виникнення помилки. Використовуйте функцію [mysql\_tablename()](function.mysql-tablename.html), щоб отримати дані з результату, або будь-яку іншу функцію, що працює з результатами запитів, наприклад [mysql\_fetch\_array()](function.mysql-fetch-array.html)

### Приклади

**Приклад #1 Приклад використання **mysqllistdbs()****

```php
<?php
// Без использования mysql_list_dbs()
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$res = mysql_query("SHOW DATABASES");

while ($row = mysql_fetch_assoc($res)) {
    echo $row['Database'] . "\n";
}

// Устарело, начиная с PHP 5.4.0
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$db_list = mysql_list_dbs($link);

while ($row = mysql_fetch_object($db_list)) {
     echo $row->Database . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
database1
database2
database3
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqllistdbs()**

### Дивіться також

-   [mysql\_db\_name()](function.mysql-db-name.html) - Повертає назву бази даних із виклику до mysqllistdbs
-   [mysql\_select\_db()](function.mysql-select-db.html) - Вибирає базу даних MySQL