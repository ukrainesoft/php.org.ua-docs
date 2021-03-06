- [« Функції SQLSRV](ref.sqlsrv.md)
- [sqlsrv_cancel »](function.sqlsrv-cancel.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- починає транзакцію бази даних

#sqlsrv_begin_transaction

(No version information available, might only be in Git)

sqlsrv_begin_transaction — Починає транзакцію бази даних

### Опис

**sqlsrv_begin_transaction**(resource `$conn`): bool

Транзакція, розпочата за допомогою **sqlsrv_begin_transaction()**, включає
всі оператори, які були виконані після виклику
**sqlsrv_begin_transaction()** та до викликів
[sqlsrv_rollback()](function.sqlsrv-rollback.md) або
[sqlsrv_commit()](function.sqlsrv-commit.md). Явні транзакції мають
запускатися і фіксуватися або відкочуватися з використанням цих
функцій замість виконання операторів SQL, які запускають та
фіксують/відкочують транзакції. Для отримання додаткової інформації
дивіться [» Транзакції SQLSRV](http://msdn.microsoft.com/en-us/library/cc296206.aspx).

### Список параметрів

`conn`
Ресурс підключення, що повертається викликом
[sqlsrv_connect()](function.sqlsrv-connect.md).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrv_begin_transaction()****

У наступному прикладі показано, як
використовувати**sqlsrv_begin_transaction()** разом з
[sqlsrv_commit()](function.sqlsrv-commit.md) та
[sqlsrv_rollback()](function.sqlsrv-rollback.md).

` <?php$serverName = "serverName\sqlexpress";$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");$conn = sqlsrv_connect ( $serverName, $connectionInfo);if( $conn === false ) {    die( print_r( sqlsrv_errors(), true )));}/* Початок транзакції. */if ( sqlsrv_begin_transaction( $conn ) === false ) {    die( print_r( sqlsrv_errors(), true )));}/* Ініціалізація значень пара */$orderId = 1; $qty = 10; $productId = 100;/* Налаштування і виконання першого запиту. */$sql1 = "INSERT INTO OrdersTable (ID, Quantity, ProductID)          VALUES (?, ?, ?)";$params1 = array( $orderId| sql1, $params1 );/* Налаштування і виконання другого запиту. */$sql2 = "UPDATE InventoryTable          SET Quantity = (Quantity - ?)          WHERE ProductID = ?";$params2 = array($qty, $productId);$stmt2 = sqlsrv_query( $conn, $sql2, $params2 );/ * Якщо обидва запити були успішними, зафіксуйте транзакцію. *//* У протилежному випадку відкотіть транзакцію. */if( $stmt1 && $stmt2 ) {    sqlsrv_commit( $conn ); echo "Транзакція зафіксована.<br />";} else {     sqlsrv_rollback( $conn ); echo "Транзація відкачена.<br />";}?> `

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

- [sqlsrv_commit()](function.sqlsrv-commit.md) - Фіксує
транзакцію, розпочату за допомогою sqlsrv_begin_transaction
- [sqlsrv_rollback()](function.sqlsrv-rollback.md) - Відкочує
транзакцію, розпочату sqlsrv_begin_transaction
