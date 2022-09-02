---
navigation:
  - function.preg-match-all.md: « pregmatchall
  - function.preg-quote.md: pregquote »
  - index.md: PHP Manual
  - ref.pcre.md: Функции PCRE
title: pregmatch
---
# pregmatch

(PHP 4, PHP 5, PHP 7, PHP 8)

pregmatch — Виконує перевірку на відповідність регулярному виразу

### Опис

```methodsynopsis
preg_match(    string $pattern,    string $subject,    array &$matches = null,    int $flags = 0,    int $offset = 0): int|false
```

Шукає у заданому тексті `subject` збіги з шаблоном `pattern`

### Список параметрів

`pattern`

Шуканий шаблон у вигляді рядка.

`subject`

Вхідний рядок.

`matches`

Якщо вказано додатковий параметр `matches`, він буде заповнений результатами пошуку. Елемент $matches міститиме частину рядка, що відповідає входу всього шаблону, $matches - частина рядка, що відповідає першій підмасці тощо.

`flags`

`flags` може бути комбінацією наступних прапорів:

**`PREG_OFFSET_CAPTURE`**

У випадку, якщо цей прапор вказаний, для кожного знайденого підрядка буде вказано її позицію (в байтах) у вихідному рядку. Необхідно пам'ятати, що цей прапор змінює формат масиву, що повертається. `matches` масив, кожен елемент якого містить масив, що містить в індексі з номером `0` знайдений підрядок, а зміщення цього підрядка у параметрі `subject` - в індексі `1`

```php
<?php
preg_match('/(foo)(bar)(baz)/', 'foobarbaz', $matches, PREG_OFFSET_CAPTURE);
print_r($matches);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => Array
        (
            [0] => foobarbaz
            [1] => 0
        )

    [1] => Array
        (
            [0] => foo
            [1] => 0
        )

    [2] => Array
        (
            [0] => bar
            [1] => 3
        )

    [3] => Array
        (
            [0] => baz
            [1] => 6
        )

)
```

**`PREG_UNMATCHED_AS_NULL`**

Якщо цей прапор передано, незбігаються підмаски будуть представлені значеннями **`null`**; інакше вони відображаються як порожніх рядків (string).

```php
<?php
preg_match('/(a)(b)*(c)/', 'ac', $matches);
var_dump($matches);
preg_match('/(a)(b)*(c)/', 'ac', $matches, PREG_UNMATCHED_AS_NULL);
var_dump($matches);
?>
```

Результат виконання цього прикладу:

```
array(4) {
  [0]=>
  string(2) "ac"
  [1]=>
  string(1) "a"
  [2]=>
  string(0) ""
  [3]=>
  string(1) "c"
}
array(4) {
  [0]=>
  string(2) "ac"
  [1]=>
  string(1) "a"
  [2]=>
  NULL
  [3]=>
  string(1) "c"
}
```

`offset`

Зазвичай пошук здійснюється зліва направо, з початку рядка. Можна використовувати додатковий параметр `offset` для вказівки альтернативної початкової позиції пошуку (в байтах).

> **Зауваження**
> 
> Використання параметра `offset` не еквівалентно заміні зіставного рядка виразом `substr($subject, $offset)` при виклику функції **pregmatch()**, оскільки шаблон `pattern` може містити такі умови як або *(?<=x)*. Порівняйте:
> 
> ```php
> <?php
> $subject = "abcdef";
> $pattern = '/^def/';
> preg_match($pattern, $subject, $matches, PREG_OFFSET_CAPTURE, 3);
> print_r($matches);
> ?>
> ```
> 
> Результат виконання цього прикладу:
> 
> ```
> Array
> (
> )
> ```
> 
> У той час як цей приклад
> 
> ```php
> <?php
> $subject = "abcdef";
> $pattern = '/^def/';
> preg_match($pattern, substr($subject,3), $matches, PREG_OFFSET_CAPTURE);
> print_r($matches);
> ?>
> ```
> 
> виведе наступне:
> 
> ```
> Array
> (
>     [0] => Array
>         (
>             [0] => def
>             [1] => 0
>         )
> 
> )
> ```
> 
> Як альтернатива **substr()()**, використовуйте затвердження `\G` замість якоря `^` або модифікатор `A`. Обидва вони працюють із параметром `offset`

### Значення, що повертаються

**pregmatch()** повертає 1, якщо параметр `pattern` відповідає переданому параметру `subject`, 0 якщо ні **`false`** у разі виникнення помилки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.md). Використовуйте [оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Помилки

Якщо переданий шаблон регулярного виразу не компілюється в допустимий регулярний вираз, видається помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер константа **`PREG_UNMATCHED_AS_NULL`** підтримується для параметра `$flags` |

### Приклади

**Приклад #1 Пошук підрядки "php" у тексті**

```php
<?php
// Символ "i" после закрывающего ограничителя шаблона означает
// регистронезависимый поиск.
if (preg_match("/php/i", "PHP is the web scripting language of choice.")) {
    echo "Вхождение найдено.";
} else {
    echo "Вхождение не найдено.";
}
?>
```

**Приклад #2 Пошук слова "web" у тексті**

```php
<?php
/* Специальная последовательность \b в шаблоне означает границу слова,
   следовательно, только изолированное вхождение слова 'web' будет
   соответствовать маске, в отличие от "webbing" или "cobweb" */
if (preg_match("/\bweb\b/i", "PHP is the web scripting language of choice.")) {
    echo "Вхождение найдено.";
} else {
    echo "Вхождение не найдено.";
}

if (preg_match("/\bweb\b/i", "PHP is the website scripting language of choice.")) {
    echo "Вхождение найдено.";
} else {
    echo "Вхождение не найдено.";
}
?>
```

**Приклад #3 Вилучення домену з URL**

```php
<?php
// Извлекаем имя хоста из URL
preg_match('@^(?:http://)?([^/]+)@i',
    "http://www.php.net/index.html", $matches);
$host = $matches[1];

// извлекаем две последние части имени хоста
preg_match('/[^.]+\.[^.]+$/', $host, $matches);
echo "доменное имя: {$matches[0]}\n";
?>
```

Результат виконання цього прикладу:

```
доменное имя: php.net
```

**Приклад #4 Використання іменованих підмасок**

```php
<?php

$str = 'foobar: 2008';

preg_match('/(?P<name>\w+): (?P<digit>\d+)/', $str, $matches);

/* Альтернативный вариант */
// preg_match('/(?<name>\w+): (?<digit>\d+)/', $str, $matches);

print_r($matches);

?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => foobar: 2008
    [name] => foobar
    [1] => foobar
    [digit] => 2008
    [2] => 2008
)
```

### Примітки

**Підказка**

Не використовуйте функцію **pregmatch()**, якщо необхідно перевірити наявність підрядка у заданому рядку. Використовуйте для цього [strpos()](function.strpos.md) оскільки вона виконає це завдання набагато швидше.

### Дивіться також

-   "[Регулярні вирази PCRE](pcre.pattern.md)"
-   [pregquote()](function.preg-quote.md) - Екранує символи у регулярних виразах
-   [pregmatchall()](function.preg-match-all.md) - Виконує глобальний пошук шаблону у рядку
-   [pregreplace()](function.preg-replace.md) - Виконує пошук та заміну за регулярним виразом
-   [pregsplit()](function.preg-split.md) - Розбиває рядок за регулярним виразом
-   [preglasterror()](function.preg-last-error.md) - Повертає код помилки виконання останнього регулярного вираження PCRE
-   [preglasterrormsg()](function.preg-last-error-msg.md) - Повертає повідомлення про помилку останньої запущеної функції PCRE
