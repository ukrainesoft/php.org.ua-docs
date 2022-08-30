Видаляє один документ із колекції

-   [« Collection::remove](mysql-xdevapi-collection.remove.html)
    
-   [Collection::replaceOne »](mysql-xdevapi-collection.replaceone.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiCollection](class.mysql-xdevapi-collection.html)
    
-   Видаляє один документ із колекції
    

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

Ідентифікатор документа колекції, який потрібно видалити. Зазвичай це id, який було згенеровано MySQL Server при додаванні запису.

### Значення, що повертаються

Об'єкт Result, який можна використовувати для запиту кількості порушених елементів чи кількості попереджень, згенерованих операцією.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollection::removeOne()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$result = $collection->add('{"name": "Alfred", "age": 18, "job": "Butler"}')->execute();

// Обычно _id известен другими способами,
// но для этого примера давайте извлечём сгенерированный идентификатор и используем его
$ids       = $result->getGeneratedIds();
$alfred_id = $ids[0];

$result = $collection->removeOne($alfred_id);

if(!$result->getAffectedItemsCount()) {
    echo "Alfred с идентификатором $alfred_id не был удален.";
} else {
    echo "До свидания, Alfred, ты можешь взять с собой _id $alfred_id.";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
До свидания, Alfred, ты можешь взять с собой _id 00005b6b536100000000000000cb.
```