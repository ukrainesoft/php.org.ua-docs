---
navigation:
  - function.sqlsrv-next-result.md: « sqlsrv\_next\_result
  - function.sqlsrv-num-rows.md: sqlsrv\_num\_rows »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_num\_fields
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_num\_fields

(No version information available, might only be in Git)

sqlsrv\_num\_fields — Витягує кількість полів (стовпців) оператора

### Опис

```methodsynopsis
sqlsrv_num_fields(resource $stmt): mixed
```

Витягує кількість полів (стовпців) оператора.

### Список параметрів

`stmt`

Оператор, для якого повертається кількість полів . **sqlsrv\_num\_fields()** може викликатися оператора до або після виконання оператора.

### Значення, що повертаються

У разі успішного виконання повертає кількість полів. В іншому випадку повертає **`false`**

### Приклади

**Пример #1 Пример использования**sqlsrv\_num\_fields()\*\*\*\*

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
   die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT * FROM Table_1";
$stmt = sqlsrv_query($conn, $sql);
if( $stmt === false) {
   die( print_r( sqlsrv_errors(), true));
}

$numFields = sqlsrv_num_fields( $stmt );

while( sqlsrv_fetch( $stmt )) {
   // Пройдитесь по полям каждой строки.
   for($i = 0; $i < $numFields; $i++) {
      echo sqlsrv_get_field($stmt, $i)." ";
   }
   echo "<br />";
}
?>
```

### Дивіться також

-   [sqlsrv\_field\_metadata()](function.sqlsrv-field-metadata.md) \- Отримує метадані для полів оператора, підготовленого за допомогою sqlsrv\_prepare або sqlsrv\_query
-   [sqlsrv\_fetch()](function.sqlsrv-fetch.md) \- Робить наступний рядок у наборі результатів доступного для читання
-   [sqlsrv\_get\_field()](function.sqlsrv-get-field.md) \- Отримує дані поля з поточного вибраного рядка
