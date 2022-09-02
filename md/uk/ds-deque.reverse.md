---
navigation:
  - ds-deque.remove.md: '« DsDeque::remove'
  - ds-deque.reversed.md: 'ДсDeque::reversed »'
  - index.md: PHP Manual
  - class.ds-deque.md: Двостороння черга
title: 'ДсDeque::reverse'
---
# ДсDeque::reverse

(PECL ds >= 1.0.0)

ДсDeque::reverse — Перевертає поточну двосторонню чергу.

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

**Приклад #1 Приклад використання **ДсDeque::reverse()****

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);
$deque->reverse();

print_r($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Deque Object
(
    [0] => c
    [1] => b
    [2] => a
)
```
