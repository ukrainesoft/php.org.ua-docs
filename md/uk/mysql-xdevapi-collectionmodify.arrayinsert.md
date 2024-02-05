---
navigation:
  - mysql-xdevapi-collectionmodify.arrayappend.md: '« CollectionModify::arrayAppend'
  - mysql-xdevapi-collectionmodify.bind.md: 'CollectionModify::bind »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::arrayInsert'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionModify::arrayInsert

(No version information available, might only be in Git)

CollectionModify::arrayInsert — Додає елемент до поля масиву

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::arrayInsert(string $collection_field, string $expression_or_literal): mysql_xdevapi\CollectionModify
```

Додає елемент у поле документа, коли поле це масив з декількох елементів. Через цей метод, на відміну від методу **mysql\_xdevapi\\CollectionModify::arrayAppend()**, можна вказати, куди додасться новий елемент, визначаючи, після якого елемента він йтиме, тоді як метод **mysql\_xdevapi\\CollectionModify::arrayAppend()** додає новий елемент до кінця масиву.

### Список параметрів

`collection_field`

Визначте елемент у масиві, після якого додасться новий елемент. Формат цього параметра: `FIELD_NAME[ INDEX ]`де FIELD\_NAME – це ім'я поля документа, до якого потрібно додати елемент, а INDEX – це INDEX елемента у полі.

Поле INDEX засноване на нулі, тому перший елемент масиву має індекс — 0.

`expression_or_literal`

Новий елемент для додавання після FIELD\_NAME\[INDEX\]

### Значення, що повертаються

Об'єкт CollectionModify, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionModify::arrayInsert()\*\*\*\*

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
  ->modify("name in ('Bernie', 'Jane')")
  ->arrayInsert('traits[1]', 'Happy')
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
            [_id] => 00005b6b5361000000000000010d
            [name] => Bernie
            [traits] => Array
                (
                    [0] => Friend
                    [1] => Happy
                    [2] => Brother
                    [3] => Human
                )
        )
)
```
