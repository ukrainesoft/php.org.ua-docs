---
navigation:
  - function.preg-filter.md: « pregfilter
  - function.preg-last-error-msg.md: preglasterrormsg »
  - index.md: PHP Manual
  - ref.pcre.md: Функции PCRE
title: preggrep
---
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
// Возвращает все элементы Масива,
// содержащие числа с плавающей точкой
$fl_array = preg_grep("/^(\d+)?\.\d+$/", $array);
?>
```

### Дивіться також

-   [Регулярні вирази PCRE](pcre.pattern.md)
-   [pregquote()](function.preg-quote.md) - Екранує символи у регулярних виразах
-   [pregmatchall()](function.preg-match-all.md) - Виконує глобальний пошук шаблону у рядку
-   [pregfilter()](function.preg-filter.md) - Здійснює пошук та заміну за регулярним виразом
-   [preglasterror()](function.preg-last-error.md) - Повертає код помилки виконання останнього регулярного вираження PCRE
