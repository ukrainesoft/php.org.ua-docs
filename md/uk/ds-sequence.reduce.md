---
navigation:
  - ds-sequence.push.md: '« DsSequence::push'
  - ds-sequence.remove.md: 'ДсSequence::remove »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Послідовність
title: 'ДсSequence::reduce'
---
# ДсSequence::reduce

(PECL ds >= 1.0.0)

ДсSequence::reduce - Сплескує колекцію до одного значення використовуючи callback-функцію

### Опис

```methodsynopsis
abstract public Ds\Sequence::reduce(callable $callback, mixed $initial = ?): mixed
```

Сплескує колекцію до одного значення використовуючи callback-функцію.

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

Значення, повернене фінальним запуском callback-функції.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::reduce()** з початковим значенням**

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

$callback = function($carry, $value) {
    return $carry * $value;
};

var_dump($sequence->reduce($callback, 5));

// Итерации:
//
// $carry = $initial = 5
//
// $carry = $carry * 1 =  5
// $carry = $carry * 2 = 10
// $carry = $carry * 3 = 30
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(30)
```

**Приклад #2 Приклад використання **ДсSequence::reduce()** без початкового значення**

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

var_dump($sequence->reduce(function($carry, $value) {
    return $carry + $value + 5;
}));

// Итерации:
//
// $carry = $initial = null
//
// $carry = $carry + 1 + 5 =  6
// $carry = $carry + 2 + 5 = 13
// $carry = $carry + 3 + 5 = 21
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(21)
```
