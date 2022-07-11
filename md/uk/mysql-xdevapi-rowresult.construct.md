- [«mysql_xdevapi\RowResult](class.mysql-xdevapi-rowresult.md)
- [RowResult::fetchAll »](mysql-xdevapi-rowresult.fetchall.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\RowResult](class.mysql-xdevapi-rowresult.md)
- Конструктор класу RowResult

# RowResult::\_\_construct

(No version information available, might only be in Git)

RowResult::\_\_construct - Конструктор класу RowResult

### Опис

private **mysql_xdevapi\RowResult::\_\_construct**()

Представляє набір результатів, отриманий під час звернення до бази даних.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\RowResult::\_\_construct()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$schema = $session->getSchema("addressbook");$table  = $schema->getTable("names" );$row = $table->select('name', 'age')->where('age > 18')->execute()->fetchAll();print_r($row); `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[name] => John
[age] => 42
)
[1] => Array
(
[name] => Sam
[age] => 33
)
)
