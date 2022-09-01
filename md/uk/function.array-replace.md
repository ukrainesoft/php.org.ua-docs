---
navigation:
  - function.array-replace-recursive.html: « arrayreplacerecursive
  - function.array-reverse.html: arrayreverse »
  - index.html: PHP Manual
  - ref.array.html: Функції для роботи з масивами
title: arrayreplace
---
# arrayreplace

(PHP 5> = 5.3.0, PHP 7, PHP 8)

arrayreplace — Замінює елементи масиву на інші передані масиви.

### Опис

```methodsynopsis
array_replace(array $array, array ...$replacements): array
```

**arrayreplace()** замінює значення масиву `array` значеннями з такими ж ключами інших переданих масивів. Якщо ключ з першого масиву присутній у другому масиві, його значення замінюється значенням з другого масиву. Якщо ключ є у другому масиві, але відсутній у першому – він буде створений у першому масиві. Якщо ключ є тільки в першому масиві, то збережеться як є. Якщо для заміни передано кілька масивів, вони будуть оброблені в порядку передачі і наступні масиви перезаписуватимуть значення з попередніх.

**arrayreplace()** не рекурсивна: значення першого масиву буде замінено незалежно від типу значень другого масиву, навіть якщо це будуть вкладені масиви.

### Список параметрів

`array`

Масив, елементи якого потрібно замінити.

`replacements`

Масиви, з яких братимуться елементи для заміни. Значення наступного масиву затирають значення попереднього.

### Значення, що повертаються

Повертає масив (array).

### Приклади

**Приклад #1 Приклад використання **arrayreplace()****

```php
<?php
$base = array("orange", "banana", "apple", "raspberry");
$replacements = array(0 => "pineapple", 4 => "cherry");
$replacements2 = array(0 => "grape");

$basket = array_replace($base, $replacements, $replacements2);
print_r($basket);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => grape
    [1] => banana
    [2] => apple
    [3] => raspberry
    [4] => cherry
)
```

### Дивіться також

-   [arrayreplacerecursive()](function.array-replace-recursive.html) - Рекурсивно замінює елементи першого масиву на елементи переданих масивів.
-   [arraymerge()](function.array-merge.html) - Зливає один або більше масивів
