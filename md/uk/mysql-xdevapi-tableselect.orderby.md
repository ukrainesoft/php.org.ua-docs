- [«TableSelect::offset](mysql-xdevapi-tableselect.offset.md)
- [TableSelect::where »](mysql-xdevapi-tableselect.where.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\TableSelect](class.mysql-xdevapi-tableselect.md)
- Встановлює критерії сортування вибірки

# TableSelect::orderby

(No version information available, might only be in Git)

TableSelect::orderby — Встановлює критерії сортування вибірки

### Опис

public
**mysql_xdevapi\TableSelect::orderby**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$sort_expr`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$sort_exprs`):
[mysql_xdevapi\TableSelect](class.mysql-xdevapi-tableselect.md)

Встановлює порядок за критеріями.

### Список параметрів

`sort_expr`
Вирази, що визначають порядок за критеріями. Може бути масивом
з одним або декількома виразами чи рядком.

`sort_exprs`
Додаткові опції sort_expr.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\TableSelect::orderBy()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$schema = $session->getSchema("addressbook");$table  = $schema->getTable("names" );$result = $table->select('name', 'age') ->orderBy('name desc') ->execute();$row = $result->fetchAll();print_r($row) ;?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[name] => Sam
[age] => 42
)
[1] => Array
(
[name] => John
[age] => 42
)
)
