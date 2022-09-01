---
navigation:
  - mysql-xdevapi-collectionremove.execute.html: '« CollectionRemove::execute'
  - mysql-xdevapi-collectionremove.sort.html: 'CollectionRemove::sort »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionremove.html: mysqlxdevapiCollectionRemove
title: 'CollectionRemove::limit'
---
# CollectionRemove::limit

(No version information available, might only be in Git)

Collection Remove::limit — Обмежує кількість документів для видалення

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionRemove::limit(int $rows): mysql_xdevapi\CollectionRemove
```

Встановлює максимальну кількість документів для видалення.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`rows`

Максимальна кількість документів видалення.

### Значення, що повертаються

Повертає об'єкт CollectionRemove, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionRemove::limit()****

```php
<?php

$res = $coll->remove('job in (\'Barista\', \'Programmatore\', \'Ballerino\', \'Programmatrice\')')->limit(5)->sort(['age desc', 'name asc'])->execute();

?>
```
