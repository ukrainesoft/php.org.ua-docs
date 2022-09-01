---
navigation:
  - function.mysql-create-db.html: « mysqlcreateдб
  - function.mysql-db-name.html: mysqlдбname »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqldataseek
---
# mysqldataseek

(PHP 4, PHP 5)

mysqldataseek — Переміщує внутрішній покажчик в результаті запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlidataseek()](mysqli-result.data-seek.md)
-   **`PDO::FETCH_ORI_ABS`**

### Опис

```methodsynopsis
mysql_data_seek(resource $result, int $row_number): bool
```

**mysqldataseek()** переміщує внутрішній покажчик результату запиту, з яким пов'язаний переданий дескриптор, до ряду із зазначеним номером. Наступний дзвінок до функції отримання даних MySQL, такий як [mysqlfetchassoc()](function.mysql-fetch-assoc.md), Поверне саме його.

Нумерація `row_number` починається з 0 . `row_number` має бути значенням у діапазоні від 0 до [mysqlnumrows()](function.mysql-num-rows.html) - 1. Однак, якщо результат порожній ([mysqlnumrows()](function.mysql-num-rows.md) == 0), то спроба зсуву покажчика до нульового ряду завершиться невдачею - буде викликана помилка рівня **`E_WARNING`** і **mysqldataseek()** поверне **`false`**

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.md)

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
> Функція **mysqldataseek()** може бути використана тільки з [mysqlquery()](function.mysql-query.html), але не з [mysqlunbufferedquery()](function.mysql-unbuffered-query.md)

### Дивіться також

-   [mysqlquery()](function.mysql-query.md) - Надсилає запит MySQL
-   [mysqlnumrows()](function.mysql-num-rows.md) - Повертає кількість рядів результату запиту
-   [mysqlfetchrow()](function.mysql-fetch-row.md) - Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysqlfetchassoc()](function.mysql-fetch-assoc.md) - Повертає ряд результату запиту як асоціативний масив.
-   [mysqlfetcharray()](function.mysql-fetch-array.md) - Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysqlfetchobject()](function.mysql-fetch-object.md) - обробляє ряд результату запиту та повертає об'єкт
