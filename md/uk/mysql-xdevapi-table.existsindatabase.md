---
navigation:
  - mysql-xdevapi-table.delete.md: '« Table::delete'
  - mysql-xdevapi-table.getname.md: 'Table::getName »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-table.md: mysqlxdevapiTable
title: 'Table::existsInDatabase'
---
# Table::existsInDatabase

(No version information available, might only be in Git)

Table::existsInDatabase — Перевірити, чи існує таблиця в базі даних

### Опис

```methodsynopsis
public mysql_xdevapi\Table::existsInDatabase(): bool
```

Перевіряє, чи існує таблиця в базі даних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо таблиця існує в базі даних, інакше \*\*`false`\*\*якщо таблиці немає.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTable::existsInDatabase()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

if ($table->existsInDatabase()) {
  echo "Да, эта таблица всё ещё существует в схеме сессии.";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Да, эта таблица всё ещё существует в схеме сессии.
```
