---
navigation:
  - function.array-filter.md: « array\_filter
  - function.array-intersect-assoc.md: array\_intersect\_assoc »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_flip
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_flip

(PHP 4, PHP 5, PHP 7, PHP 8)

array\_flip — Змінює місцями ключі зі своїми значеннями в масиві

### Опис

```methodsynopsis
array_flip(array $array): array
```

Функция**array\_flip()** повертає масив (array) навпаки, тобто ключі масиву `array`становятся значениями, а значения массива`array`становятся ключами.

Обратите внимание, что значения массива`array` повинні бути коректними ключами, тобто вони повинні мати тип int чи string. Якщо значення має невірний тип, буде видано попередження та дана пара ключ/значення *не буде включено до результату*

Якщо значення зустрічається кілька разів, для обробки буде використовуватися останній зустрінутий ключ, а всі інші будуть втрачені.

### Список параметрів

`array`

Масив пар, що перевертаються, ключ/значення.

### Значення, що повертаються

Повертає перевернутий масив.

### Приклади

**Пример #1 Пример использования**array\_flip()\*\*\*\*

```php
<?php
$input = array("oranges", "apples", "pears");
$flipped = array_flip($input);

print_r($flipped);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [oranges] => 0
    [apples] => 1
    [pears] => 2
)
```

**Пример #2 Пример использования**array\_flip()\*\* з колізіями\*\*

```php
<?php
$input = array("a" => 1, "b" => 1, "c" => 2);
$flipped = array_flip($input);

print_r($flipped);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [1] => b
    [2] => c
)
```

### Дивіться також

-   [array\_values()](function.array-values.md) \- Повертає всі значення масиву
-   [array\_keys()](function.array-keys.md) \- Повертає все або деяке підмножина ключів масиву
-   [array\_reverse()](function.array-reverse.md) \- Повертає масив із елементами у зворотному порядку
