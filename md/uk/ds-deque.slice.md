---
navigation:
  - ds-deque.shift.md: '« Ds\\Deque::shift'
  - ds-deque.sort.md: 'Ds\\Deque::sort »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::slice'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::slice

(PECL ds >= 1.0.0)

Ds\\Deque::slice — Повертає почергово із заданого діапазону

### Опис

```methodsynopsis
public Ds\Deque::slice(int $index, int $length = ?): Ds\Deque
```

Повертає почергово з діапазону заданого початковим індексом `index` та довжиною `length`

### Список параметрів

`index`

Індекс, що задає початок діапазону.

Якщо позитивний, то відраховуватиметься від початку колекції. Якщо негативний, від кінця.

`length`

Позитивне значення визначає, скільки елементів буде взято. Якщо кількість елементів двосторонньої черги менша за задане значення, повернеться стільки елементів, скільки є. Негативне значення задасть індекс, відрахований від кінця двосторонньої черги, що визначає кінець діапазону. Якщо довжина не задана, то буде повернено всі елементи двосторонньої черги від заданого індексу до кінця колекції.

### Значення, що повертаються

Підчергово із заданого діапазону.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::slice()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c", "d", "e"]);

// Slice from 2 onwards
print_r($deque->slice(2));

// Slice from 1, for a length of 3
print_r($deque->slice(1, 3));

// Slice from 1 onwards
print_r($deque->slice(1));

// Slice from 2 from the end onwards
print_r($deque->slice(-2));

// Slice from 1 to 1 from the end
print_r($deque->slice(1, -1));
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Deque Object
(
    [0] => c
    [1] => d
    [2] => e
)
Ds\Deque Object
(
    [0] => b
    [1] => c
    [2] => d
)
Ds\Deque Object
(
    [0] => b
    [1] => c
    [2] => d
    [3] => e
)
Ds\Deque Object
(
    [0] => d
    [1] => e
)
Ds\Deque Object
(
    [0] => b
    [1] => c
    [2] => d
)
```
