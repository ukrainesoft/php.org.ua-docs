---
navigation:
  - mysqli.error.html: '« mysqli::$error'
  - mysqli.get-charset.html: 'mysqli::getcharset »'
  - index.html: PHP Manual
  - class.mysqli.html: mysqli
title: 'mysqli::$fieldcount'
---
# mysqli::$fieldcount

# mysqlifieldcount

(PHP 5, PHP 7, PHP 8)

mysqli::$fieldcount - mysqlifieldcount — Повертає кількість стовпців, зачеплених останнім запитом

### Опис

Об'єктно-орієнтований стиль

int [$mysqli->fieldcount](mysqli.field-count.html)

Процедурний стиль

```methodsynopsis
mysqli_field_count(mysqli $mysql): int
```

Повертає кількість стовпців, які торкнулися останнім запитом для з'єднання, зазначеного в `mysql`. Ця функція може бути корисною під час використання [mysqlistoreresult()](mysqli.store-result.html) для того, щоб визначити, чи виданий непустий результат, або у разі невідомого призначення запиту.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

### Значення, що повертаються

Ціле число, що містить кількість полів у результаті запиту.

### Приклади

**Приклад #1 Приклад використання $mysqli->fieldcount**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "test");

$mysqli->query( "DROP TABLE IF EXISTS friends");
$mysqli->query( "CREATE TABLE friends (id int, name varchar(20))");

$mysqli->query( "INSERT INTO friends VALUES (1,'Hartmut'), (2, 'Ulf')");


$mysqli->real_query("SELECT * FROM friends");

if ($mysqli->field_count) {
    /* Определить тип запроса (select/show или describe) */
    $result = $mysqli->store_result();

    /* Создать выборку */
    $row = $result->fetch_row();

    /* Очистить выборку */
    $result->close();
}

/* Закрыть соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "test");

mysqli_query($link, "DROP TABLE IF EXISTS friends");
mysqli_query($link, "CREATE TABLE friends (id int, name varchar(20))");

mysqli_query($link, "INSERT INTO friends VALUES (1,'Hartmut'), (2, 'Ulf')");

mysqli_real_query($link, "SELECT * FROM friends");

if (mysqli_field_count($link)) {
    /* Определить тип запроса (select/show или describe) */
    $result = mysqli_store_result($link);

    /* Создать выборку */
    $row = mysqli_fetch_row($result);

    /* Очистить выборку */
    mysqli_free_result($result);
}

/* Закрыть соединение */
mysqli_close($link);
?>
```
