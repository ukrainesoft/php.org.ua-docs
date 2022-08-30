Перемикається на вказану базу даних та надсилає запит

-   [« mysqlдбname](function.mysql-db-name.html)
    
-   [mysqldropdb »](function.mysql-drop-db.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Перемикається на вказану базу даних та надсилає запит
    

# mysqlдбquery

(PHP 4, PHP 5)

mysqlдбquery — Переключається на вказану базу даних та надсилає запит

**Увага**

Ця функція оголошена застарілою в PHP 5.3.0, і, разом з [модулем MySQL](book.mysql.html)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Також дивіться розділ [MySQL: вибір API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqliselectdb()](mysqli.select-db.html) then the query
-   [PDO::construct()](pdo.construct.html)

### Опис

```methodsynopsis
mysql_db_query(string $database, string $query, resource $link_identifier = NULL): resource|bool
```

**mysqlдбquery()** вибирає базу даних та виконує запит до неї.

### Список параметрів

`database`

Ім'я бази даних, яку відбудеться переключення.

`query`

Запит MySQL.

Дані у запиті мають бути [коректно проекрановано](function.mysql-real-escape-string.html)

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає ресурс результату запиту до MySQL або **`false`** у разі виникнення помилки. Функція також повертає **`true`\*\*\*\*`false`** для `INSERT``UPDATE``DELETE` запитів для індикації успіху/провалу.

### Приклади

**Приклад #1 Приклад використання альтернативи **mysqlдбquery()****

```php
<?php

if (!$link = mysql_connect('mysql_host', 'mysql_user', 'mysql_password')) {
    echo 'Не удалось подключиться к mysql';
    exit;
}

if (!mysql_select_db('mysql_dbname', $link)) {
    echo 'Не удалось выбрать базу данных';
    exit;
}

$sql    = 'SELECT foo FROM bar WHERE id = 42';
$result = mysql_query($sql, $link);

if (!$result) {
    echo "Ошибка DB, запрос не удался\n";
    echo 'MySQL Error: ' . mysql_error();
    exit;
}

while ($row = mysql_fetch_assoc($result)) {
    echo $row['foo'];
}

mysql_free_result($result);

?>
```

### Примітки

> **Зауваження**
> 
> Врахуйте, що ця функція *НЕ* перемикає з'єднання назад до попередньої бази даних. Іншими словами, ви не можете використовувати цю функцію, щоб *тимчасово* перейти на іншу базу даних і виконати запит. Перейти назад вам доведеться вручну. Вкрай рекомендується використовувати синтаксис `database.table` у SQL-запитах чи функцію [mysqlselectdb()](function.mysql-select-db.html)замість використання цієї функції.

### Дивіться також

-   [mysqlquery()](function.mysql-query.html) - Надсилає запит MySQL
-   [mysqlselectdb()](function.mysql-select-db.html) - Вибирає базу даних MySQL