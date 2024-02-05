---
navigation:
  - ds-vector.push.md: '« Ds\\Vector::push'
  - ds-vector.remove.md: 'Ds\\Vector::remove »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::reduce'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::reduce

(PECL ds >= 1.0.0)

Ds\\Vector::reduce — Зменшує вектор до одного значення, використовуючи callback-функцію

### Опис

```methodsynopsis
public Ds\Vector::reduce(callable $callback, mixed $initial = ?): mixed
```

Сплескує вектор до одного значення, використовуючи callback-функцію.

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

Значення повернене остаточним запуском callback-функції.

### Приклади

**Приклад #1 Приклад використання** Ds\\Vector::reduce()\*\* з початковим значенням\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

$callback = function($carry, $value) {
    return $carry * $value;
};

var_dump($vector->reduce($callback, 5));

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

**Приклад #2 Приклад використання** Ds\\Vector::reduce()\*\* без початкового значення\*\*

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->reduce(function($carry, $value) {
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
