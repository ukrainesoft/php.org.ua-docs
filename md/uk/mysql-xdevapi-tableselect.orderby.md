---
navigation:
  - mysql-xdevapi-tableselect.offset.md: '« TableSelect::offset'
  - mysql-xdevapi-tableselect.where.md: 'TableSelect::where »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableselect.md: mysql\_xdevapi\\TableSelect
title: 'TableSelect::orderby'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableSelect::orderby

(No version information available, might only be in Git)

TableSelect::orderby — Встановлює критерії сортування вибірки

### Опис

```methodsynopsis
public mysql_xdevapi\TableSelect::orderby(mixed $sort_expr, mixed ...$sort_exprs): mysql_xdevapi\TableSelect
```

Встановлює порядок за критеріями.

### Список параметрів

`sort_expr`

Вирази, що визначають порядок за критеріями. Може бути масивом з одним або декількома виразами чи рядком.

`sort_exprs`

Додаткові параметри sort\_expr.

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\TableSelect::orderBy()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->select('name', 'age')
  ->orderBy('name desc')
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
            [name] => Sam
            [age] => 42
        )
    [1] => Array
        (
            [name] => John
            [age] => 42
        )
)
```
