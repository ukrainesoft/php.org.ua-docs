Витягує кількість полів (стовпців) оператора

-   [« sqlsrv\_next\_result](function.sqlsrv-next-result.html)
    
-   [sqlsrv\_num\_rows »](function.sqlsrv-num-rows.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SQLSRV](ref.sqlsrv.html)
    
-   Витягує кількість полів (стовпців) оператора
    

# sqlsrvnumfields

(No version information available, might only be in Git)

sqlsrvnumfields — Витягує кількість полів (стовпців) оператора

### Опис

```methodsynopsis
sqlsrv_num_fields(resource $stmt): mixed
```

Витягує кількість полів (стовпців) оператора.

### Список параметрів

`stmt`

Оператор, для якого повертається кількість полів . **sqlsrvnumfields()** може викликатися оператора до або після виконання оператора.

### Значення, що повертаються

У разі успішного виконання повертає кількість полів. В іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **sqlsrvnumfields()****

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
   die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT * FROM Table_1";
$stmt = sqlsrv_query($conn, $sql);
if( $stmt === false) {
   die( print_r( sqlsrv_errors(), true));
}

$numFields = sqlsrv_num_fields( $stmt );

while( sqlsrv_fetch( $stmt )) {
   // Пройдитесь по полям каждой строки.
   for($i = 0; $i < $numFields; $i++) {
      echo sqlsrv_get_field($stmt, $i)." ";
   }
   echo "<br />";
}
?>
```

### Дивіться також

-   [sqlsrv\_field\_metadata()](function.sqlsrv-field-metadata.html) - Отримує метадані для полів оператора, підготовленого за допомогою sqlsrvprepare або sqlsrvquery
-   [sqlsrv\_fetch()](function.sqlsrv-fetch.html) - Робить наступний рядок у наборі результатів доступного для читання
-   [sqlsrv\_get\_field()](function.sqlsrv-get-field.html) - Отримує дані поля з поточного вибраного рядка