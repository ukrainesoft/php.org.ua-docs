- [« TableSelect::\_\_construct](mysql-xdevapi-tableselect.construct.md)
- [TableSelect::groupBy »](mysql-xdevapi-tableselect.groupby.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\TableSelect](class.mysql-xdevapi-tableselect.md)
- Виконує оператор вибірки

# TableSelect::execute

(No version information available, might only be in Git)

TableSelect::execute — Виконує оператор вибірки

### Опис

public **mysql_xdevapi\TableSelect::execute**():
[mysql_xdevapi\RowResult](class.mysql-xdevapi-rowresult.md)

Виконує затвердження вибірки, пов'язуючи його методом execute().

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт RowResult.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\TableSelect::execute()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$schema = $session->getSchema("addressbook");$table  = $schema->getTable("names" );$result = $table->select('name','age') ->where('name like :name and age > :age') ->bind(['name' => 'John', ' age' => 42]) ->orderBy('age desc')  ->execute();$row = $result->fetchAll();?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[name] => John
[age] => 42
)
)
