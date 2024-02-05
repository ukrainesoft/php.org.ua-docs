---
navigation:
  - ref.pcre.md: « Функції PCRE
  - function.preg-grep.md: preg\_grep »
  - index.md: PHP Manual
  - ref.pcre.md: Функції PCRE
title: preg\_filter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# preg\_filter

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

preg\_filter — Здійснює пошук та заміну за регулярним виразом

### Опис

```methodsynopsis
preg_filter(    string|array $pattern,    string|array $replacement,    string|array $subject,    int $limit = -1,    int &$count = null): string|array|null
```

Функция**preg\_filter()** ідентична функції [preg\_replace()](function.preg-replace.md) крім того, що повертає ті значення (можливо, перетворені), у яких знайдено збіг. Докладніше про роботу функції читайте у документації до [preg\_replace()](function.preg-replace.md)

### Список параметрів

Параметри описані в документації для функції [preg\_replace()](function.preg-replace.md)

### Значення, що повертаються

Повертає масив (array), якщо аргумент `subject` має тип array або рядок (string) в іншому випадку.

Якщо збігів не знайдено або виникла помилка, повертається порожній масив (array), коли `subject` має тип array або **`null`** в іншому випадку.

### Помилки

Якщо переданий шаблон регулярного виразу не компілюється в допустимий регулярний вираз, видається помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад для сравнения функций**preg\_filter()**и[preg\_replace()](function.preg-replace.md)**

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

Результат виконання наведеного прикладу:

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
-   [preg\_quote()](function.preg-quote.md) \- Екранує символи у регулярних виразах
-   [preg\_replace()](function.preg-replace.md) \- Виконує пошук та заміну за регулярним виразом
-   [preg\_replace\_callback()](function.preg-replace-callback.md) \- Виконує пошук за регулярним виразом та заміною з використанням callback-функції
-   [preg\_grep()](function.preg-grep.md) \- Повертає масив входжень, які відповідають шаблону
-   [preg\_last\_error()](function.preg-last-error.md) \- Повертає код помилки виконання останнього регулярного вираження PCRE
