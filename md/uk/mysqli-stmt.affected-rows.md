---
navigation:
  - class.mysqli-stmt.md: « mysqli\_stmt
  - mysqli-stmt.attr-get.md: 'mysqli\_stmt::attr\_get »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::$affected\_rows'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::$affected\_rows

# mysqli\_stmt\_affected\_rows

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::$affected\_rows -- mysqli\_stmt\_affected\_rows - Повертає загальну кількість рядків, змінених, віддалених, вставлених або зіставлених останнім виконаним виразом

### Опис

Об'єктно-орієнтований стиль

int|string[$mysqli\_stmt->affected\_rows](mysqli-stmt.affected-rows.md)

Процедурний стиль

```methodsynopsis
mysqli_stmt_affected_rows(mysqli_stmt $statement): int|string
```

Повертає кількість рядків, змінених запитом `INSERT` `UPDATE`или`DELETE`. Працює аналогічно [mysqli\_stmt\_num\_rows()](mysqli-stmt.num-rows.md) для виразів `SELECT`

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Ціле число більше за нуль вказує кількість порушених або витягнутих рядків. Нуль означає, що записи для оператора `UPDATE` не оновлювалися, жодний рядок не відповідав виразу `WHERE` у запиті або що жодного запиту ще не було виконано . `-1` означає, що під час виконання запиту сталася помилка або для запиту `SELECT` **mysqli\_stmt\_affected\_rows()** була викликана до виклику [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md)

> **Зауваження** :
> 
> Якщо кількість змінених рядків більша за максимальне значення для цілого числа в PHP, то ця кількість буде повернена у вигляді рядкового значення.

### Приклади

**Приклад #1 Приклад використання** mysqli\_stmt\_affected\_rows()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* создание временной таблицы */
$mysqli->query("CREATE TEMPORARY TABLE myCountry LIKE Country");

$query = "INSERT INTO myCountry SELECT * FROM Country WHERE Code LIKE ?";

/* подготовка выражения */
$stmt = $mysqli->prepare($query);

/* связывание переменных */
$code = 'A%';
$stmt->bind_param("s", $code);

/* выполнение выражения */
$stmt->execute();

printf("Добавлено строк: %d\n", $stmt->affected_rows);
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* создание временной таблицы */
mysqli_query($link, "CREATE TEMPORARY TABLE myCountry LIKE Country");

$query = "INSERT INTO myCountry SELECT * FROM Country WHERE Code LIKE ?";

/* подготовка выражения */
$stmt = mysqli_prepare($link, $query);

/* связывание переменных */
$code = 'A%';
mysqli_stmt_bind_param($stmt, "s", $code);

/* выполнение выражения */
mysqli_stmt_execute($stmt);

printf("Добавлено строк: %d\n", mysqli_stmt_affected_rows($stmt));
?>
```

Результат виконання наведених прикладів:

```
Добавлено строк: 17
```

### Дивіться також

-   [mysqli\_stmt\_num\_rows()](mysqli-stmt.num-rows.md) \- Повертає кількість рядків, отриманих із сервера
-   [mysqli\_stmt\_store\_result()](mysqli-stmt.store-result.md) \- Зберігає набір результатів у внутрішньому буфері
