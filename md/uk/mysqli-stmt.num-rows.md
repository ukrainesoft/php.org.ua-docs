---
navigation:
  - mysqli-stmt.next-result.md: '« mysqli\_stmt::next\_result'
  - mysqli-stmt.param-count.md: 'mysqli\_stmt::$param\_count »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::$num\_rows'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::$num\_rows

# mysqli\_stmt::num\_rows

# mysqli\_stmt\_num\_rows

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::$num\_rows -- mysqli\_stmt::num\_rows -- mysqli\_stmt\_num\_rows — Повертає кількість рядків, отриманих із сервера

### Опис

Об'єктно-орієнтований стиль

int|string[$mysqli\_stmt->num\_rows](mysqli-stmt.num-rows.md)

```methodsynopsis
public mysqli_stmt::num_rows(): int|string
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_num_rows(mysqli_stmt $statement): int|string
```

Повертає кількість рядків, поміщених у буфер у виразі. Функція буде працювати лише після дзвінка [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md) для буферизації всього набору результатів у дескрипторі оператора.

Функція повертає , якщо з сервера не було отримано всі рядки.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Ціле число (int), що становить кількість буферизованих рядків. Повертає у небуферизованому режимі, якщо з сервера не було отримано всі рядки.

> **Зауваження** :
> 
> Якщо кількість рядків більша, ніж **`PHP_INT_MAX`**, число буде повернутий як рядок (string).

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name LIMIT 20";
$stmt = $mysqli->prepare($query);
$stmt->execute();

/* сохранение результата во внутреннем буфере */
$stmt->store_result();

printf("Число строк: %d.\n", $stmt->num_rows);
```

**Приклад #2 Процедурний стиль**

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

$query = "SELECT Name, CountryCode FROM City ORDER BY Name LIMIT 20";
$stmt = mysqli_prepare($link, $query);
mysqli_stmt_execute($stmt);

/* сохранение результата во внутреннем буфере */
mysqli_stmt_store_result($stmt);

printf("Число строк: %d.\n", mysqli_stmt_num_rows($stmt));
```

Результат виконання наведених прикладів:

```
Число строк: 20.
```

### Дивіться також

-   [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md) \- Зберігає набір результатів у внутрішньому буфері
-   [mysqli\_stmt\_affected\_rows()](mysqli-stmt.affected-rows.md) \- Повертає загальну кількість рядків, змінених, віддалених, вставлених чи зіставлених останнім виконаним виразом
-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
