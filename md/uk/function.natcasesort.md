Сортує масив, використовуючи алгоритм "natural order" без урахування регістру символів

-   [« list](function.list.html)
    
-   [natsort »](function.natsort.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з масивами](ref.array.html)
    
-   Сортує масив, використовуючи алгоритм "natural order" без урахування регістру символів
    

# natcasesort

(PHP 4, PHP 5, PHP 7, PHP 8)

natcasesort — Сортує масив, використовуючи алгоритм "natural order" без урахування регістру символів

### Опис

```methodsynopsis
natcasesort(array &$array): bool
```

**natcasesort()** - це реєстронезалежний аналог [natsort()](function.natsort.html)

Ця функція реалізує алгоритм сортування, у якому порядок літерно-цифрових рядків буде звичним для людини. Такий алгоритм називається "natural ordering".

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

**Приклад #1 Приклад використання **natcasesort()****

```php
<?php
$array1 = $array2 = array('IMG0.png', 'img12.png', 'img10.png', 'img2.png', 'img1.png', 'IMG3.png');

sort($array1);
echo "Обычная сортировка\n";
print_r($array1);

natcasesort($array2);
echo "\nNatural order сортировка (без учёта регистра)\n";
print_r($array2);
?>
```

Результат виконання цього прикладу:

```
Обычная сортировка
Array
(
    [0] => IMG0.png
    [1] => IMG3.png
    [2] => img1.png
    [3] => img10.png
    [4] => img12.png
    [5] => img2.png
)

Natural order сортировка (без учёта регистра)
Array
(
    [0] => IMG0.png
    [4] => img1.png
    [3] => img2.png
    [5] => IMG3.png
    [2] => img10.png
    [1] => img12.png
)
```

Детальніше дивіться статтю Martin Pool [» Natural Order String Comparison](https://github.com/sourcefrog/natsort)

### Дивіться також

-   [natsort()](function.natsort.html) - Сортує масив, використовуючи алгоритм "natural order"
-   [Порівняння функцій сортування масивів](array.sorting.html)
-   [strnatcmp()](function.strnatcmp.html) - Порівняння рядків із використанням алгоритму "natural order"
-   [strnatcasecmp()](function.strnatcasecmp.html) - Порівняння рядків без урахування регістру з використанням алгоритму "natural order"