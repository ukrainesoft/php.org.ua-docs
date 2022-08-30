Отримати всі рядки

-   [« DocResult::construct](mysql-xdevapi-docresult.construct.html)
    
-   [DocResult::fetchOne »](mysql-xdevapi-docresult.fetchone.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiDocResult](class.mysql-xdevapi-docresult.html)
    
-   Отримати всі рядки
    

# DocResult::fetchAll

(No version information available, might only be in Git)

DocResult::fetchAll — Отримати всі рядки

### Опис

```methodsynopsis
public mysql_xdevapi\DocResult::fetchAll(): array
```

Отримати всі результати результуючого набору.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив з усіма результатами із запиту; кожен результат – це асоціативний масив. Якщо немає рядків результату запиту, повертається порожній масив.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiDocResult::fetchAll()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

$create->add('{"name": "Alfred", "age": 18, "job": "Butler"}')->execute();
$create->add('{"name": "Reginald", "age": 42, "job": "Butler"}')->execute();

// ...

$collection = $schema->getCollection("people");

// Возвращает объект DocResult
$result = $collection
  ->find('job like :job and age > :age')
  ->bind(['job' => 'Butler', 'age' => 16])
  ->sort('age desc')
  ->execute();

var_dump($result->fetchAll());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {

  [0]=>
  array(4) {
    ["_id"]=>
    string(28) "00005b6b53610000000000000123"
    ["age"]=>
    int(42)
    ["job"]=>
    string(6) "Butler"
    ["name"]=>
    string(8) "Reginald"
  }

  [1]=>
  array(4) {
    ["_id"]=>
    string(28) "00005b6b53610000000000000122"
    ["age"]=>
    int(18)
    ["job"]=>
    string(6) "Butler"
    ["name"]=>
    string(6) "Alfred"
  }

}
```