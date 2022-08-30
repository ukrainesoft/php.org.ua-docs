Отримує кількість попереджень останньої операції

-   [« BaseResult::getWarnings](mysql-xdevapi-baseresult.getwarnings.html)
    
-   [mysqlxdevapiClient »](class.mysql-xdevapi-client.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlxdevapiBaseResult](class.mysql-xdevapi-baseresult.html)
    
-   Отримує кількість попереджень останньої операції
    

# BaseResult::getWarningsCount

(No version information available, might only be in Git)

BaseResult::getWarningsCount — Отримує кількість попереджень останньої операції

### Опис

```methodsynopsis
abstract public mysql_xdevapi\BaseResult::getWarningsCount(): int
```

Повертає кількість попереджень, виданих останньою операцією. Зокрема ці попередження викликаються сервером MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість попереджень останньої операції.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiRowResult::getWarningsCount()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS foo")->execute();
$session->sql("CREATE DATABASE foo")->execute();
$session->sql("CREATE TABLE foo.test_table(x int)")->execute();

$schema = $session->getSchema("foo");
$table  = $schema->getTable("test_table");

$table->insert(['x'])->values([1])->values([2])->execute();

$res = $table->select(['x/0 as bad_x'])->execute();

echo $res->getWarningsCount();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
2
```