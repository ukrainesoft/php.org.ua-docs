---
navigation:
  - class.mysql-xdevapi-collectionremove.md: « mysql\_xdevapi\\CollectionRemove
  - mysql-xdevapi-collectionremove.construct.md: 'CollectionRemove::\_\_construct »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionremove.md: mysql\_xdevapi\\CollectionRemove
title: 'CollectionRemove::bind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionRemove::bind

(No version information available, might only be in Git)

CollectionRemove::bind — Прив'язує значення до заповнювача

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionRemove::bind(array $placeholder_values): mysql_xdevapi\CollectionRemove
```

Прив'язує параметр до заповнювача за умови пошуку операції видалення.

Заповнювач має вигляд: NAME, де ':' - це загальний префікс, який повинен завжди вказаний перед будь-яким NAME, де NAME - це ім'я заповнювача. Метод bind приймає список заповнювачів, якщо за умови пошуку операції видалення необхідно замінити кілька об'єктів.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`placeholder_values`

Значення заповнювача для заміни за умови пошуку. Допускається використання кількох значень, які необхідно передати у вигляді масиву зіставлень PLACEHOLDER\_NAME->PLACEHOLDER\_VALUE.

### Значення, що повертаються

Об'єкт CollectionRemove, який можна використовувати для виконання команди або додавання додаткових операцій.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\CollectionRemove::bind()\*\*\*\*

```php
<?php

$res = $coll->remove('age > :age_from and age < :age_to')->bind(['age_from' => 20, 'age_to' => 50])->limit(7)->execute();

?>
```
