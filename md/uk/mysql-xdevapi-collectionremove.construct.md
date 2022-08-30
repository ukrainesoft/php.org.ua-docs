Конструктор класу CollectionRemove

-   [« CollectionRemove::bind](mysql-xdevapi-collectionremove.bind.html)
    
-   [CollectionRemove::execute »](mysql-xdevapi-collectionremove.execute.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiCollectionRemove](class.mysql-xdevapi-collectionremove.html)
    
-   Конструктор класу CollectionRemove
    

# CollectionRemove::construct

(No version information available, might only be in Git)

CollectionRemove::construct — Конструктор класу CollectionRemove

### Опис

private **mysqlxdevapiCollectionRemove::construct**

Видаляє документи колекції та створюється екземпляром методу Collection::remove().

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollection::remove()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$collection->add('{"name": "Alfred", "age": 18, "job": "Butler"}')->execute();
$collection->add('{"name": "Bob",    "age": 19, "job": "Painter"}')->execute();

// Удаление всех художников
$collection
  ->remove("job in ('Painter')")
  ->execute();

// Удалить самого старого дворецкого
$collection
  ->remove("job in ('Butler')")
  ->sort('age desc')
  ->limit(1)
  ->execute();

// Удалить запись с самым низким возрастом
$collection
  ->remove('true')
  ->sort('age desc')
  ->limit(1)
  ->execute();
?>
```