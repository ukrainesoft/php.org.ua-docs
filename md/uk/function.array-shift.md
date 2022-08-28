Витягує перший елемент масиву

-   [« array\_search](function.array-search.html)
    
-   [array\_slice »](function.array-slice.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Витягує перший елемент масиву
    

# arrayshift

(PHP 4, PHP 5, PHP 7, PHP 8)

arrayshift — Витягує перший елемент масиву

### Опис

```methodsynopsis
array_shift(array &$array): mixed
```

**arrayshift()** здобуває перше значення масиву `array` і повертає його, скорочуючи розмір `array` на один елемент. Усі числові ключі будуть змінені таким чином, що нумерація масиву розпочнеться з нуля, тоді як рядкові ключі залишаться незмінними.

> **Зауваження**: Ця функція під час виклику [сбрасывает](function.reset.html) вказівник масиву, переданого параметром.

### Список параметрів

`array`

Вхідний масив

### Значення, що повертаються

Повертає значення або **`null`**, якщо `array` порожній чи не є масивом.

### Приклади

**Приклад #1 Приклад використання **arrayshift()****

```php
<?php
$stack = array("orange", "banana", "apple", "raspberry");
$fruit = array_shift($stack);
print_r($stack);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => banana
    [1] => apple
    [2] => raspberry
)
```

та значення `orange` буде присвоєно змінною $fruit.

### Дивіться також

-   [array\_unshift()](function.array-unshift.html) - Додає один або кілька елементів на початок масиву
-   [array\_push()](function.array-push.html) - Додає один або кілька елементів у кінець масиву
-   [array\_pop()](function.array-pop.html) - Витягує останній елемент масиву