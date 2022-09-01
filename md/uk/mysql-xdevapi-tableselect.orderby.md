---
navigation:
  - mysql-xdevapi-tableselect.offset.html: '« TableSelect::offset'
  - mysql-xdevapi-tableselect.where.html: 'TableSelect::where »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableselect.html: mysqlxdevapiTableSelect
title: 'TableSelect::orderby'
---
# TableSelect::orderby

(No version information available, might only be in Git)

TableSelect::orderby — Встановлює критерії сортування вибірки

### Опис

```methodsynopsis
public mysql_xdevapi\TableSelect::orderby(mixed $sort_expr, mixed ...$sort_exprs): mysql_xdevapi\TableSelect
```

Встановлює порядок за критеріями.

### Список параметрів

`sort_expr`

Вирази, що визначають порядок за критеріями. Може бути масивом з одним або декількома виразами чи рядком.

`sort_exprs`

Додаткові параметри sortexpr.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableSelect::orderBy()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('name', 'age')
  ->orderBy('name desc')
  ->execute();

$row = $result->fetchAll();
print_r($row);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
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
```
