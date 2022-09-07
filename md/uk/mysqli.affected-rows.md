---
navigation:
  - class.mysqli.md: « mysqli
  - mysqli.autocommit.md: 'mysqli::autocommit »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$affectedrows'
---
# mysqli::$affectedrows

# mysqliaffectedrows

(PHP 5, PHP 7, PHP 8)

mysqli::$affectedrows - mysqliaffectedrows — Отримує кількість рядків, які стосуються попередньої операції MySQL

### Опис

Об'єктно-орієнтований стиль

int|string [$mysqli->affectedrows](mysqli.affected-rows.md)

Процедурний стиль

```methodsynopsis
mysqli_affected_rows(mysqli $mysql): int|string
```

Повертає кількість рядків, які торкнулися останнім запитом `INSERT` `UPDATE` `REPLACE` або `DELETE`. Працює аналогічно [mysqlinumrows()](mysqli-result.num-rows.md) для виразів `SELECT`

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Ціле число, більше нуля, означає кількість порушених чи отриманих рядків. Нуль означає, що записи для оператора `UPDATE` не оновлювалися, жодний рядок не відповідав виразу `WHERE` у запиті або що жодного запиту ще не було виконано . `-1` означає, що під час виконання запиту сталася помилка або що **mysqliaffectedrows()** була викликана для небуферизованого запиту `SELECT`

> **Зауваження**
> 
> Якщо число порушених рядків більше, ніж максимальне значення цілого числа (**`PHP_INT_MAX`**), то число порушених рядків буде повернено у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання $mysqli->affectedrows**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Добавление строк */
$mysqli->query("CREATE TABLE Language SELECT * from CountryLanguage");
printf("Затронутые строки (INSERT): %d\n", $mysqli->affected_rows);

$mysqli->query("ALTER TABLE Language ADD Status int default 0");

/* Обновление строк */
$mysqli->query("UPDATE Language SET Status=1 WHERE Percentage > 50");
printf("Затронутые строки (UPDATE): %d\n", $mysqli->affected_rows);

/* Удаление строк */
$mysqli->query("DELETE FROM Language WHERE Percentage < 50");
printf("Затронутые строки (DELETE): %d\n", $mysqli->affected_rows);

/* Выборка всех строк */
$result = $mysqli->query("SELECT CountryCode FROM Language");
printf("Затронутые строки (SELECT): %d\n", $mysqli->affected_rows);

/* Удаление таблицы Language */
$mysqli->query("DROP TABLE Language");
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Добавление строк */
mysqli_query($link, "CREATE TABLE Language SELECT * from CountryLanguage");
printf("Затронутые строки (INSERT): %d\n", mysqli_affected_rows($link));

mysqli_query($link, "ALTER TABLE Language ADD Status int default 0");

/* Обновление строк */
mysqli_query($link, "UPDATE Language SET Status=1 WHERE Percentage > 50");
printf("Затронутые строки (UPDATE): %d\n", mysqli_affected_rows($link));

/* Удаление строк */
mysqli_query($link, "DELETE FROM Language WHERE Percentage < 50");
printf("Затронутые строки (DELETE): %d\n", mysqli_affected_rows($link));

/* Выборка всех строк */
$result = mysqli_query($link, "SELECT CountryCode FROM Language");
printf("Затронутые строки (SELECT): %d\n", mysqli_affected_rows($link));

/* Удаление таблицы Language */
mysqli_query($link, "DROP TABLE Language");
?>
```

Результат виконання даних прикладів:

```
Затронутые строки (INSERT): 984
Затронутые строки (UPDATE): 168
Затронутые строки (DELETE): 815
Затронутые строки (SELECT): 169
```

### Дивіться також

-   [mysqlinumrows()](mysqli-result.num-rows.md) - Отримує кількість рядків у наборі результатів
-   [mysqliinfo()](mysqli.info.md) - Витягує інформацію про останній виконаний запит
