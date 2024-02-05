---
navigation:
  - mysql-xdevapi-collectionfind.groupby.md: '« CollectionFind::groupBy'
  - mysql-xdevapi-collectionfind.limit.md: 'CollectionFind::limit »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.md: mysql\_xdevapi\\CollectionFind
title: 'CollectionFind::having'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionFind::having

(No version information available, might only be in Git)

CollectionFind::having — Встановлює умову для агрегатних функцій

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::having(string $sort_expr): mysql_xdevapi\CollectionFind
```

Функція може бути використана після операції 'field', щоб зробити вибірку документів для вилучення.

### Список параметрів

`sort_expr`

Має бути коректний вираз SQL, дозволено використання агрегатних функцій.

### Значення, що повертаються

Об'єкт CollectionFind, який можна використовувати для подальшої обробки.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionFind::having()\*\*\*\*

```php
<?php

//Предполагая, что $coll является корректным объектом Collection

//Найти все документы, у которых 'age' больше 40,
//В объекте Result возвращаются только столбцы 'name' и 'age'.
$res = $coll->find()->fields(['name','age'])->having('age > 40')->execute();

?>
```
