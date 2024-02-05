---
navigation:
  - function.array-search.md: « array\_search
  - function.array-slice.md: array\_slice »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_shift
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_shift

(PHP 4, PHP 5, PHP 7, PHP 8)

array\_shift — Витягує перший елемент масиву

### Опис

```methodsynopsis
array_shift(array &$array): mixed
```

**array\_shift()** здобуває перше значення масиву `array` і повертає його, скорочуючи розмір `array` на один елемент. Усі числові ключі будуть змінені таким чином, що нумерація масиву розпочнеться з нуля, тоді як рядкові ключі залишаться незмінними.

> **Зауваження**: При виклику функція [скидає](function.reset.md) вказівник масиву, переданого параметром.

### Список параметрів

`array`

Вхідний масив

### Значення, що повертаються

Возвращает извлекаемое значение или\*\*`null`\*\*, якщо `array` порожній чи не є масивом.

### Приклади

**Приклад #1 Приклад використання** array\_shift()\*\*\*\*

```php
<?php
$stack = array("orange", "banana", "apple", "raspberry");
$fruit = array_shift($stack);
print_r($stack);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => banana
    [1] => apple
    [2] => raspberry
)
```

и значение`orange`будет присвоено переменной $fruit.

### Дивіться також

-   [array\_unshift()](function.array-unshift.md) \- Додає один або кілька елементів на початок масиву
-   [array\_push()](function.array-push.md) \- Додає один або кілька елементів у кінець масиву
-   [array\_pop()](function.array-pop.md) \- Витягує останній елемент масиву
