Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва

-   [« mysqlescapestring](function.mysql-escape-string.html)
    
-   [mysqlfetchassoc »](function.mysql-fetch-assoc.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
    

# mysqlfetcharray

(PHP 4, PHP 5)

mysqlfetcharray - Обробляє ряд результату запиту, повертаючи асоціативний масив, чисельний масив або обидва

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlifetcharray()](mysqli-result.fetch-array.html)
-   [PDOStatement::fetch()](pdostatement.fetch.html)

### Опис

```methodsynopsis
mysql_fetch_array(resource $result, int $result_type = MYSQL_BOTH): array
```

Повертає масив, що відповідає обробленому ряду результату запиту та зсуває внутрішній покажчик даних уперед.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.html)

`result_type`

Тип масива, що повертається. Є константою і може приймати такі значення: **`MYSQL_ASSOC`** **`MYSQL_NUM`** і **`MYSQL_BOTH`**

### Значення, що повертаються

Повертає масив рядків, що відповідають обробленому ряду результату запиту, або \*\*`false`\*\*якщо рядів більше немає. Тип масиву, що повертається, залежить від значення параметра `result_type`. При використанні **`MYSQL_BOTH`** (за умовчанням), ви отримаєте масив, що складається як з асоціативних індексів, так і з чисельних . **`MYSQL_ASSOC`** поверне лише асоціативні індекси (аналогічно функції [mysqlfetchassoc()](function.mysql-fetch-assoc.html)), а **`MYSQL_NUM`** - лише чисельні (аналогічно функції [mysqlfetchrow()](function.mysql-fetch-row.html)

Якщо кілька колонок в результаті матимуть однакові назви, то буде повернуто останню колонку. Щоб отримати доступ до інших колонок з тим самим ім'ям, використовуйте чисельні індекси масиву або псевдоніми у запиті. У разі псевдонімів використовуйте саме їх – ви не зможете використати справжні імена колонок.

### Приклади

**Приклад #1 Запит із застосуванням псевдонімів для імен колонок, що дублюються.**

SELECT table1.field AS foo, table2.field AS bar FROM table1, table2

**Приклад #2 **mysqlfetcharray()** з **`MYSQL_NUM`****

```php
<?php
mysql_connect("localhost", "mysql_user", "mysql_password") or
    die("Ошибка соединения: " . mysql_error());
mysql_select_db("mydb");

$result = mysql_query("SELECT id, name FROM mytable");

while ($row = mysql_fetch_array($result, MYSQL_NUM)) {
    printf("ID: %s  Имя: %s", $row[0], $row[1]);
}

mysql_free_result($result);
?>
```

**Приклад #3 **mysqlfetcharray()** з **`MYSQL_ASSOC`****

```php
<?php
mysql_connect("localhost", "mysql_user", "mysql_password") or
    die("Ошибка соединения: " . mysql_error());
mysql_select_db("mydb");

$result = mysql_query("SELECT id, name FROM mytable");

while ($row = mysql_fetch_array($result, MYSQL_ASSOC)) {
    printf("ID: %s  Имя: %s", $row["id"], $row["name"]);
}

mysql_free_result($result);
?>
```

**Приклад #4 **mysqlfetcharray()** з **`MYSQL_BOTH`****

```php
<?php
mysql_connect("localhost", "mysql_user", "mysql_password") or
    die("Ошибка соединения: " . mysql_error());
mysql_select_db("mydb");

$result = mysql_query("SELECT id, name FROM mytable");

while ($row = mysql_fetch_array($result, MYSQL_BOTH)) {
    printf ("ID: %s  Имя: %s", $row[0], $row["name"]);
}

mysql_free_result($result);
?>
```

### Примітки

> **Зауваження** **Продуктивність**
> 
> Важливо зауважити, що **mysqlfetcharray()** працює *незначно* повільніше, ніж [mysqlfetchrow()](function.mysql-fetch-row.html), в той же час надаючи набагато більш зручний доступ до даних.

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Дивіться також

-   [mysqlfetchrow()](function.mysql-fetch-row.html) - Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysqlfetchassoc()](function.mysql-fetch-assoc.html) - Повертає ряд результату запиту як асоціативний масив.
-   [mysqldataseek()](function.mysql-data-seek.html) - Переміщує внутрішній покажчик у результаті запиту
-   [mysqlquery()](function.mysql-query.html) - Надсилає запит MySQL