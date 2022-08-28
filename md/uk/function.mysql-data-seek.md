Переміщує внутрішній покажчик у результаті запиту

-   [« mysql\_create\_db](function.mysql-create-db.html)
    
-   [mysql\_db\_name »](function.mysql-db-name.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Переміщує внутрішній покажчик у результаті запиту
    

# mysqldataseek

(PHP 4, PHP 5)

mysqldataseek — Переміщує внутрішній покажчик в результаті запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_data\_seek()](mysqli-result.data-seek.html)
-   **`PDO::FETCH_ORI_ABS`**

### Опис

```methodsynopsis
mysql_data_seek(resource $result, int $row_number): bool
```

**mysqldataseek()** переміщує внутрішній покажчик результату запиту, з яким пов'язаний переданий дескриптор, до ряду із зазначеним номером. Наступний дзвінок до функції отримання даних MySQL, такий як [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.html), Поверне саме його.

Нумерація `row_number` починається з 0 . `row_number` має бути значенням у діапазоні від 0 до [mysql\_num\_rows()](function.mysql-num-rows.html) - 1. Однак, якщо результат порожній ([mysql\_num\_rows()](function.mysql-num-rows.html) == 0), то спроба зсуву покажчика до нульового ряду завершиться невдачею - буде викликана помилка рівня **`E_WARNING`** і **mysqldataseek()** поверне **`false`**

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.html). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.html)

`row_number`

Бажаний номер ряду в отриманому дескрипторі результату.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqldataseek()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
$db_selected = mysql_select_db('sample_db');
if (!$db_selected) {
    die('Не удалось выбрать базу данных: ' . mysql_error());
}
$query = 'SELECT last_name, first_name FROM friends';
$result = mysql_query($query);
if (!$result) {
    die('Ошибка запроса: ' . mysql_error());
}
/* получение рядов в обратном порядке */
for ($i = mysql_num_rows($result) - 1; $i >= 0; $i--) {
    if (!mysql_data_seek($result, $i)) {
        echo "Не удалось переместиться к ряду $i: " . mysql_error() . "\n";
        continue;
    }

    if (!($row = mysql_fetch_assoc($result))) {
        continue;
    }

    echo $row['last_name'] . ' ' . $row['first_name'] . "<br />\n";
}

mysql_free_result($result);
?>
```

### Примітки

> **Зауваження**
> 
> Функція **mysqldataseek()** може бути використана тільки з [mysql\_query()](function.mysql-query.html), але не з [mysql\_unbuffered\_query()](function.mysql-unbuffered-query.html)

### Дивіться також

-   [mysql\_query()](function.mysql-query.html) - Надсилає запит MySQL
-   [mysql\_num\_rows()](function.mysql-num-rows.html) - Повертає кількість рядів результату запиту
-   [mysql\_fetch\_row()](function.mysql-fetch-row.html) - Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.html) - Повертає ряд результату запиту як асоціативний масив.
-   [mysql\_fetch\_array()](function.mysql-fetch-array.html) - Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysql\_fetch\_object()](function.mysql-fetch-object.html) - обробляє ряд результату запиту та повертає об'єкт