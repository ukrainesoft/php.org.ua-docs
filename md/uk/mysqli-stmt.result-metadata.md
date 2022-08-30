Повертає метадані результуючої таблиці запиту, що готується.

-   [« mysqlistmt::reset](mysqli-stmt.reset.html)
    
-   [mysqlistmt::sendlongdata »](mysqli-stmt.send-long-data.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlistmt](class.mysqli-stmt.html)
    
-   Повертає метадані результуючої таблиці запиту, що готується.
    

# mysqlistmt::resultmetadata

# mysqlistmtresultmetadata

(PHP 5, PHP 7, PHP 8)

mysqlistmt::resultmetadata - mysqlistmtresultmetadata — Повертає метадані результуючої таблиці запиту, що готується.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::result_metadata(): mysqli_result|false
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_result_metadata(mysqli_stmt $statement): mysqli_result|false
```

Якщо запит, переданий у [mysqliprepare()](mysqli.prepare.html), генерує результуючу таблицю, **mysqlistmtresultmetadata()** повертає об'єкт, за допомогою якого можна отримати опис цього результуючого набору. Зокрема, можна отримати кількість полів та опис кожного окремого поля.

> **Зауваження**
> 
> Отриманий об'єктний покажчик можна передавати як аргумент функції обробки метаданих результуючих таблиць, як наприклад:
> 
> -   [mysqlinumfields()](mysqli-result.field-count.html)
>     
> -   [mysqlifetchfield()](mysqli-result.fetch-field.html)
>     
> -   [mysqlifetchfielddirect()](mysqli-result.fetch-field-direct.html)
>     
> -   [mysqlifetchfields()](mysqli-result.fetch-fields.html)
>     
> -   [mysqlifieldcount()](mysqli.field-count.html)
>     
> -   [mysqlifieldseek()](mysqli-result.field-seek.html)
>     
> -   [mysqlifieldtell()](mysqli-result.current-field.html)
>     
> -   [mysqlifreeresult()](mysqli-result.free.html)
>     

Після завершення роботи з цим об'єктом пам'ять, яку він займає, необхідно звільнити. Зробити це можна, передавши об'єктний покажчик на функцію [mysqlifreeresult()](mysqli-result.free.html)

> **Зауваження**
> 
> Результуючий набір, що повертається з \*\*mysqlistmtresultmetadata()\*\*містить тільки метадані. У ньому немає рядків вибірки. Результати запиту можна отримати за допомогою функції [mysqlistmtfetch()](mysqli-stmt.fetch.html)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

### Значення, що повертаються

Повертає об'єкт або **`false`** у разі помилки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "test");

$mysqli->query("DROP TABLE IF EXISTS friends");
$mysqli->query("CREATE TABLE friends (id int, name varchar(20))");

$mysqli->query("INSERT INTO friends VALUES (1,'Hartmut'), (2, 'Ulf')");

$stmt = $mysqli->prepare("SELECT id, name FROM friends");
$stmt->execute();

/* получаем результирующий набор метаданных */
$result = $stmt->result_metadata();

/* извлекаем информацию о столбце из метаданных */
$field = $result->fetch_field();

printf("Имя столбца: %s\n", $field->name);

/* закрываем результирующий набор */
$result->close();

/* закрываем подключение */
$mysqli->close();
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "test");

mysqli_query($link, "DROP TABLE IF EXISTS friends");
mysqli_query($link, "CREATE TABLE friends (id int, name varchar(20))");

mysqli_query($link, "INSERT INTO friends VALUES (1,'Hartmut'), (2, 'Ulf')");

$stmt = mysqli_prepare($link, "SELECT id, name FROM friends");
mysqli_stmt_execute($stmt);

/* получаем результирующий набор метаданных */
$result = mysqli_stmt_result_metadata($stmt);

/* извлекаем информацию о столбце из метаданных */
$field = mysqli_fetch_field($result);

printf("Имя столбца: %s\n", $field->name);

/* закрываем результирующий набор */
mysqli_free_result($result);

/* закрываем подключение */
mysqli_close($link);
?>
```

### Дивіться також

-   [mysqliprepare()](mysqli.prepare.html) - готує SQL вираз до виконання
-   [mysqlifreeresult()](mysqli-result.free.html) - звільняє пам'ять, зайняту результатами запиту