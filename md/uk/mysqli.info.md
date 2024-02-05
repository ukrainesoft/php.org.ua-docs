---
navigation:
  - mysqli.get-warnings.md: '« mysqli::get\_warnings'
  - mysqli.init.md: 'mysqli::init »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$info'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$info

# mysqli\_info

(PHP 5, PHP 7, PHP 8)

mysqli::$info -- mysqli\_info — Витягує інформацію про останній виконаний запит

### Опис

Об'єктно-орієнтований стиль

?string[$mysqli->info](mysqli.info.md)

Процедурний стиль

```methodsynopsis
mysqli_info(mysqli $mysql): ?string
```

Функция**mysqli\_info()** повертає рядок з інформацією про останній виконаний запит до бази даних. Опис рядка наведено нижче:

**Можливі значення, що повертаються mysqli\_info**

| Тип запроса | Приклад результирующей строки |
| --- | --- |
| INSERT INTO...SELECT... | Records: 100 Duplicates: 0 Warnings: 0 |
| INSERT INTO...VALUES (...),(...),(...) | Records: 3 Duplicates: 0 Warnings: 0 |
| LOAD DATA INFILE ... | Records: 1 Deleted: 0 Skipped: 0 Warnings: 0 |
| ALTER TABLE ... | Records: 3 Duplicates: 0 Warnings: 0 |
| UPDATE ... | Rows matched: 40 Changed: 40 Warnings: 0 |

> **Зауваження** :
> 
> Запити, які не потрапляють до списку, не підтримуються. У таких ситуаціях **mysqli\_info()** поверне порожній рядок.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Рядок символів представляє додаткову інформацію про останній запущений запит.

### Приклади

**Приклад #1 Приклад використання $mysqli->info**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$mysqli->query("CREATE TEMPORARY TABLE t1 LIKE City");

/* INSERT INTO ... SELECT */
$mysqli->query("INSERT INTO t1 SELECT * FROM City ORDER BY ID LIMIT 150");
printf("%s\n", $mysqli->info);
?>
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

mysqli_query($link, "CREATE TEMPORARY TABLE t1 LIKE City");

/* INSERT INTO ... SELECT */
mysqli_query($link, "INSERT INTO t1 SELECT * FROM City ORDER BY ID LIMIT 150");
printf("%s\n", mysqli_info($link));
?>
```

Результат виконання наведених прикладів:

```
Records: 150  Duplicates: 0  Warnings: 0
```

### Дивіться також

-   [mysqli\_affected\_rows()](mysqli.affected-rows.md) \- Отримує кількість рядків, порушених попередньою операцією MySQL
-   [mysqli\_warning\_count()](mysqli.warning-count.md) \- Повертає кількість попереджень із останнього запиту заданого підключення
-   [mysqli\_num\_rows()](mysqli-result.num-rows.md) \- Отримує кількість рядків у наборі результатів
