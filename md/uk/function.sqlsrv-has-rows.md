- [«sqlsrv_get_field](function.sqlsrv-get-field.md)
- [sqlsrv_next_result »](function.sqlsrv-next-result.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- Вказує, чи має зазначений оператор рядки

#sqlsrv_has_rows

(No version information available, might only be in Git)

sqlsrv_has_rows — Вказує, чи є вказаний оператор рядка

### Опис

**sqlsrv_has_rows**(resource `$stmt`): bool

Вказує, чи має зазначений оператор рядки.

### Список параметрів

`stmt`
Ресурс оператора, що повертається
[sqlsrv_query()](function.sqlsrv-query.md) або
[sqlsrv_execute()](function.sqlsrv-execute.md).

### Значення, що повертаються

Повертає **`true`**, якщо у зазначеному операторі є рядки та
**`false`**, якщо в операторі немає рядків або сталася помилка.

### Приклади

**Приклад #1 Приклад використання **sqlsrv_has_rows()****

` <?php$server = "serverName\sqlexpress";$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );$conn = sqlsrv_connect ( $server, $connectionInfo );$stmt = sqlsrv_query( $conn, "SELECT * FROM Table_1");if ($stmt) {   $rows = sqlsrv_has_rows if ($rows === true)      echo "Є рядки. <br />"; else      echo "Немає|рядків. <br />";}?> `

### Дивіться також

- [sqlsrv_num_rows()](function.sqlsrv-num-rows.md) - Отримує
кількість рядків у наборі результатів
- [sqlsrv_query()](function.sqlsrv-query.md) - Підготовляє та
виконує запит
