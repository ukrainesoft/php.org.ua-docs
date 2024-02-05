---
navigation:
  - mysql-xdevapi-tableselect.bind.md: '« TableSelect::bind'
  - mysql-xdevapi-tableselect.execute.md: 'TableSelect::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableselect.md: mysql\_xdevapi\\TableSelect
title: 'TableSelect::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableSelect::\_\_construct

(No version information available, might only be in Git)

TableSelect::\_\_construct - Конструктор класу TableSelect

### Опис

private **mysql\_xdevapi\\TableSelect::\_\_construct**()

Об'єкт, який повертається методом select(); Використовуйте execute() для виконання запиту.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\TableSelect::\_\_construct()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('name','age')
  ->where('name like :name and age > :age')
  ->bind(['name' => 'John', 'age' => 42])
  ->orderBy('age desc')
  ->execute();

$row = $result->fetchAll();
print_r($row);

?>
```

Висновок наведеного прикладу буде схожим на:

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
