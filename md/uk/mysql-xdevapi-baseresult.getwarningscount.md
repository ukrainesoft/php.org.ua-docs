---
navigation:
  - mysql-xdevapi-baseresult.getwarnings.md: '« BaseResult::getWarnings'
  - class.mysql-xdevapi-client.md: mysql\_xdevapi\\Client »
  - index.md: PHP Manual
  - class.mysql-xdevapi-baseresult.md: mysql\_xdevapi\\BaseResult
title: 'BaseResult::getWarningsCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# BaseResult::getWarningsCount

(No version information available, might only be in Git)

BaseResult::getWarningsCount — Отримує кількість попереджень останньої операції

### Опис

```methodsynopsis
abstract public mysql_xdevapi\BaseResult::getWarningsCount(): int
```

Повертає кількість попереджень, виданих останньою операцією. Зокрема ці попередження викликаються сервером MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість попереджень останньої операції.

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
