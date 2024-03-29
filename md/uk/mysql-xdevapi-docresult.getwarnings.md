---
navigation:
  - mysql-xdevapi-docresult.fetchone.md: '« DocResult::fetchOne'
  - mysql-xdevapi-docresult.getwarningscount.md: 'DocResult::getWarningsCount »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-docresult.md: mysql\_xdevapi\\DocResult
title: 'DocResult::getWarnings'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DocResult::getWarnings

(No version information available, might only be in Git)

DocResult::getWarnings — Отримати попередження з останньої операції

### Опис

```methodsynopsis
public mysql_xdevapi\DocResult::getWarnings(): Array
```

Отримує попередження від останньої операції з сервером MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів із попередженнями, викликаними останньою операцією. Кожен об'єкт містить поля 'message', 'level' та 'code'. Повертає порожній масив, якщо помилок немає.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\DocResult::getWarnings()\*\*\*\*

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
There was an error:

Array
(
    [0] => mysql_xdevapi\Warning Object
        (
            [message] => Something bad and so on
            [level] => 2
            [code] => 1365
        )
    [1] => mysql_xdevapi\Warning Object
        (
            [message] => Something bad and so on
            [level] => 2
            [code] => 1365
        )
)
```
