Отримує кількість порушених рядків

-   [« Result::\_\_construct](mysql-xdevapi-result.construct.html)
    
-   [Result::getAutoIncrementValue »](mysql-xdevapi-result.getautoincrementvalue.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Result](class.mysql-xdevapi-result.html)
    
-   Отримує кількість порушених рядків
    

# Result::getAffectedItemsCount

(No version information available, might only be in Git)

Result::getAffectedItemsCount — Отримує кількість порушених рядків

### Опис

```methodsynopsis
public mysql_xdevapi\Result::getAffectedItemsCount(): int
```

Отримує кількість рядків, порушених попередньою операцією.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість (як ціле число) порушених рядків.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiResult::getAffectedItemsCount()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$collection = $schema->getCollection("people");

$result = $collection->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')->execute();

var_dump( $res->getAffectedItemsCount() );
?>
```

Результат виконання цього прикладу:

```
int(1)
```