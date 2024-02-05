---
navigation:
  - mysql-xdevapi-collection.getschema.md: '« Collection::getSchema'
  - mysql-xdevapi-collection.modify.md: 'Collection::modify »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::getSession'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::getSession

(No version information available, might only be in Git)

Collection::getSession — Повертає об'єкт Session

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::getSession(): Session
```

Повертає новий об'єкт Session із об'єкта Collection.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Session.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Collection::getSession()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

// ...

$newsession = $collection->getSession();

var_dump($session);
var_dump($newsession);
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(mysql_xdevapi\Session)#1 (0) {
}
object(mysql_xdevapi\Session)#4 (0) {
}
```
