Встановлює критерії угруповання вибірки

-   [« TableSelect::execute](mysql-xdevapi-tableselect.execute.html)
    
-   [TableSelect::having »](mysql-xdevapi-tableselect.having.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\TableSelect](class.mysql-xdevapi-tableselect.html)
    
-   Встановлює критерії угруповання вибірки
    

# TableSelect::groupBy

(No version information available, might only be in Git)

TableSelect::groupBy — Встановлює критерії угруповання вибірки

### Опис

```methodsynopsis
public mysql_xdevapi\TableSelect::groupBy(mixed $sort_expr): mysql_xdevapi\TableSelect
```

Встановлює критерії угруповання для набору результатів.

### Список параметрів

`sort_expr`

Критерії угруповання.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableSelect::groupBy()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 42)")->execute();
$session->sql("INSERT INTO addressbook.names values ('Suki', 31)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('count(*) as count', 'age')
  ->groupBy('age')->orderBy('age asc')
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
            [count] => 1
            [age] => 31
        )
    [1] => Array
        (
            [count] => 2
            [age] => 42
        )
)
```