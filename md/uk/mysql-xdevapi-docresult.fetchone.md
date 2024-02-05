---
navigation:
  - mysql-xdevapi-docresult.fetchall.md: '« DocResult::fetchAll'
  - mysql-xdevapi-docresult.getwarnings.md: 'DocResult::getWarnings »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-docresult.md: mysql\_xdevapi\\DocResult
title: 'DocResult::fetchOne'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DocResult::fetchOne

(No version information available, might only be in Git)

DocResult::fetchOne — Отримати один рядок

### Опис

```methodsynopsis
public mysql_xdevapi\DocResult::fetchOne(): array
```

Отримати один результат із результуючого набору.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Результат у вигляді асоціативного масиву, або \*\*`null`\*\*якщо результатів немає.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\DocResult::fetchOne()\*\*\*\*

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

var_dump($result->fetchOne());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(4) {
  ["_id"]=>
  string(28) "00005b6b53610000000000000125"
  ["age"]=>
  int(42)
  ["job"]=>
  string(6) "Butler"
  ["name"]=>
  string(8) "Reginald"
}
```
