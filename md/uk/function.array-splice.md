---
navigation:
  - function.array-slice.html: « arrayslice
  - function.array-sum.html: arraysum »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arraysplice
---
# arraysplice

(PHP 4, PHP 5, PHP 7, PHP 8)

arraysplice — Видаляє частину масиву і замінює її чимось ще

### Опис

```methodsynopsis
array_splice(    array &$array,    int $offset,    ?int $length = null,    mixed $replacement = []): array
```

Видаляє `length` елементів, розташованих на відстані `offset` з масиву `array`, та замінює їх елементами масиву `replacement`, якщо він передано як параметр.

> **Зауваження**
> 
> Зверніть увагу, що числові ключі в масиві `array` не зберігаються.

> **Зауваження**: Якщо параметр `replacement` не є масивом, він буде [преобразован](language.types.array.html#language.types.array.casting) до нього (тобто `(array) $parameter`). Це може призвести до несподіваних результатів під час використання об'єкта або **`null`** в якості `replacement`

### Список параметрів

`array`

Вхідний масив

`offset`

Якщо параметр `offset` позитивний, будуть видалені елементи, що знаходяться на відстані offset від початку `array`

Якщо `offset` негативний, будуть видалені елементи, що знаходяться на відстані offset від кінця `input`

`length`

Якщо параметр `length` опущено, будуть видалені всі елементи, починаючи з позиції `offset` та до кінця масиву.

Якщо `length` вказаний і він позитивний, буде видалено саме стільки елементів.

Якщо параметр `length` від'ємний, то кінець частини елементів, що видаляється, буде відстояти на цю кількість від кінця масиву.

Якщо `length` заданий як 0, нічого видалено не буде.

**Підказка**

Порада: щоб видалити всі елементи масиву, починаючи з позиції `offset` до кінця масиву, тоді як вказано параметр `replacement`, використовуйте `count($input)` як параметр `length`

`replacement`

Якщо передано масив `replacement` як аргумент, тоді видалені елементи будуть замінені елементами цього масиву.

Якщо параметри `offset` і `length` такі, що з вихідного масиву нічого очікувати видалено, тоді елементи масиву `replacement` буде вставлено на позицію `offset`

> **Зауваження**
> 
> Зверніть увагу, що ключі масиву `replacement` не зберігаються.

Порада: якщо `replacement` є просто одним елементом, немає необхідності укладати його в `array()` або квадратні дужки, якщо тільки цей елемент сам не є масивом, об'єктом або **`null`**

### Значення, що повертаються

Повертає масив, що містить видалені елементи.

### список змін

| Версия | Описание |
| --- | --- |
|  | `length` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклади використання **arraysplice()****

```php
<?php
$input = array("red", "green", "blue", "yellow");
array_splice($input, 2);
var_dump($input);

$input = array("red", "green", "blue", "yellow");
array_splice($input, 1, -1);
var_dump($input);

$input = array("red", "green", "blue", "yellow");
array_splice($input, 1, count($input), "orange");
var_dump($input);

$input = array("red", "green", "blue", "yellow");
array_splice($input, -1, 1, array("black", "maroon"));
var_dump($input);
?>
```

Результат виконання цього прикладу:

```
array(2) {
  [0]=>
  string(3) "red"
  [1]=>
  string(5) "green"
}
array(2) {
  [0]=>
  string(3) "red"
  [1]=>
  string(6) "yellow"
}
array(2) {
  [0]=>
  string(3) "red"
  [1]=>
  string(6) "orange"
}
array(5) {
  [0]=>
  string(3) "red"
  [1]=>
  string(5) "green"
  [2]=>
  string(4) "blue"
  [3]=>
  string(5) "black"
  [4]=>
  string(6) "maroon"
}
```

**Приклад #2 Приклади використання **arraysplice()****

Наступні вирази еквівалентні:

```php
<?php

// добавить два элемента в $input
array_push($input, $x, $y);
array_splice($input, count($input), 0, array($x, $y));


// удалить последний элемент из $input
array_pop($input);
array_splice($input, -1);


// удалить первый элемент из $input
array_shift($input);
array_splice($input, 0, 1);


// добавить элемент в начало $input
array_unshift($input, $x, $y);
array_splice($input, 0, 0, array($x, $y));


// заменить в $input элемент с индексом $x на значение $y
$input[$x] = $y; // для Масивов, где ключ равен смещению
array_splice($input, $x, 1, $y);
?>
```

### Дивіться також

-   [arraymerge()](function.array-merge.html) - Зливає один або більше масивів
-   [arrayslice()](function.array-slice.html) - Вибирає зріз масиву
-   [unset()](function.unset.md) - Видаляє змінну
