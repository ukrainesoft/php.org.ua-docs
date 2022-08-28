Виконує EXCLUSIVE LOCK

-   [« TableSelect::limit](mysql-xdevapi-tableselect.limit.html)
    
-   [TableSelect::lockShared »](mysql-xdevapi-tableselect.lockshared.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\TableSelect](class.mysql-xdevapi-tableselect.html)
    
-   Виконує EXCLUSIVE LOCK
    

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

**Приклад #1 Приклад використання **mysqlxdevapiTableSelect::lockExclusive()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$session->startTransaction();

$result = $table->select('name', 'age')
  ->lockExclusive(MYSQLX_LOCK_NOWAIT)
  ->execute();

$session->commit();

$row = $result->fetchAll();
print_r($row);
?>
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
            [age] => 42
        )
)
```