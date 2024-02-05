---
navigation:
  - mysql-xdevapi-collection.remove.md: '« Collection::remove'
  - mysql-xdevapi-collection.replaceone.md: 'Collection::replaceOne »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::removeOne'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::removeOne

(No version information available, might only be in Git)

Collection::removeOne — Видаляє один документ із колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::removeOne(string $id): mysql_xdevapi\Result
```

Видаляє один документ із колекції з відповідним ідентифікатором. Скорочений запис для `Collection.remove("_id = :id").bind("id", id).execute()`

### Список параметрів

`id`

Ідентифікатор документа колекції, який потрібно видалити. Зазвичай це \_id, який було згенеровано MySQL Server при додаванні запису.

### Значення, що повертаються

Об'єкт Result, який можна використовувати для запиту кількості порушених елементів чи кількості попереджень, згенерованих операцією.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Collection::removeOne()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$result = $collection->add('{"name": "Alfred", "age": 18, "job": "Butler"}')->execute();

// Обычно _id известен другими способами,
// но для этого Приклада давайте извлечём сгенерированный идентификатор и используем его
$ids       = $result->getGeneratedIds();
$alfred_id = $ids[0];

$result = $collection->removeOne($alfred_id);

if(!$result->getAffectedItemsCount()) {
    echo "Alfred с идентификатором $alfred_id не был удален.";
} else {
    echo "До свидания, Alfred, ты можешь взять с собой _id $alfred_id.";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
До свидания, Alfred, ты можешь взять с собой _id 00005b6b536100000000000000cb.
```
