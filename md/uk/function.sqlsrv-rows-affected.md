---
navigation:
  - function.sqlsrv-rollback.md: « sqlsrv\_rollback
  - function.sqlsrv-send-stream-data.md: sqlsrv\_send\_stream\_data »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_rows\_affected
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_rows\_affected

(No version information available, might only be in Git)

sqlsrv\_rows\_affected — Повертає кількість рядків, змінених останнім запитом INSERT, UPDATE або DELETE

### Опис

```methodsynopsis
sqlsrv_rows_affected(resource $stmt): int|false
```

Повертає кількість рядків, змінених останнім запитом INSERT, UPDATE або DELETE. Для отримання інформації про кількість рядків, які повертаються запитом SELECT, дивіться [sqlsrv\_num\_rows()](function.sqlsrv-num-rows.md)

### Список параметрів

`stmt`

Ресурс виконаного виразу, для якого повертається кількість порушених рядків.

### Значення, що повертаються

Повертає кількість рядків, які торкнулися останнім запитом INSERT, UPDATE або DELETE. Якщо жодних рядків не було порушено, повертається 0. Якщо кількість порушених рядків не може бути визначена, повертається -1. У разі виникнення помилки повертається **`false`**

### Приклади

**Приклад #1 Приклад використання** sqlsrv\_rows\_affected()\*\*\*\*

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "UPDATE Table_1 SET data = ? WHERE id = ?";

$params = array("updated data", 1);

$stmt = sqlsrv_query( $conn, $sql, $params);

$rows_affected = sqlsrv_rows_affected( $stmt);
if( $rows_affected === false) {
     die( print_r( sqlsrv_errors(), true));
} elseif( $rows_affected == -1) {
      echo "Нет доступной информации.<br />";
} else {
      echo $rows_affected." строк было обновлено.<br />";
}
?>
```

### Дивіться також

-   [sqlsrv\_num\_rows()](function.sqlsrv-num-rows.md) \- Отримує кількість рядків у наборі результатів
