---
navigation:
  - mysql-xdevapi-tableselect.limit.md: '« TableSelect::limit'
  - mysql-xdevapi-tableselect.lockshared.md: 'TableSelect::lockShared »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-tableselect.md: mysql\_xdevapi\\TableSelect
title: 'TableSelect::lockExclusive'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# TableSelect::lockExclusive

(No version information available, might only be in Git)

TableSelect::lockExclusive — Виконує EXCLUSIVE LOCK

### Опис

```methodsynopsis
public mysql_xdevapi\TableSelect::lockExclusive(int $lock_waiting_option = ?): mysql_xdevapi\TableSelect
```

Виконує операцію читання із EXCLUSIVE LOCK. Лише один замок може бути активним одночасно.

### Список параметрів

`lock_waiting_option`

Необов'язковий параметр очікування, який за замовчуванням дорівнює **`MYSQLX_LOCK_DEFAULT`**. Допустимі значення:

-   **`MYSQLX_LOCK_DEFAULT`**
    
-   **`MYSQLX_LOCK_NOWAIT`**
    
-   **`MYSQLX_LOCK_SKIP_LOCKED`**
    

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\TableSelect::lockExclusive()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$session->startTransaction();

$result = $table->select('name', 'age')
  ->lockExclusive(MYSQLX_LOCK_NOWAIT)
  ->execute();

$session->commit();

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
    [1] => Array
        (
            [name] => Sam
            [age] => 42
        )
)
```
