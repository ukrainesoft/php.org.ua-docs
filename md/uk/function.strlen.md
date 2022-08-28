Повертає довжину рядка

-   [« stristr](function.stristr.html)
    
-   [strnatcasecmp »](function.strnatcasecmp.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
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

-   [count()](function.count.html) - Підраховує кількість елементів масиву або Countable об'єкті
-   [grapheme\_strlen()](function.grapheme-strlen.html) - отримує довжину рядка в одиницях графеми
-   [iconv\_strlen()](function.iconv-strlen.html) - Повертає кількість символів у рядку
-   [mb\_strlen()](function.mb-strlen.html) - Отримує довжину рядка