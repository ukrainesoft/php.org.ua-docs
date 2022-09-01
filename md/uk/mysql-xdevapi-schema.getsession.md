---
navigation:
  - mysql-xdevapi-schema.getname.html: '« Schema::getName'
  - mysql-xdevapi-schema.gettable.html: 'Schema::getTable »'
  - index.html: PHP Manual
  - class.mysql-xdevapi-schema.html: mysqlxdevapiSchema
title: 'Schema::getSession'
---
# Schema::getSession

(No version information available, might only be in Git)

Schema::getSession — Отримати сесію схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getSession(): mysql_xdevapi\Session
```

Отримання нового об'єкта Session із Schema.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Session.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSchema::getSession()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema  = $session->getSchema("addressbook");

// ...

$newsession = $schema->getSession();

var_dump($session);
var_dump($newsession);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(mysql_xdevapi\Session)#1 (0) {
}

object(mysql_xdevapi\Session)#3 (0) {
}
```
