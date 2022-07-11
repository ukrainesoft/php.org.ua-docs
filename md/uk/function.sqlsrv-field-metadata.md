- [«sqlsrv_fetch](function.sqlsrv-fetch.md)
- [sqlsrv_free_stmt »](function.sqlsrv-free-stmt.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- Отримує метадані для полів оператора, підготовленого за допомогою
sqlsrv_prepare або sqlsrv_query

#sqlsrv_field_metadata

(No version information available, might only be in Git)

sqlsrv_field_metadata — Отримує метадані для полів оператора,
підготовленого за допомогою
[sqlsrv_prepare()](function.sqlsrv-prepare.md) або
[sqlsrv_query()](function.sqlsrv-query.md)

### Опис

**sqlsrv_field_metadata**(resource `$stmt`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Отримує метадані для полів оператора, підготовленого за допомогою
[sqlsrv_prepare()](function.sqlsrv-prepare.md) або
[sqlsrv_query()](function.sqlsrv-query.md).
**sqlsrv_field_metadata()** може викликатися для оператора до або після
виконання оператора.

### Список параметрів

`stmt`
Ресурс оператора, для якого повертаються метадані.

### Значення, що повертаються

У разі успішного виконання, повертає масив масивів. В протилежному
у разі повертає **`false`**. Кожен повертається масив описується
наступною таблицею:

| Ключ      | Опис                                                                                                                  |
| --------- | --------------------------------------------------------------------------------------------------------------------- |
| Name      | Назва поля.                                                                                                           |
| Тип       | Числове значення типу SQL.                                                                                            |
| Size      | Кількість символів для полів символьного типу, кількість байтів для полів двійкового типу або **null для інших типів. |
| Precision | Точність для типів змінної точності, ** null** для інших типів.                                                       |
| Scale     | Масштаб для типів масштабованих типів даних, ** null** для інших типів.                                               |
| Nullable  | Перелік, що вказує, чи стовпець допускає значення NULL, неприпустиме значення NULL або невідоме.                      |

**Масив, що повертається sqlsrv_field_metadata**

Для отримання додаткової інформації дивіться
[» sqlsrv_field_metadata](http://msdn.microsoft.com/en-us/library/cc296197.aspx)
у документації Microsoft SQLSRV.

### Приклади

**Приклад #1 Приклад використання **sqlsrv_field_metadata()****

` <?php$serverName = "serverName\sqlexpress";$connectionInfo = array( "Database"=>"AdventureWorks", "UID"=>"username", "PWD"=>"password");$conn = sqlsrv_connect ( $serverName, $connectionInfo);if( $conn === false ) {   die( print_r( sqlsrv_errors(), true));}$sql = "SELECT * FROM Table_1"; sql );foreach( sqlsrv_field_metadata( $stmt ) as $fieldMetadata ) {    foreach( $fieldMetadata as $name => $value) { |$| }      echo "<br />";}?> `

### Дивіться також

- [sqlsrv_client_info()](function.sqlsrv-client-info.md) -
Повертає інформацію про клієнта та зазначене підключення
