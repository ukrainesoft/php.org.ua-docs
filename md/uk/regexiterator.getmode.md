---
navigation:
  - regexiterator.getflags.html: '« RegexIterator::getFlags'
  - regexiterator.getpregflags.html: 'RegexIterator::getPregFlags »'
  - index.html: PHP Manual
  - class.regexiterator.html: RegexIterator
title: 'RegexIterator::getMode'
---
# RegexIterator::getMode

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RegexIterator::getMode — Повертає режим роботи

### Опис

```methodsynopsis
public RegexIterator::getMode(): int
```

Повертає режим роботи. Список можливих режимів наведено на сторінці [RegexIterator::setMode()](regexiterator.setmode.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає режим роботи.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::getMode()****

```php
<?php

$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/^[a-z]+/', RegexIterator::GET_MATCH);

$mode = $regexIterator->getMode();
if ($mode & RegexIterator::GET_MATCH) {
    echo 'Проверка соответствий для каждого элемента.';
} elseif ($mode & RegexIterator::ALL_MATCHES) {
    echo 'Получение всех соответствий для каждого элемента.';
} elseif ($mode & RegexIterator::MATCH) {
    echo 'Получение элементов, прошедших отбор.';
} elseif ($mode & RegexIterator::SPLIT) {
    echo 'Получение отдельных частей каждого элемента.';
}
?>
```

Результат виконання цього прикладу:

```
Проверка соответствий для каждого элемента.
```

### Дивіться також

-   [RegexIterator::setMode()](regexiterator.setmode.html) - Встановлення режиму роботи
