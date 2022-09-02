---
navigation:
  - mysql-xdevapi-schema.dropcollection.md: '« Schema::dropCollection'
  - mysql-xdevapi-schema.getcollection.md: 'Schema::getCollection »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysqlxdevapiSchema
title: 'Schema::existsInDatabase'
---
# Schema::existsInDatabase

(No version information available, might only be in Git)

Schema::existsInDatabase — Перевірити, чи існує у базі даних

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::existsInDatabase(): bool
```

Перевіряє, чи існує поточний об'єкт (схема, таблиця, колекція або вистава) в об'єкті схеми.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо схема, таблиця, колекція або подання все ще існують у схемі, в іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSchema::getCollection()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS food")->execute();
$session->sql("CREATE DATABASE food")->execute();
$session->sql("CREATE TABLE food.fruit(name text, rating text)")->execute();

$schema = $session->getSchema("food");
$schema->createCollection("trees");

// ...

$trees = $schema->getCollection("trees");

// ...

// Эта коллекция всё ещё находится в базе данных (схеме)?
if ($trees->existsInDatabase()) {
    echo "Да, коллекция 'trees' всё ещё существует.";
}
```

Результатом виконання цього прикладу буде щось подібне:

```
Да, коллекция 'trees' всё ещё существует.
```
