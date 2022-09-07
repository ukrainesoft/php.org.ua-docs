---
navigation:
  - class.mysql-xdevapi-result.md: « mysqlxdevapiResult
  - mysql-xdevapi-result.getaffecteditemscount.md: 'Result::getAffectedItemsCount »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-result.md: mysqlxdevapiResult
title: 'Result::construct'
---
# Result::construct

(No version information available, might only be in Git)

Result::construct - Конструктор класу Result

### Опис

private **mysqlxdevapiResult::construct**

Об'єкт, який витягує згенеровані ідентифікатори, значення AUTOINCREMENT та попередження для набору Result.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiResult::construct()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("
  CREATE TABLE addressbook.names
    (id INT NOT NULL AUTO_INCREMENT, name VARCHAR(30), age INT, PRIMARY KEY (id))
  ")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->insert("name", "age")->values(["Suzanne", 31],["Julie", 43])->execute();
$result = $table->insert("name", "age")->values(["Suki", 34])->execute();

$ai = $result->getAutoIncrementValue();
var_dump($ai);
?>
```

Результат виконання цього прикладу:

```
int(3)
```
