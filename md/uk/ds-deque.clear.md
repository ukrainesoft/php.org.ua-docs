---
navigation:
  - ds-deque.capacity.html: '« DsDeque::capacity'
  - ds-deque.construct.html: 'ДсDeque::construct »'
  - index.html: PHP Manual
  - class.ds-deque.html: Двостороння черга
title: 'ДсDeque::clear'
---
# ДсDeque::clear

(PECL ds >= 1.0.0)

ДсDeque::clear — Видаляє всі значення з двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::clear(): void
```

Видаляє всі значення двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::clear()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
print_r($deque);

$deque->clear();
print_r($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Deque Object
(
)
```
