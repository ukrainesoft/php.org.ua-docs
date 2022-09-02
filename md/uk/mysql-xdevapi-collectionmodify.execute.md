---
navigation:
  - mysql-xdevapi-collectionmodify.construct.md: '« CollectionModify::construct'
  - mysql-xdevapi-collectionmodify.limit.md: 'CollectionModify::limit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysqlxdevapiCollectionModify
title: 'CollectionModify::execute'
---
# CollectionModify::execute

(No version information available, might only be in Git)

CollectionModify::execute — Виконує операцію зміни

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::execute(): mysql_xdevapi\Result
```

Метод execute необхідний відправки запиту операції CRUD на сервер MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт Result, який можна використовувати для перевірки стану операції, наприклад кількості порушених рядків.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionModify::execute()****

```php
<?php

/* ... */

?>
```
