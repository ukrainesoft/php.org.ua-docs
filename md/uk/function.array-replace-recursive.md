---
navigation:
  - function.array-reduce.html: « arrayreduce
  - function.array-replace.html: arrayreplace »
  - index.html: PHP Manual
  - ref.array.html: Функції для роботи з масивами
title: arrayreplacerecursive
---
# arrayreplacerecursive

(PHP 5> = 5.3.0, PHP 7, PHP 8)

arrayreplacerecursive — Рекурсивно замінює елементи першого масиву на елементи переданих масивів.

### Опис

```methodsynopsis
array_replace_recursive(array $array, array ...$replacements): array
```

**arrayreplacerecursive()** замінює значення масиву `array` на відповідні за ключами значення всіх наступних масивів. Якщо ключ першого масиву є у другому, його значення буде замінено на значення другого масиву. Якщо ключ є у другому масиві, але відсутній у першому, він буде створений у першому масиві. Якщо ключ є лише у першому масиві, він залишається як є. Якщо передано кілька масивів, вони будуть оброблені за порядком, наступні перезаписують попередні значення.

**arrayreplacerecursive()** - рекурсивна функція: вона рекурсивно заглиблюватиметься в масиви і застосовуватиме до всіх внутрішніх значень той самий процес.

Якщо значення, передане перший масив є скалярним, воно буде замінено значенням у другому масиві, яке може бути скалярним значенням або масивом. Якщо обидва значення передані в перший масив і в другий масив - масиви, **arrayreplacerecursive()** замінюватиме їх значення рекурсивно.

### Список параметрів

`array`

Масив, елементи якого буде замінено.

`replacements`

Масиви, з яких братимуться елементи для заміни.

### Значення, що повертаються

Повертає масив (array).

### Приклади

**Приклад #1 Приклад використання **arrayreplacerecursive()****

```php
<?php
$base = array('citrus' => array( "orange") , 'berries' => array("blackberry", "raspberry"), );
$replacements = array('citrus' => array('pineapple'), 'berries' => array('blueberry'));

$basket = array_replace_recursive($base, $replacements);
print_r($basket);

$basket = array_replace($base, $replacements);
print_r($basket);
?>
```

Результат виконання цього прикладу:

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

**Приклад #2 **arrayreplacerecursive()** та рекурсивна поведінка**

```php
<?php
$base = array('citrus' => array("orange") , 'berries' => array("blackberry", "raspberry"), 'others' => 'banana' );
$replacements = array('citrus' => 'pineapple', 'berries' => array('blueberry'), 'others' => array('litchis'));
$replacements2 = array('citrus' => array('pineapple'), 'berries' => array('blueberry'), 'others' => 'litchis');

$basket = array_replace_recursive($base, $replacements, $replacements2);
print_r($basket);

?>
```

Результат виконання цього прикладу:

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

-   [arrayreplace()](function.array-replace.html) - Замінює елементи масиву елементами інших переданих масивів
-   [arraymergerecursive()](function.array-merge-recursive.html) - Рекурсивне злиття одного або більше масивів
