Конструктор класу RegexIterator

-   [« RegexIterator::accept](regexiterator.accept.html)
    
-   [RegexIterator::getFlags »](regexiterator.getflags.html)
    
-   [PHP Manual](index.html)
    
-   [RegexIterator](class.regexiterator.html)
    
-   Конструктор класу RegexIterator
    

# RegexIterator::construct

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RegexIterator::construct - Конструктор класу RegexIterator

### Опис

public **RegexIterator::construct**  
[Iterator](class.iterator.html) `$iterator`  
string `$pattern`  
int `$mode` = RegexIterator::MATCH,  
int `$flags`  
int `$pregFlags`  

Створює новий об'єкт класу [RegexIterator](class.regexiterator.html), який фільтрує елементи ітератора [Iterator](class.iterator.html) ґрунтуючись на регулярному вираженні.

### Список параметрів

`iterator`

Ітератор, до якого потрібно застосувати фільтр.

`pattern`

Регулярний вираз, з урахуванням якого проводиться відбір елементів.

`mode`

Режим роботи. Список можливих режимів можна переглянути в описі методу [RegexIterator::setMode()](regexiterator.setmode.html)

`flags`

Спеціальні прапори. Список можливих прапорів наведено в описі методу [RegexIterator::setFlags()](regexiterator.setflags.html)

`pregFlags`

Прапори регулярного вираження. Список можливих прапорів залежить від режиму роботи:

**[RegexIterator](class.regexiterator.html) pregflags**

| режим работы | доступные флаги |
| --- | --- |
| RegexIterator::ALLMATCHES | Дивіться [preg\_match\_all()](function.preg-match-all.html) |
| RegexIterator::GETMATCH | Дивіться [preg\_match()](function.preg-match.html) |
| RegexIterator::MATCH | Дивіться [preg\_match()](function.preg-match.html) |
| RegexIterator::REPLACE | ні |
| RegexIterator::SPLIT | Дивіться [preg\_split()](function.preg-split.html) |

### Помилки

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.html), якщо `pattern` заданий некоректно.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::construct()****

Створює новий об'єкт RegexIterator, який відбирає рядки, що починаються зі слова 'test'.

```php
<?php
$arrayIterator = new ArrayIterator(array('test 1', 'another test', 'test 123'));
$regexIterator = new RegexIterator($arrayIterator, '/^test/');

foreach ($regexIterator as $value) {
    echo $value . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
test 1
test 123
```

### Дивіться також

-   [preg\_match()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу
-   [preg\_match\_all()](function.preg-match-all.html) - Виконує глобальний пошук шаблону у рядку
-   [preg\_replace()](function.preg-replace.html) - Виконує пошук та заміну за регулярним виразом
-   [preg\_split()](function.preg-split.html) - Розбиває рядок за регулярним виразом