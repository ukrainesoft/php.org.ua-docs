---
navigation:
  - mysql-xdevapi-docresult.getwarnings.md: '« DocResult::getWarnings'
  - class.mysql-xdevapi-exception.md: mysql\_xdevapi\\Exception »
  - index.md: PHP Manual
  - class.mysql-xdevapi-docresult.md: mysql\_xdevapi\\DocResult
title: 'DocResult::getWarningsCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DocResult::getWarningsCount

(No version information available, might only be in Git)

DocResult::getWarningsCount — Отримати кількість попереджень з останньої операції

### Опис

```methodsynopsis
public mysql_xdevapi\DocResult::getWarningsCount(): int
```

Повертає кількість попереджень, спричинених останньою операцією. Зокрема ці попередження викликаються сервером MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість попереджень із останньої операції.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\DocResult::getWarningsCount()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$create->add('{"name": "Alfred", "age": 18, "job": "Butler"}')->execute();
$create->add('{"name": "Reginald", "age": 42, "job": "Butler"}')->execute();

// ...

$collection = $schema->getCollection("people");

// Возвращает объект DocResult
$result = $collection
  ->find('job like :job and age > :age')
  ->bind(['job' => 'Butler', 'age' => 16])
  ->sort('age desc')
  ->execute();

if (!$result->getWarningsCount()) {
    echo "Произошла ошибка:\n";
    print_r($result->getWarnings());
    exit;
}

var_dump($result->fetchOne());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(4) {
  ["_id"]=>
  string(28) "00005b6b53610000000000000135"
  ["age"]=>
  int(42)
  ["job"]=>
  string(6) "Butler"
  ["name"]=>
  string(8) "Reginald"
}
```
