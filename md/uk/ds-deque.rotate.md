---
navigation:
  - ds-deque.reversed.md: '« Ds\\Deque::reversed'
  - ds-deque.set.md: 'Ds\\Deque::set »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::rotate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::rotate

(PECL ds >= 1.0.0)

Ds\\Deque::rotate — Перемотує двосторонню чергу на задану кількість значень.

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

**Пример #1 Пример использования**Ds\\Deque::rotate()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c", "d"]);

$deque->rotate(1);  // Аналогично $a = $sequence->deque(); $deque->push($a);
print_r($deque);

$deque->rotate(2);
print_r($deque);
?>
```

Висновок наведеного прикладу буде схожим на:

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
