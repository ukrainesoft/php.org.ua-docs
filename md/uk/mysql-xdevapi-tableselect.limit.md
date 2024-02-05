---
navigation:
  - mysql-xdevapi-tableselect.having.md: '« TableSelect::having'
  - mysql-xdevapi-tableselect.lockexclusive.md: 'TableSelect::lockExclusive »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableselect.md: mysql\_xdevapi\\TableSelect
title: 'TableSelect::limit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableSelect::limit

(No version information available, might only be in Git)

TableSelect::limit — Обмежує вибрані рядки

### Опис

```methodsynopsis
public mysql_xdevapi\TableSelect::limit(int $rows): mysql_xdevapi\TableSelect
```

Встановлює максимальну кількість записів або документів для повернення.

### Список параметрів

`rows`

Максимальна кількість записів чи документів.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\TableSelect::limit()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('name', 'age')
  ->limit(1)
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
