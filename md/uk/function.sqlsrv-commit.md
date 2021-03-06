- [«sqlsrv_close](function.sqlsrv-close.md)
- [sqlsrv_configure »](function.sqlsrv-configure.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- Фіксує транзакцію, розпочату за допомогою sqlsrv_begin_transaction

#sqlsrv_commit

(No version information available, might only be in Git)

sqlsrv_commit — Фіксує транзакцію, розпочату за допомогою
[sqlsrv_begin_transaction()](function.sqlsrv-begin-transaction.md)

### Опис

**sqlsrv_commit**(resource `$conn`): bool

Фіксує транзакцію, розпочату за допомогою
[sqlsrv_begin_transaction()](function.sqlsrv-begin-transaction.md).
З'єднання повертається в режим автоматичної фіксації після дзвінка
**sqlsrv_commit()**. Підтверджена транзакція включає всі оператори,
які були виконані після виклику
[sqlsrv_begin_transaction()](function.sqlsrv-begin-transaction.md).
Явні транзакції повинні запускатися та фіксуватися чи відкочуватися з
використанням цих функцій замість виконання SQL-операторів, які
запускають та фіксують/відкочують транзакції. Для отримання
додаткову інформацію дивіться [»Транзакції SQLSRV](http://msdn.microsoft.com/en-us/library/cc296206.aspx).

### Список параметрів

`conn`
З'єднання, на якому має бути здійснено транзакцію.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrv_commit()****

У цьому прикладі показано, як використовувати **sqlsrv_commit()**
разом з
[sqlsrv_begin_transaction()](function.sqlsrv-begin-transaction.md) та
[sqlsrv_rollback()](function.sqlsrv-rollback.md).

` <?php$serverName = "serverName\sqlexpress";$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");$conn = sqlsrv_connect ( $serverName, $connectionInfo);if( $conn === false ) {    die( print_r( sqlsrv_errors(), true )));}/* Початок транзакції. */if ( sqlsrv_begin_transaction( $conn ) === false ) {    die( print_r( sqlsrv_errors(), true )));}/* Ініціалізація значення */$orderId = 1; $qty = 10; $productId = 100;/* Налаштування і виконання першого запиту. */$sql1 ='INSERT INTO OrdersTable (ID, Quantity, ProductID)        VALUES (?, ?, ?)';$params1 = array( $orderId, $$; sql1, $params1 );/* Налаштування і виконання другого запиту. */$sql2 = "UPDATE InventoryTable         SET Quantity = (Quantity - ?)         WHERE ProductID = ?";$params2 = array($qty, $productId);$stmt2 = sqlsrv_query( $conn, $sql2, $params2 );/ * Якщо обидва запити були успішними, зафіксуйте транзакцію. *//* У протилежному випадку відкотіть транзакцію */if( $stmt1 && $stmt2 ) {     sqlsrv_commit( $conn ); echo "Транзакція зафіксована.<br />";} else {     sqlsrv_rollback( $conn ); echo "Транзакція відкачена.<br />";}?> `

### Дивіться також

- [sqlsrv_begin_transaction()](function.sqlsrv-begin-transaction.md) -
Розпочинає транзакцію бази даних
- [sqlsrv_rollback()](function.sqlsrv-rollback.md) - Відкочує
транзакцію, розпочату sqlsrv_begin_transaction
