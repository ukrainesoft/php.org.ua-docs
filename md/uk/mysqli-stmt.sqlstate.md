---
navigation:
  - mysqli-stmt.send-long-data.md: '« mysqli\_stmt::send\_long\_data'
  - mysqli-stmt.store-result.md: 'mysqli\_stmt::store\_result »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::$sqlstate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::$sqlstate

# mysqli\_stmt\_sqlstate

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::$sqlstate -- mysqli\_stmt\_sqlstate — Повернення коду помилки SQLSTATE, викликаної під час виконання останньої операції над запитом

### Опис

Об'єктно-орієнтований стиль

string[$mysqli\_stmt->sqlstate](mysqli-stmt.sqlstate.md)

Процедурний стиль

```methodsynopsis
mysqli_stmt_sqlstate(mysqli_stmt $statement): string
```

Повертає рядок, що містить код SQLSTATE, помилки, викликаної в результаті виконання останньої операції над запитом, яка може завершуватися успішно або неуспішно. Цей код складається з п'яти символів . `'00000'` означає відсутність помилок. Значення цього коду визначено у стандарті ANSI SQL, а також у ODBC. Повний список можливих кодів можна переглянути на сторінці [» http://dev.mysql.com/doc/mysql/en/error-handling.md](http://dev.mysql.com/doc/mysql/en/error-handling.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає рядок, що містить код помилки SQLSTATE останньої досконалої операції. Цей код складається з п'яти символів . `'00000'` означає відсутність помилок.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
/* Открываем соединение */
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Проверяем соединение */
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

    printf("Ошибка: %s.\n", $stmt->sqlstate);

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
/* Открываем соединение */
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Проверяем соединение */
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

    printf("Ошибка: %s.\n", mysqli_stmt_sqlstate($stmt));

    /* закрываем запрос */
    mysqli_stmt_close($stmt);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
Ошибка: 42S02.
```

### Примітки

> **Зауваження** :
> 
> Слід зазначити, що не всі помилки MySQL мають свій відбиток у кодах SQLSTATE. Для таких помилок використовується загальний код `HY000` (Загальна помилка).

### Дивіться також

-   [mysqli\_stmt\_errno()](mysqli-stmt.errno.md) \- Повертає код помилки виконання останнього запиту
-   [mysqli\_stmt\_error()](mysqli-stmt.error.md) \- Повертає рядок із поясненням останньої помилки під час виконання запиту
