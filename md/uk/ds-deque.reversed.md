---
navigation:
  - ds-deque.reverse.md: '« Ds\\Deque::reverse'
  - ds-deque.rotate.md: 'Ds\\Deque::rotate »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::reversed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::reversed

(PECL ds >= 1.0.0)

Ds\\Deque::reversed — Повертає перегорнуту копію двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::reversed(): Ds\Deque
```

Повертає перегорнуту копію двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія двосторонньої черги.

> **Зауваження** :
> 
> Поточна двостороння черга не зміниться.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::reversed()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

print_r($deque->reversed());
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
Ds\Deque Object
(
    [0] => a
    [1] => b
    [2] => c
)
```
