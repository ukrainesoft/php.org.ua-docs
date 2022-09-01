---
navigation:
  - mysql-xdevapi-table.insert.html: '« Table::insert'
  - mysql-xdevapi-table.select.html: 'Table::select »'
  - index.html: PHP Manual
  - class.mysql-xdevapi-table.html: mysqlxdevapiTable
title: 'Table::isView'
---
# Table::isView

(No version information available, might only be in Git)

Table::isView — Перевірити, чи є таблиця поданням

### Опис

```methodsynopsis
public mysql_xdevapi\Table::isView(): bool
```

Визначте, чи є базовий об'єкт поданням чи ні.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо базовий об'єкт є поданням, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTable::isView()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

if ($table->isView()) {
    echo "Это представление.";
} else {
    echo "Это не представление.";
}
?>
```

Результат виконання цього прикладу:

```
int(2)
```
