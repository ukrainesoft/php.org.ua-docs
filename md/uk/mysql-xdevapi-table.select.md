---
navigation:
  - mysql-xdevapi-table.isview.md: '« Table::isView'
  - mysql-xdevapi-table.update.md: 'Table::update »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.md: mysqlxdevapiTable
title: 'Table::select'
---
# Table::select

(No version information available, might only be in Git)

Table::select — Вибрати рядки з таблиці

### Опис

```methodsynopsis
public mysql_xdevapi\Table::select(mixed $columns, mixed ...$more_columns): mysql_xdevapi\TableSelect
```

Витягує дані з таблиці.

### Список параметрів

`columns`

Стовпчики для вибору даних. Може бути масивом з одним або декількома значеннями чи рядком.

`more_columns`

Додаткові визначення параметрів шпальт.

### Значення, що повертаються

Об'єкт TableSelect; використовуйте метод execute() для виконання select та повернення об'єкта RowResult.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTable::count()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$row = $table->select('name', 'age')->execute()->fetchAll();

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
