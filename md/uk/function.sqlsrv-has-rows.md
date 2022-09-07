---
navigation:
  - function.sqlsrv-get-field.md: « sqlsrvgetfield
  - function.sqlsrv-next-result.md: sqlsrvnextresult »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrvhasrows
---
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

Ресурс оператора, що повертається [sqlsrvquery()](function.sqlsrv-query.md) або [sqlsrvexecute()](function.sqlsrv-execute.md)

### Значення, що повертаються

Повертає **`true`**, якщо у вказаному операторі є рядки та **`false`**, якщо в операторі немає рядків або виникла помилка.

### Приклади

**Приклад #1 Приклад використання **sqlsrvhasrows()****

```php
<?php
$server = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $server, $connectionInfo );

$stmt = sqlsrv_query( $conn, "SELECT * FROM Table_1");

if ($stmt) {
   $rows = sqlsrv_has_rows( $stmt );
   if ($rows === true)
      echo "Есть строки. <br />";
   else
      echo "Нет строк. <br />";
}
?>
```

### Дивіться також

-   [sqlsrvnumrows()](function.sqlsrv-num-rows.md) - Отримує кількість рядків у наборі результатів
-   [sqlsrvquery()](function.sqlsrv-query.md) - готує та виконує запит
