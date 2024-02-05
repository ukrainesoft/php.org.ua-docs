---
navigation:
  - mysqli-stmt.reset.md: '« mysqli\_stmt::reset'
  - mysqli-stmt.send-long-data.md: 'mysqli\_stmt::send\_long\_data »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::result\_metadata'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::result\_metadata

# mysqli\_stmt\_result\_metadata

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::result\_metadata -- mysqli\_stmt\_result\_metadata — Повертає метадані результуючої таблиці запиту, що готується.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::result_metadata(): mysqli_result|false
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_result_metadata(mysqli_stmt $statement): mysqli_result|false
```

Якщо запит, переданий у [mysqli\_prepare()](mysqli.prepare.md), генерирует результирующую таблицу,**mysqli\_stmt\_result\_metadata()** повертає об'єкт, за допомогою якого можна отримати опис цього результуючого набору. Зокрема, можна отримати кількість полів та опис кожного окремого поля.

> **Зауваження** :
> 
> Отриманий об'єктний покажчик можна передавати як аргумент у функції обробки метаданих результуючих таблиць, як:
> 
> -   [mysqli\_num\_fields()](mysqli-result.field-count.md)
>     
> -   [mysqli\_fetch\_field()](mysqli-result.fetch-field.md)
>     
> -   [mysqli\_fetch\_field\_direct()](mysqli-result.fetch-field-direct.md)
>     
> -   [mysqli\_fetch\_fields()](mysqli-result.fetch-fields.md)
>     
> -   [mysqli\_field\_count()](mysqli.field-count.md)
>     
> -   [mysqli\_field\_seek()](mysqli-result.field-seek.md)
>     
> -   [mysqli\_field\_tell()](mysqli-result.current-field.md)
>     
> -   [mysqli\_free\_result()](mysqli-result.free.md)
>     

Після завершення роботи з цим об'єктом пам'ять, яку він займає, необхідно звільнити. Зробити це можна, передавши об'єктний покажчик на функцію [mysqli\_free\_result()](mysqli-result.free.md)

> **Зауваження** :
> 
> Результуючий набір, що повертається з \*\*mysqli\_stmt\_result\_metadata()\*\*містить тільки метадані. У ньому немає рядків вибірки. Результати запиту можна отримати за допомогою функції [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає об'єкт або \*\*`false`\*\*случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "test");

$mysqli->query("DROP TABLE IF EXISTS friends");
$mysqli->query("CREATE TABLE friends (id int, name varchar(20))");

$mysqli->query("INSERT INTO friends VALUES (1,'Hartmut'), (2, 'Ulf')");

$stmt = $mysqli->prepare("SELECT id, name FROM friends");
$stmt->execute();

/* получаем результирующий набор метаданных */
$result = $stmt->result_metadata();

/* извлекаем информацию о столбце из метаданных */
$field = $result->fetch_field();

printf("Имя столбца: %s\n", $field->name);

/* закрываем результирующий набор */
$result->close();

/* закрываем подключение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "test");

mysqli_query($link, "DROP TABLE IF EXISTS friends");
mysqli_query($link, "CREATE TABLE friends (id int, name varchar(20))");

mysqli_query($link, "INSERT INTO friends VALUES (1,'Hartmut'), (2, 'Ulf')");

$stmt = mysqli_prepare($link, "SELECT id, name FROM friends");
mysqli_stmt_execute($stmt);

/* получаем результирующий набор метаданных */
$result = mysqli_stmt_result_metadata($stmt);

/* извлекаем информацию о столбце из метаданных */
$field = mysqli_fetch_field($result);

printf("Имя столбца: %s\n", $field->name);

/* закрываем результирующий набор */
mysqli_free_result($result);

/* закрываем подключение */
mysqli_close($link);
?>
```

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_free\_result()](mysqli-result.free.md) \- звільняє пам'ять, зайняту результатами запиту
