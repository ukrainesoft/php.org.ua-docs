Отримує метадані для полів оператора, підготовленого за допомогою sqlsrvprepare або sqlsrvquery

-   [« sqlsrvfetch](function.sqlsrv-fetch.html)
    
-   [sqlsrvfreestmt »](function.sqlsrv-free-stmt.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SQLSRV](ref.sqlsrv.md)
    
-   Отримує метадані для полів оператора, підготовленого за допомогою sqlsrvprepare або sqlsrvquery
    

# sqlsrvfieldmetadata

(No version information available, might only be in Git)

sqlsrvfieldmetadata — Отримує метадані для полів оператора, підготовленого за допомогою [sqlsrvprepare()](function.sqlsrv-prepare.html) або [sqlsrvquery()](function.sqlsrv-query.html)

### Опис

```methodsynopsis
sqlsrv_field_metadata(resource $stmt): mixed
```

Отримує метадані для полів оператора, підготовленого за допомогою [sqlsrvprepare()](function.sqlsrv-prepare.html) або [sqlsrvquery()](function.sqlsrv-query.html). . **sqlsrvfieldmetadata()** може викликатися оператора до або після виконання оператора.

### Список параметрів

`stmt`

Ресурс оператора, для якого повертаються метадані.

### Значення, що повертаються

У разі успішного виконання повертає масив масивів. В іншому випадку повертає **`false`**. Кожен масив, що повертається, описується наступною таблицею:

**Масив, що повертається sqlsrvfieldmetadata**

| Ключ | Описание |
| --- | --- |
| Name | Ім'я поля. |
| Type | Числове значення для типу SQL. |
| Size | Кількість символів для полів символьного типу, кількість байтів для полів двійкового типу або **`null`** для інших типів. |
| Precision | Точність для типів змінної точності, **`null`** для інших типів. |
| Scale | Масштаб для типів масштабованих типів даних, **`null`** для інших типів. |
| Nullable | Перелік, що вказує, чи стовпець допускає значення NULL, неприпустиме значення NULL або невідоме. |

Для отримання додаткової інформації дивіться [» sqlsrvfieldmetadata](http://msdn.microsoft.com/en-us/library/cc296197.aspx) у документації Microsoft SQLSRV.

### Приклади

**Приклад #1 Приклад використання **sqlsrvfieldmetadata()****

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"AdventureWorks", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
   die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT * FROM Table_1";
$stmt = sqlsrv_prepare( $conn, $sql );

foreach( sqlsrv_field_metadata( $stmt ) as $fieldMetadata ) {
    foreach( $fieldMetadata as $name => $value) {
       echo "$name: $value<br />";
    }
      echo "<br />";
}
?>
```

### Дивіться також

-   [sqlsrvclientinfo()](function.sqlsrv-client-info.html) - Повертає інформацію про клієнта та зазначене підключення