Отримати колекцію зі схеми

-   [« Schema::existsInDatabase](mysql-xdevapi-schema.existsindatabase.html)
    
-   [Schema::getCollectionAsTable »](mysql-xdevapi-schema.getcollectionastable.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiSchema](class.mysql-xdevapi-schema.html)
    
-   Отримати колекцію зі схеми
    

# Schema::getCollection

(No version information available, might only be in Git)

Schema::getCollection — Отримати колекцію зі схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getCollection(string $name): mysql_xdevapi\Collection
```

Отримати колекцію зі схеми.

### Список параметрів

`name`

Ім'я колекції для отримання.

### Значення, що повертаються

Об'єкт Collection для вибраної колекції.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSchema::getCollection()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS food")->execute();
$session->sql("CREATE DATABASE food")->execute();

$schema = $session->getSchema("food");
$schema->createCollection("trees");

// ...

$trees = $schema->getCollection("trees");

var_dump($trees);
```

Результатом виконання цього прикладу буде щось подібне:

```
object(mysql_xdevapi\Collection)#3 (1) {
  ["name"]=>
  string(5) "trees"
}
```