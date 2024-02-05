---
navigation:
  - function.mysql-create-db.md: « mysql\_create\_db
  - function.mysql-db-name.md: mysql\_db\_name »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_data\_seek
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_data\_seek

(PHP 4, PHP 5)

mysql\_data\_seek — Переміщує внутрішній покажчик в результаті запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_data\_seek()](mysqli-result.data-seek.md)
-   **`PDO::FETCH_ORI_ABS`**

### Опис

```methodsynopsis
mysql_data_seek(resource $result, int $row_number): bool
```

**mysql\_data\_seek()** переміщує внутрішній покажчик результату запиту, з яким пов'язаний переданий дескриптор, до ряду із зазначеним номером. Наступний дзвінок до функції отримання даних MySQL, такий як [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.md), Поверне саме його.

Нумерация`row_number` починається з 0 . `row_number` має бути значенням у діапазоні від 0 до [mysql\_num\_rows()](function.mysql-num-rows.md) \- 1. Однако, если результат пуст ([mysql\_num\_rows()](function.mysql-num-rows.md) == 0), то спроба зсуву покажчика до нульового ряду завершиться невдачею - буде викликана помилка рівня **`E_WARNING`**и**mysql\_data\_seek()** поверне **`false`**

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

`row_number`

Бажаний номер ряду в отриманому дескрипторі результату.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**mysql\_data\_seek()\*\*\*\*

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
$db_selected = mysql_select_db('sample_db');
if (!$db_selected) {
    die('Не удалось выбрать базу данных: ' . mysql_error());
}
$query = 'SELECT last_name, first_name FROM friends';
$result = mysql_query($query);
if (!$result) {
    die('Ошибка запроса: ' . mysql_error());
}
/* получение рядов в обратном порядке */
for ($i = mysql_num_rows($result) - 1; $i >= 0; $i--) {
    if (!mysql_data_seek($result, $i)) {
        echo "Не удалось переместиться к ряду $i: " . mysql_error() . "\n";
        continue;
    }

    if (!($row = mysql_fetch_assoc($result))) {
        continue;
    }

    echo $row['last_name'] . ' ' . $row['first_name'] . "<br />\n";
}

mysql_free_result($result);
?>
```

### Примітки

> **Зауваження** :
> 
> Функция**mysql\_data\_seek()** може бути використана тільки з [mysql\_query()](function.mysql-query.md), але не з [mysql\_unbuffered\_query()](function.mysql-unbuffered-query.md)

### Дивіться також

-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
-   [mysql\_num\_rows()](function.mysql-num-rows.md) \- Повертає кількість рядів результату запиту
-   [mysql\_fetch\_row()](function.mysql-fetch-row.md) \- Обробляє ряд результату запиту та повертає масив із числовими індексами
-   [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.md) \- Повертає ряд результату запиту як асоціативний масив.
-   [mysql\_fetch\_array()](function.mysql-fetch-array.md) \- Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysql\_fetch\_object()](function.mysql-fetch-object.md) \- обробляє ряд результату запиту та повертає об'єкт
