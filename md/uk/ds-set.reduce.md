---
navigation:
  - ds-set.merge.html: '« DsSet::merge'
  - ds-set.remove.html: 'ДсSet::remove »'
  - index.html: PHP Manual
  - class.ds-set.html: Набор
title: 'ДсSet::reduce'
---
# ДсSet::reduce

(PECL ds >= 1.0.0)

ДсSet::reduce — Зменшує колекцію до одного значення, використовуючи callback-функцію

### Опис

```methodsynopsis
public Ds\Set::reduce(callable $callback, mixed $initial = ?): mixed
```

Зменшує колекцію до одного значення, використовуючи callback-функцію.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $carry, mixed $value): mixed
```

`carry`

Значення, повернене попереднім запуском функції або `initial`, якщо функцію запущено вперше.

`value`

Значення поточної ітерації.

`initial`

Початкове значення параметра carry. Можна вказати **`null`**

### Значення, що повертаються

Значення, повернене остаточним запуском callback-функції.

### Приклади

**Приклад #1 Приклад використання **ДсSet::reduce()** з початковим значенням**

```php
<?php
$set = new \Ds\Set([1, 2, 3]);

$callback = function($carry, $value) {
    return $carry * $value;
};

var_dump($set->reduce($callback, 5));

// Итерации:
//
// $carry = $initial = 5
//
// $carry = $carry * 1 =  5
// $carry = $carry * 2 = 10
// $carry = $carry * 3 = 30
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(30)
```

**Приклад #2 Приклад використання **ДсSet::reduce()** без початкового значення**

```php
<?php
$set = new \Ds\Set([1, 2, 3]);

var_dump($set->reduce(function($carry, $value) {
    return $carry + $value + 5;
}));

// Итерации:
//
// $carry = $initial = null
//
// $carry = $carry + 1 + 5 =  6
// $carry = $carry + 2 + 5 = 13
// $carry = $carry + 3 + 5 = 21
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(21)
```
