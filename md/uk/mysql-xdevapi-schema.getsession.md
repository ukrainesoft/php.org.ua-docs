---
navigation:
  - mysql-xdevapi-schema.getname.md: '« Schema::getName'
  - mysql-xdevapi-schema.gettable.md: 'Schema::getTable »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::getSession'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::getSession

(No version information available, might only be in Git)

Schema::getSession — Отримує сесію схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getSession(): mysql_xdevapi\Session
```

Отримує новий об'єкт класу Session із об'єкта класу Schema.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт класу Session.

### Приклади

**Приклад #1 Приклад использования метода**mysql\_xdevapi\\Schema::getSession()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema  = $session->getSchema("addressbook");

// ...

$newsession = $schema->getSession();

var_dump($session);
var_dump($newsession);
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(mysql_xdevapi\Session)#1 (0) {
}

object(mysql_xdevapi\Session)#3 (0) {
}
```
