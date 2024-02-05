---
navigation:
  - class.mysql-xdevapi-tableselect.md: « mysql\_xdevapi\\TableSelect
  - mysql-xdevapi-tableselect.construct.md: 'TableSelect::\_\_construct »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableselect.md: mysql\_xdevapi\\TableSelect
title: 'TableSelect::bind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableSelect::bind

(No version information available, might only be in Git)

TableSelect::bind — Прив'язує параметри запиту вибірки

### Опис

```methodsynopsis
public mysql_xdevapi\TableSelect::bind(array $placeholder_values): mysql_xdevapi\TableSelect
```

Прив'язує значення до певного наповнювача.

### Список параметрів

`placeholder_values`

Назва заповнювача та значення для прив'язки.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\TableSelect::bind()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('name','age')
  ->where('name like :name and age > :age')
  ->bind(['name' => 'John', 'age' => 42])
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
