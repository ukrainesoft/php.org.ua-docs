---
navigation:
  - function.sqlsrv-close.md: « sqlsrv\_close
  - function.sqlsrv-configure.md: sqlsrv\_configure »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_commit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_commit

(No version information available, might only be in Git)

sqlsrv\_commit - Фіксує транзакцію, розпочату за допомогою [sqlsrv\_begin\_transaction()](function.sqlsrv-begin-transaction.md)

### Опис

```methodsynopsis
sqlsrv_commit(resource $conn): bool
```

Фіксує транзакцію, розпочату за допомогою [sqlsrv\_begin\_transaction()](function.sqlsrv-begin-transaction.md). З'єднання повертається в режим автоматичної фіксації після дзвінка **sqlsrv\_commit()**. Підтверджена транзакція включає всі оператори, які були виконані після виклику [sqlsrv\_begin\_transaction()](function.sqlsrv-begin-transaction.md). Явні транзакції повинні запускатися та фіксуватися або відкочуватися з використанням цих функцій замість виконання SQL-операторів, які запускають та фіксують/відкочують транзакції. Для отримання додаткової інформації дивіться [» Транзакції SQLSRV](http://msdn.microsoft.com/en-us/library/cc296206.aspx)

### Список параметрів

`conn`

З'єднання, на якому має бути здійснено транзакцію.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**sqlsrv\_commit()\*\*\*\*

У наступному прикладі показано, як використовувати \*\*sqlsrv\_commit()\*\*вместе с[sqlsrv\_begin\_transaction()](function.sqlsrv-begin-transaction.md) і [sqlsrv\_rollback()](function.sqlsrv-rollback.md)

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

/* Инициализация значения параметров. */
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
/* В противном случае откатите транзакцию */
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
-   [sqlsrv\_rollback()](function.sqlsrv-rollback.md) \- Відкочує транзакцію, розпочату sqlsrv\_begin\_transaction
