---
navigation:
  - function.sqlsrv-rollback.html: « sqlsrvrollback
  - function.sqlsrv-send-stream-data.html: sqlsrvsendstreamdata »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrvrowsaffected
---
# sqlsrvrowsaffected

(No version information available, might only be in Git)

sqlsrvrowsaffected — Повертає кількість рядків, змінених останнім виконаним запитом INSERT, UPDATE або DELETE

### Опис

```methodsynopsis
sqlsrv_rows_affected(resource $stmt): int|false
```

Повертає кількість рядків, змінених останнім запитом INSERT, UPDATE або DELETE. Для отримання інформації про кількість рядків, які повертаються запитом SELECT, дивіться [sqlsrvnumrows()](function.sqlsrv-num-rows.html)

### Список параметрів

`stmt`

Ресурс виконаного виразу, для якого повертається кількість порушених рядків.

### Значення, що повертаються

Повертає кількість рядків, які торкнулися останнім запитом INSERT, UPDATE або DELETE. Якщо жодних рядків не було порушено, повертається 0. Якщо кількість порушених рядків не може бути визначена, повертається -1. У разі виникнення помилки повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **sqlsrvrowsaffected()****

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "UPDATE Table_1 SET data = ? WHERE id = ?";

$params = array("updated data", 1);

$stmt = sqlsrv_query( $conn, $sql, $params);

$rows_affected = sqlsrv_rows_affected( $stmt);
if( $rows_affected === false) {
     die( print_r( sqlsrv_errors(), true));
} elseif( $rows_affected == -1) {
      echo "Нет доступной информации.<br />";
} else {
      echo $rows_affected." строк было обновлено.<br />";
}
?>
```

### Дивіться також

-   [sqlsrvnumrows()](function.sqlsrv-num-rows.html) - Отримує кількість рядків у наборі результатів
