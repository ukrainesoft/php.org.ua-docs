---
navigation:
  - class.mysql-xdevapi-columnresult.md: « mysql\_xdevapi\\ColumnResult
  - mysql-xdevapi-columnresult.getcharactersetname.md: 'ColumnResult::getCharacterSetName »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-columnresult.md: mysql\_xdevapi\\ColumnResult
title: 'ColumnResult::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ColumnResult::\_\_construct

(No version information available, might only be in Git)

ColumnResult::\_\_construct - Конструктор класу ColumnResult

### Опис

private**mysql\_xdevapi\\ColumnResult::\_\_construct**()

Отримує метадані стовпця, такі як набір символів; створюється методом **mysql\_xdevapi\\RowResult::getColumns()**

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Пример #1 Пример использования метода**mysql\_xdevapi\\ColumnResult::\_\_construct()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS nonsense")->execute();
$session->sql("CREATE DATABASE nonsense")->execute();
$session->sql("CREATE TABLE nonsense.numbers (hello int, world float unsigned)")->execute();
$session->sql("INSERT INTO  nonsense.numbers values (42, 42)")->execute();

$schema = $session->getSchema("nonsense");
$table  = $schema->getTable("numbers");

$result1 = $table->select('hello','world')->execute();

// Возвращает массив объектов ColumnResult
$columns = $result1->getColumns();

foreach ($columns as $column) {
    echo "\nМетка столбца " , $column->getColumnLabel();
    echo " принадлежит типу "       , $column->getType();
    echo " и это ", ($column->isNumberSigned() === 0) ? "беззнаковое число." : "знаковое число.";
}

// Альтернативный вариант
$result2 = $session->sql("SELECT * FROM nonsense.numbers")->execute();

// Возвращает массив объектов FieldMetadata
print_r($result2->getColumns());
```

Висновок наведеного прикладу буде схожим на:

```
Метка столбца hello принадлежит типу 19 и это знаковое число.
Метка столбца world принадлежит типу 4 и это беззнаковое число.

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
