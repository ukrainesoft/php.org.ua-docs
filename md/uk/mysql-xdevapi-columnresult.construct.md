- [« mysql_xdevapi\ColumnResult](class.mysql-xdevapi-columnresult.md)
- [ColumnResult::getCharacterSetName »](mysql-xdevapi-columnresult.getcharactersetname.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\ColumnResult](class.mysql-xdevapi-columnresult.md)
- Конструктор класу ColumnResult

# ColumnResult::\_\_construct

(No version information available, might only be in Git)

ColumnResult::\_\_construct - Конструктор класу ColumnResult

### Опис

private **mysql_xdevapi\ColumnResult::\_\_construct**()

Отримує метадані стовпця, такі як набір символів; створюється методом
RowResult::getColumns().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\ColumnResult::\_\_construct()****

` <?php$session== mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS nonsense")->execute();$session->sql( "CREATE DATABASE nonsense")->execute();$session->sql("CREATE TABLE nonsense.numbers (hello int, world float unsigned)")->execute();$session->sql("INSERT INTO .numbers values (42, 42)")->execute();$schema = $session->getSchema("nonsense");$table  = $schema->getTable("numbers");$result1 = $table- >select('hello','world')->execute();// Повертає масив об'єктів ColumnResult$columns = $result1->getColumns();foreach ($columns as $column) {      
Мітка стовпця " , $column->getColumnLabel();   echo " є типом "       , $column->getType();    echo "> і | "Підписаний.";}// Альтернативний варіант$result2 = $session->sql("SELECT * FROM nonsense.numbers")->execute();// Повертає масив об'єктів FieldMetadataprint_r `

Результатом виконання цього прикладу буде щось подібне:


Мітка стовпця hello є типом 19 і підписано.
Мітка стовпця світ є типом 4 і непідписаний.

Array
(
[0] => mysql_xdevapi\FieldMetadata Object
(
[type] => 1
[type_name] => SINT
[name] => hello
[original_name] => hello
[table] => numbers
[original_table] => numbers
[schema] => nonsense
[catalog] => def
[collation] => 0
[fractional_digits] => 0
[length] => 11
[flags] => 0
[content_type] => 0
)
[1] => mysql_xdevapi\FieldMetadata Object
(
[type] => 6
[type_name] => FLOAT
[name] => world
[original_name] => world
[table] => numbers
[original_table] => numbers
[schema] => nonsense
[catalog] => def
[collation] => 0
[fractional_digits] => 31
[length] => 12
[flags] => 1
[content_type] => 0
)
)
