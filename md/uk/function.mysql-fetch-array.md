---
navigation:
  - function.mysql-escape-string.md: « mysql\_escape\_string
  - function.mysql-fetch-assoc.md: mysql\_fetch\_assoc »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_fetch\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_fetch\_array

(PHP 4, PHP 5)

mysql\_fetch\_array - Обробляє ряд результату запиту, повертаючи асоціативний масив, чисельний масив або обидва

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_fetch\_array()](mysqli-result.fetch-array.md)
-   [PDOStatement::fetch()](pdostatement.fetch.md)

### Опис

```methodsynopsis
mysql_fetch_array(resource $result, int $result_type = MYSQL_BOTH): array
```

Повертає масив, що відповідає обробленому ряду результату запиту та зсуває внутрішній покажчик даних уперед.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

`result_type`

Тип масива, що повертається. Є константою і може приймати такі значення: **`MYSQL_ASSOC`** **`MYSQL_NUM`**и**`MYSQL_BOTH`**

### Значення, що повертаються

Возвращает массив строк, соответствующих обработанному ряду результата запроса, или\*\*`false`**якщо рядів більше немає. Тип масиву, що повертається, залежить від значення параметра `result_type`При использовании**`MYSQL_BOTH`\*\* (за умовчанням), ви отримаєте масив, що складається як з асоціативних індексів, так і з чисельних . **`MYSQL_ASSOC`** поверне лише асоціативні індекси (аналогічно функції [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.md)), а\*\*`MYSQL_NUM`\*\* - лише чисельні (аналогічно функції [mysql\_fetch\_row()](function.mysql-fetch-row.md)

Якщо кілька колонок в результаті матимуть однакові назви, то буде повернуто останню колонку. Щоб отримати доступ до інших колонок з тим самим ім'ям, використовуйте чисельні індекси масиву або псевдоніми у запиті. У разі псевдонімів використовуйте саме їх – ви не зможете використати справжні імена колонок.

### Приклади

**Приклад #1 Запит із застосуванням псевдонімів для імен колонок, що дублюються.**

SELECT table1.field AS foo, table2.field AS bar FROM table1, table2

**Пример #2**mysql\_fetch\_array()**с**`MYSQL_NUM`\*\*\*\*

```php
<?php
mysql_connect("localhost", "mysql_user", "mysql_password") or
    die("Ошибка соединения: " . mysql_error());
mysql_select_db("mydb");

$result = mysql_query("SELECT id, name FROM mytable");

while ($row = mysql_fetch_array($result, MYSQL_NUM)) {
    printf("ID: %s  Имя: %s", $row[0], $row[1]);
}

mysql_free_result($result);
?>
```

**Пример #3**mysql\_fetch\_array()**с**`MYSQL_ASSOC`\*\*\*\*

```php
<?php
mysql_connect("localhost", "mysql_user", "mysql_password") or
    die("Ошибка соединения: " . mysql_error());
mysql_select_db("mydb");

$result = mysql_query("SELECT id, name FROM mytable");

while ($row = mysql_fetch_array($result, MYSQL_ASSOC)) {
    printf("ID: %s  Имя: %s", $row["id"], $row["name"]);
}

mysql_free_result($result);
?>
```

**Пример #4**mysql\_fetch\_array()**с**`MYSQL_BOTH`\*\*\*\*

```php
<?php
mysql_connect("localhost", "mysql_user", "mysql_password") or
    die("Ошибка соединения: " . mysql_error());
mysql_select_db("mydb");

$result = mysql_query("SELECT id, name FROM mytable");

while ($row = mysql_fetch_array($result, MYSQL_BOTH)) {
    printf ("ID: %s  Имя: %s", $row[0], $row["name"]);
}

mysql_free_result($result);
?>
```

### Примітки

> **Зауваження** **Продуктивність**
> 
> Важливо зауважити, що **mysql\_fetch\_array()** працює *незначно*медленнее, чем[mysql\_fetch\_row()](function.mysql-fetch-row.md), в той же час надаючи набагато більш зручний доступ до даних.

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

### Дивіться також

-   [mysql\_fetch\_row()](function.mysql-fetch-row.md) \- Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.md) \- Повертає ряд результату запиту як асоціативний масив.
-   [mysql\_data\_seek()](function.mysql-data-seek.md) \- Переміщує внутрішній покажчик у результаті запиту
-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
