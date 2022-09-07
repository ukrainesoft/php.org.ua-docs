---
navigation:
  - regexiterator.accept.md: '« RegexIterator::accept'
  - regexiterator.getflags.md: 'RegexIterator::getFlags »'
  - index.md: PHP Manual
  - class.regexiterator.md: RegexIterator
title: 'RegexIterator::construct'
---
# RegexIterator::construct

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RegexIterator::construct - Конструктор класу RegexIterator

### Опис

public **RegexIterator::construct**  
[Iterator](class.iterator.md) `$iterator`  
string `$pattern`  
int `$mode` = RegexIterator::MATCH,  
int `$flags`  
int `$pregFlags`

Створює новий об'єкт класу [RegexIterator](class.regexiterator.md), який фільтрує елементи ітератора [Iterator](class.iterator.md) ґрунтуючись на регулярному вираженні.

### Список параметрів

`iterator`

Ітератор, до якого потрібно застосувати фільтр.

`pattern`

Регулярний вираз, з урахуванням якого проводиться відбір елементів.

`mode`

Режим роботи. Список можливих режимів можна переглянути в описі методу [RegexIterator::setMode()](regexiterator.setmode.md)

`flags`

Спеціальні прапори. Список можливих прапорів наведено в описі методу [RegexIterator::setFlags()](regexiterator.setflags.md)

`pregFlags`

Прапори регулярного вираження. Список можливих прапорів залежить від режиму роботи:

**[RegexIterator](class.regexiterator.md) pregflags**

| режим работы | доступные флаги |
| --- | --- |
| RegexIterator::ALLMATCHES | Дивіться [pregmatchall()](function.preg-match-all.md) |
| RegexIterator::GETMATCH | Дивіться [pregmatch()](function.preg-match.md) |
| RegexIterator::MATCH | Дивіться [pregmatch()](function.preg-match.md) |
| RegexIterator::REPLACE | ні |
| RegexIterator::SPLIT | Дивіться [pregsplit()](function.preg-split.md) |

### Помилки

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), якщо `pattern` заданий некоректно.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::construct()****

Створює новий об'єкт RegexIterator, який відбирає рядки, що починаються зі слова 'test'.

```php
<?php
$arrayIterator = new ArrayIterator(array('test 1', 'another test', 'test 123'));
$regexIterator = new RegexIterator($arrayIterator, '/^test/');

foreach ($regexIterator as $value) {
    echo $value . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
test 1
test 123
```

### Дивіться також

-   [pregmatch()](function.preg-match.md) - Виконує перевірку на відповідність регулярному виразу
-   [pregmatchall()](function.preg-match-all.md) - Виконує глобальний пошук шаблону у рядку
-   [pregreplace()](function.preg-replace.md) - Виконує пошук та заміну за регулярним виразом
-   [pregsplit()](function.preg-split.md) - Розбиває рядок за регулярним виразом
