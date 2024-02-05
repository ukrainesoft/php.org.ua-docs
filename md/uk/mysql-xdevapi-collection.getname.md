---
navigation:
  - mysql-xdevapi-collection.find.md: '« Collection::find'
  - mysql-xdevapi-collection.getone.md: 'Collection::getOne »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::getName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::getName

(No version information available, might only be in Git)

Collection::getName — Отримує назву колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::getName(): string
```

Отримує назву колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Назва колекції у вигляді рядка.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Collection::getName()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");


// ...

var_dump($collection->getName());
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(6) "people"
```
