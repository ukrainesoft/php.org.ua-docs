---
navigation:
  - ds-vector.reversed.md: '« Ds\\Vector::reversed'
  - ds-vector.set.md: 'Ds\\Vector::set »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::rotate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::rotate

(PECL ds >= 1.0.0)

Ds\\Vector::rotate — Перемотує вектор на задану кількість значень

### Опис

```methodsynopsis
public Ds\Vector::rotate(int $rotations): void
```

Перемотує вектор на задану кількість значень. Ця операція аналогічна до виконання задану кількість разів коду `$vector->push($vector->shift())`якщо кількість оборотів позитивно і `$vector->unshift($vector->pop())`якщо негативно.

### Список параметрів

`rotations`

Кількість значень, які треба "перемотати".

### Значення, що повертаються

Функція не повертає значення після виконання. Буде змінено поточний вектор.

### Приклади

**Пример #1 Пример использования**Ds\\Vector::rotate()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c", "d"]);

$vector->rotate(1); // Аналогично $a = $vector->shift(); $vector->push($a);
print_r($vector);

$vector->rotate(2);
print_r($vector);
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
Ds\Vector Object
(
    [0] => d
    [1] => a
    [2] => b
    [3] => c
)
```
