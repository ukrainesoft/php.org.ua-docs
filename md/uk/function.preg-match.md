---
navigation:
  - function.preg-match-all.md: « preg\_match\_all
  - function.preg-quote.md: preg\_quote »
  - index.md: PHP Manual
  - ref.pcre.md: Функції PCRE
title: preg\_match
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# preg\_match

(PHP 4, PHP 5, PHP 7, PHP 8)

preg\_match — Виконує перевірку на відповідність регулярному виразу

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

Якщо вказано додатковий параметр `matches`, він буде заповнений результатами пошуку. Елемент $matches\[ \] міститиме частину рядка, що відповідає входу всього шаблону, $matches\[ \] - частина рядка, що відповідає першій підмасці тощо.

`flags`

`flags` може бути комбінацією наступних прапорів:

**`PREG_OFFSET_CAPTURE`**

У випадку, якщо цей прапор вказано, для кожного знайденого підрядка буде вказано її позицію (в байтах) у вихідному рядку. Необхідно пам'ятати, що цей прапор змінює формат масиву, що повертається. `matches` масив, кожен елемент якого містить масив, що містить в індексі з номером знайдений підрядок, а зміщення цього підрядка у параметрі `subject`\- в индексе

```php
<?php
preg_match('/(foo)(bar)(baz)/', 'foobarbaz', $matches, PREG_OFFSET_CAPTURE);
print_r($matches);
?>
```

Результат виконання наведеного прикладу:

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

Якщо цей прапор передано, несупадні підмаски будуть представлені значеннями **`null`**; інакше вони відображаються як порожніх рядків (string).

```php
<?php
preg_match('/(a)(b)*(c)/', 'ac', $matches);
var_dump($matches);
preg_match('/(a)(b)*(c)/', 'ac', $matches, PREG_UNMATCHED_AS_NULL);
var_dump($matches);
?>
```

Результат виконання наведеного прикладу:

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

> **Зауваження** :
> 
> Использование параметра`offset` не еквівалентно заміні зіставного рядка виразом `substr($subject, $offset)` при виклику функції **preg\_match()**, оскільки шаблон `pattern` може містити такі умови як *^* \*$*или*(?<=x)\*Сравните:
> 
> ```php
> <?php
> $subject = "abcdef";
> $pattern = '/^def/';
> preg_match($pattern, $subject, $matches, PREG_OFFSET_CAPTURE, 3);
> print_r($matches);
> ?>
> ```
> 
> Результат виконання наведеного прикладу:
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
> $subject = "abcdef";
> $pattern = '/^def/';
> preg_match($pattern, substr($subject,3), $matches, PREG_OFFSET_CAPTURE);
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
> Як альтернатива **substr()()**, используйте утверждение`\G` замість якоря `^` або модифікатор `A`Оба они работают с параметром`offset`

### Значення, що повертаються

**preg\_match()** повертає 1, якщо параметр `pattern`соответствует переданному параметру`subject`, 0 якщо ні \*\*`false`\*\*в случае возникновения ошибки.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Помилки

Якщо переданий шаблон регулярного виразу не компілюється в допустимий регулярний вираз, видається помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Тепер константа **`PREG_UNMATCHED_AS_NULL`** підтримується для параметра `$flags` |

### Приклади

**Приклад #1 Пошук підрядки "php" у тексті**

```php
<?php
// Символ "i" после закрывающего ограничителя шаблона означает
// регистронезависимый поиск.
if (preg_match("/php/i", "PHP is the web scripting language of choice.")) {
    echo "Вхождение найдено.";
} else {
    echo "Вхождение не найдено.";
}
?>
```

**Приклад #2 Пошук слова "web" у тексті**

```php
<?php
/* Специальная последовательность \b в шаблоне означает границу слова,
   следовательно, только изолированное вхождение слова 'web' будет
   соответствовать маске, в отличие от "webbing" или "cobweb" */
if (preg_match("/\bweb\b/i", "PHP is the web scripting language of choice.")) {
    echo "Вхождение найдено.";
} else {
    echo "Вхождение не найдено.";
}

if (preg_match("/\bweb\b/i", "PHP is the website scripting language of choice.")) {
    echo "Вхождение найдено.";
} else {
    echo "Вхождение не найдено.";
}
?>
```

**Приклад #3 Вилучення домену з URL**

```php
<?php
// Извлекаем имя хоста из URL
preg_match('@^(?:http://)?([^/]+)@i',
    "http://www.php.net/index.md", $matches);
$host = $matches[1];

// извлекаем две последние части имени хоста
preg_match('/[^.]+\.[^.]+$/', $host, $matches);
echo "доменное имя: {$matches[0]}\n";
?>
```

Результат виконання наведеного прикладу:

```
доменное имя: php.net
```

**Приклад #4 Використання іменованих підмасок**

```php
<?php

$str = 'foobar: 2008';

preg_match('/(?P<name>\w+): (?P<digit>\d+)/', $str, $matches);

/* Альтернативный вариант */
// preg_match('/(?<name>\w+): (?<digit>\d+)/', $str, $matches);

print_r($matches);

?>
```

Результат виконання наведеного прикладу:

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

Не используйте функцию**preg\_match()**, якщо необхідно перевірити наявність підрядка у заданому рядку. Використовуйте для цього [strpos()](function.strpos.md) оскільки вона виконає це завдання набагато швидше.

### Дивіться також

-   " [Регулярні вирази PCRE](pcre.pattern.md) "
-   [preg\_quote()](function.preg-quote.md) \- Екранує символи у регулярних виразах
-   [preg\_match\_all()](function.preg-match-all.md) \- Виконує глобальний пошук шаблону у рядку
-   [preg\_replace()](function.preg-replace.md) \- Виконує пошук та заміну за регулярним виразом
-   [preg\_split()](function.preg-split.md) \- Розбиває рядок за регулярним виразом
-   [preg\_last\_error()](function.preg-last-error.md) \- Повертає код помилки виконання останнього регулярного вираження PCRE
-   [preg\_last\_error\_msg()](function.preg-last-error-msg.md) \- Повертає повідомлення про помилку останньої запущеної функції PCRE
