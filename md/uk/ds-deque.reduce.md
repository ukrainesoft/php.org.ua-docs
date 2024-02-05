---
navigation:
  - ds-deque.push.md: '« Ds\\Deque::push'
  - ds-deque.remove.md: 'Ds\\Deque::remove »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::reduce'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::reduce

(PECL ds >= 1.0.0)

Ds\\Deque::reduce — Зменшує колекцію до одного значення, використовуючи callback-функцію

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

**Пример #1 Пример использования**Ds\\Deque::reduce()\*\* з початковим значенням\*\*

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

Висновок наведеного прикладу буде схожим на:

```
int(30)
```

**Пример #2 Пример использования**Ds\\Deque::reduce()\*\* без початкового значення\*\*

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

Висновок наведеного прикладу буде схожим на:

```
int(21)
```
