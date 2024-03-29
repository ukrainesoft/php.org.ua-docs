---
navigation:
  - function.sort.md: « sort
  - function.uksort.md: uksort »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: uasort
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# uasort

(PHP 4, PHP 5, PHP 7, PHP 8)

uasort — Сортує масив користувальницької функції порівняння, зберігаючи асоціацію індексів

### Опис

```methodsynopsis
uasort(array &$array, callable $callback): true
```

Сортує масив `array` функцією користувача порівняння так, щоб ключі масиву зберігали кореляцію зі значеннями, з якими вони пов'язані.

Функцією користуються для сортування асоціативних масивів, котрим важливий поточний порядок елементів.

> **Зауваження** :
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

> **Зауваження** :
> 
> Скидає внутрішній покажчик масиву перший елемент.

### Список параметрів

`array`

Вхідний масив

`callback`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |
| 8.0.0 | Тепер функція видасть помилку рівня **`E_WARNING`**, якщо параметр callback-функції, переданої у параметр `callback`, очікує на передачу значення за посиланням. |

### Приклади

**Приклад #1 Простий приклад використання функції **uasort()****

```php
<?php

// Функция сравнения
function cmp($a, $b) {
    if ($a == $b) {
        return 0;
    }
    return ($a < $b) ? -1 : 1;
}

// Сортируемый массив
$array = array('a' => 4, 'b' => 8, 'c' => -1, 'd' => -9, 'e' => 2, 'f' => 5, 'g' => 3, 'h' => -4);
print_r($array);

// Сортируем и выводим получившийся массив
uasort($array, 'cmp');
print_r($array);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [a] => 4
    [b] => 8
    [c] => -1
    [d] => -9
    [e] => 2
    [f] => 5
    [g] => 3
    [h] => -4
)
Array
(
    [d] => -9
    [h] => -4
    [c] => -1
    [e] => 2
    [g] => 3
    [a] => 4
    [f] => 5
    [b] => 8
)
```

### Дивіться також

-   [usort()](function.usort.md) \- Сортує масив за значеннями використовуючи функцію користувача для порівняння елементів
-   [uksort()](function.uksort.md) \- Сортує масив за ключами користувальницькою функцією порівняння
-   [Порівняння функцій сортування масивів](array.sorting.md)
