---
navigation:
  - mysql-xdevapi-rowresult.getwarnings.md: '« RowResult::getWarnings'
  - class.mysql-xdevapi-schema.md: mysql\_xdevapi\\Schema »
  - index.md: PHP Manual
  - class.mysql-xdevapi-rowresult.md: mysql\_xdevapi\\RowResult
title: 'RowResult::getWarningsCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RowResult::getWarningsCount

(No version information available, might only be in Git)

RowResult::getWarningsCount — Отримує кількість попереджень останньої операції

### Опис

```methodsynopsis
public mysql_xdevapi\RowResult::getWarningsCount(): int
```

Отримує кількість попереджень останньої операції RowResult.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість попереджень, згенерованих останньою операцією.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\RowResult::getWarningsCount()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS foo")->execute();
$session->sql("CREATE DATABASE foo")->execute();
$session->sql("CREATE TABLE foo.test_table(x int)")->execute();

$schema = $session->getSchema("foo");
$table  = $schema->getTable("test_table");

$table->insert(['x'])->values([1])->values([2])->execute();

$res = $table->select(['x/0 as bad_x'])->execute();

echo $res->getWarningsCount();
?>
```

Висновок наведеного прикладу буде схожим на:

```
2
```
