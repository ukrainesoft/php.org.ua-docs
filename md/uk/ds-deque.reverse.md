---
navigation:
  - ds-deque.remove.md: '« Ds\\Deque::remove'
  - ds-deque.reversed.md: 'Ds\\Deque::reversed »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::reverse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::reverse

(PECL ds >= 1.0.0)

Ds\\Deque::reverse — Перевертає поточну двосторонню чергу.

### Опис

```methodsynopsis
public Ds\Deque::reverse(): void
```

Перевертає поточну двосторонню чергу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::reverse()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);
$deque->reverse();

print_r($deque);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Deque Object
(
    [0] => c
    [1] => b
    [2] => a
)
```
