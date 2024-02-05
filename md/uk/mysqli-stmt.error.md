---
navigation:
  - mysqli-stmt.error-list.md: '« mysqli\_stmt::$error\_list'
  - mysqli-stmt.execute.md: 'mysqli\_stmt::execute »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::$error'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::$error

# mysqli\_stmt\_error

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::$error -- mysqli\_stmt\_error — Повертає рядок із поясненням останньої помилки під час виконання запиту

### Опис

Об'єктно-орієнтований стиль

string[$mysqli\_stmt->error](mysqli-stmt.error.md)

Процедурний стиль

```methodsynopsis
mysqli_stmt_error(mysqli_stmt $statement): string
```

Повертає рядок із повідомленням про помилку для останнього виклику функції, яка могла його викликати.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Рядок повідомлення про помилку. Порожній рядок означає відсутність помилок.

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

    printf("Ошибка: %s.\n", $stmt->error);

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

    printf("Ошибка: %s.\n", mysqli_stmt_error($stmt));

    /* закрываем запрос */
    mysqli_stmt_close($stmt);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
Ошибка: Table 'world.myCountry' doesn't exist.
```

### Дивіться також

-   [mysqli\_stmt\_errno()](mysqli-stmt.errno.md) \- Повертає код помилки виконання останнього запиту
-   [mysqli\_stmt\_sqlstate()](mysqli-stmt.sqlstate.md) \- Повертає код помилки SQLSTATE, викликаної під час виконання останньої операції над запитом
