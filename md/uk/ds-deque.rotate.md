---
navigation:
  - ds-deque.reversed.html: '« DsDeque::reversed'
  - ds-deque.set.html: 'ДсDeque::set »'
  - index.html: PHP Manual
  - class.ds-deque.html: Двостороння черга
title: 'ДсDeque::rotate'
---
# ДсDeque::rotate

(PECL ds >= 1.0.0)

ДсDeque::rotate — Перемотує двосторонню чергу на задану кількість значень.

### Опис

```methodsynopsis
public Ds\Deque::rotate(int $rotations): void
```

Перемотує двосторонню чергу на задану кількість значень. Ця операція аналогічна до виконання задану кількість разів коду `$deque->push($deque->shift())`якщо кількість оборотів позитивно і `$deque->unshift($deque->pop())`якщо негативно.

### Список параметрів

`rotations`

Кількість значень, які треба "перемотати".

### Значення, що повертаються

Функція не повертає значення після виконання. Буде змінено поточну двосторонню чергу.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::rotate()****

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c", "d"]);

$deque->rotate(1);  // Аналогично $a = $sequence->deque(); $deque->push($a);
print_r($deque);

$deque->rotate(2);
print_r($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
(
    [0] => b
    [1] => c
    [2] => d
    [3] => a
)
Ds\Deque Object
(
    [0] => d
    [1] => a
    [2] => b
    [3] => c
)
```
