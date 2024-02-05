---
navigation:
  - function.mysql-real-escape-string.md: « mysql\_real\_escape\_string
  - function.mysql-select-db.md: mysql\_select\_db »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_result

(PHP 4, PHP 5)

mysql\_result — Повертає дані результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_data\_seek()](mysqli-result.data-seek.md)у зв'язку з[mysqli\_field\_seek()](mysqli-result.field-seek.md) і [mysqli\_fetch\_field()](mysqli-result.fetch-field.md)
-   [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.md)

### Опис

```methodsynopsis
mysql_result(resource $result, int $row, mixed $field = 0): string
```

Повертає вміст одного поля із набору результату MySQL.

Працюючи з великими результатами запитів, слід використовувати одну з функцій, що опрацьовують одразу цілий ряд результатів (наведені нижче). Так як ці функції повертають значення декількох осередків відразу, вони набагато швидше **mysql\_result()**. Крім того, врахуйте, що вказівка ​​чисельного зміщення працює набагато швидше, ніж вказівка ​​колонки або колонки з таблицею через точку.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

`row`

Номер получаемого ряда из результата. Нумерация рядов начинается с

`field`

Ім'я або зміщення одержуваного поля.

Можливо як зміщенням поля, ім'ям поля, і ім'ям поля разом із таблицею (таблица.поле). Якщо для поля було вказано псевдонім ('select foo as bar from...'), використовуйте його замість імені поля. Якщо не вказано, перше поле повертається.

### Значення, що повертаються

Вміст одного поля з набору результату MySQL у разі успішного виконання, або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**mysql\_result()\*\*\*\*

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
if (!mysql_select_db('database_name')) {
    die('Ошибка выбора базы данных: ' . mysql_error());
}
$result = mysql_query('SELECT name FROM work.employee');
if (!$result) {
    die('Ошибка выполнения запроса:' . mysql_error());
}
echo mysql_result($result, 2); // выведет имя третьего сотрудника

mysql_close($link);
?>
```

### Примітки

> **Зауваження** :
> 
> Виклики функції **mysql\_result()** не повинні змішуватись з іншими функціями, що працюють з результатом запиту.

### Дивіться також

-   [mysql\_fetch\_row()](function.mysql-fetch-row.md) \- Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysql\_fetch\_array()](function.mysql-fetch-array.md) \- Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.md) \- Повертає ряд результату запиту як асоціативний масив.
-   [mysql\_fetch\_object()](function.mysql-fetch-object.md) \- обробляє ряд результату запиту та повертає об'єкт
