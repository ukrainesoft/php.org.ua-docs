---
navigation:
  - mysqli.use-result.md: '« mysqli::useresult'
  - class.mysqli-stmt.md: mysqlistmt »
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$warningcount'
---
# mysqli::$warningcount

# mysqliwarningcount

(PHP 5, PHP 7, PHP 8)

mysqli::$warningcount - mysqliwarningcount — Повертає кількість попереджень із останнього запиту заданого підключення

### Опис

Об'єктно-орієнтований стиль

int [$mysqli->warningcount](mysqli.warning-count.md)

Процедурний стиль

```methodsynopsis
mysqli_warning_count(mysqli $mysql): int
```

Повертає кількість попереджень із останнього запиту.

> **Зауваження**
> 
> Для отримання попереджень можна використовувати SQL-команду `SHOW WARNINGS [limit row_count]`

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Кількість попереджень чи нуль, якщо таких немає.

### Приклади

**Приклад #1 Приклад використання $mysqli->warningcount**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$mysqli->query("CREATE TABLE myCity LIKE City");

/* знаменитый город в Уэльсе */
$query = "INSERT INTO myCity (CountryCode, Name) VALUES('GBR',
        'Llanfairpwllgwyngyllgogerychwyrndrobwllllantysiliogogogoch')";

$mysqli->query($query);

if ($mysqli->warning_count) {
    if ($result = $mysqli->query("SHOW WARNINGS")) {
        $row = $result->fetch_row();
        printf("%s (%d): %s\n", $row[0], $row[1], $row[2]);
        $result->close();
    }
}

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

mysqli_query($link, "CREATE TABLE myCity LIKE City");

/* знаменитый город в Уэльсе */
$query = "INSERT INTO myCity (CountryCode, Name) VALUES('GBR',
        'Llanfairpwllgwyngyllgogerychwyrndrobwllllantysiliogogogoch')";

mysqli_query($link, $query);

if (mysqli_warning_count($link)) {
    if ($result = mysqli_query($link, "SHOW WARNINGS")) {
        $row = mysqli_fetch_row($result);
        printf("%s (%d): %s\n", $row[0], $row[1], $row[2]);
        mysqli_free_result($result);
    }
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Warning (1264): Data truncated for column 'Name' at row 1
```

### Дивіться також

-   [mysqlierrno()](mysqli.errno.md) - Повертає код помилки останнього виклику функції
-   [mysqlierror()](mysqli.error.md) - Повертає рядок із описом останньої помилки
-   [mysqlisqlstate()](mysqli.sqlstate.md) - Повертає код стану SQLSTATE останній MySQL операції
