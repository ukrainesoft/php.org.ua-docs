---
navigation:
  - mysqli-result.fetch-assoc.md: '« mysqli\_result::fetch\_assoc'
  - mysqli-result.fetch-field-direct.md: 'mysqli\_result::fetch\_field\_direct »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::fetch\_column'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::fetch\_column

# mysqli\_fetch\_column

(PHP 8 >= 8.1.0)

mysqli\_result::fetch\_column -- mysqli\_fetch\_column — Отримує один стовпець з наступного рядка набору результатів

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::fetch_column(int $column = 0): null|int|float|string|false
```

Процедурний стиль

```methodsynopsis
mysqli_fetch_column(mysqli_result $result, int $column = 0): null|int|float|string|false
```

Вибирає один рядок даних із набору результатів і повертає стовпець із зазначеним індексом, починаючи з 0. Кожен наступний виклик цієї функції повертатиме значення з наступного рядка у наборі результатів або \*\*`false`\*\*якщо рядків більше немає.

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

`column`

Номер стовпця, починаючи з 0, який потрібно витягти з рядка. Якщо значення не вказано, буде повернено перший стовпець.

### Значення, що повертаються

Повертає один стовпець з наступного рядка набору результатів або \*\*`false`\*\*якщо рядків більше немає.

**Увага**

Неможливо повернути інший стовпець з того ж рядка, якщо ви використовуєте цю функцію для отримання даних.

### Приклади

**Приклад #1 Приклад використання** mysqli\_result::fetch\_column()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");
$query = "SELECT CountryCode, Name FROM City ORDER BY ID DESC LIMIT 5";
$result = $mysqli->query($query);
/* получение значения из второго столбца */
while ($Name = $result->fetch_column(1)) {
    printf("%s\n", $Name);
}
```

Процедурний стиль

```php
<?php
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");
$query = "SELECT CountryCode, Name FROM City ORDER BY ID DESC LIMIT 5";
$result = mysqli_query($mysqli, $query);
/* получение значения из второго столбца */
while ($Name = mysqli_fetch_column($result, 1)) {
    printf("%s\n", $Name);
}
```

Висновок наведених прикладів буде схожим на:

```
Rafah
Nablus
Jabaliya
Hebron
Khan Yunis
```

### Дивіться також

-   [mysqli\_fetch\_all()](mysqli-result.fetch-all.md) \- Вибирає всі рядки з результуючого набору і поміщає їх в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_fetch\_array()](mysqli-result.fetch-array.md) \- Вибирає наступний рядок з набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_fetch\_assoc()](mysqli-result.fetch-assoc.md) \- Вибирає наступний рядок із набору результатів та поміщає його в асоціативний масив
-   [mysqli\_fetch\_object()](mysqli-result.fetch-object.md) \- Вибирає наступний рядок із набору результатів у вигляді об'єкта
-   [mysqli\_fetch\_row()](mysqli-result.fetch-row.md) \- Вибирає наступний рядок із набору результатів і поміщає його у звичайний масив
-   [mysqli\_data\_seek()](mysqli-result.data-seek.md) \- Переміщує покажчик результату на вибраний рядок
