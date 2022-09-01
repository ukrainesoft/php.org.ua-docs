---
navigation:
  - mysql-xdevapi-schema.createcollection.html: '« Schema::createCollection'
  - mysql-xdevapi-schema.existsindatabase.html: 'Schema::existsInDatabase »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.html: mysqlxdevapiSchema
title: 'Schema::dropCollection'
---
# Schema::dropCollection

(No version information available, might only be in Git)

Schema::dropCollection — Видалити колекції зі схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::dropCollection(string $collection_name): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`collection_name`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSchema::getCollection()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS food")->execute();
$session->sql("CREATE DATABASE food")->execute();
$session->sql("CREATE TABLE food.fruit(name text, rating text)")->execute();

$schema = $session->getSchema("food");

$schema->createCollection("trees");
$schema->dropCollection("trees");
$schema->createCollection("buildings");

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
    [buildings] => mysql_xdevapi\Collection Object
        (
            [name] => buildings
        )
)
```
