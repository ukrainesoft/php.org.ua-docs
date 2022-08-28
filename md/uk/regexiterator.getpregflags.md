Повертає прапори регулярного вираження

-   [« RegexIterator::getMode](regexiterator.getmode.html)
    
-   [RegexIterator::getRegex »](regexiterator.getregex.html)
    
-   [PHP Manual](index.html)
    
-   [RegexIterator](class.regexiterator.html)
    
-   Повертає прапори регулярного вираження
    

# RegexIterator::getPregFlags

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RegexIterator::getPregFlags — Повертає прапори регулярного виразу

### Опис

```methodsynopsis
public RegexIterator::getPregFlags(): int
```

Повертає прапори регулярного виразу. Список можливих прапорів наведено в описі методу [RegexIterator::\_\_construct()](regexiterator.construct.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає бітову маску прапорів регулярного вираження.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::getPregFlags()****

```php
<?php

$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/\s/', RegexIterator::SPLIT);
$regexIterator->setPregFlags(PREG_SPLIT_NO_EMPTY | PREG_SPLIT_OFFSET_CAPTURE);

if ($regexIterator->getPregFlags() & PREG_SPLIT_NO_EMPTY) {
    echo 'Не принимать во внимание пустые участки';
} else {
    echo 'Рассматривать пустые участки';
}

?>
```

Результат виконання цього прикладу:

```
Не принимать во внимание пустые участки
```

### Дивіться також

-   [RegexIterator::setPregFlags()](regexiterator.setpregflags.html) - Завдання прапорів регулярного вираження