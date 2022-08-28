Здійснює пошук та заміну за регулярним виразом

-   [« Функции PCRE](ref.pcre.html)
    
-   [preg\_grep »](function.preg-grep.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCRE](ref.pcre.html)
    
-   Здійснює пошук та заміну за регулярним виразом
    

# pregfilter

(PHP 5> = 5.3.0, PHP 7, PHP 8)

pregfilter — Здійснює пошук та заміну за регулярним виразом

### Опис

```methodsynopsis
preg_filter(    string|array $pattern,    string|array $replacement,    string|array $subject,    int $limit = -1,    int &$count = null): string|array|null
```

Функція **pregfilter()** ідентична функції [preg\_replace()](function.preg-replace.html) крім того, що повертає ті значення (можливо, перетворені), у яких знайдено збіг. Докладніше про роботу функції читайте у документації до [preg\_replace()](function.preg-replace.html)

### Список параметрів

Параметри описані в документації для функції [preg\_replace()](function.preg-replace.html)

### Значення, що повертаються

Повертає масив (array), якщо аргумент `subject` має тип array або рядок (string) в іншому випадку.

Якщо збігів не знайдено або виникла помилка, повертається порожній масив (array), коли `subject` має тип array або **`null`** в іншому випадку.

### Помилки

Якщо переданий шаблон регулярного виразу не компілюється в допустимий регулярний вираз, видається помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад для порівняння функцій **pregfilter()** і [preg\_replace()](function.preg-replace.html)**

```php
<?php
$subject = array('1', 'а', '2', 'б', '3', 'А', 'Б', '4');
$pattern = array('/\d/', '/[а-я]/', '/[1а]/');
$replace = array('А:$0', 'Б:$0', 'В:$0');

echo "preg_filter возвращает\n";
print_r(preg_filter($pattern, $replace, $subject));

echo "preg_replace возвращает\n";
print_r(preg_replace($pattern, $replace, $subject));
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

-   [Шаблоны PCRE](pcre.pattern.html)
-   [preg\_quote()](function.preg-quote.html) - Екранує символи у регулярних виразах
-   [preg\_replace()](function.preg-replace.html) - Виконує пошук та заміну за регулярним виразом
-   [preg\_replace\_callback()](function.preg-replace-callback.html) - Виконує пошук за регулярним виразом та заміною з використанням callback-функції
-   [preg\_grep()](function.preg-grep.html) - Повертає масив входжень, які відповідають шаблону
-   [preg\_last\_error()](function.preg-last-error.html) - Повертає код помилки виконання останнього регулярного вираження PCRE