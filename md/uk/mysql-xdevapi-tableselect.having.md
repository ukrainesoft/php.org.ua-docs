---
navigation:
  - mysql-xdevapi-tableselect.groupby.md: '« TableSelect::groupBy'
  - mysql-xdevapi-tableselect.limit.md: 'TableSelect::limit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableselect.md: mysqlxdevapiTableSelect
title: 'TableSelect::having'
---
# TableSelect::having

(No version information available, might only be in Git)

TableSelect::having — Встановлює вибір з умовою

### Опис

```methodsynopsis
public mysql_xdevapi\TableSelect::having(string $sort_expr): mysql_xdevapi\TableSelect
```

Встановлює умову для записів до розгляду в операціях агрегатної функції.

### Список параметрів

`sort_expr`

Умова для агрегатних функцій, що використовуються в умовах угруповання.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableSelect::having()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 42)")->execute();
$session->sql("INSERT INTO addressbook.names values ('Suki', 31)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('count(*) as count', 'age')
  ->groupBy('age')->orderBy('age asc')
  ->having('count > 1')
  ->execute();

$row = $result->fetchAll();
print_r($row);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => Array
        (
            [count] => 2
            [age] => 42
        )
)
```
