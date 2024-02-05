---
navigation:
  - function.sqlsrv-begin-transaction.md: « sqlsrv\_begin\_transaction
  - function.sqlsrv-client-info.md: sqlsrv\_client\_info »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_cancel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_cancel

(No version information available, might only be in Git)

sqlsrv\_cancel — Скасує оператор

### Опис

```methodsynopsis
sqlsrv_cancel(resource $stmt): bool
```

Скасує оператор. Усі невикористані результати, пов'язані з оператором, видаляються. Після виклику **sqlsrv\_cancel()** вказаний оператор може бути виконаний повторно, якщо він був створений за допомогою [sqlsrv\_prepare()](function.sqlsrv-prepare.md). Виклик **sqlsrv\_cancel()** не потрібно, якщо всі результати, пов'язані з оператором, були використані.

### Список параметрів

`stmt`

Ресурс оператора, який потрібно скасувати.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** sqlsrv\_cancel()\*\*\*\*

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT Sales FROM Table_1";

$stmt = sqlsrv_prepare( $conn, $sql);

if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

if( sqlsrv_execute( $stmt ) === false) {
     die( print_r( sqlsrv_errors(), true));
}

$salesTotal = 0;
$count = 0;

while( ($row = sqlsrv_fetch_array( $stmt)) && $salesTotal <=100000)
{
     $qty = $row[0];
     $price = $row[1];
     $salesTotal += ( $price * $qty);
     $count++;
}

echo "$count продаж составили первый $$salesTotal выручки.<br />";

// Отменить ожидающие результаты. Оператор можно использовать повторно.
sqlsrv_cancel( $stmt);
?>
```

### Примітки

Основна відмінність між [sqlsrv\_free\_stmt()](function.sqlsrv-free-stmt.md)и**sqlsrv\_cancel()** полягає в тому, що ресурс оператора, скасований за допомогою **sqlsrv\_cancel()**, може бути повторно виконаний, якщо він був створений за допомогою [sqlsrv\_prepare()](function.sqlsrv-prepare.md). Ресурс оператора, скасований за допомогою **sqlsrv\_free\_statement()**, не може бути повторно виконано.

### Дивіться також

-   [sqlsrv\_free\_stmt()](function.sqlsrv-free-stmt.md) \- звільняє всі ресурси для вказаного оператора
-   [sqlsrv\_prepare()](function.sqlsrv-prepare.md) \- готує запит до виконання
