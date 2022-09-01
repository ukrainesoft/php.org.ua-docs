---
navigation:
  - class.mysqli-stmt.html: « mysqlistmt
  - mysqli-stmt.attr-get.html: 'mysqlistmt::attrget »'
  - index.md: PHP Manual
  - class.mysqli-stmt.html: mysqlistmt
title: 'mysqlistmt::$affectedrows'
---
# mysqlistmt::$affectedrows

# mysqlistmtaffectedrows

(PHP 5, PHP 7, PHP 8)

mysqlistmt::$affectedrows - mysqlistmtaffectedrows - Повертає загальну кількість рядків, змінених, віддалених, вставлених або зіставлених останнім виконаним виразом

### Опис

Об'єктно-орієнтований стиль

int|string [$mysqlistmt->affectedrows](mysqli-stmt.affected-rows.html)

Процедурний стиль

```methodsynopsis
mysqli_stmt_affected_rows(mysqli_stmt $statement): int|string
```

Повертає кількість рядків, змінених запитом `INSERT` `UPDATE` або `DELETE`. Працює аналогічно [mysqlistmtnumrows()](mysqli-stmt.num-rows.html) для виразів `SELECT`

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Ціле число більше за нуль вказує кількість порушених або вилучених рядків. Нуль означає, що записи для оператора `UPDATE` не оновлювалися, жодний рядок не відповідав виразу `WHERE` у запиті або що жодного запиту ще не було виконано . `-1` означає, що під час виконання запиту сталася помилка або для запиту `SELECT` **mysqlistmtaffectedrows()** була викликана до виклику [mysqlistmtstoreresult()](mysqli-stmt.store-result.html)

> **Зауваження**
> 
> Якщо кількість змінених рядків більша за максимальне значення для цілого числа в PHP, то ця кількість буде повернена у вигляді рядкового значення.

### Приклади

**Приклад #1 Приклад використання **mysqlistmtaffectedrows()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* создание временной таблицы */
$mysqli->query("CREATE TEMPORARY TABLE myCountry LIKE Country");

$query = "INSERT INTO myCountry SELECT * FROM Country WHERE Code LIKE ?";

/* подготовка выражения */
$stmt = $mysqli->prepare($query);

/* связывание переменных */
$code = 'A%';
$stmt->bind_param("s", $code);

/* выполнение выражения */
$stmt->execute();

printf("Добавлено строк: %d\n", $stmt->affected_rows);
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* создание временной таблицы */
mysqli_query($link, "CREATE TEMPORARY TABLE myCountry LIKE Country");

$query = "INSERT INTO myCountry SELECT * FROM Country WHERE Code LIKE ?";

/* подготовка выражения */
$stmt = mysqli_prepare($link, $query);

/* связывание переменных */
$code = 'A%';
mysqli_stmt_bind_param($stmt, "s", $code);

/* выполнение выражения */
mysqli_stmt_execute($stmt);

printf("Добавлено строк: %d\n", mysqli_stmt_affected_rows($stmt));
?>
```

Результат виконання даних прикладів:

```
Добавлено строк: 17
```

### Дивіться також

-   [mysqlistmtnumrows()](mysqli-stmt.num-rows.html) - Повертає кількість рядків, отриманих із сервера
-   [mysqlistmtstoreresult()](mysqli-stmt.store-result.html) - Зберігає набір результатів у внутрішньому буфері
