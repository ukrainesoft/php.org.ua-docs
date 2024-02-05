---
navigation:
  - mysql-xdevapi-collectionmodify.arrayinsert.md: '« CollectionModify::arrayInsert'
  - mysql-xdevapi-collectionmodify.construct.md: 'CollectionModify::\_\_construct »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::bind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionModify::bind

(No version information available, might only be in Git)

CollectionModify::bind — Прив'язує значення до заповнювача запиту

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::bind(array $placeholder_values): mysql_xdevapi\CollectionModify
```

Прив'язує параметр до заповнювача за умови пошуку операції зміни.

Заповнювач має вигляд :NAME, де ':' - це загальний префікс, який повинен завжди існувати до будь-якого NAME, де NAME - ім'я заповнювача. Метод bind приймає список заповнювачів, якщо за умови пошуку операції зміни необхідно замінити кілька об'єктів.

### Список параметрів

`placeholder_values`

Підстановочні значення для заміни за умови пошуку. Допускається використання кількох значень, які необхідно передати у вигляді масиву зіставлень PLACEHOLDER\_NAME->PLACEHOLDER\_VALUE.

### Значення, що повертаються

Об'єкт CollectionModify, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionModify::bind()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$result = $collection
  ->add(
  '{"name":   "Bernie",
    "traits": ["Friend", "Brother", "Human"]}')
  ->execute();

$collection
  ->modify("name = :name")
  ->bind(['name' => 'Bernie'])
  ->arrayAppend('traits', 'Happy')
  ->execute();

$result = $collection
  ->find()
  ->execute();

print_r($result->fetchAll());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => Array
        (
            [_id] => 00005b6b53610000000000000110
            [name] => Bernie
            [traits] => Array
                (
                    [0] => Friend
                    [1] => Brother
                    [2] => Human
                    [3] => Happy
                )
        )
)
```
