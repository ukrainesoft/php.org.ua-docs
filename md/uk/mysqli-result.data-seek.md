Переміщує покажчик результату на вибраний рядок

-   [« mysqli\_result::$current\_field](mysqli-result.current-field.html)
    
-   [mysqli\_result::fetch\_all »](mysqli-result.fetch-all.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_result](class.mysqli-result.html)
    
-   Переміщує покажчик результату на вибраний рядок
    

# mysqliresult::dataseek

# mysqlidataseek

(PHP 5, PHP 7, PHP 8)

mysqliresult::dataseek - mysqlidataseek — Переміщує покажчик результату на вибраний рядок

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::data_seek(int $offset): bool
```

Процедурний стиль

```methodsynopsis
mysqli_data_seek(mysqli_result $result, int $offset): bool
```

Функція **mysqlidataseek()** переміщує покажчик в результаті на рядок, вказаний у параметрі `offset`

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.html), отриманий за допомогою [mysqli\_query()](mysqli.query.html) [mysqli\_store\_result()](mysqli.store-result.html) [mysqli\_use\_result()](mysqli.use-result.html) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.html)

`offset`

Зміщення рядків. Повинно бути між нулем і числом рядків у результаті мінус один (0..[mysqli\_num\_rows()](mysqli-result.num-rows.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::dataseek()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name";
$result = $mysqli->query($query);

/* Переход к строке 401 */
$result->data_seek(400);

/* Получение строки */
$row = $result->fetch_row();

printf("Город: %s  Код страны: %s\n", $row[0], $row[1]);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name";

$result = mysqli_query($link, $query);

/* Переход к строке 401 */
mysqli_data_seek($result, 400);

/* Получение строки */
$row = mysqli_fetch_row($result);

printf ("Город: %s  Код страны: %s\n", $row[0], $row[1]);
```

Результат виконання даних прикладів:

```
Город: Benin City  Код страны: NGA
```

**Приклад #2 Регулювання вказівника результату під час переміщення**

Функція може бути корисна при переміщенні по набору результатів для накладання порядку або перемотування набору результатів при багаторазовому повторенні.

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name LIMIT 15,4";
$result = $mysqli->query($query);

/* Перемещение по набору результатов в обратном порядке */
for ($row_no = $result->num_rows - 1; $row_no >= 0; $row_no--) {
    $result->data_seek($row_no);

    /* Получение строки */
    $row = $result->fetch_row();

    printf("Город: %s  Код страны: %s\n", $row[0], $row[1]);
}

/* Сброс указателя на начало набора результатов */
$result->data_seek(0);

print "\n";

/* Снова перемещение по тому же набору результатов */
while ($row = $result->fetch_row()) {
    printf("Город: %s  Код страны: %s\n", $row[0], $row[1]);
}
```

Результат виконання даних прикладів:

```
Город: Acmbaro  Код страны: MEX
Город: Abuja  Код страны: NGA
Город: Abu Dhabi  Код страны: ARE
Город: Abottabad  Код страны: PAK

Город: Abottabad  Код страны: PAK
Город: Abu Dhabi  Код страны: ARE
Город: Abuja  Код страны: NGA
Город: Acmbaro  Код страны: MEX
```

### Примітки

> **Зауваження**
> 
> Функція може бути використана тільки з буферизованими результатами, які можна отримати за допомогою функцій [mysqli\_store\_result()](mysqli.store-result.html) або [mysqli\_query()](mysqli.query.html)

### Дивіться також

-   [mysqli\_store\_result()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту
-   [mysqli\_fetch\_row()](mysqli-result.fetch-row.html) - Вибирає наступний рядок із набору результатів і поміщає його у звичайний масив
-   [mysqli\_fetch\_array()](mysqli-result.fetch-array.html) - Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_fetch\_assoc()](mysqli-result.fetch-assoc.html) - Вибирає наступний рядок із набору результатів та поміщає його в асоціативний масив
-   [mysqli\_fetch\_object()](mysqli-result.fetch-object.html) - Вибирає наступний рядок із набору результатів у вигляді об'єкта
-   [mysqli\_query()](mysqli.query.html) - Виконує запит до бази даних
-   [mysqli\_num\_rows()](mysqli-result.num-rows.html) - Отримує кількість рядків у наборі результатів