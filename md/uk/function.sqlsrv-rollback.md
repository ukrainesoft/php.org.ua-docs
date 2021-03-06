- [«sqlsrv_query](function.sqlsrv-query.md)
- [sqlsrv_rows_affected »](function.sqlsrv-rows-affected.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- Відкочує транзакцію, розпочату sqlsrv_begin_transaction

#sqlsrv_rollback

(No version information available, might only be in Git)

sqlsrv_rollback - Відкочує транзакцію, розпочату
[sqlsrv_begin_transaction()](function.sqlsrv-begin-transaction.md)

### Опис

**sqlsrv_rollback**(resource `$conn`): bool

Відкочує транзакцію, розпочату
[sqlsrv_begin_transaction()](function.sqlsrv-begin-transaction.md) та
повертає підключення до режиму автоматичної фіксації.

### Список параметрів

`conn`
Ресурс підключення, що повертається викликом
[sqlsrv_connect()](function.sqlsrv-connect.md).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrv_rollback()****

У цьому прикладі показано, як використовувати
[sqlsrv_begin_transaction()](function.sqlsrv-begin-transaction.md)
разом з [sqlsrv_commit()](function.sqlsrv-commit.md) або
**sqlsrv_rollback()**.

` <?php$serverName = "serverName\sqlexpress";$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");$conn = sqlsrv_connect ( $serverName, $connectionInfo);if( $conn === false ) {    die( print_r( sqlsrv_errors(), true )));}/* Початок транзакції. */if ( sqlsrv_begin_transaction( $conn ) === false ) {    die( print_r( sqlsrv_errors(), true )));}/* Ініціалізація значень пара */$orderId = 1; $qty = 10; $productId==100;/* Настройка і виконання першого запиту */$sql1 = "INSERT INTO OrdersTable (ID, Quantity, ProductID) ?| productId );$stmt1 = sqlsrv_query( $conn, $sql1, $params1 );/* Настройка и выполнение второго запроса */$sql2 = "UPDATE InventoryTable         SET Quantity = (Quantity - ?)         WHERE ProductID = ?";$params2 = array($qty, $productId);$stmt2 = sqlsrv_query( $conn, $sql2, $params2 );/* Якщо оби запити виконані успішно, зафіксуйте транзакцію. *//* У протилежному випадку, відкотіть транзакцію. */if( $stmt1 && $stmt2 ) {    sqlsrv_commit( $conn ); echo "Транзакція зафіксована.<br />";} else {     sqlsrv_rollback( $conn ); echo "Транзакція відкачена.<br />";}?> `

### Дивіться також

- [sqlsrv_begin_transaction()](function.sqlsrv-begin-transaction.md) -
Розпочинає транзакцію бази даних
- [sqlsrv_commit()](function.sqlsrv-commit.md) - Фіксує
транзакцію, розпочату за допомогою sqlsrv_begin_transaction
