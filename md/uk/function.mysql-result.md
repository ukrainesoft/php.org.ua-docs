Повертає дані результату запиту

-   [« mysql\_real\_escape\_string](function.mysql-real-escape-string.html)
    
-   [mysql\_select\_db »](function.mysql-select-db.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає дані результату запиту
    

# mysqlresult

(PHP 4, PHP 5)

mysqlresult — Повертає дані результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_data\_seek()](mysqli-result.data-seek.html) у зв'язку з [mysqli\_field\_seek()](mysqli-result.field-seek.html) і [mysqli\_fetch\_field()](mysqli-result.fetch-field.html)
-   [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.html)

### Опис

```methodsynopsis
mysql_result(resource $result, int $row, mixed $field = 0): string
```

Повертає вміст одного поля із набору результату MySQL.

Працюючи з великими результатами запитів, слід використовувати одну з функцій, що опрацьовують одразу цілий ряд результатів (наведено нижче). Так як ці функції повертають значення декількох осередків відразу, вони набагато швидше **mysqlresult()**. Крім того, врахуйте, що вказівка ​​чисельного зміщення працює набагато швидше, ніж вказівка ​​колонки або колонки з таблицею через точку.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.html)

`row`

Номер одержуваного ряду результату. Нумерація рядів починається з `0`

`field`

Ім'я або зміщення одержуваного поля.

Можливо як зміщенням поля, ім'ям поля, і ім'ям поля разом із таблицею (таблица.поле). Якщо для поля було вказано псевдонім ('select foo as bar from...'), використовуйте його замість імені поля. Якщо не вказано, повертається перше поле.

### Значення, що повертаються

Вміст одного поля з набору результату MySQL у разі успішного виконання, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlresult()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
if (!mysql_select_db('database_name')) {
    die('Ошибка выбора базы данных: ' . mysql_error());
}
$result = mysql_query('SELECT name FROM work.employee');
if (!$result) {
    die('Ошибка выполнения запроса:' . mysql_error());
}
echo mysql_result($result, 2); // выведет имя третьего сотрудника

mysql_close($link);
?>
```

### Примітки

> **Зауваження**
> 
> Виклики функції **mysqlresult()** не повинні змішуватись з іншими функціями, що працюють з результатом запиту.

### Дивіться також

-   [mysql\_fetch\_row()](function.mysql-fetch-row.html) - Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysql\_fetch\_array()](function.mysql-fetch-array.html) - обробляє ряд результату запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.html) - Повертає ряд результату запиту як асоціативний масив.
-   [mysql\_fetch\_object()](function.mysql-fetch-object.html) - обробляє ряд результату запиту та повертає об'єкт