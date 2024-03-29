---
navigation:
  - mysql-xdevapi-collection.getsession.md: '« Collection::getSession'
  - mysql-xdevapi-collection.remove.md: 'Collection::remove »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::modify'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::modify

(No version information available, might only be in Git)

Collection::modify — Змінює документи колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::modify(string $search_condition): mysql_xdevapi\CollectionModify
```

Змінює документи колекції, які відповідають певним умовам пошуку.

### Список параметрів

`search_condition`

Параметр повинен бути допустимим виразом SQL, який використовується для відповідності документам, які потрібно змінити. Цей вираз може бути простим значенням **`true`**, що відповідає всім документам, або може використовувати функції та оператори, такі як `'CAST(_id AS SIGNED) >= 10'` `'age MOD 2 = 0 OR age MOD 3 = 0'`или`'_id IN ["2","5","7","10"]'`

### Значення, що повертаються

Якщо операцію не здійснено, функція поверне об'єкт Modify, який можна використовувати для додавання додаткових операцій MODIFY.

Якщо операція MODIFY виконана, то об'єкт, що повертається, міститиме результат операції.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Collection::modify()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$collection->add('{"name": "Альфред", "age": 18, "job": "Дворецкий"}')->execute();
$collection->add('{"name": "Боб",    "age": 19, "job": "Художник"}')->execute();

// Добавление двух работ для всех художников: артист и мастер
$collection
  ->modify("job in ('Дворецкий', 'Художник')")
  ->arrayAppend('job', 'Артист')
  ->arrayAppend('job', 'Мастер')
  ->execute();

// Удаление поля 'beer' из всех документов с возрастом 21
$collection
  ->modify('age < 21')
  ->unset(['beer'])
  ->execute();
?>
```
