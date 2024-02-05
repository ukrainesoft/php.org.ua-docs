---
navigation:
  - mysql-xdevapi-schema.createcollection.md: '« Schema::createCollection'
  - mysql-xdevapi-schema.existsindatabase.md: 'Schema::existsInDatabase »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::dropCollection'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::dropCollection

(No version information available, might only be in Git)

Schema::dropCollection — Видаляє колекції зі схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::dropCollection(string $collection_name): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`collection_name`

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования метода**mysql\_xdevapi\\Schema::dropCollection()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS food")->execute();
$session->sql("CREATE DATABASE food")->execute();
$session->sql("CREATE TABLE food.fruit(name text, rating text)")->execute();

$schema = $session->getSchema("food");

$schema->createCollection("trees");
$schema->dropCollection("trees");
$schema->createCollection("buildings");

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
    [buildings] => mysql_xdevapi\Collection Object
        (
            [name] => buildings
        )
)
```
