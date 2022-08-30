Підготовляє SQL-вираз до виконання

-   [« cubridpconnect](function.cubrid-pconnect.html)
    
-   [cubridput »](function.cubrid-put.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Підготовляє SQL-вираз до виконання
    

# cubridprepare

(PECL CUBRID >= 8.3.0)

cubridprepare — Підготовка SQL-виразу до виконання

### Опис

```methodsynopsis
cubrid_prepare(resource $conn_identifier, string $prepare_stmt, int $option = 0): resource
```

Функція **cubridprepare()** - це свого роду API, який представляє вирази SQL, раніше скомпільовані для даного дескриптора з'єднання. Цей попередньо скомпільований SQL-вираз буде включений у функцію **cubridprepare()**

Відповідно, ви можете ефективно використовувати цей оператор для багаторазового виконання або обробки великих даних. Можна використовувати лише один оператор, а в параметрі можна вказати знак запитання (?) у відповідну область SQL-виразу. Додайте параметр при прив'язці значення у VALUES виразу INSERT або WHERE. Зверніть увагу, що можна прив'язати значення до знака запитання (?) тільки за допомогою функції [cubridbind()](function.cubrid-bind.html)

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`prepare_stmt`

Підготовлений запит.

`option`

Опція повернення OID **`CUBRID_INCLUDE_OID`**

### Значення, що повертаються

Ідентифікатор запиту у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridprepare()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$sql = <<<EOD
SELECT g.event_code, e.name
FROM game g
JOIN event e ON g.event_code=e.code
WHERE host_year = ? AND event_code NOT IN (SELECT event_code FROM game WHERE host_year=?) GROUP BY event_code;
EOD;

$req = cubrid_prepare($conn, $sql);

cubrid_bind($req, 1, 2004);
cubrid_bind($req, 2, 2000);
cubrid_execute($req);

$row_num = cubrid_num_rows($req);
printf("%d соревнований пройдут на олимпиаде 2004, но не в 2000. Например:\n\n", $row_num);

printf("%-15s %s\n", "Код соревнования", "Название");
printf("----------------------------\n");

$row = cubrid_fetch_assoc($req);
printf("%-15d %s\n", $row["event_code"], $row["name"]);
$row = cubrid_fetch_assoc($req);
printf("%-15d %s\n", $row["event_code"], $row["name"]);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
27 соревнований пройдут на олимпиаде 2004, но не в 2000. Например:

Код соревнования   Название
----------------------------
20063           +91kg
20070           64kg
```

### Дивіться також

-   [cubridexecute()](function.cubrid-execute.html) - Виконує підготовлений SQL-оператор
-   [cubridbind()](function.cubrid-bind.html) - пов'язує змінні з підготовленим запитом