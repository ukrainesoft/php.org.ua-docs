---
navigation:
  - mysql-xdevapi-collectionmodify.construct.md: '« CollectionModify::\_\_construct'
  - mysql-xdevapi-collectionmodify.limit.md: 'CollectionModify::limit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionModify::execute()\*\*\*\*

```php
<?php

/* ... */

?>
```
