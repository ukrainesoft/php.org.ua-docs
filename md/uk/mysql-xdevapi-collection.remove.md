Видаляє документи колекції

-   [« Collection::modify](mysql-xdevapi-collection.modify.html)
    
-   [Collection::removeOne »](mysql-xdevapi-collection.removeone.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Collection](class.mysql-xdevapi-collection.html)
    
-   Видаляє документи колекції
    

# Collection::remove

(No version information available, might only be in Git)

Collection::remove — Видаляє документи колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::remove(string $search_condition): mysql_xdevapi\CollectionRemove
```

Видаляє колекції, які відповідають певним умовам пошуку. Дозволяється кілька операцій та підтримується прив'язка параметрів.

### Список параметрів

`search_condition`

Має бути коректним виразом SQL, що використовується для зіставлення документів, які потрібно змінити. Вираз може бути таким самим простим, як **`true`**, яке відповідає всім документам, або воно може використовувати функції та оператори, такі як `'CAST(_id AS SIGNED) >= 10'` `'age MOD 2 = 0 OR age MOD 3 = 0'`, або `'_id IN ["2","5","7","10"]'`

### Значення, що повертаються

Якщо операцію не здійснено, функція поверне об'єкт Remove, який можна використовувати для додавання додаткових операцій видалення.

Якщо операцію видалення виконано, то повернутий об'єкт міститиме результат операції.

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

// Удаление самого старого дворецкого
$collection
  ->remove("job in ('Butler')")
  ->sort('age desc')
  ->limit(1)
  ->execute();

// Удаление записи с самым низким возрастом
$collection
  ->remove('true')
  ->sort('age desc')
  ->limit(1)
  ->execute();
?>
```