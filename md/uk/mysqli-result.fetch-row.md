Вибирає наступний рядок із набору результатів і поміщає його у звичайний масив

-   [« mysqli\_result::fetch\_object](mysqli-result.fetch-object.html)
    
-   [mysqli\_result::$field\_count »](mysqli-result.field-count.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_result](class.mysqli-result.html)
    
-   Вибирає наступний рядок із набору результатів і поміщає його у звичайний масив
    

# mysqliresult::fetchrow

# mysqlifetchrow

(PHP 5, PHP 7, PHP 8)

mysqliresult::fetchrow - mysqlifetchrow - Вибирає наступний рядок з набору результатів і поміщає його у звичайний масив

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::fetch_row(): array|null|false
```

Процедурний стиль

```methodsynopsis
mysqli_fetch_row(mysqli_result $result): array|null|false
```

Вибирає один рядок даних із результуючого набору та повертає її у вигляді масиву, в якому індекси елементів відповідають номерам стовпців (починаючи з 0). Кожен наступний виклик функції повертатиме масив з даними наступного рядка набору або **`null`**якщо рядки закінчилися.

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.html), отриманий за допомогою [mysqli\_query()](mysqli.query.html) [mysqli\_store\_result()](mysqli.store-result.html) [mysqli\_use\_result()](mysqli.use-result.html) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.html)

### Значення, що повертаються

Повертає нумерований масив, що представляє обраний рядок, **`null`**якщо в наборі результатів більше немає рядків або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqliresult::fetchrow()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID DESC";

$result = $mysqli->query($query);

/* получение массива объектов */
while ($row = $result->fetch_row()) {
    printf("%s (%s)\n", $row[0], $row[1]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID DESC";

$result = mysqli_query($mysqli, $query);

/* получение ассоциативного массива */
while ($row = mysqli_fetch_row($result)) {
    printf("%s (%s)\n", $row[0], $row[1]);
}
```

Результат виконання даних прикладів:

```
Pueblo (USA)
Arvada (USA)
Cape Coral (USA)
Green Bay (USA)
Santa Clara (USA)
```

### Дивіться також

-   [mysqli\_fetch\_array()](mysqli-result.fetch-array.html) - Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_fetch\_assoc()](mysqli-result.fetch-assoc.html) - Вибирає наступний рядок із набору результатів та поміщає його в асоціативний масив
-   [mysqli\_fetch\_column()](mysqli-result.fetch-column.html) - отримує один стовпець з наступного рядка набору результатів
-   [mysqli\_fetch\_object()](mysqli-result.fetch-object.html) - Вибирає наступний рядок із набору результатів у вигляді об'єкта
-   [mysqli\_query()](mysqli.query.html) - Виконує запит до бази даних
-   [mysqli\_data\_seek()](mysqli-result.data-seek.html) - Переміщує покажчик результату на вибраний рядок