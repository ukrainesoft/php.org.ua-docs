---
navigation:
  - mysql-xdevapi-collectionremove.execute.md: '« CollectionRemove::execute'
  - mysql-xdevapi-collectionremove.sort.md: 'CollectionRemove::sort »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionremove.md: mysql\_xdevapi\\CollectionRemove
title: 'CollectionRemove::limit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`rows`

Максимальна кількість документів видалення.

### Значення, що повертаються

Повертає об'єкт CollectionRemove, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\CollectionRemove::limit()\*\*\*\*

```php
<?php

$res = $coll->remove('job in (\'Barista\', \'Programmatore\', \'Ballerino\', \'Programmatrice\')')->limit(5)->sort(['age desc', 'name asc'])->execute();

?>
```
