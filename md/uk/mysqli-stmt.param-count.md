---
navigation:
  - mysqli-stmt.num-rows.html: '« mysqlistmt::$numrows'
  - mysqli-stmt.prepare.html: 'mysqlistmt::prepare »'
  - index.html: PHP Manual
  - class.mysqli-stmt.html: mysqlistmt
title: 'mysqlistmt::$paramcount'
---
# mysqlistmt::$paramcount

# mysqlistmtparamcount

(PHP 5, PHP 7, PHP 8)

mysqlistmt::$paramcount - mysqlistmtparamcount — Повертає кількість параметрів у запиті

### Опис

Об'єктно-орієнтований стиль

int [$mysqlistmt->paramcount](mysqli-stmt.param-count.html)

Процедурний стиль

```methodsynopsis
mysqli_stmt_param_count(mysqli_stmt $statement): int
```

Повертає кількість позначок параметрів у підготовленому запиті.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Повертає ціле число, що дорівнює кількості параметрів.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

if ($stmt = $mysqli->prepare("SELECT Name FROM Country WHERE Name=? OR Code=?")) {

    $marker = $stmt->param_count;
    printf("В запросе %d меток.\n", $marker);

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
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

if ($stmt = mysqli_prepare($link, "SELECT Name FROM Country WHERE Name=? OR Code=?")) {

    $marker = mysqli_stmt_param_count($stmt);
    printf("В запросе %d меток.\n", $marker);

    /* закрываем запрос */
    mysqli_stmt_close($stmt);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
В запросе 2 меток.
```

### Дивіться також

-   [mysqliprepare()](mysqli.prepare.html) - готує SQL вираз до виконання
