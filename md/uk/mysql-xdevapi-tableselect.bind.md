- [«mysql_xdevapi\TableSelect](class.mysql-xdevapi-tableselect.md)
- [TableSelect::\_\_construct »](mysql-xdevapi-tableselect.construct.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\TableSelect](class.mysql-xdevapi-tableselect.md)
- Прив'язує параметри запиту вибірки

# TableSelect::bind

(No version information available, might only be in Git)

TableSelect::bind — Прив'язує параметри запиту вибірки

### Опис

public **mysql_xdevapi\TableSelect::bind**(array `$placeholder_values`):
[mysql_xdevapi\TableSelect](class.mysql-xdevapi-tableselect.md)

Прив'язує значення до певного наповнювача.

### Список параметрів

`placeholder_values`
Назва заповнювача та значення для прив'язки.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Приклад #1 Приклад використання **mysql_xdevapi\TableSelect::bind()****

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
