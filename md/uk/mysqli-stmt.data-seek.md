Перехід до заданого рядка в результуючому наборі

-   [« mysqli\_stmt::\_\_construct](mysqli-stmt.construct.html)
    
-   [mysqli\_stmt::$errno »](mysqli-stmt.errno.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_stmt](class.mysqli-stmt.html)
    
-   Перехід до заданого рядка в результуючому наборі
    

# mysqlistmt::dataseek

# mysqlistmtdataseek

(PHP 5, PHP 7, PHP 8)

mysqlistmt::dataseek - mysqlistmtdataseek — Перехід до заданого рядка в результуючому наборі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::data_seek(int $offset): void
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_data_seek(mysqli_stmt $statement, int $offset): void
```

Переміщує покажчик на заданий рядок у результуючому наборі.

[mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.html) must be called prior to **mysqlistmtdataseek()**

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.html), отриманий за допомогою [mysqli\_stmt\_init()](mysqli.stmt-init.html)

`offset`

Значення повинне бути в діапазоні від 0 до числа рядків мінус один (0. . [mysqli\_stmt\_num\_rows()](mysqli-stmt.num-rows.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

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

$query = "SELECT Name, CountryCode FROM City ORDER BY Name";
if ($stmt = $mysqli->prepare($query)) {

    /* выполняем запрос */
    $stmt->execute();

    /* привязываем переменные к результату запроса */
    $stmt->bind_result($name, $code);

    /* помещаем результаты запроса в переменные */
    $stmt->store_result();

    /* переходим к строке 400 результирующей таблицы */
    $stmt->data_seek(399);

    /* извлекаем данные */
    $stmt->fetch();

    printf ("Город: %s  Код страны: %s\n", $name, $code);

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

$query = "SELECT Name, CountryCode FROM City ORDER BY Name";
if ($stmt = mysqli_prepare($link, $query)) {

    /* выполняем запрос */
    mysqli_stmt_execute($stmt);

    /* привязываем переменные к результату запроса */
    mysqli_stmt_bind_result($stmt, $name, $code);

    /* помещаем результаты запроса в переменные */
    mysqli_stmt_store_result($stmt);

    /* переходим к строке 400 результирующей таблицы */
    mysqli_stmt_data_seek($stmt, 399);

    /* извлекаем данные */
    mysqli_stmt_fetch($stmt);

    printf ("Город: %s  Код страны: %s\n", $name, $code);

    /* закрываем запрос */
    mysqli_stmt_close($stmt);
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Город: Benin City  Код страны: NGA
```

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.html) - готує SQL вираз до виконання