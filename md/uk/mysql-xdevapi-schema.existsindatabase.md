---
navigation:
  - mysql-xdevapi-schema.dropcollection.md: '« Schema::dropCollection'
  - mysql-xdevapi-schema.getcollection.md: 'Schema::getCollection »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema
title: 'Schema::existsInDatabase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Schema::existsInDatabase

(No version information available, might only be in Git)

Schema::existsInDatabase — Перевіряє, чи існує база даних.

### Опис

```methodsynopsis
public mysql_xdevapi\Schema::existsInDatabase(): bool
```

Перевіряє, чи існує поточний об'єкт (схема, таблиця, колекція або вистава) в об'єкті схеми.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо схема, таблиця, колекція або подання все ще існують у схемі, в іншому випадку повертає **`false`**

### Приклади

**Пример #1 Пример использования метода**mysql\_xdevapi\\Schema::existsInDatabase()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS food")->execute();
$session->sql("CREATE DATABASE food")->execute();
$session->sql("CREATE TABLE food.fruit(name text, rating text)")->execute();

$schema = $session->getSchema("food");
$schema->createCollection("trees");

// ...

$trees = $schema->getCollection("trees");

// ...

// Эта коллекция всё ещё находится в базе данных (схеме)?
if ($trees->existsInDatabase()) {
    echo "Да, коллекция 'trees' всё ещё существует.";
}
```

Висновок наведеного прикладу буде схожим на:

```
Да, коллекция 'trees' всё ещё существует.
```
