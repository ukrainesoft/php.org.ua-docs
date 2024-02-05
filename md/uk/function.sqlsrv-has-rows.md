---
navigation:
  - function.sqlsrv-get-field.md: « sqlsrv\_get\_field
  - function.sqlsrv-next-result.md: sqlsrv\_next\_result »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_has\_rows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_has\_rows

(No version information available, might only be in Git)

sqlsrv\_has\_rows — Вказує, чи є вказаний оператор рядка

### Опис

```methodsynopsis
sqlsrv_has_rows(resource $stmt): bool
```

Вказує, чи має вказаний оператор рядка.

### Список параметрів

`stmt`

Ресурс оператора, що повертається [sqlsrv\_query()](function.sqlsrv-query.md) або [sqlsrv\_execute()](function.sqlsrv-execute.md)

### Значення, що повертаються

Повертає **`true`**, якщо у вказаному операторі є рядки та **`false`**, якщо в операторі немає рядків або виникла помилка.

### Приклади

**Приклад #1 Приклад використання** sqlsrv\_has\_rows()\*\*\*\*

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

-   [sqlsrv\_num\_rows()](function.sqlsrv-num-rows.md) \- Отримує кількість рядків у наборі результатів
-   [sqlsrv\_query()](function.sqlsrv-query.md) \- готує та виконує запит
