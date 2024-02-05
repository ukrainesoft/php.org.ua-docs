---
navigation:
  - mysql-xdevapi-collectionremove.construct.md: '« CollectionRemove::\_\_construct'
  - mysql-xdevapi-collectionremove.limit.md: 'CollectionRemove::limit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionremove.md: mysql\_xdevapi\\CollectionRemove
title: 'CollectionRemove::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionRemove::execute

(No version information available, might only be in Git)

CollectionRemove::execute — Виконує операцію видалення

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionRemove::execute(): mysql_xdevapi\Result
```

Функція execute повинна викликатись, щоб змусити клієнта відправити запит операції CRUD на сервер.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Result.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionRemove::execute()\*\*\*\*

```php
<?php

$res = $coll->remove('true')->sort('age desc')->limit(2)->execute();

?>
```
