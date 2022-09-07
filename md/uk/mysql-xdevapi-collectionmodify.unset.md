---
navigation:
  - mysql-xdevapi-collectionmodify.sort.md: '« CollectionModify::sort'
  - class.mysql-xdevapi-collectionremove.md: mysqlxdevapiCollectionRemove »
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysqlxdevapiCollectionModify
title: 'CollectionModify::unset'
---
# CollectionModify::unset

(No version information available, might only be in Git)

CollectionModify::unset — Скидає значення полів документа

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::unset(array $fields): mysql_xdevapi\CollectionModify
```

Видаляє атрибути з документів у колекції.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`fields`

Атрибути для видалення документів у колекції.

### Значення, що повертаються

Об'єкт CollectionModify, який можна використовувати для подальшої обробки.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionModify::unset()****

```php
<?php

$res = $coll->modify('job like :job_name')->unset(["age", "name"])->bind(['job_name' => 'Plumber'])->execute();

?>
```
