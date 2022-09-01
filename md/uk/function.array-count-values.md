---
navigation:
  - function.array-combine.html: « arraycombine
  - function.array-diff-assoc.html: arraydiffassoc »
  - index.html: PHP Manual
  - ref.array.html: Функції для роботи з масивами
title: arraycountvalues
---
# arraycountvalues

(PHP 4, PHP 5, PHP 7, PHP 8)

arraycountvalues ​​— Підраховує кількість усіх значень масиву

### Опис

```methodsynopsis
array_count_values(array $array): array
```

Функція **arraycountvalues()** повертає масив, ключами якого є значення масиву `array`, а значеннями - кількість повторень значень `array`

### Список параметрів

`array`

Масив значень, що підраховуються

### Значення, що повертаються

Повертає асоціативний масив із значеннями `array` як ключі та їх кількість як значення.

### Помилки

Генерує помилку рівня **`E_WARNING`** для кожного елемента, який не є рядком (string) або цілим числом (int).

### Приклади

**Приклад #1 Приклад використання **arraycountvalues()****

```php
<?php
$array = array(1, "hello", 1, "world", "hello");
print_r(array_count_values($array));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [1] => 2
    [hello] => 2
    [world] => 1
)
```

### Дивіться також

-   [count()](function.count.html) - Підраховує кількість елементів масиву або Countable об'єкті
-   [arrayunique()](function.array-unique.html) - Прибирає значення, що повторюються, з масиву
-   [arrayvalues()](function.array-values.html) - Вибирає всі значення масиву
-   [countchars()](function.count-chars.html) - Повертає інформацію про символи, що входять до рядка
