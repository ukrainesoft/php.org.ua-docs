---
navigation:
  - class.mysql-xdevapi-schema.md: « mysql\_xdevapi\\Schema
  - mysql-xdevapi-schema.createcollection.md: 'Schema::createCollection »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::\_\_construct

(No version information available, might only be in Git)

Schema::\_\_construct - Конструктор класу Schema

### Опис

private **mysql\_xdevapi\\Schema::\_\_construct**()

Об'єкт класу Schema надає повний доступ до схеми (бази даних).

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад использования метода**mysql\_xdevapi\\Schema::\_\_construct()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS food")->execute();
$session->sql("CREATE DATABASE food")->execute();
$session->sql("CREATE TABLE food.fruit(name text, rating text)")->execute();

$schema = $session->getSchema("food");
$schema->createCollection("trees");

print_r($schema->gettables());
print_r($schema->getcollections());
```

Висновок наведеного прикладу буде схожим на:

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
