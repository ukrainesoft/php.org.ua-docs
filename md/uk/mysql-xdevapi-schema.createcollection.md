Додати колекцію до схеми

-   [« Schema::\_\_construct](mysql-xdevapi-schema.construct.html)
    
-   [Schema::dropCollection »](mysql-xdevapi-schema.dropcollection.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Schema](class.mysql-xdevapi-schema.html)
    
-   Додати колекцію до схеми
    

# Schema::createCollection

(No version information available, might only be in Git)

Schema::createCollection — Додати колекцію до схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::createCollection(string $name, string $validate = ?): mysql_xdevapi\Collection
```

Створити колекцію усередині схеми.

### Список параметрів

`name`

Ім'я колекції.

`validate`

Визначення перевірки як об'єкт JSON.

### Значення, що повертаються

Колекція об'єкта.

### список змін

| Версия | Описание                                  |
|--------|-------------------------------------------|
|        | Доданий необов'язковий параметр validate. |

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

**Приклад #2 Приклад використання Schema::createCollection з параметром validate**

```php
<?php
 $collection = $schema->createCollection("mycollection", '{
    "validation": {
        "level": "strict",
        "schema": {
            "id": "http://json-schema.org/geo",
            "description": "A geographical coordinate",
            "type": "object",
            "properties": {
                "latitude": {
                    "type": "number"
                },
                "longitude": {
                    "type": "number"
                }
            },
            "required": ["latitude", "longitude"]
        }
    }
}');
// Успешное выполнение
$collection->add('{"latitude": 10, "longitude": 20}')->execute();
// Ошибка, недопустимые типы (не числа)
$collection->add('{"latitude": "lat", "longitude": "long"}')->execute();
```