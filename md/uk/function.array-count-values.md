---
navigation:
  - function.array-combine.md: « array\_combine
  - function.array-diff-assoc.md: array\_diff\_assoc »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_count\_values
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_count\_values

(PHP 4, PHP 5, PHP 7, PHP 8)

array\_count\_values ​​- Підраховує кількість входжень кожного окремого значення в масиві

### Опис

```methodsynopsis
array_count_values(array $array): array
```

Функция**array\_count\_values()** повертає масив, ключами якого є значення масиву `array` (які мають бути цілими числами (int) чи рядками (string)), а значеннями - кількість повторень значень `array`

### Список параметрів

`array`

Масив значень, що підраховуються

### Значення, що повертаються

Повертає асоціативний масив із значеннями `array` як ключі та їх кількість як значення.

### Помилки

Генерирует ошибку уровня\*\*`E_WARNING`\*\* для кожного елемента, який не є рядком (string) або цілим числом (int).

### Приклади

**Пример #1 Пример использования**array\_count\_values()\*\*\*\*

```php
<?php
$array = array(1, "hello", 1, "world", "hello");
print_r(array_count_values($array));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [1] => 2
    [hello] => 2
    [world] => 1
)
```

### Дивіться також

-   [count()](function.count.md) \- Підраховує кількість елементів масиву або Countable об'єкті
-   [array\_unique()](function.array-unique.md) \- Прибирає значення, що повторюються, з масиву
-   [array\_values()](function.array-values.md) \- Повертає всі значення масиву
-   [count\_chars()](function.count-chars.md) \- Повертає інформацію про символи, що входять до рядка
