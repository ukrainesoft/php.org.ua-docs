Відкочує транзакцію, розпочату sqlsrvbegintransaction

-   [« sqlsrvquery](function.sqlsrv-query.html)
    
-   [sqlsrvrowsaffected »](function.sqlsrv-rows-affected.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SQLSRV](ref.sqlsrv.md)
    
-   Відкочує транзакцію, розпочату sqlsrvbegintransaction
    

# sqlsrvrollback

(No version information available, might only be in Git)

sqlsrvrollback - Відкочує транзакцію, розпочату [sqlsrvbegintransaction()](function.sqlsrv-begin-transaction.html)

### Опис

```methodsynopsis
sqlsrv_rollback(resource $conn): bool
```

Відкочує транзакцію, розпочату [sqlsrvbegintransaction()](function.sqlsrv-begin-transaction.html) та повертає з'єднання з режимом автоматичної фіксації.

### Список параметрів

`conn`

Ресурс підключення, що повертається викликом [sqlsrvconnect()](function.sqlsrv-connect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrvrollback()****

У наступному прикладі показано, як використовувати [sqlsrvbegintransaction()](function.sqlsrv-begin-transaction.html) разом з [sqlsrvcommit()](function.sqlsrv-commit.html) або **sqlsrvrollback()**

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true ));
}

/* Начало транзакции. */
if ( sqlsrv_begin_transaction( $conn ) === false ) {
     die( print_r( sqlsrv_errors(), true ));
}

/* Инициализация значений параметров. */
$orderId = 1; $qty = 10; $productId = 100;

/* Настройка и выполнение первого запроса */
$sql1 = "INSERT INTO OrdersTable (ID, Quantity, ProductID)
         VALUES (?, ?, ?)";
$params1 = array( $orderId, $qty, $productId );
$stmt1 = sqlsrv_query( $conn, $sql1, $params1 );

/* Настройка и выполнение второго запроса */
$sql2 = "UPDATE InventoryTable
         SET Quantity = (Quantity - ?)
         WHERE ProductID = ?";
$params2 = array($qty, $productId);
$stmt2 = sqlsrv_query( $conn, $sql2, $params2 );

/* Если оба запроса выполнены успешно, зафиксируйте транзакцию. */
/* В противном случае, откатите транзакцию. */
if( $stmt1 && $stmt2 ) {
     sqlsrv_commit( $conn );
     echo "Транзакция зафиксирована.<br />";
} else {
     sqlsrv_rollback( $conn );
     echo "Транзакция откачена.<br />";
}
?>
```

### Дивіться також

-   [sqlsrvbegintransaction()](function.sqlsrv-begin-transaction.html) - Починає транзакцію бази даних
-   [sqlsrvcommit()](function.sqlsrv-commit.html) - Фіксує транзакцію, розпочату за допомогою sqlsrvbegintransaction