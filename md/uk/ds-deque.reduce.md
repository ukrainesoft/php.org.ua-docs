---
navigation:
  - ds-deque.push.md: '« DsDeque::push'
  - ds-deque.remove.md: 'ДсDeque::remove »'
  - index.md: PHP Manual
  - class.ds-deque.md: Двостороння черга
title: 'ДсDeque::reduce'
---
# ДсDeque::reduce

(PECL ds >= 1.0.0)

ДсDeque::reduce — Зменшує колекцію до одного значення, використовуючи callback-функцію

### Опис

```methodsynopsis
public Ds\Deque::reduce(callable $callback, mixed $initial = ?): mixed
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

**Приклад #1 Приклад використання **ДсDeque::reduce()** з початковим значенням**

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

$callback = function($carry, $value) {
    return $carry * $value;
};

var_dump($deque->reduce($callback, 5));

// Iterations:
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

**Приклад #2 Приклад використання **ДсDeque::reduce()** без початкового значення**

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

var_dump($deque->reduce(function($carry, $value) {
    return $carry + $value + 5;
}));

// Iterations:
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
