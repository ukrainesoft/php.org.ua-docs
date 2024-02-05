---
navigation:
  - class.mysql-xdevapi-collectionadd.md: « mysql\_xdevapi\\CollectionAdd
  - mysql-xdevapi-collectionadd.execute.md: 'CollectionAdd::execute »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionadd.md: mysql\_xdevapi\\CollectionAdd
title: 'CollectionAdd::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionAdd::\_\_construct

(No version information available, might only be in Git)

CollectionAdd::\_\_construct - Конструктор класу CollectionAdd

### Опис

private**mysql\_xdevapi\\CollectionAdd::\_\_construct**()

Використовується для додавання документа до колекції; Викликається з об'єкта Collection.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\CollectionAdd::\_\_construct()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$collection = $schema->getCollection("people");

// Добавляем два документа
$collection
  ->add('{"name": "Fred",  "age": 21, "job": "Construction"}')
  ->execute();

$collection
  ->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')
  ->execute();

// Добавляем два документа, используя один объект JSON
$result = $collection
  ->add(
    '{"name": "Bernie",
      "jobs": [{"title":"Cat Herder","Salary":42000}, {"title":"Father","Salary":0}],
      "hobbies": ["Sports","Making cupcakes"]}',
    '{"name": "Jane",
      "jobs": [{"title":"Scientist","Salary":18000}, {"title":"Mother","Salary":0}],
      "hobbies": ["Walking","Making pies"]}')
  ->execute();

// Получаем список сгенерированных идентификаторов из последнего выполнения add()
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
