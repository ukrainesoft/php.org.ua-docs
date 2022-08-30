Отримує значення автоінкремента

-   [« Result::getAffectedItemsCount](mysql-xdevapi-result.getaffecteditemscount.html)
    
-   [Result::getGeneratedIds »](mysql-xdevapi-result.getgeneratedids.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiResult](class.mysql-xdevapi-result.html)
    
-   Отримує значення автоінкремента
    

# Result::set Auto\_Increment Value

(No version information available, might only be in Git)

Result::getAutoIncrementValue — Отримує значення автоінкремента

### Опис

```methodsynopsis
public mysql_xdevapi\Result::getAutoIncrementValue(): int
```

Отримує останнє значення AUTOINCREMENT (ідентифікатор останньої вставки).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення AUTOINCREMENT.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiResult::set Auto\_Increment Value()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("
  CREATE TABLE addressbook.names
    (id INT NOT NULL AUTO_INCREMENT, name VARCHAR(30), age INT, PRIMARY KEY (id))
  ")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->insert("name", "age")->values(["Suzanne", 31],["Julie", 43])->execute();
$result = $table->insert("name", "age")->values(["Suki", 34])->execute();

$ai = $result->getAutoIncrementValue();
var_dump($ai);
?>
```

Результат виконання цього прикладу:

```
int(3)
```