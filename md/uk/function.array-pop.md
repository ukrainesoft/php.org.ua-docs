---
navigation:
  - function.array-pad.md: « array\_pad
  - function.array-product.md: array\_product »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_pop
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_pop

(PHP 4, PHP 5, PHP 7, PHP 8)

array\_pop — Витягує останній елемент масиву

### Опис

```methodsynopsis
array_pop(array &$array): mixed
```

**array\_pop()** витягує та повертає значення останнього елемента масиву `array`зменшуючи розмір `array` на один елемент.

> **Зауваження**: При виклику функція [скидає](function.reset.md) вказівник масиву, переданого параметром.

### Список параметрів

`array`

Масив, з якого береться значення.

### Значення, що повертаються

Повертає значення останнього елемента масиву `array`. Якщо `array` нехай, буде повернутий **`null`**

### Приклади

**Приклад #1 Приклад використання** array\_pop()\*\*\*\*

```php
<?php
$stack = array("orange", "banana", "apple", "raspberry");
$fruit = array_pop($stack);
print_r($stack);
?>
```

Після цього $stack буде лише 3 елемента:

```
Array
(
    [0] => orange
    [1] => banana
    [2] => apple
)
```

и`raspberry`будет присвоено переменной $fruit.

### Дивіться також

-   [array\_push()](function.array-push.md) \- Додає один або кілька елементів у кінець масиву
-   [array\_shift()](function.array-shift.md) \- Витягує перший елемент масиву
-   [array\_unshift()](function.array-unshift.md) \- Додає один або кілька елементів на початок масиву
