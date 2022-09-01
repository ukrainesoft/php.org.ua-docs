---
navigation:
  - ds-deque.allocate.html: '« DsDeque::allocate'
  - ds-deque.capacity.html: 'ДсDeque::capacity »'
  - index.md: PHP Manual
  - class.ds-deque.html: Двостороння черга
title: 'ДсDeque::apply'
---
# ДсDeque::apply

(PECL ds >= 1.0.0)

ДсDeque::apply — Оновлює всі значення, застосовуючи callback-функцію до кожного значення

### Опис

```methodsynopsis
public Ds\Deque::apply(callable $callback): void
```

Оновлює всі значення, застосовуючи `callback`функцію до кожного значення.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): mixed
```

Об'єкт типу [callable](language.types.callable.md)

Callback-функція має повертати нове значення, яке замінить поточне.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::apply()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
$deque->apply(function($value) { return $value * 2; });

print_r($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Deque Object
(
    [0] => 2
    [1] => 4
    [2] => 6
)
```
