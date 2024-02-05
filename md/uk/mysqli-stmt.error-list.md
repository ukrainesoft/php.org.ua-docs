---
navigation:
  - mysqli-stmt.errno.md: '« mysqli\_stmt::$errno'
  - mysqli-stmt.error.md: 'mysqli\_stmt::$error »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::$error\_list'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::$error\_list

# mysqli\_stmt\_error\_list

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

mysqli\_stmt::$error\_list -- mysqli\_stmt\_error\_list — Повертає список помилок виконання останнього запиту

### Опис

Об'єктно-орієнтований стиль

array[$mysqli\_stmt->error\_list](mysqli-stmt.error-list.md)

Процедурний стиль

```methodsynopsis
mysqli_stmt_error_list(mysqli_stmt $statement): array
```

Повертає список помилок, які виникли під час виконання останньої операції над запитом, яка може завершуватися успішно чи неуспішно.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Список помилок, кожна з яких представлена ​​у вигляді масиву (array), що містить код помилки, повідомлення про помилку, а також код стану sqlstate.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
/* открываем соединение */
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$mysqli->query("CREATE TABLE myCountry LIKE Country");
$mysqli->query("INSERT INTO myCountry SELECT * FROM Country");


$query = "SELECT Name, Code FROM myCountry ORDER BY Name";
if ($stmt = $mysqli->prepare($query)) {

    /* удаляем таблицу */
    $mysqli->query("DROP TABLE myCountry");

    /* выполняем запрос */
    $stmt->execute();

    echo "Ошибка:\n";
    print_r($stmt->error_list);

    /* закрываем запрос */
    $stmt->close();
}

/* закрываем соединение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
/* открываем соединение */
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

mysqli_query($link, "CREATE TABLE myCountry LIKE Country");
mysqli_query($link, "INSERT INTO myCountry SELECT * FROM Country");


$query = "SELECT Name, Code FROM myCountry ORDER BY Name";
if ($stmt = mysqli_prepare($link, $query)) {

    /* удаляем таблицу */
    mysqli_query($link, "DROP TABLE myCountry");

    /* выполняем запрос */
    mysqli_stmt_execute($stmt);

    echo "Ошибка:\n";
    print_r(mysql_stmt_error_list($stmt));

    /* закрываем запрос */
    mysqli_stmt_close($stmt);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
Ошибка:
Array
(
    [0] => Array
        (
            [errno] => 1146
            [sqlstate] => 42S02
            [error] => Table 'world.myCountry' doesn't exist
        )

)
```

### Дивіться також

-   [mysqli\_stmt\_error()](mysqli-stmt.error.md) \- Повертає рядок із поясненням останньої помилки під час виконання запиту
-   [mysqli\_stmt\_errno()](mysqli-stmt.errno.md) \- Повертає код помилки виконання останнього запиту
-   [mysqli\_stmt\_sqlstate()](mysqli-stmt.sqlstate.md) \- Повертає код помилки SQLSTATE, викликаної під час виконання останньої операції над запитом
