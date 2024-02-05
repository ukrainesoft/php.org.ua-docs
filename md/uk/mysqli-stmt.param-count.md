---
navigation:
  - mysqli-stmt.num-rows.md: '« mysqli\_stmt::$num\_rows'
  - mysqli-stmt.prepare.md: 'mysqli\_stmt::prepare »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::$param\_count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::$param\_count

# mysqli\_stmt\_param\_count

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::$param\_count -- mysqli\_stmt\_param\_count — Повертає кількість параметрів у запиті

### Опис

Об'єктно-орієнтований стиль

int[$mysqli\_stmt->param\_count](mysqli-stmt.param-count.md)

Процедурний стиль

```methodsynopsis
mysqli_stmt_param_count(mysqli_stmt $statement): int
```

Повертає кількість позначок параметрів у підготовленому запиті.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає ціле число, що дорівнює кількості параметрів.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

if ($stmt = $mysqli->prepare("SELECT Name FROM Country WHERE Name=? OR Code=?")) {

    $marker = $stmt->param_count;
    printf("В запросе %d меток.\n", $marker);

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
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверяем соединение */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

if ($stmt = mysqli_prepare($link, "SELECT Name FROM Country WHERE Name=? OR Code=?")) {

    $marker = mysqli_stmt_param_count($stmt);
    printf("В запросе %d меток.\n", $marker);

    /* закрываем запрос */
    mysqli_stmt_close($stmt);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

```
В запросе 2 меток.
```

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
