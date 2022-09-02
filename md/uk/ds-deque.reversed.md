---
navigation:
  - ds-deque.reverse.md: '« DsDeque::reverse'
  - ds-deque.rotate.md: 'ДсDeque::rotate »'
  - index.md: PHP Manual
  - class.ds-deque.md: Двостороння черга
title: 'ДсDeque::reversed'
---
# ДсDeque::reversed

(PECL ds >= 1.0.0)

ДсDeque::reversed — Повертає перегорнуту копію двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::reversed(): Ds\Deque
```

Повертає перегорнуту копію двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія двосторонньої черги.

> **Зауваження**
> 
> Поточна двостороння черга не зміниться.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::reversed()****

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

print_r($deque->reversed());
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
Ds\Deque Object
(
    [0] => a
    [1] => b
    [2] => c
)
```
