---
navigation:
  - ref.sqlsrv.md: « Функції SQLSRV
  - function.sqlsrv-cancel.md: sqlsrvcancel »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrvbegintransaction
---
# sqlsrvbegintransaction

(No version information available, might only be in Git)

sqlsrvbegintransaction — Починає транзакцію бази даних

### Опис

```methodsynopsis
sqlsrv_begin_transaction(resource $conn): bool
```

Транзакція, розпочата за допомогою **sqlsrvbegintransaction()**, включає всі оператори, які були виконані після виклику **sqlsrvbegintransaction()** та до викликів [sqlsrvrollback()](function.sqlsrv-rollback.md) або [sqlsrvcommit()](function.sqlsrv-commit.md). Явні транзакції повинні запускатися та фіксуватися або відкочуватися з використанням цих функцій замість виконання операторів SQL, які запускають та фіксують/відкочують транзакції. Для отримання додаткової інформації дивіться [» Транзакції SQLSRV](http://msdn.microsoft.com/en-us/library/cc296206.aspx)

### Список параметрів

`conn`

Ресурс підключення, що повертається викликом [sqlsrvconnect()](function.sqlsrv-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrvbegintransaction()****

У наступному прикладі показано, як використовувати**sqlsrvbegintransaction()** разом з [sqlsrvcommit()](function.sqlsrv-commit.md) і [sqlsrvrollback()](function.sqlsrv-rollback.md)

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true ));
}

/* Начало транзакции. */
if ( sqlsrv_begin_transaction( $conn ) === false ) {
     die( print_r( sqlsrv_errors(), true ));
}

/* Инициализация значений параметров. */
$orderId = 1; $qty = 10; $productId = 100;

/* Настройка и выполнение первого запроса. */
$sql1 = "INSERT INTO OrdersTable (ID, Quantity, ProductID)
          VALUES (?, ?, ?)";
$params1 = array( $orderId, $qty, $productId );
$stmt1 = sqlsrv_query( $conn, $sql1, $params1 );

/* Настройка и выполнение второго запроса. */
$sql2 = "UPDATE InventoryTable
          SET Quantity = (Quantity - ?)
          WHERE ProductID = ?";
$params2 = array($qty, $productId);
$stmt2 = sqlsrv_query( $conn, $sql2, $params2 );

/* Если оба запроса были успешными, зафиксируйте транзакцию. */
/* В противном случае откатите транзакцию. */
if( $stmt1 && $stmt2 ) {
     sqlsrv_commit( $conn );
     echo "Транзакция зафиксирована.<br />";
} else {
     sqlsrv_rollback( $conn );
     echo "Транзация откачена.<br />";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [sqlsrvcommit()](function.sqlsrv-commit.md) - Фіксує транзакцію, розпочату за допомогою sqlsrvbegintransaction
-   [sqlsrvrollback()](function.sqlsrv-rollback.md) - Відкочує транзакцію, розпочату sqlsrvbegintransaction
