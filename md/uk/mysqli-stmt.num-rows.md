---
navigation:
  - mysqli-stmt.next-result.html: '« mysqlistmt::nextresult'
  - mysqli-stmt.param-count.html: 'mysqlistmt::$paramcount »'
  - index.md: PHP Manual
  - class.mysqli-stmt.html: mysqlistmt
title: 'mysqlistmt::$numrows'
---
# mysqlistmt::$numrows

# mysqlistmt::numrows

# mysqlistmtnumrows

(PHP 5, PHP 7, PHP 8)

mysqlistmt::$numrows - mysqlistmt::numrows - mysqlistmtnumrows — Повертає кількість рядків, отриманих із сервера

### Опис

Об'єктно-орієнтований стиль

int|string [$mysqlistmt->numrows](mysqli-stmt.num-rows.html)

```methodsynopsis
public mysqli_stmt::num_rows(): int|string
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_num_rows(mysqli_stmt $statement): int|string
```

Повертає кількість рядків, поміщених у буфер у виразі. Функція працюватиме лише після виклику [mysqlistmtstoreresult()](mysqli-stmt.store-result.html) для буферизації всього набору результатів у дескрипторі оператора.

Функція повертає `0`, якщо з сервера не було отримано всі рядки.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Ціле число (int), що становить кількість буферизованих рядків. Повертає `0` у небуферизованому режимі, якщо з сервера не було отримано всі рядки.

> **Зауваження**
> 
> Якщо кількість рядків більша, ніж **`PHP_INT_MAX`**, число буде повернутий як рядок (string).

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name LIMIT 20";
$stmt = $mysqli->prepare($query);
$stmt->execute();

/* сохранение результата во внутреннем буфере */
$stmt->store_result();

printf("Число строк: %d.\n", $stmt->num_rows);
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name LIMIT 20";
$stmt = mysqli_prepare($link, $query);
mysqli_stmt_execute($stmt);

/* сохранение результата во внутреннем буфере */
mysqli_stmt_store_result($stmt);

printf("Число строк: %d.\n", mysqli_stmt_num_rows($stmt));
```

Результат виконання даних прикладів:

```
Число строк: 20.
```

### Дивіться також

-   [mysqlistmtstoreresult()](mysqli-stmt.store-result.html) - Зберігає набір результатів у внутрішньому буфері
-   [mysqlistmtaffectedrows()](mysqli-stmt.affected-rows.html) - Повертає загальну кількість рядків, змінених, віддалених, вставлених чи зіставлених останнім виконаним виразом
-   [mysqliprepare()](mysqli.prepare.md) - готує SQL вираз до виконання
