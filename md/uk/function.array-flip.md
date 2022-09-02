---
navigation:
  - function.array-filter.md: « arrayfilter
  - function.array-intersect-assoc.md: arrayintersectassoc »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayflip
---
# arrayflip

(PHP 4, PHP 5, PHP 7, PHP 8)

arrayflip — Змінює місцями ключі зі своїми значеннями в масиві

### Опис

```methodsynopsis
array_flip(array $array): array
```

Функція **arrayflip()** повертає масив (array) навпаки, тобто ключі масиву `array` стають значеннями, а значення масиву `array` стають ключами.

Зверніть увагу, що значення масиву `array` повинні бути коректними ключами, тобто вони повинні мати тип int чи string. Якщо значення має невірний тип, буде видано попередження та дана пара ключ/значення *не буде включено до результату*

Якщо значення зустрічається кілька разів, для обробки буде використовуватися останній зустрінутий ключ, а всі інші будуть втрачені.

### Список параметрів

`array`

Масив пар, що перевертаються, ключ/значення.

### Значення, що повертаються

Повертає перевернутий масив.

### Приклади

**Приклад #1 Приклад використання **arrayflip()****

```php
<?php
$input = array("oranges", "apples", "pears");
$flipped = array_flip($input);

print_r($flipped);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [oranges] => 0
    [apples] => 1
    [pears] => 2
)
```

**Приклад #2 Приклад використання **arrayflip()** з колізіями**

```php
<?php
$input = array("a" => 1, "b" => 1, "c" => 2);
$flipped = array_flip($input);

print_r($flipped);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [1] => b
    [2] => c
)
```

### Дивіться також

-   [arrayvalues()](function.array-values.md) - Вибирає всі значення масиву
-   [arraykeys()](function.array-keys.md) - Повертає все або деяке підмножина ключів масиву
-   [arrayreverse()](function.array-reverse.md) - Повертає масив із елементами у зворотному порядку
