---
navigation:
  - mysql-xdevapi-result.construct.md: '« Result::\_\_construct'
  - mysql-xdevapi-result.getautoincrementvalue.md: 'Result::getAutoIncrementValue »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-result.md: mysql\_xdevapi\\Result
title: 'Result::getAffectedItemsCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

**Приклад #1 Приклад використання** mysql\_xdevapi\\Result::getAffectedItemsCount()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$collection = $schema->getCollection("people");

$result = $collection->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')->execute();

var_dump( $res->getAffectedItemsCount() );
?>
```

Результат виконання наведеного прикладу:

```
int(1)
```
