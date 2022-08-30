Виконує затвердження

-   [« mysqlxdevapiExecutable](class.mysql-xdevapi-executable.html)
    
-   [mysqlxdevapiExecutionStatus »](class.mysql-xdevapi-executionstatus.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiExecutable](class.mysql-xdevapi-executable.html)
    
-   Виконує затвердження
    

# Executable::execute

(No version information available, might only be in Git)

Executable::execute — Виконує затвердження

### Опис

```methodsynopsis
abstract public mysql_xdevapi\Executable::execute(): mysql_xdevapi\Result
```

Виконує затвердження з операції збору чи запиту таблиці; ця функціональність дозволена для ланцюжка методів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Один із об'єктів Result, наприклад, Result або SqlStatementResult.

### Приклади

**Приклад #1 Приклади використання execute()**

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$result_sql = $session->sql("CREATE DATABASE addressbook")->execute();

var_dump($result_sql);


$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("humans");

$result_collection = $collection->add(
  '{"name": "Jane",
    "jobs": [{"title":"Scientist","Salary":18000}, {"title":"Mother","Salary":0}],
    "hobbies": ["Walking","Making pies"]}');

$result_collection_executed = $result_collection->execute();

var_dump($result_collection);
var_dump($result_collection_executed);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(mysql_xdevapi\SqlStatementResult)#3 (0) {
}

object(mysql_xdevapi\CollectionAdd)#5 (0) {
}

object(mysql_xdevapi\Result)#7 (0) {
}
```