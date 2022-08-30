Встановити покажчик поля на певне усунення

-   [« mysqliresult::$fieldcount](mysqli-result.field-count.html)
    
-   [mysqliresult::free »](mysqli-result.free.html)
    
-   [PHP Manual](index.md)
    
-   [mysqliresult](class.mysqli-result.html)
    
-   Встановити покажчик поля на певне усунення
    

# mysqliresult::fieldseek

# mysqlifieldseek

(PHP 5, PHP 7, PHP 8)

mysqliresult::fieldseek - mysqlifieldseek — Встановити вказівник поля на певне усунення

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::field_seek(int $index): bool
```

Процедурний стиль

```methodsynopsis
mysqli_field_seek(mysqli_result $result, int $index): bool
```

Встановлює вказівник поля на задане усунення. Наступний виклик [mysqlifetchfield()](mysqli-result.fetch-field.html) дозволить отримати інформацію про стовпчик з позицією усунення.

> **Зауваження**
> 
> Для пошуку з початку рядка необхідно встановити нульове значення усунення.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.html), отриманий за допомогою [mysqliquery()](mysqli.query.md) [mysqlistoreresult()](mysqli.store-result.html) [mysqliuseresult()](mysqli.use-result.html) або [mysqlistmtgetresult()](mysqli-stmt.get-result.html)

`index`

Номер поля. Це значення має бути в наступному діапазоні: від `0` до `число полей - 1`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

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

    /* Получить информацию о поле во втором столбце */
    $result->field_seek(1);
    $finfo = $result->fetch_field();

    printf("Имя:     %s\n", $finfo->name);
    printf("Таблица:    %s\n", $finfo->table);
    printf("Макс. длина: %d\n", $finfo->max_length);
    printf("Флаги:    %d\n", $finfo->flags);
    printf("Тип:     %d\n\n", $finfo->type);

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

    /* Получить информацию о поле во втором столбце */
    mysqli_field_seek($result, 1);
    $finfo = mysqli_fetch_field($result);

    printf("Имя:     %s\n", $finfo->name);
    printf("Таблица:    %s\n", $finfo->table);
    printf("Макс. длина: %d\n", $finfo->max_length);
    printf("Флаги:    %d\n", $finfo->flags);
    printf("Тип:     %d\n\n", $finfo->type);

    mysqli_free_result($result);
}

/* Закрыть соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Имя:     SurfaceArea
Таблица:    Country
Макс. длина: 10
Флаги:    32769
Тип:     4
```

### Дивіться також

-   [mysqlifetchfield()](mysqli-result.fetch-field.html) - Повертає наступне поле результуючого набору