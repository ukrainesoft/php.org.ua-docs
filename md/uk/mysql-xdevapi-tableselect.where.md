---
navigation:
  - mysql-xdevapi-tableselect.orderby.md: '« TableSelect::orderby'
  - class.mysql-xdevapi-tableupdate.md: mysqlxdevapiTableUpdate »
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableselect.md: mysqlxdevapiTableSelect
title: 'TableSelect::where'
---
# TableSelect::where

(No version information available, might only be in Git)

TableSelect::where — Встановлює умову пошуку вибірки

### Опис

```methodsynopsis
public mysql_xdevapi\TableSelect::where(string $where_expr): mysql_xdevapi\TableSelect
```

Встановлює умову пошуку фільтрації.

### Список параметрів

`where_expr`

Визначає умову пошуку фільтрації документів або записів.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableSelect::where()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('name','age')
  ->where('name like :name and age > :age')
  ->bind(['name' => 'John', 'age' => 42])
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
            [name] => John
            [age] => 42
        )
)
```
