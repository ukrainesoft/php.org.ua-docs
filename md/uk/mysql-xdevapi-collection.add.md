---
navigation:
  - class.mysql-xdevapi-collection.md: « mysql\_xdevapi\\Collection
  - mysql-xdevapi-collection.addorreplaceone.md: 'Collection::addOrReplaceOne »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::add

(No version information available, might only be in Git)

Collection::add — Додає документ до колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::add(mixed $document): mysql_xdevapi\CollectionAdd
```

Запускає додавання цього документа (документів) до колекції, підтримуються кілька варіантів методу. Можливі варіанти:

1.  Додавання одного документа у вигляді рядка JSON.
    
2.  Додавання одного документа у вигляді масиву, наприклад:`[ 'field' => 'value', 'field2' => 'value2' ... ]`
    
3.  В ту саму операцію можна додати, як документ, так і кілька документів.
    

### Список параметрів

`document`

Один або кілька документів може бути або JSON, або масив полів з відповідними значеннями. Масив не може бути порожнім.

Сервер MySQL автоматично генерує унікальні значення `_id` для кожного документа (рекомендується), хоча його також можна додати вручну. Це значення має бути унікальним, інакше операцію додавання не буде виконано.

### Значення, що повертаються

Об'єкт CollectionAdd. Використовуйте execute() для повернення Result, який можна використовувати для запиту кількості порушених елементів, кількості попереджень, згенерованих операцією, або для отримання списку згенерованих ідентифікаторів для доданих документів.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Collection::add()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$collection = $schema->getCollection("people");

// Добавление двух документов
$collection->add('{"name": "Fred",  "age": 21, "job": "Construction"}')->execute();
$collection->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')->execute();

// Добавление двух документов используя один объект JSON
$result = $collection->add(
  '{"name": "Bernie",
    "jobs": [{"title":"Cat Herder","Salary":42000}, {"title":"Father","Salary":0}],
    "hobbies": ["Sports","Making cupcakes"]}',
  '{"name": "Jane",
    "jobs": [{"title":"Scientist","Salary":18000}, {"title":"Mother","Salary":0}],
    "hobbies": ["Walking","Making pies"]}')->execute();

// Получение списка сгенерированных идентификаторов последней операции add()
$ids = $result->getGeneratedIds();
print_r($ids);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => 00005b6b53610000000000000056
    [1] => 00005b6b53610000000000000057
)
```

### Примітки

> **Зауваження** :
> 
> MySQL Server 8.0 або вище генерує унікальний \_id, як показано у прикладі. Поле \_id слід визначити вручну, якщо використовується MySQL Server 5.7.
