---
navigation:
  - regexiterator.construct.md: '« RegexIterator::construct'
  - regexiterator.getmode.md: 'RegexIterator::getMode »'
  - index.md: PHP Manual
  - class.regexiterator.md: RegexIterator
title: 'RegexIterator::getFlags'
---
# RegexIterator::getFlags

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RegexIterator::getFlags — Отримання прапорів налаштування

### Опис

```methodsynopsis
public RegexIterator::getFlags(): int
```

Повертає прапори настроювання. Список можливих прапорів наведено в описі методу [RegexIterator::setFlags()](regexiterator.setflags.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає набір прапорів.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::getFlags()****

```php
<?php

$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/^test/');
$regexIterator->setFlags(RegexIterator::USE_KEY);

if ($regexIterator->getFlags() & RegexIterator::USE_KEY) {
    echo 'Фильтрация на основе ключей Масива.';
} else {
    echo 'Фильтрация на основе значений Масива.';
}
?>
```

Результат виконання цього прикладу:

```
Фильтрация на основе ключей Масива.
```

### Дивіться також

-   [RegexIterator::setFlags()](regexiterator.setflags.md) - Установка прапорів
