Отримання метаданих конкретного поля

-   [« mysqliresult::fetchcolumn](mysqli-result.fetch-column.html)
    
-   [mysqliresult::fetchfield »](mysqli-result.fetch-field.html)
    
-   [PHP Manual](index.html)
    
-   [mysqliresult](class.mysqli-result.html)
    
-   Отримання метаданих конкретного поля
    

# mysqliresult::fetchfielddirect

# mysqlifetchfielddirect

(PHP 5, PHP 7, PHP 8)

mysqliresult::fetchfielddirect -- mysqlifetchfielddirect — Отримання метаданих конкретного поля

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::fetch_field_direct(int $index): object|false
```

Процедурний стиль

```methodsynopsis
mysqli_fetch_field_direct(mysqli_result $result, int $index): object|false
```

Повертає інформацію про стовпчик результуючого набору у вигляді об'єкта.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqliresult](class.mysqli-result.html), отриманий за допомогою [mysqliquery()](mysqli.query.html) [mysqlistoreresult()](mysqli.store-result.html) [mysqliuseresult()](mysqli.use-result.html) або [mysqlistmtgetresult()](mysqli-stmt.get-result.html)

`index`

Номер поля. Число повинне лежати в діапазоні від `0` до `количество полей - 1`

### Значення, що повертаються

Повертає об'єкт, що містить визначення поля або **`false`**, якщо поле з номером `fieldnr` недоступне.

**Властивості об'єкту**

| Свойство  | Описание                                                           |
|-----------|--------------------------------------------------------------------|
| name      | Ім'я стовпця                                                       |
| orgname   | Вихідне ім'я стовпця, якщо він має псевдонім                       |
| table     | Ім'я таблиці, якій належить стовпець (якщо не обчислено)           |
| orgtable  | Початкове ім'я таблиці, якщо є псевдонім                           |
| def       | Зарезервовано для стандартного значення, на даний момент завжди "" |
| maxlength | Максимальна ширина поля результуючого набору.                      |
| length    | Ширина поля, як вона задана щодо таблиці.                          |
| charsetnr | Кількість наборів символів для поля.                               |
| flags     | Ціла кількість, що представляє бітові прапори для поля.            |
| type      | Тип даних поля                                                     |
| decimals  | Число знаків після коми (для числових полів)                       |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка подключения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, SurfaceArea from Country ORDER BY Name LIMIT 5";

if ($result = $mysqli->query($query)) {

    /* получение метаданных столбца 'SurfaceArea' */
    $finfo = $result->fetch_field_direct(1);

        printf("Имя:         %s\n", $finfo->name);
        printf("Таблица:     %s\n", $finfo->table);
        printf("Макс. длина: %d\n", $finfo->max_length);
        printf("Флаги:       %d\n", $finfo->flags);
        printf("Тип:         %d\n\n", $finfo->type);

    $result->close();
}

/* закрываем подключение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка подключения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$query = "SELECT Name, SurfaceArea from Country ORDER BY Name LIMIT 5";

if ($result = mysqli_query($link, $query)) {

    /* получение метаданных столбца 'SurfaceArea' */
    $finfo = mysqli_fetch_field_direct($result, 1);

    printf("Имя:         %s\n", $finfo->name);
    printf("Таблица:     %s\n", $finfo->table);
    printf("Макс. длина: %d\n", $finfo->max_length);
    printf("Флаги:       %d\n", $finfo->flags);
    printf("Тип:         %d\n\n", $finfo->type);

    mysqli_free_result($result);
}

/* закрываем подключение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Имя:         SurfaceArea
Таблица:     Country
Макс. длина: 10
Флаги:       32769
Тип:         4
```

### Дивіться також

-   [mysqlinumfields()](mysqli-result.field-count.html) - Отримує кількість полів у наборі результатів
-   [mysqlifetchfield()](mysqli-result.fetch-field.html) - Повертає наступне поле результуючого набору
-   [mysqlifetchfields()](mysqli-result.fetch-fields.html) - Повертає масив об'єктів, що становлять поля результуючого набору