---
navigation:
  - ds-sequence.shift.md: '« Ds\\Sequence::shift'
  - ds-sequence.sort.md: 'Ds\\Sequence::sort »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::slice'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::slice

(PECL ds >= 1.0.0)

Ds\\Sequence::slice — Повертає під-колекцію із заданого діапазону

### Опис

```methodsynopsis
abstract public Ds\Sequence::slice(int $index, int $length = ?): Ds\Sequence
```

Повертає під-колекцію з діапазону, заданого початковим індексом `index` та довжиною `length`

### Список параметрів

`index`

Індекс, що задає початок діапазону.

Якщо позитивний, то відраховуватиметься від початку колекції. Якщо негативний, від кінця.

`length`

Позитивне значення визначає, скільки елементів буде взято. Якщо кількість елементів колекції менша від заданого значення, повернеться стільки елементів, скільки є. Негативне значення задасть індекс, відрахований від кінця колекції, що визначає кінець діапазону. Якщо довжина не задана, то буде повернено всі елементи колекції від заданого індексу до кінця колекції.

### Значення, що повертаються

Під-колекція із заданого діапазону.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::slice()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", "d", "e"]);

// Диапазон от 2 до конца
print_r($sequence->slice(2));

// Диапазон от 1 с длиной 3
print_r($sequence->slice(1, 3));

// Диапазон от 1 до конца
print_r($sequence->slice(1));

// Диапазон от 2 с конца до начала
print_r($sequence->slice(-2));

// Диапазон от 1 от 1 с конца
print_r($sequence->slice(1, -1));
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Vector Object
(
    [0] => c
    [1] => d
    [2] => e
)
Ds\Vector Object
(
    [0] => b
    [1] => c
    [2] => d
)
Ds\Vector Object
(
    [0] => b
    [1] => c
    [2] => d
    [3] => e
)
Ds\Vector Object
(
    [0] => d
    [1] => e
)
Ds\Vector Object
(
    [0] => b
    [1] => c
    [2] => d
)
```
