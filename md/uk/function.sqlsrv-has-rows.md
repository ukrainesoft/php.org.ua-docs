Вказує, чи є у вказаного оператора рядки

-   [« sqlsrvgetfield](function.sqlsrv-get-field.html)
    
-   [sqlsrvnextresult »](function.sqlsrv-next-result.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SQLSRV](ref.sqlsrv.html)
    
-   Вказує, чи є у вказаного оператора рядки
    

# sqlsrvhasrows

(No version information available, might only be in Git)

sqlsrvhasrows — Вказує, чи є вказаний оператор рядка

### Опис

```methodsynopsis
sqlsrv_has_rows(resource $stmt): bool
```

Вказує, чи має вказаний оператор рядка.

### Список параметрів

`stmt`

Ресурс оператора, що повертається [sqlsrvquery()](function.sqlsrv-query.html) або [sqlsrvexecute()](function.sqlsrv-execute.html)

### Значення, що повертаються

Повертає **`true`**, якщо у вказаному операторі є рядки та **`false`**, якщо в операторі немає рядків або виникла помилка.

### Приклади

**Приклад #1 Приклад використання **sqlsrvhasrows()****

```php
<?php
$server = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $server, $connectionInfo );

$stmt = sqlsrv_query( $conn, "SELECT * FROM Table_1");

if ($stmt) {
   $rows = sqlsrv_has_rows( $stmt );
   if ($rows === true)
      echo "Есть строки. <br />";
   else
      echo "Нет строк. <br />";
}
?>
```

### Дивіться також

-   [sqlsrvnumrows()](function.sqlsrv-num-rows.html) - Отримує кількість рядків у наборі результатів
-   [sqlsrvquery()](function.sqlsrv-query.html) - готує та виконує запит