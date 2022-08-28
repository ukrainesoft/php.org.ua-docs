Екранування спеціальних символів у SQL-запиті

-   [« cubrid\_query](function.cubrid-query.html)
    
-   [cubrid\_result »](function.cubrid-result.html)
    
-   [PHP Manual](index.html)
    
-   [Функции совместимости CUBRID MySQL](cubridmysql.cubrid.html)
    
-   Екранування спеціальних символів у SQL-запиті
    

# cubridrealescapestring

(PECL CUBRID >= 8.3.0)

cubridrealescapestring — Екранування спеціальних символів у SQL-запиті

### Опис

```methodsynopsis
cubrid_real_escape_string(string $unescaped_string, resource $conn_identifier = ?): string
```

Функція повертає екрановану версію переданого рядка. Вона екранує символи: **`'`**. Загалом одинарна лапка використовується для обгортання символьного рядка. Також можна використовувати подвійні лапки, залежно від значення ansiquotes. Якщо ansiquotes встановлено в "no", то рядок обгорнутий у подвійні лапки буде розглядатися як рядок символів, а не як ідентифікатор. Значення за промовчанням - "yes". Якщо ви хочете використовувати одинарну лапку як частину рядка - поставте дві одинарні лапки поспіль.

### Список параметрів

`unescaped_string`

Рядок, який необхідно екранувати

`conn_identifier`

Ідентифікатор з'єднання CUBRID. Якщо не встановлено, то буде використано останнє з'єднання, повернене [cubrid\_connect()](function.cubrid-connect.html)

### Значення, що повертаються

Екранований рядок.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridrealescapestring()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$unescaped_str = ' !"#$%&\'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~';
$escaped_str = cubrid_real_escape_string($unescaped_str);

$len = strlen($unescaped_str);

@cubrid_execute($conn, "DROP TABLE cubrid_test");
cubrid_execute($conn, "CREATE TABLE cubrid_test (t char($len))");
cubrid_execute($conn, "INSERT INTO cubrid_test (t) VALUES('$escaped_str')");

$req = cubrid_execute($conn, "SELECT * FROM cubrid_test");
$row = cubrid_fetch_assoc($req);

var_dump($row);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
array(1) {
  ["t"]=>
  string(95) " !"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~"
}
```