---
navigation:
  - class.mysql-xdevapi-collectionmodify.md: « mysql\_xdevapi\\CollectionModify
  - mysql-xdevapi-collectionmodify.arrayinsert.md: 'CollectionModify::arrayInsert »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::arrayAppend'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionModify::arrayAppend

(No version information available, might only be in Git)

CollectionModify::arrayAppend — Додає елемент до поля масиву

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::arrayAppend(string $collection_field, string $expression_or_literal): mysql_xdevapi\CollectionModify
```

Додає елемент у поле документа, коли кілька елементів поля подаються як масиву. На відміну від arrayInsert(), arrayAppend() завжди додає новий елемент до кінця масиву, тоді як arrayInsert() може визначати місцезнаходження.

### Список параметрів

`collection_field`

Ідентифікатор поля, до якого вставляється новий елемент.

`expression_or_literal`

Новий елемент для додавання до кінця масиву полів документа.

### Значення, що повертаються

Об'єкт CollectionModify, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\CollectionModify::arrayAppend()\*\*\*\*

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
            [_id] => 00005b6b5361000000000000010c
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
