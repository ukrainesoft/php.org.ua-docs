---
navigation:
  - mysql-xdevapi-result.getaffecteditemscount.md: '« Result::getAffectedItemsCount'
  - mysql-xdevapi-result.getgeneratedids.md: 'Result::getGeneratedIds »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-result.md: mysql\_xdevapi\\Result
title: 'Result::getAutoIncrementValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Result::getAutoIncrementValue

(No version information available, might only be in Git)

Result::getAutoIncrementValue — Отримує значення автоінкремента

### Опис

```methodsynopsis
public mysql_xdevapi\Result::getAutoIncrementValue(): int
```

Отримує останнє значення AUTO\_INCREMENT (ідентифікатор останньої вставки).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення AUTO\_INCREMENT.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\Result::getAutoIncrementValue()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();
$session->sql("
  CREATE TABLE addressbook.names
    (id INT NOT NULL AUTO_INCREMENT, name VARCHAR(30), age INT, PRIMARY KEY (id))
  ")->execute();

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$result = $table->insert("name", "age")->values(["Suzanne", 31],["Julie", 43])->execute();
$result = $table->insert("name", "age")->values(["Suki", 34])->execute();

$ai = $result->getAutoIncrementValue();
var_dump($ai);
?>
```

Результат виконання наведеного прикладу:

```
int(3)
```
