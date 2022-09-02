---
navigation:
  - mysql-xdevapi-result.getautoincrementvalue.md: '« Result::getAutoIncrementValue'
  - mysql-xdevapi-result.getwarnings.md: 'Result::getWarnings »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-result.md: mysqlxdevapiResult
title: 'Result::getGeneratedIds'
---
# Result::getGeneratedIds

(No version information available, might only be in Git)

Result::getGeneratedIds — Отримує згенеровані ідентифікатори

### Опис

```methodsynopsis
public mysql_xdevapi\Result::getGeneratedIds(): array
```

Отримує згенеровані значення id з останньої операції. Унікальне поле ID генерується сервером MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив згенерованих id з останньої операції чи порожній масив, якщо таких немає.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiResult::getGeneratedIds()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$collection = $schema->getCollection("people");

$result = $collection->add(
  '{"name": "Bernie",
    "jobs": [{"title":"Cat Herder","Salary":42000}, {"title":"Father","Salary":0}],
    "hobbies": ["Sports","Making cupcakes"]}',
  '{"name": "Jane",
    "jobs": [{"title":"Scientist","Salary":18000}, {"title":"Mother","Salary":0}],
    "hobbies": ["Walking","Making pies"]}')->execute();

$ids = $result->getGeneratedIds();
var_dump($ids);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  [0]=>
  string(28) "00005b6b53610000000000000064"
  [1]=>
  string(28) "00005b6b53610000000000000065"
}
```
