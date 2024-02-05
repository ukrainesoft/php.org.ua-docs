---
navigation:
  - mysql-xdevapi-schema.gettable.md: '« Schema::getTable'
  - class.mysql-xdevapi-schemaobject.md: mysql\_xdevapi\\SchemaObject »
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::getTables'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::getTables

(No version information available, might only be in Git)

Schema::getTables — Отримує таблиці схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::getTables(): array
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив усіх таблиць у цій схемі, де кожне значення елемента масиву є об'єктом класу Table з іменем таблиці як ключ.

### Приклади

**Приклад #1 Приклад использования метода**mysql\_xdevapi\\Schema::getTables()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$session->sql("CREATE TABLE addressbook.cities(name text, population int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('Portland', 639863), ('Seattle', 704352)")->execute();

$schema = $session->getSchema("addressbook");
$tables = $schema->getTables();

var_dump($tables);
?>
```

Висновок наведеного прикладу буде схожим на:

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
