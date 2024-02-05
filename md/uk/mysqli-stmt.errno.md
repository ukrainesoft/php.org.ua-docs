---
navigation:
  - mysqli-stmt.data-seek.md: '« mysqli\_stmt::data\_seek'
  - mysqli-stmt.error-list.md: 'mysqli\_stmt::$error\_list »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::$errno'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::$errno

# mysqli\_stmt\_errno

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::$errno -- mysqli\_stmt\_errno — Повертає код помилки виконання останнього запиту

### Опис

Об'єктно-орієнтований стиль

int[$mysqli\_stmt->errno](mysqli-stmt.errno.md)

Процедурний стиль

```methodsynopsis
mysqli_stmt_errno(mysqli_stmt $statement): int
```

Повертає код помилки для останнього виклику функції, яка могла завершитись вдало або невдало.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Код помилки. Нуль означає відсутність помилок.

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

    printf("Ошибка: %d.\n", $stmt->errno);

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

    printf("Ошибка: %d.\n", mysqli_stmt_errno($stmt));

    /* закрываем запрос */
    mysqli_stmt_close($stmt);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
Ошибка: 1146.
```

### Дивіться також

-   [mysqli\_stmt\_error()](mysqli-stmt.error.md) \- Повертає рядок із поясненням останньої помилки під час виконання запиту
-   [mysqli\_stmt\_sqlstate()](mysqli-stmt.sqlstate.md) \- Повертає код помилки SQLSTATE, викликаної під час виконання останньої операції над запитом
