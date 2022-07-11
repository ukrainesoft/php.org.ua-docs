- [«TableSelect::orderby](mysql-xdevapi-tableselect.orderby.md)
- [mysql_xdevapi\TableUpdate »](class.mysql-xdevapi-tableupdate.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\TableSelect](class.mysql-xdevapi-tableselect.md)
- Встановлює умову пошуку вибірки

# TableSelect::where

(No version information available, might only be in Git)

TableSelect::where — Встановлює умову пошуку вибірки

### Опис

public **mysql_xdevapi\TableSelect::where**(string `$where_expr`):
[mysql_xdevapi\TableSelect](class.mysql-xdevapi-tableselect.md)

Встановлює умову пошуку фільтрації.

### Список параметрів

`where_expr`
Визначає умову пошуку фільтрації документів або записів.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\TableSelect::where()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$schema = $session->getSchema("addressbook");$table  = $schema->getTable("names" );$result = $table->select('name','age') ->where('name like :name and age > :age') ->bind(['name' => 'John', ' age' => 42]) ->execute();$row = $result->fetchAll();print_r($row);?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[name] => John
[age] => 42
)
)
