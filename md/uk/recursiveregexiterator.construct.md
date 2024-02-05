---
navigation:
  - class.recursiveregexiterator.md: « RecursiveRegexIterator
  - recursiveregexiterator.getchildren.md: 'RecursiveRegexIterator::getChildren »'
  - index.md: PHP Manual
  - class.recursiveregexiterator.md: RecursiveRegexIterator
title: 'RecursiveRegexIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveRegexIterator::\_\_construct

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

RecursiveRegexIterator::\_\_construct - Конструктор класу RecursiveRegexIterator

### Опис

public**RecursiveRegexIterator::\_\_construct**  
[RecursiveIterator](class.recursiveiterator.md) `$iterator`,  
string`$pattern`,  
int`$mode`\= RecursiveRegexIterator::MATCH,  
int`$flags`  
int`$pregFlags`  
) .

Створює новий об'єкт-ітератор регулярного вираження.

### Список параметрів

`iterator`

Рекурсивний ітератор якого потрібно застосувати фільтр з урахуванням регулярного висловлювання.

`pattern`

Регулярний вираз.

`mode`

Режим роботи, список доступних режимів наведено в описі методу [RegexIterator::setMode()](regexiterator.setmode.md)

`flags`

Спеціальні прапори. Список доступних прапорів наведено в описі методу [RegexIterator::setFlags()](regexiterator.setflags.md)

`pregFlags`

Прапори регулярного виразу. Список прапорів залежить від режиму роботи:

**[RegexIterator](class.regexiterator.md)preg\_flags**

| режим работы | доступные флаги |
| --- | --- |
| RecursiveRegexIterator::ALL\_MATCHES | Смотрите[preg\_match\_all()](function.preg-match-all.md) |
| RecursiveRegexIterator::GET\_MATCH | Смотрите[preg\_match()](function.preg-match.md) |
| RecursiveRegexIterator::MATCH | Смотрите[preg\_match()](function.preg-match.md) |
| RecursiveRegexIterator::REPLACE | ні |
| RecursiveRegexIterator::SPLIT | Смотрите[preg\_split()](function.preg-split.md) |

### Приклади

**Пример #1 Пример использования**RecursiveRegexIterator::\_\_construct()\*\*\*\*

Створює новий об'єкт-ітератор RegexIterator, який вибирає всі рядки, що починаються зі слова 'test'.

```php
<?php
$rArrayIterator = new RecursiveArrayIterator(array('test1', array('tet3', 'test4', 'test5')));
$rRegexIterator = new RecursiveRegexIterator($rArrayIterator, '/^test/',
    RecursiveRegexIterator::ALL_MATCHES);

foreach ($rRegexIterator as $key1 => $value1) {

    if ($rRegexIterator->hasChildren()) {

        // выведем все дочерние элементы
        echo "Дочерние элементы: ";
        foreach ($rRegexIterator->getChildren() as $key => $value) {
            echo $value . " ";
        }
        echo "\n";
    } else {
        echo "Нет дочерних элементов\n";
    }

}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Нет дочерних элементов
Дочерние элементы: test4 test5
```

### Дивіться також

-   [preg\_match()](function.preg-match.md) \- Виконує перевірку на відповідність регулярному виразу
-   [preg\_match\_all()](function.preg-match-all.md) \- Виконує глобальний пошук шаблону у рядку
-   [preg\_replace()](function.preg-replace.md) \- Виконує пошук та заміну за регулярним виразом
-   [preg\_split()](function.preg-split.md) \- Розбиває рядок за регулярним виразом
