---
navigation:
  - class.mysql-xdevapi-rowresult.md: « mysqlxdevapiRowResult
  - mysql-xdevapi-rowresult.fetchall.md: 'RowResult::fetchAll »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-rowresult.md: mysqlxdevapiRowResult
title: 'RowResult::construct'
---
# RowResult::construct

(No version information available, might only be in Git)

RowResult::construct - Конструктор класу RowResult

### Опис

private **mysqlxdevapiRowResult::construct**

Представляє набір результатів, отриманий під час звернення до бази даних.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiRowResult::construct()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$row = $table->select('name', 'age')->where('age > 18')->execute()->fetchAll();

print_r($row);
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
    [1] => Array
        (
            [name] => Sam
            [age] => 33
        )
)
```
