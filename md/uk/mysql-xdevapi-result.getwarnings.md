Отримує попередження останньої операції

-   [« Result::getGeneratedIds](mysql-xdevapi-result.getgeneratedids.html)
    
-   [Result::getWarningsCount »](mysql-xdevapi-result.getwarningscount.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlxdevapiResult](class.mysql-xdevapi-result.html)
    
-   Отримує попередження останньої операції
    

# Result::getWarnings

(No version information available, might only be in Git)

Result::getWarnings — Отримує попередження останньої операції

### Опис

```methodsynopsis
public mysql_xdevapi\Result::getWarnings(): array
```

Отримує попередження останньої операції Result.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів Warning останньої операції. Кожен об'єкт визначає 'message' про помилку, 'level' помилки та 'code' помилки. Повертається порожній масив, якщо помилок немає.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiRowResult::getWarnings()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("CREATE DATABASE foo")->execute();
$session->sql("CREATE TABLE foo.test_table(x int)")->execute();

$schema = $session->getSchema("foo");
$table  = $schema->getTable("test_table");

$table->insert(['x'])->values([1])->values([2])->execute();

$res = $table->select(['x/0 as bad_x'])->execute();
$warnings = $res->getWarnings();

print_r($warnings);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => mysql_xdevapi\Warning Object
        (
            [message] => Division by 0
            [level] => 2
            [code] => 1365
        )
    [1] => mysql_xdevapi\Warning Object
        (
            [message] => Division by 0
            [level] => 2
            [code] => 1365
        )
)
```