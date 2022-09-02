---
navigation:
  - class.mysql-xdevapi-columnresult.md: « mysqlxdevapiColumnResult
  - mysql-xdevapi-columnresult.getcharactersetname.md: 'ColumnResult::getCharacterSetName »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-columnresult.md: mysqlxdevapiColumnResult
title: 'ColumnResult::construct'
---
# ColumnResult::construct

(No version information available, might only be in Git)

ColumnResult::construct - Конструктор класу ColumnResult

### Опис

private **mysqlxdevapiColumnResult::construct**

Отримує метадані стовпця, такі як набір символів; створюється методом RowResult::getColumns().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiColumnResult::construct()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS nonsense")->execute();
$session->sql("CREATE DATABASE nonsense")->execute();
$session->sql("CREATE TABLE nonsense.numbers (hello int, world float unsigned)")->execute();
$session->sql("INSERT INTO  nonsense.numbers values (42, 42)")->execute();

$schema = $session->getSchema("nonsense");
$table  = $schema->getTable("numbers");

$result1 = $table->select('hello','world')->execute();

// Возвращает Масив объектов ColumnResult
$columns = $result1->getColumns();

foreach ($columns as $column) {
    echo "\nМетка столбца " , $column->getColumnLabel();
    echo " является типом "       , $column->getType();
    echo " и ", ($column->isNumberSigned() === 0) ? "Неподписан." : "Подписан.";
}

// Альтернативный вариант
$result2 = $session->sql("SELECT * FROM nonsense.numbers")->execute();

// Возвращает Масив объектов FieldMetadata
print_r($result2->getColumns());
```

Результатом виконання цього прикладу буде щось подібне:

```
Метка столбца hello является типом 19 и Подписан.
Метка столбца world является типом 4 и Неподписан.

Array
(
    [0] => mysql_xdevapi\FieldMetadata Object
        (
            [type] => 1
            [type_name] => SINT
            [name] => hello
            [original_name] => hello
            [table] => numbers
            [original_table] => numbers
            [schema] => nonsense
            [catalog] => def
            [collation] => 0
            [fractional_digits] => 0
            [length] => 11
            [flags] => 0
            [content_type] => 0
        )
    [1] => mysql_xdevapi\FieldMetadata Object
        (
            [type] => 6
            [type_name] => FLOAT
            [name] => world
            [original_name] => world
            [table] => numbers
            [original_table] => numbers
            [schema] => nonsense
            [catalog] => def
            [collation] => 0
            [fractional_digits] => 31
            [length] => 12
            [flags] => 1
            [content_type] => 0
        )
)
```
