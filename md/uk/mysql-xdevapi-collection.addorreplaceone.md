---
navigation:
  - mysql-xdevapi-collection.add.md: '« Collection::add'
  - mysql-xdevapi-collection.construct.md: 'Collection::construct »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysqlxdevapiCollection
title: 'Collection::addOrReplaceOne'
---
# Collection::addOrReplaceOne

(No version information available, might only be in Git)

Collection::addOrReplaceOne — Додає або замінює документ колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::addOrReplaceOne(string $id, string $doc): mysql_xdevapi\Result
```

Додає новий документ або замінює існуючий.

Ось кілька сценаріїв для цього методу:

-   Якщо ні ідентифікатор, ні якесь унікальне значення ключа не конфліктують з будь-яким документом у колекції, цей документ додається.
    
-   Якщо ідентифікатор не відповідає жодному документу, але одне або кілька унікальних значень ключів конфліктують із документом у колекції, видається помилка.
    
-   Якщо ідентифікатор відповідає існуючому документу та унікальні ключі не визначені для колекції, документ замінюється.
    
-   Якщо ідентифікатор відповідає існуючому документу, або всі унікальні ключі в документі заміни відповідають цьому документу або не конфліктують з іншими документами в колекції, документ замінюється.
    
-   Якщо ідентифікатор відповідає існуючому документу, а один або кілька унікальних ключів відповідають документу, який відрізняється від колекції, видається помилка.
    

### Список параметрів

`id`

Ідентифікатор фільтру. Якщо ідентифікатор або інше поле з унікальним індексом вже існує в колекції, він оновить відповідний документ.

За замовчуванням цей ідентифікатор автоматично генерується MySQL Server при додаванні запису і згадується як поле з ім'ям 'id'.

`doc`

Це документ для додавання або заміни, що є рядком JSON.

### Значення, що повертаються

Об'єкт Result.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollection::addOrReplaceOne()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$collection = $schema->getCollection("people");

// Использование add()
$result = $collection->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')->execute();

// Использование addOrReplaceOne()
// Примечания: мы передаём известное значение _id
$result = $collection->addOrReplaceOne('00005b6b53610000000000000056', '{"name": "Fred",  "age": 21, "job": "Construction"}');

?>
```
