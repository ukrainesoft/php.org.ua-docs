---
navigation:
  - mysqli.execute-query.md: '« mysqli::execute\_query'
  - mysqli.get-charset.md: 'mysqli::get\_charset »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$field\_count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$field\_count

# mysqli\_field\_count

(PHP 5, PHP 7, PHP 8)

mysqli::$field\_count -- mysqli\_field\_count — Повертає кількість стовпців, зачеплених останнім запитом

### Опис

Об'єктно-орієнтований стиль

int[$mysqli->field\_count](mysqli.field-count.md)

Процедурний стиль

```methodsynopsis
mysqli_field_count(mysqli $mysql): int
```

Повертає кількість стовпців, які торкнулися останнім запитом для з'єднання, зазначеного в `mysql`. Ця функція може бути корисною під час використання [mysqli\_store\_result()](mysqli.store-result.md) для того, щоб визначити, чи виданий непустий результат, або у разі невідомого призначення запиту.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Ціле число, що містить кількість полів у результаті запиту.

### Приклади

**Приклад #1 Приклад використання $mysqli->field\_count**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "test");

$mysqli->query( "DROP TABLE IF EXISTS friends");
$mysqli->query( "CREATE TABLE friends (id int, name varchar(20))");

$mysqli->query( "INSERT INTO friends VALUES (1,'Hartmut'), (2, 'Ulf')");


$mysqli->real_query("SELECT * FROM friends");

if ($mysqli->field_count) {
    /* Определить тип запроса (select/show или describe) */
    $result = $mysqli->store_result();

    /* Создать выборку */
    $row = $result->fetch_row();

    /* Очистить выборку */
    $result->close();
}

/* Закрыть соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "test");

mysqli_query($link, "DROP TABLE IF EXISTS friends");
mysqli_query($link, "CREATE TABLE friends (id int, name varchar(20))");

mysqli_query($link, "INSERT INTO friends VALUES (1,'Hartmut'), (2, 'Ulf')");

mysqli_real_query($link, "SELECT * FROM friends");

if (mysqli_field_count($link)) {
    /* Определить тип запроса (select/show или describe) */
    $result = mysqli_store_result($link);

    /* Создать выборку */
    $row = mysqli_fetch_row($result);

    /* Очистить выборку */
    mysqli_free_result($result);
}

/* Закрыть соединение */
mysqli_close($link);
?>
```
