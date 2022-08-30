Обробляє ряд результату запиту та повертає об'єкт

-   [« mysqlfetchlengths](function.mysql-fetch-lengths.html)
    
-   [mysqlfetchrow »](function.mysql-fetch-row.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Обробляє ряд результату запиту та повертає об'єкт
    

# mysqlfetchobject

(PHP 4, PHP 5)

mysqlfetchobject — Обробляє ряд результатів запиту та повертає об'єкт.

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlifetchobject()](mysqli-result.fetch-object.html)
-   [PDOStatement::fetch(PDO::FETCHOBJ)](pdostatement.fetch.html)

### Опис

```methodsynopsis
mysql_fetch_object(resource $result, string $class_name = ?, array $params = ?): object
```

Повертає об'єкт із властивостями, що відповідають колонкам в обробленому ряду та зсуває внутрішній покажчик результату вперед.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.html)

`class_name`

Назва класу. Буде створено екземпляр зазначеного класу, заповнений властивостями та повернутий. Якщо не вказано, повертається екземпляр **stdClass**

`params`

Необов'язковий масив (array) параметрів, що передаються в конструктор створюваного екземпляра `class_name`

### Значення, що повертаються

Повертає об'єкт (object) з рядковими властивостями, що відповідають отриманому ряду, або \*\*`false`\*\*якщо рядів більше немає.

### Приклади

**Приклад #1 Приклад використання **mysqlfetchobject()****

```php
<?php
mysql_connect("hostname", "user", "password");
mysql_select_db("mydb");
$result = mysql_query("select * from mytable");
while ($row = mysql_fetch_object($result)) {
    echo $row->user_id;
    echo $row->fullname;
}
mysql_free_result($result);
?>
```

**Приклад #2 Приклад використання **mysqlfetchobject()****

```php
<?php
class foo {
    public $name;
}

mysql_connect("hostname", "user", "password");
mysql_select_db("mydb");

$result = mysql_query("select name from mytable limit 1");
$obj = mysql_fetch_object($result, 'foo');
var_dump($obj);
?>
```

### Примітки

> **Зауваження** **Продуктивність**
> 
> У плані швидкості ця функція аналогічна [mysqlfetcharray()](function.mysql-fetch-array.html) і майже також швидка, як [mysqlfetchrow()](function.mysql-fetch-row.html) (Різниця незначна).

> **Зауваження**
> 
> **mysqlfetchobject()** працює аналогічно [mysqlfetcharray()](function.mysql-fetch-array.html), з єдиною відмінністю - функція повертає об'єкт замість масиву. Це, крім усього іншого, означає, що ви зможете працювати з полями тільки на ім'я колонок, а не індексів (числа не можуть бути властивостями об'єкта).

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Дивіться також

-   [mysqlfetcharray()](function.mysql-fetch-array.html) - обробляє ряд результату запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysqlfetchassoc()](function.mysql-fetch-assoc.html) - Повертає ряд результату запиту як асоціативний масив.
-   [mysqlfetchrow()](function.mysql-fetch-row.html) - Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysqldataseek()](function.mysql-data-seek.html) - Переміщує внутрішній покажчик у результаті запиту
-   [mysqlquery()](function.mysql-query.html) - Надсилає запит MySQL