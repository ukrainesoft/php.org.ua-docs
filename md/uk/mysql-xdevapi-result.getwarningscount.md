---
navigation:
  - mysql-xdevapi-result.getwarnings.md: '« Result::getWarnings'
  - class.mysql-xdevapi-rowresult.md: mysql\_xdevapi\\RowResult »
  - index.md: PHP Manual
  - class.mysql-xdevapi-result.md: mysql\_xdevapi\\Result
title: 'Result::getWarningsCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Result::getWarningsCount

(No version information available, might only be in Git)

Result::getWarningsCount — Отримує кількість попереджень останньої операції

### Опис

```methodsynopsis
public mysql_xdevapi\Result::getWarningsCount(): int
```

Отримує кількість застережень останньої операції Result.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість попереджень, згенерованих останньою операцією.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\RowResult::getWarningsCount()\*\*\*\*

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
