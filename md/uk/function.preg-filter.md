---
navigation:
  - ref.pcre.md: « Функции PCRE
  - function.preg-grep.md: preggrep »
  - index.md: PHP Manual
  - ref.pcre.md: Функции PCRE
title: pregfilter
---
# pregfilter

(PHP 5> = 5.3.0, PHP 7, PHP 8)

pregfilter — Здійснює пошук та заміну за регулярним виразом

### Опис

```methodsynopsis
preg_filter(    string|array $pattern,    string|array $replacement,    string|array $subject,    int $limit = -1,    int &$count = null): string|array|null
```

Функція **pregfilter()** ідентична функції [pregreplace()](function.preg-replace.md) крім того, що повертає ті значення (можливо, перетворені), у яких знайдено збіг. Докладніше про роботу функції читайте у документації до [pregreplace()](function.preg-replace.md)

### Список параметрів

Параметри описані в документації для функції [pregreplace()](function.preg-replace.md)

### Значення, що повертаються

Повертає масив (array), якщо аргумент `subject` має тип array або рядок (string) в іншому випадку.

Якщо збігів не знайдено або виникла помилка, повертається порожній масив (array), коли `subject` має тип array або **`null`** в іншому випадку.

### Помилки

Якщо переданий шаблон регулярного виразу не компілюється в допустимий регулярний вираз, видається помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад для порівняння функцій **pregfilter()** і [pregreplace()](function.preg-replace.md)**

```php
<?php
$subject = array('1', 'а', '2', 'б', '3', 'А', 'Б', '4');
$pattern = array('/\d/', '/[а-я]/', '/[1а]/');
$replace = array('А:$0', 'Б:$0', 'В:$0');

echo "preg_filter возвращает\n";
print_r(preg_filter($pattern, $replace, $subject));

echo "preg_replace возвращает\n";
print_r(preg_replace($pattern, $replace, $subject));
?>
```

Результат виконання цього прикладу:

```
preg_filter возвращает
Array
(
    [0] => А:В:1
    [1] => Б:В:а
    [2] => А:2
    [3] => Б:б
    [4] => А:3
    [7] => А:4
)
preg_replace возвращает
Array
(
    [0] => А:В:1
    [1] => Б:В:а
    [2] => А:2
    [3] => Б:б
    [4] => А:3
    [5] => А
    [6] => Б
    [7] => А:4
)
```

### Дивіться також

-   [Шаблони PCRE](pcre.pattern.md)
-   [pregquote()](function.preg-quote.md) - Екранує символи у регулярних виразах
-   [pregreplace()](function.preg-replace.md) - Виконує пошук та заміну за регулярним виразом
-   [pregreplacecallback()](function.preg-replace-callback.md) - Виконує пошук за регулярним виразом та заміною з використанням callback-функції
-   [preggrep()](function.preg-grep.md) - Повертає масив входжень, які відповідають шаблону
-   [preglasterror()](function.preg-last-error.md) - Повертає код помилки виконання останнього регулярного вираження PCRE
