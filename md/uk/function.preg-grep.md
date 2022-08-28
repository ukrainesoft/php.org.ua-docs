Повертає масив входжень, які відповідають шаблону

-   [« preg\_filter](function.preg-filter.html)
    
-   [preg\_last\_error\_msg »](function.preg-last-error-msg.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCRE](ref.pcre.html)
    
-   Повертає масив входжень, які відповідають шаблону
    

# preggrep

(PHP 4, PHP 5, PHP 7, PHP 8)

preggrep — Повертає масив входжень, які відповідають шаблону

### Опис

```methodsynopsis
preg_grep(string $pattern, array $array, int $flags = 0): array|false
```

Повертає масив, що складається з елементів вхідного масиву `array`, які відповідають заданому шаблону `pattern`

### Список параметрів

`pattern`

Шуканий шаблон у вигляді рядка.

`array`

Вхідний масив.

`flags`

У разі, якщо встановлено **`PREG_GREP_INVERT`**, функція **preggrep()** повертає ті елементи масиву, які *Не відповідає* заданому шаблону `pattern`

### Значення, що повертаються

Повертає масив, індексований ключами з масиву `array` або **`false`** у разі виникнення помилки.

### Помилки

Якщо переданий шаблон регулярного виразу не компілюється в допустимий регулярний вираз, видається помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад використання **preggrep()****

```php
<?php
// Возвращает все элементы массива,
// содержащие числа с плавающей точкой
$fl_array = preg_grep("/^(\d+)?\.\d+$/", $array);
?>
```

### Дивіться також

-   [Регулярные выражения PCRE](pcre.pattern.html)
-   [preg\_quote()](function.preg-quote.html) - Екранує символи у регулярних виразах
-   [preg\_match\_all()](function.preg-match-all.html) - Виконує глобальний пошук шаблону у рядку
-   [preg\_filter()](function.preg-filter.html) - Здійснює пошук та заміну за регулярним виразом
-   [preg\_last\_error()](function.preg-last-error.html) - Повертає код помилки виконання останнього регулярного вираження PCRE