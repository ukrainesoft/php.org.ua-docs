---
navigation:
  - ds-vector.shift.md: '« Ds\\Vector::shift'
  - ds-vector.sort.md: 'Ds\\Vector::sort »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::slice'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::slice

(PECL ds >= 1.0.0)

Ds\\Vector::slice — Повертає підвектор із заданого діапазону

### Опис

```methodsynopsis
public Ds\Vector::slice(int $index, int $length = ?): Ds\Vector
```

Повертає підвектор із діапазону заданого початковим індексом `index` та довжиною `length`

### Список параметрів

`index`

Індекс, що задає початок діапазону.

Якщо позитивний, то відраховуватиметься від початку вектора. Якщо негативний, від кінця.

`length`

Позитивне значення визначає, скільки елементів буде взято. Якщо кількість елементів вектора менша за задане значення, повернеться стільки елементів, скільки є. Негативне значення задасть індекс, відрахований від кінця вектора, що визначає кінець діапазону. Якщо довжина не задана, то буде повернено всі елементи вектора від заданого індексу до кінця вектора.

### Значення, що повертаються

Підвектор із заданого діапазону.

### Приклади

**Приклад #1 Приклад використання** Ds\\Vector::slice()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c", "d", "e"]);

// Slice from 2 onwards
print_r($vector->slice(2));

// Slice from 1, for a length of 3
print_r($vector->slice(1, 3));

// Slice from 1 onwards
print_r($vector->slice(1));

// Slice from 2 from the end onwards
print_r($vector->slice(-2));

// Slice from 1 to 1 from the end
print_r($vector->slice(1, -1));
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
