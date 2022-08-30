Перетворює рядок на масив

-   [« strshuffle](function.str-shuffle.html)
    
-   [strstartswith »](function.str-starts-with.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з рядками](ref.strings.html)
    
-   Перетворює рядок на масив
    

# strsplit

(PHP 5, PHP 7, PHP 8)

strsplit — Перетворює рядок на масив

### Опис

```methodsynopsis
str_split(string $string, int $length = 1): array
```

Перетворює рядок на масив.

### Список параметрів

`string`

Вхідний рядок.

`length`

Максимальна довжина фрагмента.

### Значення, що повертаються

Якщо вказано необов'язковий параметр `length`, що повертається масив буде розбитий на фрагменти, кожен з яких матиме довжину `length`, За винятком останнього фрагмента, який може бути коротшим, якщо рядок ділиться нерівномірно. За замовчуванням параметр `length` дорівнює `1`тобто розмір кожного фрагмента буде один байт.

### Помилки

Якщо параметр `length` менше `1`, буде викинута помилка [ValueError](class.valueerror.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер якщо параметр `length` менше `1`, буде викинута помилка [ValueError](class.valueerror.html); раніше, натомість видавалася помилка рівня **`E_WARNING`**, а функція повертала **`false`** |

### Приклади

**Приклад #1 Приклад використання **strsplit()****

```php
<?php

$str = "Hello Friend";

$arr1 = str_split($str);
$arr2 = str_split($str, 3);

print_r($arr1);
print_r($arr2);

?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => H
    [1] => e
    [2] => l
    [3] => l
    [4] => o
    [5] =>
    [6] => F
    [7] => r
    [8] => i
    [9] => e
    [10] => n
    [11] => d
)

Array
(
    [0] => Hel
    [1] => lo
    [2] => Fri
    [3] => end
)
```

### Примітки

> **Зауваження**
> 
> Функція **strsplit()** здійснює розбивку за байтами, а не за символами, у разі використання рядків у багатобайтних кодуваннях. Використовуйте функцію [мбstrsplit()](function.mb-str-split.html), щоб розбити рядок кодових точок.

### Дивіться також

-   [мбstrsplit()](function.mb-str-split.html) - Якщо заданий багатобайтовий рядок повертає масив символів
-   [chunksplit()](function.chunk-split.html) - Розбиває рядок на фрагменти
-   [pregsplit()](function.preg-split.html) - Розбиває рядок за регулярним виразом
-   [explode()](function.explode.html) - Розбиває рядок за допомогою роздільника
-   [countchars()](function.count-chars.html) - Повертає інформацію про символи, що входять до рядка
-   [strwordcount()](function.str-word-count.html) - Повертає інформацію про слова, що входять до рядка
-   [for](control-structures.for.html)