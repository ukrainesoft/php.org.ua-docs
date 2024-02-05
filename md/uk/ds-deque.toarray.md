---
navigation:
  - ds-deque.sum.md: '« Ds\\Deque::sum'
  - ds-deque.unshift.md: 'Ds\\Deque::unshift »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::toArray

(PECL ds >= 1.0.0)

Ds\\Deque::toArray — Перетворює двосторонню чергу на масив (array)

### Опис

```methodsynopsis
public Ds\Deque::toArray(): array
```

Перетворює двосторонню чергу на масив (array).

> **Зауваження** :
> 
> Приведення до типу array поки що не підтримується.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array), що містить всі елементи двосторонньої черги із збереженням їхнього порядку.

### Приклади

**Приклад #1 Приклад использования метода**Ds\\Deque::toArray()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

var_dump($deque->toArray());
?>
```

Висновок наведеного прикладу буде схожим на:

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
