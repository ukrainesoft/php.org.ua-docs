---
navigation:
  - function.sqlsrv-begin-transaction.md: « sqlsrvbegintransaction
  - function.sqlsrv-client-info.md: sqlsrvclientinfo »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrvcancel
---
# sqlsrvcancel

(No version information available, might only be in Git)

sqlsrvcancel — Скасує оператор

### Опис

```methodsynopsis
sqlsrv_cancel(resource $stmt): bool
```

Скасує оператор. Усі невикористані результати, пов'язані з оператором, видаляються. Після виклику **sqlsrvcancel()** вказаний оператор може бути виконаний повторно, якщо він був створений за допомогою [sqlsrvprepare()](function.sqlsrv-prepare.md). Виклик **sqlsrvcancel()** не потрібно, якщо всі результати, пов'язані з оператором, були використані.

### Список параметрів

`stmt`

Ресурс оператора, який потрібно скасувати.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrvcancel()****

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT Sales FROM Table_1";

$stmt = sqlsrv_prepare( $conn, $sql);

if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

if( sqlsrv_execute( $stmt ) === false) {
     die( print_r( sqlsrv_errors(), true));
}

$salesTotal = 0;
$count = 0;

while( ($row = sqlsrv_fetch_array( $stmt)) && $salesTotal <=100000)
{
     $qty = $row[0];
     $price = $row[1];
     $salesTotal += ( $price * $qty);
     $count++;
}

echo "$count продаж составили первый $$salesTotal выручки.<br />";

// Отменить ожидающие результаты. Оператор можно использовать повторно.
sqlsrv_cancel( $stmt);
?>
```

### Примітки

Основна відмінність між [sqlsrvfreestmt()](function.sqlsrv-free-stmt.md) і **sqlsrvcancel()** полягає в тому, що ресурс оператора, скасований за допомогою **sqlsrvcancel()**, може бути повторно виконаний, якщо він був створений за допомогою [sqlsrvprepare()](function.sqlsrv-prepare.md). Ресурс оператора, скасований за допомогою **sqlsrvfreestatement()**, не може бути повторно виконано.

### Дивіться також

-   [sqlsrvfreestmt()](function.sqlsrv-free-stmt.md) - звільняє всі ресурси для вказаного оператора
-   [sqlsrvprepare()](function.sqlsrv-prepare.md) - готує запит до виконання
