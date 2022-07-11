- [« RowResult::getColumnNames](mysql-xdevapi-rowresult.getcolumnnames.md)
- [RowResult::getWarnings »](mysql-xdevapi-rowresult.getwarnings.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\RowResult](class.mysql-xdevapi-rowresult.md)
- Отримує метадані стовпця

# RowResult::getColumns

(No version information available, might only be in Git)

RowResult::getColumns — Отримує метадані стовпця

### Опис

public **mysql_xdevapi\RowResult::getColumns**(): array

Отримує метадані стовпців, присутні у наборі результатів.

**Увага**

На цей час ця функція ще була документована; для
ознайомлення доступний лише список аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів FieldMetadata, що представляють стовпці в результаті, або
порожній масив, якщо набір результатів порожній.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\RowResult::getColumns()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE addressbook")->execute();$session->sql("CREATE DATABASE foo")->execute();$session->sql("CREATE TABLE foo.test_table(x int)")->execute();$session->sql("INSERT INTO addressbook.names values ('John ', 42), ('Sam', 33)")->execute();$sql = $session->sql("SELECT * from addressbook.names")->execute();$cols = $sql- >getColumns();print_r($cols); `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => mysql_xdevapi\FieldMetadata Object
(
[type] => 7
[type_name] => BYTES
[name] => name
[original_name] => name
[table] => names
[original_table] => names
[schema] => addressbook
[catalog] => def
[collation] => 255
[fractional_digits] => 0
[length] => 65535
[flags] => 0
[content_type] => 0
)
[1] => mysql_xdevapi\FieldMetadata Object
(
[type] => 1
[type_name] => SINT
[name] => age
[original_name] => age
[table] => names
[original_table] => names
[schema] => addressbook
[catalog] => def
[collation] => 0
[fractional_digits] => 0
[length] => 11
[flags] => 0
[content_type] => 0
)
)
