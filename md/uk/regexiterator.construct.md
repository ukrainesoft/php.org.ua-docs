---
navigation:
  - regexiterator.accept.md: '« RegexIterator::accept'
  - regexiterator.getflags.md: 'RegexIterator::getFlags »'
  - index.md: PHP Manual
  - class.regexiterator.md: RegexIterator
title: 'RegexIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RegexIterator::\_\_construct

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

RegexIterator::\_\_construct - Конструктор класу RegexIterator

### Опис

public **RegexIterator::\_\_construct**  
[Iterator](class.iterator.md) `$iterator`,  
string`$pattern`,  
int`$mode`\= RegexIterator::MATCH,  
int`$flags`  
int`$pregFlags`  
) .

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

Прапори регулярного виразу. Список можливих прапорів залежить від режиму роботи:

**[RegexIterator](class.regexiterator.md)preg\_flags**

| режим работы | доступные флаги |
| --- | --- |
| RegexIterator::ALL\_MATCHES | Смотрите[preg\_match\_all()](function.preg-match-all.md) |
| RegexIterator::GET\_MATCH | Смотрите[preg\_match()](function.preg-match.md) |
| RegexIterator::MATCH | Смотрите[preg\_match()](function.preg-match.md) |
| RegexIterator::REPLACE | ні |
| RegexIterator::SPLIT | Смотрите[preg\_split()](function.preg-split.md) |

### Помилки

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), якщо `pattern`задан некорректно.

### Приклади

**Приклад #1 Приклад використання** RegexIterator::\_\_construct()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
test 1
test 123
```

### Дивіться також

-   [preg\_match()](function.preg-match.md) \- Виконує перевірку на відповідність регулярному виразу
-   [preg\_match\_all()](function.preg-match-all.md) \- Виконує глобальний пошук шаблону у рядку
-   [preg\_replace()](function.preg-replace.md) \- Виконує пошук та заміну за регулярним виразом
-   [preg\_split()](function.preg-split.md) \- Розбиває рядок за регулярним виразом
