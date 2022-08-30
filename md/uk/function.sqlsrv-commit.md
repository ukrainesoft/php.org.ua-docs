Фіксує транзакцію, розпочату за допомогою sqlsrvbegintransaction

-   [« sqlsrvclose](function.sqlsrv-close.html)
    
-   [sqlsrvconfigure »](function.sqlsrv-configure.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SQLSRV](ref.sqlsrv.md)
    
-   Фіксує транзакцію, розпочату за допомогою sqlsrvbegintransaction
    

# sqlsrvcommit

(No version information available, might only be in Git)

sqlsrvcommit - Фіксує транзакцію, розпочату за допомогою [sqlsrvbegintransaction()](function.sqlsrv-begin-transaction.html)

### Опис

```methodsynopsis
sqlsrv_commit(resource $conn): bool
```

Фіксує транзакцію, розпочату за допомогою [sqlsrvbegintransaction()](function.sqlsrv-begin-transaction.html). З'єднання повертається в режим автоматичної фіксації після дзвінка **sqlsrvcommit()**. Підтверджена транзакція включає всі оператори, які були виконані після виклику [sqlsrvbegintransaction()](function.sqlsrv-begin-transaction.html). Явні транзакції повинні запускатися та фіксуватися або відкочуватися з використанням цих функцій замість виконання SQL-операторів, які запускають та фіксують/відкочують транзакції. Для отримання додаткової інформації дивіться [» Транзакції SQLSRV](http://msdn.microsoft.com/en-us/library/cc296206.aspx)

### Список параметрів

`conn`

З'єднання, на якому має бути здійснено транзакцію.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrvcommit()****

У наступному прикладі показано, як використовувати **sqlsrvcommit()** разом з [sqlsrvbegintransaction()](function.sqlsrv-begin-transaction.html) і [sqlsrvrollback()](function.sqlsrv-rollback.html)

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

/* Инициализация значения параметров. */
$orderId = 1; $qty = 10; $productId = 100;

/* Настройка и выполнение первого запроса. */
$sql1 = "INSERT INTO OrdersTable (ID, Quantity, ProductID)
         VALUES (?, ?, ?)";
$params1 = array( $orderId, $qty, $productId );
$stmt1 = sqlsrv_query( $conn, $sql1, $params1 );

/* Настройка и выполнение второго запроса. */
$sql2 = "UPDATE InventoryTable
         SET Quantity = (Quantity - ?)
         WHERE ProductID = ?";
$params2 = array($qty, $productId);
$stmt2 = sqlsrv_query( $conn, $sql2, $params2 );

/* Если оба запроса были успешными, зафиксируйте транзакцию. */
/* В противном случае откатите транзакцию */
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
-   [sqlsrvrollback()](function.sqlsrv-rollback.html) - Відкочує транзакцію, розпочату sqlsrvbegintransaction