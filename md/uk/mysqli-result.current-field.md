Отримує зміщення вказівника по відношенню до поточного поля

-   [« mysqli\_result::\_\_construct](mysqli-result.construct.html)
    
-   [mysqli\_result::data\_seek »](mysqli-result.data-seek.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_result](class.mysqli-result.html)
    
-   Отримує зміщення вказівника по відношенню до поточного поля
    

# mysqliresult::$currentfield

# mysqlifieldtell

(PHP 5, PHP 7, PHP 8)

mysqliresult::$currentfield - mysqlifieldtell — Отримує зміщення вказівника по відношенню до поточного поля

### Опис

Об'єктно-орієнтований стиль

int [$mysqli\_result->current\_field](mysqli-result.current-field.html)

Процедурний стиль

```methodsynopsis
mysqli_field_tell(mysqli_result $result): int
```

Повертає позицію покажчика поля, що використовується під час останнього виклику [mysqli\_fetch\_field()](mysqli-result.fetch-field.html). Це значення може бути використане як аргумент для [mysqli\_field\_seek()](mysqli-result.field-seek.html)

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.html), отриманий за допомогою [mysqli\_query()](mysqli.query.html) [mysqli\_store\_result()](mysqli.store-result.html) [mysqli\_use\_result()](mysqli.use-result.html) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.html)

### Значення, що повертаються

Повертає поточне усунення вказівника поля.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Ошибка соединения: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, SurfaceArea from Country ORDER BY Code LIMIT 5";

if ($result = $mysqli->query($query)) {

    /* Получить информацию о поле для всех столбцов */
    while ($finfo = $result->fetch_field()) {

        /* Получить смещение указателя поля */
        $currentfield = $result->current_field;

        printf("Столбец %d:\n", $currentfield);
        printf("Имя:     %s\n", $finfo->name);
        printf("Таблица:    %s\n", $finfo->table);
        printf("Макс. длина: %d\n", $finfo->max_length);
        printf("Флаги:    %d\n", $finfo->flags);
        printf("Тип:     %d\n\n", $finfo->type);
    }
    $result->close();
}

/* Закрыть соединение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Ошибка соединения: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, SurfaceArea from Country ORDER BY Code LIMIT 5";

if ($result = mysqli_query($link, $query)) {

    /* Получить информацию о поле для всех столбцов */
    while ($finfo = mysqli_fetch_field($result)) {

        /* Получить смещение указателя поля */
        $currentfield = mysqli_field_tell($result);

        printf("Столбец %d:\n", $currentfield);
        printf("Имя:     %s\n", $finfo->name);
        printf("Таблица:    %s\n", $finfo->table);
        printf("Макс. длина: %d\n", $finfo->max_length);
        printf("Флаги:    %d\n", $finfo->flags);
        printf("Тип:     %d\n\n", $finfo->type);
    }
    mysqli_free_result($result);
}

/* Закрыть соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Столбец 1:
Имя:     Name
Таблица:    Country
Макс. длина: 11
Флаги:    1
Тип:     254

Столбец 2:
Имя:     SurfaceArea
Таблица:    Country
Макс. длина: 10
Флаги:    32769
Тип:     4
```

### Дивіться також

-   [mysqli\_fetch\_field()](mysqli-result.fetch-field.html) - Повертає наступне поле результуючого набору
-   [mysqli\_field\_seek()](mysqli-result.field-seek.html) - встановити покажчик поля на певне зміщення