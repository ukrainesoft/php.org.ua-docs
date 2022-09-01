---
navigation:
  - function.natcasesort.html: « natcasesort
  - function.next.html: next »
  - index.html: PHP Manual
  - ref.array.html: Функції для роботи з масивами
title: нацорт
---
# нацорт

(PHP 4, PHP 5, PHP 7, PHP 8)

natsort - Сортує масив, використовуючи алгоритм "natural order"

### Опис

```methodsynopsis
natsort(array &$array): bool
```

Ця функція реалізує алгоритм сортування, у якому порядок літерно-цифрових рядків буде звичним для людини. Такий алгоритм називається "natural ordering". Відмінність алгоритму "natural ordering" від звичайних алгоритмів сортування, які застосовуються, наприклад, функцією [sort()](function.sort.html) можна побачити у прикладі нижче.

> **Зауваження**
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

> **Зауваження**
> 
> Скидає внутрішній покажчик масиву перший елемент.

### Список параметрів

`array`

Вхідний масив

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Приклад #1 Простий приклад використання **нацорт()****

```php
<?php
$array1 = $array2 = array("img12.png", "img10.png", "img2.png", "img1.png");

asort($array1);
echo "Обычная сортировка\n";
print_r($array1);

natsort($array2);
echo "\nСортировка natural order\n";
print_r($array2);
?>
```

Результат виконання цього прикладу:

```
Обычная сортировка
Array
(
    [3] => img1.png
    [1] => img10.png
    [0] => img12.png
    [2] => img2.png
)

Сортировка natural order
Array
(
    [3] => img1.png
    [2] => img2.png
    [1] => img10.png
    [0] => img12.png
)
```

Детальніше дивіться статтю Martin Pool [» Natural Order String Comparison](https://github.com/sourcefrog/natsort)

**Приклад #2 Приклади використання різних трюків з **нацорт()****

```php
<?php
echo "Отрицательные числа\n";
$negative = array('-5','3','-2','0','-1000','9','1');
print_r($negative);
natsort($negative);
print_r($negative);

echo "Отбивка нулями\n";
$zeros = array('09', '8', '10', '009', '011', '0');
print_r($zeros);
natsort($zeros);
print_r($zeros);
?>
```

Результат виконання цього прикладу:

```
Отрицательные числа
Array
(
    [0] => -5
    [1] => 3
    [2] => -2
    [3] => 0
    [4] => -1000
    [5] => 9
    [6] => 1
)
Array
(
    [2] => -2
    [0] => -5
    [4] => -1000
    [3] => 0
    [6] => 1
    [1] => 3
    [5] => 9
)

Отбивка нулями
Array
(
    [0] => 09
    [1] => 8
    [2] => 10
    [3] => 009
    [4] => 011
    [5] => 0
)
Array
(
    [5] => 0
    [1] => 8
    [3] => 009
    [0] => 09
    [2] => 10
    [4] => 011
)
```

### Дивіться також

-   [natcasesort()](function.natcasesort.html) - Сортує масив, використовуючи алгоритм "natural order" без урахування регістру символів
-   [Порівняння функцій сортування масивів](array.sorting.html)
-   [strnatcmp()](function.strnatcmp.html) - Порівняння рядків із використанням алгоритму "natural order"
-   [strnatcasecmp()](function.strnatcasecmp.html) - Порівняння рядків без урахування регістру з використанням алгоритму "natural order"
