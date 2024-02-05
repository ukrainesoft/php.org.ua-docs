---
navigation:
  - mysql-xdevapi-tableselect.construct.md: '« TableSelect::\_\_construct'
  - mysql-xdevapi-tableselect.groupby.md: 'TableSelect::groupBy »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableselect.md: mysql\_xdevapi\\TableSelect
title: 'TableSelect::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableSelect::execute

(No version information available, might only be in Git)

TableSelect::execute — Виконує оператор вибірки

### Опис

```methodsynopsis
public mysql_xdevapi\TableSelect::execute(): mysql_xdevapi\RowResult
```

Виконує затвердження вибірки, пов'язуючи його із методом execute().

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт RowResult.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\TableSelect::execute()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('name','age')
  ->where('name like :name and age > :age')
  ->bind(['name' => 'John', 'age' => 42])
  ->orderBy('age desc')
  ->execute();

$row = $result->fetchAll();
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
