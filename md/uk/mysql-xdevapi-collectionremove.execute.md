---
navigation:
  - mysql-xdevapi-collectionremove.construct.html: '« CollectionRemove::construct'
  - mysql-xdevapi-collectionremove.limit.html: 'CollectionRemove::limit »'
  - index.html: PHP Manual
  - class.mysql-xdevapi-collectionremove.html: mysqlxdevapiCollectionRemove
title: 'CollectionRemove::execute'
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

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Result.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionRemove::execute()****

```php
<?php

$res = $coll->remove('true')->sort('age desc')->limit(2)->execute();

?>
```
