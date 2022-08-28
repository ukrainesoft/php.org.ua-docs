Конструктор класу Collection

-   [« Collection::addOrReplaceOne](mysql-xdevapi-collection.addorreplaceone.html)
    
-   [Collection::count »](mysql-xdevapi-collection.count.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Collection](class.mysql-xdevapi-collection.html)
    
-   Конструктор класу Collection
    

# Collection::construct

(No version information available, might only be in Git)

Collection::construct - Конструктор класу Collection

### Опис

private **mysqlxdevapiCollection::construct**

Створює об'єкт Collection.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollection::getOne()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$result = $collection->add('{"name": "Alfred", "age": 42, "job": "Butler"}')->execute();

// Уникальный _id (по умолчанию и рекомендуется) генерируется MySQL Server
// Возвращает сгенерированные _id; в этом примере добавлена только одна запись, поэтому $ids[0]
$ids        = $result->getGeneratedIds();
$alfreds_id = $ids[0];

// ...

print_r($alfreds_id);
print_r($collection->getOne($alfreds_id));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
00005b6b536100000000000000b1

Array
(
    [_id] => 00005b6b536100000000000000b1
    [age] => 42
    [job] => Butler
    [name] => Alfred
)
```