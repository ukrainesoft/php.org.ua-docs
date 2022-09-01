---
navigation:
  - function.array-replace.html: « arrayreplace
  - function.array-search.html: arraysearch »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayreverse
---
# arrayreverse

(PHP 4, PHP 5, PHP 7, PHP 8)

arrayreverse — Повертає масив із елементами у зворотному порядку

### Опис

```methodsynopsis
array_reverse(array $array, bool $preserve_keys = false): array
```

Приймає масив `array` та повертає новий масив, що містить елементи вихідного масиву у зворотному порядку.

### Список параметрів

`array`

Вхідний масив

`preserve_keys`

Якщо встановлено **`true`**, то числові ключі будуть збережені. Нечислові ключі не схильні до цієї опції і завжди зберігаються.

### Значення, що повертаються

Повертає масив із елементами у зворотному порядку.

### Приклади

**Приклад #1 Приклад використання **arrayreverse()****

```php
<?php
$input  = array("php", 4.0, array("green", "red"));
$reversed = array_reverse($input);
$preserved = array_reverse($input, true);

print_r($input);
print_r($reversed);
print_r($preserved);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => php
    [1] => 4
    [2] => Array
        (
            [0] => green
            [1] => red
        )

)
Array
(
    [0] => Array
        (
            [0] => green
            [1] => red
        )

    [1] => 4
    [2] => php
)
Array
(
    [2] => Array
        (
            [0] => green
            [1] => red
        )

    [1] => 4
    [0] => php
)
```

### Дивіться також

-   [arrayflip()](function.array-flip.html) - Змінює місцями ключі з їхніми значеннями у масиві
