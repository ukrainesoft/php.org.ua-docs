---
navigation:
  - mysqli-result.construct.md: '« mysqli\_result::\_\_construct'
  - mysqli-result.data-seek.md: 'mysqli\_result::data\_seek »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::$current\_field'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::$current\_field

# mysqli\_field\_tell

(PHP 5, PHP 7, PHP 8)

mysqli\_result::$current\_field -- mysqli\_field\_tell — Отримує зміщення вказівника по відношенню до поточного поля

### Опис

Об'єктно-орієнтований стиль

int[$mysqli\_result->current\_field](mysqli-result.current-field.md)

Процедурний стиль

```methodsynopsis
mysqli_field_tell(mysqli_result $result): int
```

Повертає позицію покажчика поля, що використовується під час останнього виклику [mysqli\_fetch\_field()](mysqli-result.fetch-field.md). Це значення може бути використане як аргумент для [mysqli\_field\_seek()](mysqli-result.field-seek.md)

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Повертає поточне усунення вказівника поля.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Ошибка соединения: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, SurfaceArea from Country ORDER BY Code LIMIT 5";

if ($result = $mysqli->query($query)) {

    /* Получить информацию о поле для всех столбцов */
    while ($finfo = $result->fetch_field()) {

        /* Получить смещение указателя поля */
        $currentfield = $result->current_field;

        printf("Столбец %d:\n", $currentfield);
        printf("Имя:     %s\n", $finfo->name);
        printf("Таблица:    %s\n", $finfo->table);
        printf("Макс. длина: %d\n", $finfo->max_length);
        printf("Флаги:    %d\n", $finfo->flags);
        printf("Тип:     %d\n\n", $finfo->type);
    }
    $result->close();
}

/* Закрыть соединение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Ошибка соединения: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, SurfaceArea from Country ORDER BY Code LIMIT 5";

if ($result = mysqli_query($link, $query)) {

    /* Получить информацию о поле для всех столбцов */
    while ($finfo = mysqli_fetch_field($result)) {

        /* Получить смещение указателя поля */
        $currentfield = mysqli_field_tell($result);

        printf("Столбец %d:\n", $currentfield);
        printf("Имя:     %s\n", $finfo->name);
        printf("Таблица:    %s\n", $finfo->table);
        printf("Макс. длина: %d\n", $finfo->max_length);
        printf("Флаги:    %d\n", $finfo->flags);
        printf("Тип:     %d\n\n", $finfo->type);
    }
    mysqli_free_result($result);
}

/* Закрыть соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

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

-   [mysqli\_fetch\_field()](mysqli-result.fetch-field.md) \- Повертає наступне поле результуючого набору
-   [mysqli\_field\_seek()](mysqli-result.field-seek.md) \- встановити покажчик поля на певне зміщення
