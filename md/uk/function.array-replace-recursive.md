---
navigation:
  - function.array-reduce.md: « array\_reduce
  - function.array-replace.md: array\_replace »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_replace\_recursive
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_replace\_recursive

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

array\_replace\_recursive — Рекурсивно замінює елементи першого масиву на елементи переданих масивів.

### Опис

```methodsynopsis
array_replace_recursive(array $array, array ...$replacements): array
```

**array\_replace\_recursive()** замінює значення масиву `array` на відповідні за ключами значення всіх наступних масивів. Якщо ключ із першого масиву є у другому, його значення буде замінено на значення другого масиву. Якщо ключ є у другому масиві, але відсутній у першому, він буде створений у першому масиві. Якщо ключ є лише у першому масиві, він залишається як є. Якщо передано кілька масивів, вони будуть оброблені за порядком, наступні перезаписують попередні значення.

**array\_replace\_recursive()** - рекурсивна функція: вона рекурсивно заглиблюватиметься в масиви і застосовуватиме до всіх внутрішніх значень той самий процес.

Якщо значення, передане перший масив є скалярним, воно буде замінено значенням у другому масиві, яке може бути скалярним значенням або масивом. Якщо обидва значення передані в перший масив і в другий масив - масиви, **array\_replace\_recursive()** замінюватиме їх значення рекурсивно.

### Список параметрів

`array`

Масив, елементи якого буде замінено.

`replacements`

Масиви, з яких братимуться елементи для заміни.

### Значення, що повертаються

Повертає масив (array).

### Приклади

**Приклад #1 Приклад використання** array\_replace\_recursive()\*\*\*\*

```php
<?php
$base = array('citrus' => array( "orange") , 'berries' => array("blackberry", "raspberry"), );
$replacements = array('citrus' => array('pineapple'), 'berries' => array('blueberry'));

$basket = array_replace_recursive($base, $replacements);
print_r($basket);

$basket = array_replace($base, $replacements);
print_r($basket);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [citrus] => Array
        (
            [0] => pineapple
        )

    [berries] => Array
        (
            [0] => blueberry
            [1] => raspberry
        )

)
Array
(
    [citrus] => Array
        (
            [0] => pineapple
        )

    [berries] => Array
        (
            [0] => blueberry
        )

)
```

**Приклад #2**array\_replace\_recursive()**и рекурсивное поведение**

```php
<?php
$base = array('citrus' => array("orange") , 'berries' => array("blackberry", "raspberry"), 'others' => 'banana' );
$replacements = array('citrus' => 'pineapple', 'berries' => array('blueberry'), 'others' => array('litchis'));
$replacements2 = array('citrus' => array('pineapple'), 'berries' => array('blueberry'), 'others' => 'litchis');

$basket = array_replace_recursive($base, $replacements, $replacements2);
print_r($basket);

?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [citrus] => Array
        (
            [0] => pineapple
        )

    [berries] => Array
        (
            [0] => blueberry
            [1] => raspberry
        )

    [others] => litchis
)
```

### Дивіться також

-   [array\_replace()](function.array-replace.md) \- Замінює елементи масиву елементами інших переданих масивів
-   [array\_merge\_recursive()](function.array-merge-recursive.md) \- Рекурсивне злиття одного або більше масивів
