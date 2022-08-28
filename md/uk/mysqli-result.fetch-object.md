Вибирає наступний рядок із набору результатів у вигляді об'єкта

-   [« mysqli\_result::fetch\_fields](mysqli-result.fetch-fields.html)
    
-   [mysqli\_result::fetch\_row »](mysqli-result.fetch-row.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_result](class.mysqli-result.html)
    
-   Вибирає наступний рядок із набору результатів у вигляді об'єкта
    

# mysqliresult::fetchobject

# mysqlifetchobject

(PHP 5, PHP 7, PHP 8)

mysqliresult::fetchobject - mysqlifetchobject — Вибір наступного рядка з набору результатів у вигляді об'єкта

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::fetch_object(string $class = "stdClass", array $constructor_args = []): object|null|false
```

Процедурний стиль

```methodsynopsis
mysqli_fetch_object(mysqli_result $result, string $class = "stdClass", array $constructor_args = []): object|null|false
```

Вибирає один рядок даних із набору результатів і повертає його як об'єкт, де кожна властивість представляє ім'я стовпця набору результатів. Кожен наступний виклик цієї функції повертатиме наступний рядок у наборі результатів або **`null`**якщо рядків більше немає.

Якщо у двох і більше стовпців у наборі результатів однакове ім'я, останній стовпець матиме пріоритет і перезапише будь-які попередні дані. Для доступу до кількох стовпців з однаковим ім'ям можна використовувати функцію [mysqli\_fetch\_row()](mysqli-result.fetch-row.html) Для вибору масиву з числовим індексом або у списку вибору SQL-запиту можна використовувати псевдоніми, щоб задати стовпцям різні імена.

> **Зауваження**: Функція встановлює значення властивостей об'єкта до виклику конструктора.

> **Зауваження**: Імена полів, що повертаються цією функцією *залежними від регістру*

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.html), отриманий за допомогою [mysqli\_query()](mysqli.query.html) [mysqli\_store\_result()](mysqli.store-result.html) [mysqli\_use\_result()](mysqli.use-result.html) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.html)

`class`

Ім'я класу, об'єкт якого потрібно інстанціювати, встановити значення його властивостей і повернути. Якщо параметр не встановлено, буде повернено об'єкт **stdClass**

`constructor_args`

Необов'язковий масив (array) параметрів, які передадуть конструктору класу `class`

### Значення, що повертаються

Повертає об'єкт, що представляє обраний рядок, де кожна властивість представляє ім'я стовпця набору результатів, **`null`**якщо в наборі результатів більше немає рядків або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `constructor_args` тепер приймає `[]` для конструкторів без параметрів; раніше викидався виняток. |

### Приклади

**Приклад #1 Приклад використання **mysqliresult::fetchobject()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID DESC";

$result = $mysqli->query($query);

/* получение массива объектов */
while ($obj = $result->fetch_object()) {
    printf("%s (%s)\n", $obj->Name, $obj->CountryCode);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY ID DESC";

$result = mysqli_query($link, $query);

/* получение ассоциативного массива */
while ($obj = mysqli_fetch_object($result)) {
    printf("%s (%s)\n", $obj->Name, $obj->CountryCode);
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
-   [mysqli\_fetch\_row()](mysqli-result.fetch-row.html) - Вибирає наступний рядок із набору результатів і поміщає його у звичайний масив
-   [mysqli\_query()](mysqli.query.html) - Виконує запит до бази даних
-   [mysqli\_data\_seek()](mysqli-result.data-seek.html) - Переміщує покажчик результату на вибраний рядок