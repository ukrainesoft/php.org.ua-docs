---
navigation:
  - mysql-xdevapi-collection.removeone.md: '« Collection::removeOne'
  - class.mysql-xdevapi-collectionadd.md: mysql\_xdevapi\\CollectionAdd »
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::replaceOne'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::replaceOne

(No version information available, might only be in Git)

Collection::replaceOne — Замінює один документ колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::replaceOne(string $id, string $doc): mysql_xdevapi\Result
```

Оновлює (або замінює) документ за ідентифікатором, якщо він існує.

### Список параметрів

`id`

Ідентифікатор документа для заміни чи оновлення. Зазвичай це \_id, який було згенеровано MySQL Server при додаванні запису.

`doc`

Документ колекції для оновлення або заміни документа, що відповідає параметру **id**

Документ може бути об'єктом документа або коректним рядком JSON, що описує новий документ.

### Значення, що повертаються

Об'єкт Result, який можна використовувати для запиту кількості порушених елементів та кількості попереджень, згенерованих операцією.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Collection::replaceOne()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$result = $collection->add('{"name": "Alfred", "age": 18, "job": "Butler"}')->execute();

// Обычно _id известен другими способами,
// но для этого примера давайте извлечём сгенерированный идентификатор и используем его
$ids       = $result->getGeneratedIds();
$alfred_id = $ids[0];

// ...

$alfred = $collection->getOne($alfred_id);
$alfred['age'] = 81;
$alfred['job'] = 'Guru';

$collection->replaceOne($alfred_id, $alfred);

?>
```
