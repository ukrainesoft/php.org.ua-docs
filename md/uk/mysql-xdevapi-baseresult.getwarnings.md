---
navigation:
  - class.mysql-xdevapi-baseresult.md: « mysql\_xdevapi\\BaseResult
  - mysql-xdevapi-baseresult.getwarningscount.md: 'BaseResult::getWarningsCount »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-baseresult.md: mysql\_xdevapi\\BaseResult
title: 'BaseResult::getWarnings'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# BaseResult::getWarnings

(No version information available, might only be in Git)

BaseResult::getWarnings — Отримує попередження останньої операції

### Опис

```methodsynopsis
abstract public mysql_xdevapi\BaseResult::getWarnings(): array
```

Отримує попередження згенеровані останньою операцією сервера MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів Warning останньої операції. Кожен об'єкт містить повідомлення про помилку ('message'), рівень помилки ('level') та код помилки ('code'). Повертається порожній масив, якщо помилок немає.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\RowResult::getWarnings()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("CREATE DATABASE foo")->execute();
$session->sql("CREATE TABLE foo.test_table(x int)")->execute();

$schema = $session->getSchema("foo");
$table  = $schema->getTable("test_table");

$table->insert(['x'])->values([1])->values([2])->execute();

$res = $table->select(['x/0 as bad_x'])->execute();
$warnings = $res->getWarnings();

print_r($warnings);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => mysql_xdevapi\Warning Object
        (
            [message] => Division by 0
            [level] => 2
            [code] => 1365
        )
    [1] => mysql_xdevapi\Warning Object
        (
            [message] => Division by 0
            [level] => 2
            [code] => 1365
        )
)
```
