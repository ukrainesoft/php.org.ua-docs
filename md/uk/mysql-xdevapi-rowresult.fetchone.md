---
navigation:
  - mysql-xdevapi-rowresult.fetchall.md: '« RowResult::fetchAll'
  - mysql-xdevapi-rowresult.getcolumncount.md: 'RowResult::getColumnsCount »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-rowresult.md: mysql\_xdevapi\\RowResult
title: 'RowResult::fetchOne'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RowResult::fetchOne

(No version information available, might only be in Git)

RowResult::fetchOne — Отримує рядок з результату

### Опис

```methodsynopsis
public mysql_xdevapi\RowResult::fetchOne(): array
```

Витягує один результат із набору результатів.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Результат у вигляді асоціативного масиву або \*\*`null`\*\*якщо немає результатів.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\RowResult::fetchOne()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$row = $table->select('name', 'age')->where('age < 40')->execute()->fetchOne();

print_r($row);
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [name] => Sam
    [age] => 33
)
```
