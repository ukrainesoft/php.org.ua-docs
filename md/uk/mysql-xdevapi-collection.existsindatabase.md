Перевіряє, чи існує колекція у базі даних

-   [« Collection::dropIndex](mysql-xdevapi-collection.dropindex.html)
    
-   [Collection::find »](mysql-xdevapi-collection.find.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Collection](class.mysql-xdevapi-collection.html)
    
-   Перевіряє, чи існує колекція у базі даних
    

# Collection::existsInDatabase

(No version information available, might only be in Git)

Collection::existsInDatabase — Перевіряє, чи існує колекція в базі даних

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::existsInDatabase(): bool
```

Перевіряє, чи об'єкт Collection посилається на колекцію в базі даних (схему).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** якщо колекція існує у базі даних, інакше **`false`** якщо це не так.

Таблиця, визначена двома стовпцями (doc і id), вважається колекцією, та третім стовпцем jsonschema із MySQL 8.0.21. Додавання додаткового стовпця означає, що existsInDatabase() більше не буде бачити його як колекцію.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollection::existsInDatabase()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

// ...

$collection = $schema->getCollection("people");

// ...

if (!$collection->existsInDatabase()) {
    echo "Коллекция с именем addressbook не существует в базе данных. Что случилось?";
}
?>
```