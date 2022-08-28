Повертає кількість попереджень із останнього запиту заданого підключення

-   [« mysqli::use\_result](mysqli.use-result.html)
    
-   [mysqli\_stmt »](class.mysqli-stmt.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Повертає кількість попереджень із останнього запиту заданого підключення
    

# mysqli::$warningcount

# mysqliwarningcount

(PHP 5, PHP 7, PHP 8)

mysqli::$warningcount - mysqliwarningcount — Повертає кількість попереджень із останнього запиту заданого підключення

### Опис

Об'єктно-орієнтований стиль

int [$mysqli->warning\_count](mysqli.warning-count.html)

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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

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

-   [mysqli\_errno()](mysqli.errno.html) - Повертає код помилки останнього виклику функції
-   [mysqli\_error()](mysqli.error.html) - Повертає рядок із описом останньої помилки
-   [mysqli\_sqlstate()](mysqli.sqlstate.html) - Повертає код стану SQLSTATE останній MySQL операції