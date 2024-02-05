---
navigation:
  - mysql-xdevapi-schema.construct.md: '« Schema::\_\_construct'
  - mysql-xdevapi-schema.dropcollection.md: 'Schema::dropCollection »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::createCollection'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::createCollection

(No version information available, might only be in Git)

Schema::createCollection — Додає колекцію до схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::createCollection(string $name, string $validate = ?): mysql_xdevapi\Collection
```

Створює колекцію усередині схеми.

### Список параметрів

`name`

Ім'я колекції.

`validate`

Визначення перевірки як об'єкт JSON.

### Значення, що повертаються

Повертає об'єкт класу Collection.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.20 | Доданий необов'язковий параметр validate. |

### Приклади

**Приклад #1 Приклад использования метода**mysql\_xdevapi\\Schema::createCollection()\*\*\*\*

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

**Приклад #2 Приклад использования метода**mysql\_xdevapi\\Schema::createCollection()\*\*\*\*

```php
<?php
 $collection = $schema->createCollection("mycollection", '{
    "validation": {
        "level": "strict",
        "schema": {
            "id": "http://json-schema.org/geo",
            "description": "A geographical coordinate",
            "type": "object",
            "properties": {
                "latitude": {
                    "type": "number"
                },
                "longitude": {
                    "type": "number"
                }
            },
            "required": ["latitude", "longitude"]
        }
    }
}');
// Успешное выполнение
$collection->add('{"latitude": 10, "longitude": 20}')->execute();
// Ошибка, недопустимые типы (не числа)
$collection->add('{"latitude": "lat", "longitude": "long"}')->execute();
```
