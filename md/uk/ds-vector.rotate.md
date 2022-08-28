Перемотує вектор на задану кількість значень

-   [« Ds\\Vector::reversed](ds-vector.reversed.html)
    
-   [Ds\\Vector::set »](ds-vector.set.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Перемотує вектор на задану кількість значень
    

# ДсVector::rotate

(PECL ds >= 1.0.0)

ДсVector::rotate — Перемотує вектор на задану кількість значень

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

**Приклад #1 Приклад використання **ДсVector::rotate()****

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c", "d"]);

$vector->rotate(1); // Аналогично $a = $vector->shift(); $vector->push($a);
print_r($vector);

$vector->rotate(2);
print_r($vector);
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
Ds\Vector Object
(
    [0] => d
    [1] => a
    [2] => b
    [3] => c
)
```