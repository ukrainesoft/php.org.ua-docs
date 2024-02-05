---
navigation:
  - class.mysql-xdevapi-rowresult.md: « mysql\_xdevapi\\RowResult
  - mysql-xdevapi-rowresult.fetchall.md: 'RowResult::fetchAll »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-rowresult.md: mysql\_xdevapi\\RowResult
title: 'RowResult::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RowResult::\_\_construct

(No version information available, might only be in Git)

RowResult::\_\_construct - Конструктор класу RowResult

### Опис

private**mysql\_xdevapi\\RowResult::\_\_construct**()

Представляє набір результатів, отриманий під час звернення до бази даних.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\RowResult::\_\_construct()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$row = $table->select('name', 'age')->where('age > 18')->execute()->fetchAll();

print_r($row);
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
    [1] => Array
        (
            [name] => Sam
            [age] => 33
        )
)
```
