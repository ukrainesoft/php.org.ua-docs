---
navigation:
  - mysql-xdevapi-schema.gettable.html: '« Schema::getTable'
  - class.mysql-xdevapi-schemaobject.html: mysqlxdevapiSchemaObject »
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.html: mysqlxdevapiSchema
title: 'Schema::getTables'
---
# Schema::getTables

(No version information available, might only be in Git)

Schema::getTables — Отримати таблиці схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getTables(): array
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив усіх таблиць у цій схемі, де кожне значення елемента масиву є об'єктом Table з іменем таблиці як ключ.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSchema::getTables()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$session->sql("CREATE TABLE addressbook.cities(name text, population int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('Portland', 639863), ('Seattle', 704352)")->execute();

$schema = $session->getSchema("addressbook");
$tables = $schema->getTables();

var_dump($tables);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  ["cities"]=>
  object(mysql_xdevapi\Table)#3 (1) {
    ["name"]=>
    string(6) "cities"
  }

  ["names"]=>
  object(mysql_xdevapi\Table)#4 (1) {
    ["name"]=>
    string(5) "names"
  }
}
```
