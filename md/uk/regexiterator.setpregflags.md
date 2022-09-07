---
navigation:
  - regexiterator.setmode.md: '« RegexIterator::setMode'
  - spl.interfaces.md: Інтерфейси »
  - index.md: PHP Manual
  - class.regexiterator.md: RegexIterator
title: 'RegexIterator::setPregFlags'
---
# RegexIterator::setPregFlags

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RegexIterator::setPregFlags — Завдання прапорів регулярного виразу

### Опис

```methodsynopsis
public RegexIterator::setPregFlags(int $pregFlags): void
```

Встановлює прапори регулярного виразу.

### Список параметрів

`pregFlags`

Прапори налаштування регулярного виразу. Список можливих прапорів наведено в описі методу [RegexIterator::construct()](regexiterator.construct.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::setPregFlags()****

Створює новий об'єкт RegexIterator, який відбирає елементи масиву, ключі яких починаються зі слова 'test'.

```php
<?php
$test = array ('test 1', 'another test', 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/^test/', RegexIterator::GET_MATCH);

$regexIterator->setPregFlags(PREG_OFFSET_CAPTURE);

foreach ($regexIterator as $key => $value) {
    var_dump($value);
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  [0]=>
  array(2) {
    [0]=>
    string(4) "test"
    [1]=>
    int(0)
  }
}
array(1) {
  [0]=>
  array(2) {
    [0]=>
    string(4) "test"
    [1]=>
    int(0)
  }
}
```

### Дивіться також

-   [RegexIterator::getPregFlags()](regexiterator.getpregflags.md) - Повертає прапори регулярного вираження
