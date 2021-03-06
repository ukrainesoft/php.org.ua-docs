- [«sqlsrv_rollback](function.sqlsrv-rollback.md)
- [sqlsrv_send_stream_data »](function.sqlsrv-send-stream-data.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- Повертає кількість рядків, змінених останнім виконаним
запитом INSERT, UPDATE або DELETE

#sqlsrv_rows_affected

(No version information available, might only be in Git)

sqlsrv_rows_affected — Повертає кількість рядків, змінених останнім
виконаним запитом INSERT, UPDATE або DELETE

### Опис

**sqlsrv_rows_affected**(resource `$stmt`): int\|false

Повертає кількість рядків, змінених останнім виконаним запитом
INSERT, UPDATE або DELETE. Для отримання інформації про кількість рядків,
повертаються запитом SELECT, дивіться
[sqlsrv_num_rows()](function.sqlsrv-num-rows.md).

### Список параметрів

`stmt`
Ресурс виконаного виразу, для якого повертається кількість
порушених рядків.

### Значення, що повертаються

Повертає кількість рядків, порушених останнім запитом INSERT,
UPDATE або DELETE. Якщо жодних рядків не було порушено, повертається
0. Якщо кількість порушених рядків не може бути визначена,
повертається до -1. У разі виникнення помилки повертається **`false`**.

### Приклади

**Приклад #1 Приклад використання **sqlsrv_rows_affected()****

` <?php$serverName = "serverName\sqlexpress";$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );$conn = sqlsrv_connect ( $serverName, $connectionInfo);if( $conn === false ) {     die( print_r( sqlsrv_errors(), true));}$sql = "UPDATE Table_1 SET| array("updated data", 1);$stmt = sqlsrv_query( $conn, $sql, $params);$rows_affected = sqlsrv_rows_affected( $stmt);if( false_affected  ), true));} elseif( $rows_affected == -1) {     echo "Немає доступної інформації. `

### Дивіться також

- [sqlsrv_num_rows()](function.sqlsrv-num-rows.md) - Отримує
кількість рядків у наборі результатів
