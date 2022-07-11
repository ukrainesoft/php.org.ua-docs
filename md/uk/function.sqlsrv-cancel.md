- [«sqlsrv_begin_transaction](function.sqlsrv-begin-transaction.md)
- [sqlsrv_client_info »](function.sqlsrv-client-info.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- скасовує оператор

#sqlsrv_cancel

(No version information available, might only be in Git)

sqlsrv_cancel — скасовує оператор

### Опис

**sqlsrv_cancel**(resource `$stmt`): bool

Скасує оператор. Усі невикористані результати, пов'язані з
оператором, видаляються. Після виклику **sqlsrv_cancel()** вказаний
оператор може бути виконаний повторно, якщо він був створений за допомогою
[sqlsrv_prepare()](function.sqlsrv-prepare.md). Виклик
**sqlsrv_cancel()** не потрібно, якщо всі результати, пов'язані з
оператором були використані.

### Список параметрів

`stmt`
Ресурс оператора, який потрібно скасувати.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrv_cancel()****

` <?php$serverName = "serverName\sqlexpress";$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");$conn = sqlsrv_connect ( $serverName, $connectionInfo);if( $conn === false ) {     die( print_r( sqlsrv_errors(), true)));}$sql = "SELECT Sales FROM$$ sql);if( $stmt === false ) {    die( print_r( sqlsrv_errors(), true));}if( sqlsrv_execute( $stmt ) === false)  ;}$salesTotal = 0;$count = 0;while( ($row = sqlsrv_fetch_array( $stmt)) && $salesTotal <=100000){     $qty =;| $price==$row[1]; $salesTotal+==($price**$qty); $count++;}echo "$count продаж склали перший $$salesTotal виручки.<br />";// Скасувати очікуючі результати. Оператор можна використовувати повторно.sqlsrv_cancel( $stmt);?> `

### Примітки

Основна відмінність між
[sqlsrv_free_stmt()](function.sqlsrv-free-stmt.md) та
**sqlsrv_cancel()** полягає в тому, що ресурс оператора, скасований
за допомогою **sqlsrv_cancel()**, може бути повторно виконаний, якщо він був
створено за допомогою [sqlsrv_prepare()](function.sqlsrv-prepare.md).
Ресурс оператора, скасований за допомогою **sqlsrv_free_statement()**, не
може бути повторно виконано.

### Дивіться також

- [sqlsrv_free_stmt()](function.sqlsrv-free-stmt.md) - Звільняє
всі ресурси для вказаного оператора
- [sqlsrv_prepare()](function.sqlsrv-prepare.md) - Підготовка
запит до виконання
