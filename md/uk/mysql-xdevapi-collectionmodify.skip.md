---
navigation:
  - mysql-xdevapi-collectionmodify.set.md: '« CollectionModify::set'
  - mysql-xdevapi-collectionmodify.sort.md: 'CollectionModify::sort »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::skip'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionModify::skip

(No version information available, might only be in Git)

CollectionModify::skip — Пропускає елементи

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::skip(int $position): mysql_xdevapi\CollectionModify
```

Пропускає перші N елементів, які інакше повернули б операцією пошуку. Якщо кількість пропущених елементів перевищує розмір набору результатів, пошук повертає порожній набір.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`position`

Кількість елементів, що пропускаються.

### Значення, що повертаються

Повертає об'єкт класу CollectionModify, з яким можна працювати далі.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionModify::skip()\*\*\*\*

```php
<?php

$coll->modify('age > :age')->sort('age desc')->unset(['age'])->bind(['age' => 20])->limit(4)->skip(1)->execute();

?>
```
