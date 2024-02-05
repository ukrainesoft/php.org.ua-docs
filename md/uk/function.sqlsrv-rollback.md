---
navigation:
  - function.sqlsrv-query.md: « sqlsrv\_query
  - function.sqlsrv-rows-affected.md: sqlsrv\_rows\_affected »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_rollback
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_rollback

(No version information available, might only be in Git)

sqlsrv\_rollback - Відкочує транзакцію, розпочату [sqlsrv\_begin\_transaction()](function.sqlsrv-begin-transaction.md)

### Опис

```methodsynopsis
sqlsrv_rollback(resource $conn): bool
```

Відкочує транзакцію, розпочату [sqlsrv\_begin\_transaction()](function.sqlsrv-begin-transaction.md) та повертає з'єднання з режимом автоматичної фіксації.

### Список параметрів

`conn`

Ресурс підключення, що повертається викликом [sqlsrv\_connect()](function.sqlsrv-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**sqlsrv\_rollback()\*\*\*\*

У наступному прикладі показано, як використовувати [sqlsrv\_begin\_transaction()](function.sqlsrv-begin-transaction.md)вместе с[sqlsrv\_commit()](function.sqlsrv-commit.md)или**sqlsrv\_rollback()**

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

/* Настройка и выполнение первого запроса */
$sql1 = "INSERT INTO OrdersTable (ID, Quantity, ProductID)
         VALUES (?, ?, ?)";
$params1 = array( $orderId, $qty, $productId );
$stmt1 = sqlsrv_query( $conn, $sql1, $params1 );

/* Настройка и выполнение второго запроса */
$sql2 = "UPDATE InventoryTable
         SET Quantity = (Quantity - ?)
         WHERE ProductID = ?";
$params2 = array($qty, $productId);
$stmt2 = sqlsrv_query( $conn, $sql2, $params2 );

/* Если оба запроса выполнены успешно, зафиксируйте транзакцию. */
/* В противном случае, откатите транзакцию. */
if( $stmt1 && $stmt2 ) {
     sqlsrv_commit( $conn );
     echo "Транзакция зафиксирована.<br />";
} else {
     sqlsrv_rollback( $conn );
     echo "Транзакция откачена.<br />";
}
?>
```

### Дивіться також

-   [sqlsrv\_begin\_transaction()](function.sqlsrv-begin-transaction.md) \- Починає транзакцію бази даних
-   [sqlsrv\_commit()](function.sqlsrv-commit.md) \- Фіксує транзакцію, розпочату за допомогою sqlsrv\_begin\_transaction
