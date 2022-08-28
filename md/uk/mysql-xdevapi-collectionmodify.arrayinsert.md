Додає елемент у поле масиву

-   [« CollectionModify::arrayAppend](mysql-xdevapi-collectionmodify.arrayappend.html)
    
-   [CollectionModify::bind »](mysql-xdevapi-collectionmodify.bind.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\CollectionModify](class.mysql-xdevapi-collectionmodify.html)
    
-   Додає елемент у поле масиву
    

# CollectionModify::arrayInsert

(No version information available, might only be in Git)

CollectionModify::arrayInsert — Додає елемент до поля масиву

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::arrayInsert(string $collection_field, string $expression_or_literal): mysql_xdevapi\CollectionModify
```

Додає елемент у поле документа, коли кілька елементів поля подаються як масиву. На відміну від arrayAppend(), arrayInsert() дозволяє вам вказати, куди додасться новий елемент, визначаючи, за яким елементом він слідує, тоді як arrayAppend() завжди додає новий елемент до кінця масиву.

### Список параметрів

`collection_field`

Визначте елемент у масиві, після якого додасться новий елемент. Формат цього параметра: `FIELD_NAME[ INDEX ]`де FIELDNAME – це ім'я поля документа, з якого видаляється елемент, а INDEX – це INDEX елемента у полі.

Поле INDEX засноване на нулі, тому найлівіший елемент масиву має індекс 0.

`expression_or_literal`

Новий елемент для додавання після FIELDNAME INDEX

### Значення, що повертаються

Об'єкт CollectionModify, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionModify::arrayInsert()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$result = $collection
  ->add(
  '{"name":   "Bernie",
    "traits": ["Friend", "Brother", "Human"]}')
  ->execute();

$collection
  ->modify("name in ('Bernie', 'Jane')")
  ->arrayInsert('traits[1]', 'Happy')
  ->execute();

$result = $collection
  ->find()
  ->execute();

print_r($result->fetchAll());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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