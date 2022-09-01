---
navigation:
  - function.rsort.html: « rsort
  - function.sizeof.html: sizeof »
  - index.html: PHP Manual
  - ref.array.html: Функції для роботи з масивами
title: shuffle
---
# shuffle

(PHP 4, PHP 5, PHP 7, PHP 8)

shuffle - Перемішує масив

### Опис

```methodsynopsis
shuffle(array &$array): bool
```

Ця функція перемішує елементи масиву у випадковому порядку. Використовується псевдовипадковий генератор випадкових чисел, тому дана функція не підходить для задач криптографії.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Внутрішній алгоритм отримання випадкових чисел [изменён](migration71.incompatible.html#migration71.incompatible.rand-srand-aliases) з функції rand бібліотеки libc на генератор на базі [» Вихря Мерсена.](http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.html) |

### Приклади

**Приклад #1 Приклад використання **shuffle()****

```php
<?php
$numbers = range(1, 20);
shuffle($numbers);
foreach ($numbers as $number) {
    echo "$number ";
}
?>
```

### Примітки

> **Зауваження**: Ця функція надає нові ключі елементам `array`. Вона видалить усі існуючі ключі, а не просто переупорядкує їх.

> **Зауваження**
> 
> Скидає внутрішній покажчик масиву перший елемент.

### Дивіться також

-   [arrayrand()](function.array-rand.html) - Вибирає один або кілька випадкових ключів із масиву
-   [Порівняння функцій сортування масивів](array.sorting.html)
