---
navigation:
  - mysql-xdevapi-collectionmodify.sort.md: '« CollectionModify::sort'
  - class.mysql-xdevapi-collectionremove.md: mysql\_xdevapi\\CollectionRemove »
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::unset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionModify::unset

(No version information available, might only be in Git)

CollectionModify::unset — Скидає значення полів документа

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::unset(array $fields): mysql_xdevapi\CollectionModify
```

Видаляє атрибути з документів у колекції.

### Список параметрів

`fields`

Атрибути для видалення документів у колекції.

### Значення, що повертаються

Повертає об'єкт класу CollectionModify, з яким можна працювати далі.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionModify::unset()\*\*\*\*

```php
<?php

$res = $coll->modify('job like :job_name')->unset(["age", "name"])->bind(['job_name' => 'Plumber'])->execute();

?>
```
