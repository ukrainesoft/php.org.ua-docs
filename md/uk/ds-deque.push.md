---
navigation:
  - ds-deque.pop.md: '« Ds\\Deque::pop'
  - ds-deque.reduce.md: 'Ds\\Deque::reduce »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::push'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::push

(PECL ds >= 1.0.0)

Ds\\Deque::push — Додає значення до кінця двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::push(mixed ...$values): void
```

Додає значення до кінця двосторонньої черги.

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::push()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque();

$deque->push("a");
$deque->push("b");
$deque->push("c", "d");
$deque->push(...["e", "f"]);

print_r($deque);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Deque Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
    [4] => e
    [5] => f
)
```
