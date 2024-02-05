---
navigation:
  - function.mysql-fetch-array.md: « mysql\_fetch\_array
  - function.mysql-fetch-field.md: mysql\_fetch\_field »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_fetch\_assoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_fetch\_assoc

(PHP 4 >= 4.0.3, PHP 5)

mysql\_fetch\_assoc — Повертає ряд результату запиту як асоціативний масив.

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_fetch\_assoc()](mysqli-result.fetch-assoc.md)
-   [PDOStatement::fetch()](pdostatement.fetch.md)с параметром`mode`заданим як\*\*`PDO::FETCH_ASSOC`\*\*

### Опис

```methodsynopsis
mysql_fetch_assoc(resource $result): array
```

Повертає асоціативний масив, що відповідає отриманому ряду і зсуває вперед внутрішній покажчик результату. Функція **mysql\_fetch\_assoc()** аналогічна виклику функції [mysql\_fetch\_array()](function.mysql-fetch-array.md) з другим необов'язковим параметром, що дорівнює MYSQL\_ASSOC. Функція повертає лише асоціативний масив.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

### Значення, що повертаються

Повертає асоціативний масив рядків, що відповідає отриманому ряду, або **`false`** якщо лав більше немає.

Якщо два або більше стовпців результату мають однакові імена, пріоритет матиме останній стовпець. Для доступу до іншого однойменного стовпця (або стовпців), вам необхідно або звернутися до результату запиту за числовим індексом за допомогою [mysql\_fetch\_row()](function.mysql-fetch-row.md) або додати псевдоніми до потрібних стовпців. Для більш детальної інформації про псевдоніми дивіться опис прикладу [mysql\_fetch\_array()](function.mysql-fetch-array.md)

### Приклади

**Приклад #1 Розширений приклад використання **mysql\_fetch\_assoc()****

```php
<?php

$conn = mysql_connect("localhost", "mysql_user", "mysql_password");

if (!$conn) {
    echo "Unable to connect to DB: " . mysql_error();
    exit;
}

if (!mysql_select_db("mydbname")) {
    echo "Unable to select mydbname: " . mysql_error();
    exit;
}

$sql = "SELECT id as userid, fullname, userstatus
        FROM   sometable
        WHERE  userstatus = 1";

$result = mysql_query($sql);

if (!$result) {
    echo "Could not successfully run query ($sql) from DB: " . mysql_error();
    exit;
}

if (mysql_num_rows($result) == 0) {
    echo "No rows found, nothing to print so am exiting";
    exit;
}

// До тех пор, пока в результате содержатся ряды, помещаем их в ассоциативный массив.
// Замечание: если запрос возвращает только один ряд - нет нужды в цикле.
// Замечание: если вы добавите extract($row); в начало цикла, вы сделаете
//            доступными переменные $userid, $fullname и $userstatus
while ($row = mysql_fetch_assoc($result)) {
    echo $row["userid"];
    echo $row["fullname"];
    echo $row["userstatus"];
}

mysql_free_result($result);

?>
```

### Примітки

> **Зауваження** **Продуктивність**
> 
> Важливо, що \*\*mysql\_fetch\_assoc()\**лишь*незначно\*медленнее, чем[mysql\_fetch\_row()](function.mysql-fetch-row.md), але водночас надає важливу додаткову інформацію.

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

### Дивіться також

-   [mysql\_fetch\_row()](function.mysql-fetch-row.md) \- Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysql\_fetch\_array()](function.mysql-fetch-array.md) \- Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysql\_data\_seek()](function.mysql-data-seek.md) \- Переміщує внутрішній покажчик у результаті запиту
-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
-   [mysql\_error()](function.mysql-error.md) \- Повертає текст помилки останньої операції з MySQL
