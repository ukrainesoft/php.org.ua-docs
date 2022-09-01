---
navigation:
  - class.recursiveregexiterator.html: « RecursiveRegexIterator
  - recursiveregexiterator.getchildren.html: 'RecursiveRegexIterator::getChildren »'
  - index.html: PHP Manual
  - class.recursiveregexiterator.html: RecursiveRegexIterator
title: 'RecursiveRegexIterator::construct'
---
# RecursiveRegexIterator::construct

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RecursiveRegexIterator::construct - Конструктор класу RecursiveRegexIterator

### Опис

public **RecursiveRegexIterator::construct**  
[RecursiveIterator](class.recursiveiterator.html) `$iterator`  
string `$pattern`  
int `$mode` = RecursiveRegexIterator::MATCH,  
int `$flags`  
int `$pregFlags`

Створює новий об'єкт-ітератор регулярного вираження.

### Список параметрів

`iterator`

Рекурсивний ітератор якого потрібно застосувати фільтр з урахуванням регулярного висловлювання.

`pattern`

Регулярний вираз.

`mode`

Режим роботи, список доступних режимів наведено в описі методу [RegexIterator::setMode()](regexiterator.setmode.html)

`flags`

Спеціальні прапори. Список доступних прапорів наведено в описі методу [RegexIterator::setFlags()](regexiterator.setflags.html)

`pregFlags`

Прапори регулярного вираження. Список прапорів залежить від режиму роботи:

**[RegexIterator](class.regexiterator.html) pregflags**

| режим работы | доступные флаги |
| --- | --- |
| RecursiveRegexIterator::ALLMATCHES | Дивіться [pregmatchall()](function.preg-match-all.html) |
| RecursiveRegexIterator::GETMATCH | Дивіться [pregmatch()](function.preg-match.html) |
| RecursiveRegexIterator::MATCH | Дивіться [pregmatch()](function.preg-match.html) |
| RecursiveRegexIterator::REPLACE | ні |
| RecursiveRegexIterator::SPLIT | Дивіться [pregsplit()](function.preg-split.html) |

### Приклади

**Приклад #1 Приклад використання **RecursiveRegexIterator::construct()****

Створює новий об'єкт-ітератор RegexIterator, який вибирає всі рядки, що починаються зі слова 'test'.

```php
<?php
$rArrayIterator = new RecursiveArrayIterator(array('test1', array('tet3', 'test4', 'test5')));
$rRegexIterator = new RecursiveRegexIterator($rArrayIterator, '/^test/',
    RecursiveRegexIterator::ALL_MATCHES);

foreach ($rRegexIterator as $key1 => $value1) {

    if ($rRegexIterator->hasChildren()) {

        // выведем все дочерние элементы
        echo "Дочерние элементы: ";
        foreach ($rRegexIterator->getChildren() as $key => $value) {
            echo $value . " ";
        }
        echo "\n";
    } else {
        echo "Нет дочерних элементов\n";
    }

}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Нет дочерних элементов
Дочерние элементы: test4 test5
```

### Дивіться також

-   [pregmatch()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу
-   [pregmatchall()](function.preg-match-all.html) - Виконує глобальний пошук шаблону у рядку
-   [pregreplace()](function.preg-replace.html) - Виконує пошук та заміну за регулярним виразом
-   [pregsplit()](function.preg-split.html) - Розбиває рядок за регулярним виразом
