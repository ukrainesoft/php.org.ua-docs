Повертає довжину рядка

-   [« stristr](function.stristr.md)
    
-   [strnatcasecmp »](function.strnatcasecmp.md)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з рядками](ref.strings.md)
    
-   Повертає довжину рядка
    

# strlen

(PHP 4, PHP 5, PHP 7, PHP 8)

strlen — Повертає довжину рядка

### Опис

```methodsynopsis
strlen(string $string): int
```

Повертає довжину рядка `string`

### Список параметрів

`string`

Рядок (string), на яку вимірюється довжина.

### Значення, що повертаються

Довжина рядка `string` у разі успішного виконання, та `0`, якщо `string` порожня.

### Приклади

**Приклад #1 Приклад використання **strlen()****

```php
<?php
$str = 'abcdef';
echo strlen($str); // 6

$str = ' ab cd ';
echo strlen($str); // 7
?>
```

### Примітки

> **Зауваження**
> 
> Функція **strlen()** поверне кількість байт, а не кількість символів у рядку.

> **Зауваження**
> 
> Функція **strlen()** повертає **`null`** при використанні на масивах, а також виводить помилку рівня **`E_WARNING`**

### Дивіться також

-   [count()](function.count.md) - Підраховує кількість елементів масиву або Countable об'єкті
-   [graphemestrlen()](function.grapheme-strlen.html) - отримує довжину рядка в одиницях графеми
-   [iconvstrlen()](function.iconv-strlen.html) - Повертає кількість символів у рядку
-   [мбstrlen()](function.mb-strlen.html) - Отримує довжину рядка