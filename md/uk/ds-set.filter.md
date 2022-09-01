---
navigation:
  - ds-set.diff.html: '« DsSet::diff'
  - ds-set.first.html: 'ДсSet::first »'
  - index.md: PHP Manual
  - class.ds-set.html: Набор
title: 'ДсSet::filter'
---
# ДсSet::filter

(PECL ds >= 1.0.0)

ДсSet::filter — Створює новий список з елементів, вибраних за допомогою заданої callback-функції

### Опис

```methodsynopsis
public Ds\Set::filter(callable $callback = ?): Ds\Set
```

Створює новий набір елементів, вибраних за допомогою заданої callback-функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): bool
```

Опціональний аргумент типу [callable](language.types.callable.md), який повертає **`true`**, якщо значення має бути включено та **`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи, які призводять до логічного значення **`true`** (дивитися [приведение к boolean](language.types.boolean.html#language.types.boolean.casting)

### Значення, що повертаються

Новий набір, що містить значення, для яких функція `callback` повернула **`true`**, або всі елементи, які при приведенні до логічного типу стають **`true`**, якщо параметр `callback` не заданий.

### Приклади

**Приклад #1 Приклад **ДсSet::filter()** з використанням callback-функції**

```php
<?php
$set = new \Ds\Set([1, 2, 3, 4, 5]);

var_dump($set->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Set)#3 (2) {
  [0]=>
  int(2)
  [1]=>
  int(4)
}
```

**Приклад #2 Приклад **ДсSet::filter()** без callback-функції**

```php
<?php
$set = new \Ds\Set([0, 1, 'a', true, false]);

var_dump($set->filter());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Set)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  string(1) "a"
  [2]=>
  bool(true)
}
```
