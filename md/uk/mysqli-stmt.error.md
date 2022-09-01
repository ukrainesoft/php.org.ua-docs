---
navigation:
  - mysqli-stmt.error-list.html: '« mysqlistmt::$errorlist'
  - mysqli-stmt.execute.html: 'mysqlistmt::execute »'
  - index.html: PHP Manual
  - class.mysqli-stmt.html: mysqlistmt
title: 'mysqlistmt::$error'
---
# mysqlistmt::$error

# mysqlistmterror

(PHP 5, PHP 7, PHP 8)

mysqlistmt::$error -- mysqlistmterror — Повертає рядок із поясненням останньої помилки під час виконання запиту

### Опис

Об'єктно-орієнтований стиль

string [$mysqlistmt->error](mysqli-stmt.error.html)

Процедурний стиль

```methodsynopsis
mysqli_stmt_error(mysqli_stmt $statement): string
```

Повертає рядок із повідомленням про помилку для останнього виклику функції, яка могла його викликати.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Рядок повідомлення про помилку. Порожній рядок означає відсутність помилок.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
/* открываем соединение */
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$mysqli->query("CREATE TABLE myCountry LIKE Country");
$mysqli->query("INSERT INTO myCountry SELECT * FROM Country");


$query = "SELECT Name, Code FROM myCountry ORDER BY Name";
if ($stmt = $mysqli->prepare($query)) {

    /* удаляем таблицу */
    $mysqli->query("DROP TABLE myCountry");

    /* выполняем запрос */
    $stmt->execute();

    printf("Ошибка: %s.\n", $stmt->error);

    /* закрываем запрос */
    $stmt->close();
}

/* закрываем соединение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
/* открываем соединение */
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

mysqli_query($link, "CREATE TABLE myCountry LIKE Country");
mysqli_query($link, "INSERT INTO myCountry SELECT * FROM Country");


$query = "SELECT Name, Code FROM myCountry ORDER BY Name";
if ($stmt = mysqli_prepare($link, $query)) {

    /* удаляем таблицу */
    mysqli_query($link, "DROP TABLE myCountry");

    /* выполняем запрос */
    mysqli_stmt_execute($stmt);

    printf("Ошибка: %s.\n", mysqli_stmt_error($stmt));

    /* закрываем запрос */
    mysqli_stmt_close($stmt);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Ошибка: Table 'world.myCountry' doesn't exist.
```

### Дивіться також

-   [mysqlistmterrno()](mysqli-stmt.errno.html) - Повертає код помилки виконання останнього запиту
-   [mysqlistmtsqlstate()](mysqli-stmt.sqlstate.html) - Повертає код помилки SQLSTATE, викликаної під час виконання останньої операції над запитом
