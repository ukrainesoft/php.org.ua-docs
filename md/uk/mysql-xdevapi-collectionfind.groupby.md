---
navigation:
  - mysql-xdevapi-collectionfind.fields.md: '« CollectionFind::fields'
  - mysql-xdevapi-collectionfind.having.md: 'CollectionFind::having »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionfind.md: mysql\_xdevapi\\CollectionFind
title: 'CollectionFind::groupBy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionFind::groupBy

(No version information available, might only be in Git)

CollectionFind::groupBy — Встановлює критерії угруповання

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionFind::groupBy(string $sort_expr): mysql_xdevapi\CollectionFind
```

Цю функцію викликають для угруповання набору результатів по одному або декільком стовпцям. Її часто викликають з агрегатними функціями, наприклад: `COUNT` `MAX` `MIN` `SUM`и т. д.

### Список параметрів

`sort_expr`

Стовпець або стовпці, за якими буде проведено операцію угруповання, це може бути один рядок, або масив рядкових аргументів, по одному для кожного стовпця.

### Значення, що повертаються

Повертає об'єкт класу CollectionFind, з яким можна буде працювати далі.

### Приклади

**Пример #1 Пример использования метода**mysql\_xdevapi\\CollectionFind::groupBy()\*\*\*\*

```php
<?php

// Предполагая, что $coll — корректный объект класса Collection

// Извлекает все документы из коллекции и группирует результаты по полю 'name'
$res = $coll->find()->groupBy('name')->execute();

?>
```
