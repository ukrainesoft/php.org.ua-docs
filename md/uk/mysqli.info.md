---
navigation:
  - mysqli.get-warnings.md: '« mysqli::getwarnings'
  - mysqli.init.md: 'mysqli::init »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$info'
---
# mysqli::$info

# mysqliinfo

(PHP 5, PHP 7, PHP 8)

mysqli::$info -- mysqliinfo — Витягує інформацію про останній виконаний запит

### Опис

Об'єктно-орієнтований стиль

?string [$mysqli->info](mysqli.info.md)

Процедурний стиль

```methodsynopsis
mysqli_info(mysqli $mysql): ?string
```

Функція **mysqliinfo()** повертає рядок з інформацією про останній запит до бази даних. Опис рядка наведено нижче:

**Можливі значення, що повертаються mysqliinfo**

| Тип запроса | Пример результирующей строки |
| --- | --- |
| INSERT INTO...SELECT... | Records: 100 Duplicates: 0 Warnings: 0 |
| INSERT INTO...VALUES (...),(...),(...) | Records: 3 Duplicates: 0 Warnings: 0 |
| LOAD DATA INFILE ... | Records: 1 Deleted: 0 Skipped: 0 Warnings: 0 |
| ALTER TABLE ... | Records: 3 Duplicates: 0 Warnings: 0 |
| UPDATE ... | Rows matched: 40 Changed: 40 Warnings: 0 |

> **Зауваження**
> 
> Запити, які не потрапляють до списку, не підтримуються. У таких ситуаціях **mysqliinfo()** поверне порожній рядок.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Рядок символів представляє додаткову інформацію про останній запущений запит.

### Приклади

**Приклад #1 Приклад використання $mysqli->info**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$mysqli->query("CREATE TEMPORARY TABLE t1 LIKE City");

/* INSERT INTO ... SELECT */
$mysqli->query("INSERT INTO t1 SELECT * FROM City ORDER BY ID LIMIT 150");
printf("%s\n", $mysqli->info);

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

mysqli_query($link, "CREATE TEMPORARY TABLE t1 LIKE City");

/* INSERT INTO ... SELECT */
mysqli_query($link, "INSERT INTO t1 SELECT * FROM City ORDER BY ID LIMIT 150");
printf("%s\n", mysqli_info($link));

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Records: 150  Duplicates: 0  Warnings: 0
```

### Дивіться також

-   [mysqliaffectedrows()](mysqli.affected-rows.md) - Отримує кількість рядків, порушених попередньою операцією MySQL
-   [mysqliwarningcount()](mysqli.warning-count.md) - Повертає кількість попереджень із останнього запиту заданого підключення
-   [mysqlinumrows()](mysqli-result.num-rows.md) - Отримує кількість рядків у наборі результатів
