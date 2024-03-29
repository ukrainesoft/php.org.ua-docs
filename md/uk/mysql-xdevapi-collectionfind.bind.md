---
navigation:
  - class.mysql-xdevapi-collectionfind.md: « mysql\_xdevapi\\CollectionFind
  - mysql-xdevapi-collectionfind.construct.md: 'CollectionFind::\_\_construct »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.md: mysql\_xdevapi\\CollectionFind
title: 'CollectionFind::bind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionFind::bind

(No version information available, might only be in Git)

CollectionFind::bind — Прив'язує значення до заповнювача запиту

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::bind(array $placeholder_values): mysql_xdevapi\CollectionFind
```

Дозволяє користувачеві прив'язати параметр до заповнювача за умови пошуку операції пошуку. Заповнювач має вигляд :NAME, де ':' - це загальний префікс, який має завжди існувати перед будь-яким NAME, NAME - фактичне ім'я заповнювача. Функція bind приймає список заповнювачів, якщо за умови пошуку необхідно замінити кілька об'єктів.

### Список параметрів

`placeholder_values`

Значення для підстановки за умов пошуку; допускається кілька значень, які передаються у вигляді масиву, де "PLACEHOLDER\_NAME => PLACEHOLDER\_VALUE".

### Значення, що повертаються

Об'єкт CollectionFind або ланцюжок з execute() для повернення об'єкта Result.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionFind::bind()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");
$result = $create
  ->add('{"name": "Alfred", "age": 18, "job": "Butler"}')
  ->execute();

// ...

$collection = $schema->getCollection("people");

$result = $collection
  ->find('job like :job and age > :age')
  ->bind(['job' => 'Butler', 'age' => 16])
  ->execute();

var_dump($result->fetchAll());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(1) {
  [0]=>
  array(4) {
    ["_id"]=>
    string(28) "00005b6b536100000000000000cf"
    ["age"]=>
    int(18)
    ["job"]=>
    string(6) "Butler"
    ["name"]=>
    string(6) "Alfred"
  }
}
```
