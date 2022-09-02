---
navigation:
  - function.str-shuffle.md: « strshuffle
  - function.str-starts-with.md: strstartswith »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strsplit
---
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

Якщо параметр `length` менше `1`, буде викинута помилка [ValueError](class.valueerror.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер якщо параметр `length` менше `1`, буде викинута помилка [ValueError](class.valueerror.md); раніше, натомість видавалася помилка рівня **`E_WARNING`**, а функція повертала **`false`** |

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
> Функція **strsplit()** здійснює розбивку за байтами, а не за символами, у разі використання рядків у багатобайтних кодуваннях. Використовуйте функцію [мбstrsplit()](function.mb-str-split.md), щоб розбити рядок кодових точок.

### Дивіться також

-   [мбstrsplit()](function.mb-str-split.md) - Якщо заданий багатобайтовий рядок повертає масив символів
-   [chunksplit()](function.chunk-split.md) - Розбиває рядок на фрагменти
-   [pregsplit()](function.preg-split.md) - Розбиває рядок за регулярним виразом
-   [explode()](function.explode.md) - Розбиває рядок за допомогою роздільника
-   [countchars()](function.count-chars.md) - Повертає інформацію про символи, що входять до рядка
-   [strwordcount()](function.str-word-count.md) - Повертає інформацію про слова, що входять до рядка
-   [for](control-structures.for.md)
