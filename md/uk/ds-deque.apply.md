---
navigation:
  - ds-deque.allocate.md: '« Ds\\Deque::allocate'
  - ds-deque.capacity.md: 'Ds\\Deque::capacity »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::apply'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::apply

(PECL ds >= 1.0.0)

Ds\\Deque::apply — Оновлює всі значення, застосовуючи callback-функцію до кожного значення

### Опис

```methodsynopsis
public Ds\Deque::apply(callable $callback): void
```

Обновляет все значения, применяя`callback`\-функцію до кожного значення.

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

**Приклад #1 Приклад використання** Ds\\Deque::apply()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
$deque->apply(function($value) { return $value * 2; });

print_r($deque);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Deque Object
(
    [0] => 2
    [1] => 4
    [2] => 6
)
```
