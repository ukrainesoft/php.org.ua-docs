---
navigation:
  - function.natcasesort.md: « natcasesort
  - function.next.md: next »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: natsort
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# natsort

(PHP 4, PHP 5, PHP 7, PHP 8)

natsort - Сортує масив, використовуючи алгоритм "natural order"

### Опис

```methodsynopsis
natsort(array &$array): true
```

Функція реалізує алгоритм сортування, у якому порядок буквенно-цифровых рядків буде звичним людини. Такий алгоритм називається "natural ordering". Відмінність алгоритму "natural ordering" від звичайних алгоритмів сортування, які застосовуються, наприклад, функцією [sort()](function.sort.md) можна побачити у прикладі нижче.

> **Зауваження** :
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

> **Зауваження** :
> 
> Скидає внутрішній покажчик масиву перший елемент.

### Список параметрів

`array`

Вхідний масив

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Приклади

**Приклад #1 Простий приклад використання **natsort()****

```php
<?php
$array1 = $array2 = array("img12.png", "img10.png", "img2.png", "img1.png");

asort($array1);
echo "Обычная сортировка\n";
print_r($array1);

natsort($array2);
echo "\nСортировка natural order\n";
print_r($array2);
?>
```

Результат виконання наведеного прикладу:

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

Подробнее смотрите статью Martin Pool[» Natural Order String Comparison](https://github.com/sourcefrog/natsort)

**Приклад #2 Приклади використання різних трюків з **natsort()****

```php
<?php
echo "Отрицательные числа\n";
$negative = array('-5','3','-2','0','-1000','9','1');
print_r($negative);
natsort($negative);
print_r($negative);

echo "Отбивка нулями\n";
$zeros = array('09', '8', '10', '009', '011', '0');
print_r($zeros);
natsort($zeros);
print_r($zeros);
?>
```

Результат виконання наведеного прикладу:

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

-   [natcasesort()](function.natcasesort.md) \- Сортує масив алгоритмом природного сортування (natural order) без урахування регістру символів
-   [Порівняння функцій сортування масивів](array.sorting.md)
-   [strnatcmp()](function.strnatcmp.md) - Порівняння рядків із використанням алгоритму "natural order"
-   [strnatcasecmp()](function.strnatcasecmp.md) - Порівняння рядків без урахування регістру з використанням алгоритму "natural order"
