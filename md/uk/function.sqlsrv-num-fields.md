- [«sqlsrv_next_result](function.sqlsrv-next-result.md)
- [sqlsrv_num_rows »](function.sqlsrv-num-rows.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- Витягує кількість полів (стовпців) оператора

#sqlsrv_num_fields

(No version information available, might only be in Git)

sqlsrv_num_fields — Витягує кількість полів (стовпців) оператора

### Опис

**sqlsrv_num_fields**(resource `$stmt`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Витягує кількість полів (стовпців) оператора.

### Список параметрів

`stmt`
Оператор, котрому повертається кількість полів.
**sqlsrv_num_fields()** може викликатися для оператора до або після
виконання оператора.

### Значення, що повертаються

У разі успішного виконання повертає кількість полів. В протилежному
у разі повертає **`false`**.

### Приклади

**Приклад #1 Приклад використання **sqlsrv_num_fields()****

` <?php$serverName = "serverName\sqlexpress";$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");$conn = sqlsrv_connect ( $serverName, $connectionInfo);if( $conn === false ) {   die( print_r( sqlsrv_errors(), true));}$sql = "SELECT * FROM Table_$"; sql);if( $stmt === false) {  die( print_r( sqlsrv_errors(), true)));}$numFields = sqlsrv_num_fields( $stmt х| рядки. for($i = 0; $i < $numFields; $i++) {      echo sqlsrv_get_field($stmt, $i)." "; }  echo "<br />";}?> `

### Дивіться також

- [sqlsrv_field_metadata()](function.sqlsrv-field-metadata.md) -
Отримує метадані для полів оператора, підготовленого за допомогою
sqlsrv_prepare або sqlsrv_query
- [sqlsrv_fetch()](function.sqlsrv-fetch.md) - Робить таку
рядок у наборі результатів доступного для читання
- [sqlsrv_get_field()](function.sqlsrv-get-field.md) - Отримує
дані поля з поточного вибраного рядка
