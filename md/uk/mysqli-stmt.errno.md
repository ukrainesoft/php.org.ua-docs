Повертає код помилки виконання останнього запиту

-   [« mysqlistmt::dataseek](mysqli-stmt.data-seek.html)
    
-   [mysqlistmt::$errorlist »](mysqli-stmt.error-list.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlistmt](class.mysqli-stmt.html)
    
-   Повертає код помилки виконання останнього запиту
    

# mysqlistmt::$errno

# mysqlistmterrno

(PHP 5, PHP 7, PHP 8)

mysqlistmt::$errno -- mysqlistmterrno — Повертає код помилки виконання останнього запиту

### Опис

Об'єктно-орієнтований стиль

int [$mysqlistmt->errno](mysqli-stmt.errno.html)

Процедурний стиль

```methodsynopsis
mysqli_stmt_errno(mysqli_stmt $statement): int
```

Повертає код помилки для останнього виклику функції, яка могла завершитись вдало або невдало.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Код помилки. Нуль означає відсутність помилок.

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

    printf("Ошибка: %d.\n", $stmt->errno);

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

    printf("Ошибка: %d.\n", mysqli_stmt_errno($stmt));

    /* закрываем запрос */
    mysqli_stmt_close($stmt);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Ошибка: 1146.
```

### Дивіться також

-   [mysqlistmterror()](mysqli-stmt.error.html) - Повертає рядок із поясненням останньої помилки під час виконання запиту
-   [mysqlistmtsqlstate()](mysqli-stmt.sqlstate.html) - Повертає код помилки SQLSTATE, викликаної під час виконання останньої операції над запитом