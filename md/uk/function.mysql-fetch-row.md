Обробляє ряд результату запиту та повертає масив із числовими індексами

-   [« mysql\_fetch\_object](function.mysql-fetch-object.html)
    
-   [mysql\_field\_flags »](function.mysql-field-flags.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Обробляє ряд результату запиту та повертає масив із числовими індексами
    

# mysqlfetchrow

(PHP 4, PHP 5)

mysqlfetchrow — Обробляє ряд результату запиту та повертає масив із числовими індексами

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_fetch\_row()](mysqli-result.fetch-row.html)
-   [PDOStatement::fetch(PDO::FETCH\_NUM)](pdostatement.fetch.html)

### Опис

```methodsynopsis
mysql_fetch_row(resource $result): array
```

Повертає масив з числовими індексами, що містить дані обробленого ряду, і зсуває внутрішній покажчик результату вперед.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.html)

### Значення, що повертаються

Повертає масив рядків з числовими індексами, що містить дані обробленого ряду, або **`false`**якщо рядів не залишилося.

**mysqlfetchrow()** обробляє один ряд результату, який посилається переданий покажчик. Ряд повертається як масиву. Кожна колонка розташовується в наступному осередку масиву, починаючи з нульового індексу

### Приклади

**Приклад #1 Отримання одного ряду за допомогою **mysqlfetchrow()****

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Ошибка запроса: ' . mysql_error();
    exit;
}
$row = mysql_fetch_row($result);

echo $row[0]; // 42
echo $row[1]; // email
?>
```

### Примітки

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Дивіться також

-   [mysql\_fetch\_array()](function.mysql-fetch-array.html) - Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.html) - Повертає ряд результату запиту як асоціативний масив.
-   [mysql\_fetch\_object()](function.mysql-fetch-object.html) - обробляє ряд результату запиту та повертає об'єкт
-   [mysql\_data\_seek()](function.mysql-data-seek.html) - Переміщує внутрішній покажчик у результаті запиту
-   [mysql\_fetch\_lengths()](function.mysql-fetch-lengths.html) - Повертає довжину кожного поля в результаті
-   [mysql\_result()](function.mysql-result.html) - Повертає дані результату запиту