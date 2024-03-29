---
navigation:
  - mysql-xdevapi-collectionadd.construct.md: '« CollectionAdd::\_\_construct'
  - class.mysql-xdevapi-collectionfind.md: mysql\_xdevapi\\CollectionFind »
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionadd.md: mysql\_xdevapi\\CollectionAdd
title: 'CollectionAdd::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionAdd::execute

(No version information available, might only be in Git)

CollectionAdd::execute — Виконує затвердження

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionAdd::execute(): mysql_xdevapi\Result
```

Метод execute необхідний відправки запиту операції CRUD на сервер MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Result, який можна використовувати для перевірки стану операції, наприклад кількості порушених рядків.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionAdd::execute()\*\*\*\*

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
