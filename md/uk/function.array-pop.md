Витягує останній елемент масиву

-   [« arraypad](function.array-pad.html)
    
-   [arrayproduct »](function.array-product.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з масивами](ref.array.html)
    
-   Витягує останній елемент масиву
    

# arraypop

(PHP 4, PHP 5, PHP 7, PHP 8)

arraypop — Витягує останній елемент масиву

### Опис

```methodsynopsis
array_pop(array &$array): mixed
```

**arraypop()** витягує та повертає значення останнього елемента масиву `array`зменшуючи розмір `array` на один елемент.

> **Зауваження**: Ця функція під час виклику [скидає](function.reset.html) вказівник масиву, переданого параметром.

### Список параметрів

`array`

Масив, з якого береться значення.

### Значення, що повертаються

Повертає значення останнього елемента масиву `array`. Якщо `array` нехай, буде повернутий **`null`**

### Приклади

**Приклад #1 Приклад використання **arraypop()****

```php
<?php
$stack = array("orange", "banana", "apple", "raspberry");
$fruit = array_pop($stack);
print_r($stack);
?>
```

Після цього $stack буде лише 3 елемента:

```
Array
(
    [0] => orange
    [1] => banana
    [2] => apple
)
```

і `raspberry` буде присвоєно змінною $fruit.

### Дивіться також

-   [arraypush()](function.array-push.html) - Додає один або кілька елементів у кінець масиву
-   [arrayshift()](function.array-shift.html) - Витягує перший елемент масиву
-   [arrayunshift()](function.array-unshift.html) - Додає один або кілька елементів на початок масиву