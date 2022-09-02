---
navigation:
  - ds-deque.sum.md: '« DsDeque::sum'
  - ds-deque.unshift.md: 'ДсDeque::unshift »'
  - index.md: PHP Manual
  - class.ds-deque.md: Двостороння черга
title: 'ДсDeque::toArray'
---
# ДсDeque::toArray

(PECL ds >= 1.0.0)

ДсDeque::toArray — Перетворює двосторонню чергу на масив (array)

### Опис

```methodsynopsis
public Ds\Deque::toArray(): array
```

Перетворює двосторонню чергу на масив (array).

> **Зауваження**
> 
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array), що містить всі елементи двосторонньої черги із збереженням їхнього порядку.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::toArray()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

var_dump($deque->toArray());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
