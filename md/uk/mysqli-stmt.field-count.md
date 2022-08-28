Повертає кількість стовпців у заданому виразі

-   [« mysqli\_stmt::fetch](mysqli-stmt.fetch.html)
    
-   [mysqli\_stmt::free\_result »](mysqli-stmt.free-result.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli\_stmt](class.mysqli-stmt.html)
    
-   Повертає кількість стовпців у заданому виразі
    

# mysqlistmt::$fieldcount

# mysqlistmtfieldcount

(PHP 5, PHP 7, PHP 8)

mysqlistmt::$fieldcount - mysqlistmtfieldcount — Повертає кількість стовпців у заданому виразі

### Опис

Об'єктно-орієнтований стиль

int [$mysqli\_stmt->field\_count](mysqli-stmt.field-count.html)

Процедурний стиль

```methodsynopsis
mysqli_stmt_field_count(mysqli_stmt $statement): int
```

Повертає кількість стовпців у підготовленому виразі.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.html), отриманий за допомогою [mysqli\_stmt\_init()](mysqli.stmt-init.html)

### Значення, що повертаються

Повертає ціле число, що становить кількість стовпців.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$code = 'FR';

$stmt = $mysqli->prepare("SELECT Name FROM Country WHERE Code=?");
$stmt->bind_param('s', $code);
$stmt->execute();
$row = $stmt->get_result()->fetch_row();
for ($i = 0; $i < $stmt->field_count; $i++) {
    printf("Значение номера столбца %d - %s", $i, $row[$i]);
}
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$code = 'FR';

$stmt = mysqli_prepare($mysqli, "SELECT Name FROM Country WHERE Code=?");
mysqli_stmt_bind_param($stmt, 's', $code);
mysqli_stmt_execute($stmt);
$result = mysqli_stmt_get_result($stmt);
$row = mysqli_fetch_row($result);
for ($i = 0; $i < mysqli_stmt_field_count($stmt); $i++) {
    printf("Значение номера столбца %d - %s", $i, $row[$i]);
}
```

Результатом виконання даних прикладів буде щось подібне:

```
Значение номера столбца 0 - France
```

### Дивіться також

-   [mysqli\_stmt\_num\_rows()](mysqli-stmt.num-rows.html) - Повертає кількість рядків, отриманих із сервера