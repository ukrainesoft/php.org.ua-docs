---
navigation:
  - class.mysql-xdevapi-schema.md: « mysqlxdevapiSchema
  - mysql-xdevapi-schema.createcollection.md: 'Schema::createCollection »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysqlxdevapiSchema
title: 'Schema::construct'
---
# Schema::construct

(No version information available, might only be in Git)

Schema::construct — Конструктор

### Опис

private **mysqlxdevapiSchema::construct**

Об'єкт Schema надає повний доступ до схеми (бази даних).

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSchema::construct()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS food")->execute();
$session->sql("CREATE DATABASE food")->execute();
$session->sql("CREATE TABLE food.fruit(name text, rating text)")->execute();

$schema = $session->getSchema("food");
$schema->createCollection("trees");

print_r($schema->gettables());
print_r($schema->getcollections());
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [fruit] => mysql_xdevapi\Table Object
        (
            [name] => fruit
        )
)
Array
(
    [trees] => mysql_xdevapi\Collection Object
        (
            [name] => trees
        )
)
```
