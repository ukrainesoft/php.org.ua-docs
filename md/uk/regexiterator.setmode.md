---
navigation:
  - regexiterator.setflags.md: '« RegexIterator::setFlags'
  - regexiterator.setpregflags.md: 'RegexIterator::setPregFlags »'
  - index.md: PHP Manual
  - class.regexiterator.md: RegexIterator
title: 'RegexIterator::setMode'
---
# RegexIterator::setMode

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RegexIterator::setMode — Встановлення режиму роботи

### Опис

```methodsynopsis
public RegexIterator::setMode(int $mode): void
```

Визначає режим роботи.

### Список параметрів

`mode`

Режим роботи.

Нижче наведено можливі режими. Сенс та значення режимів описані в розділі [зумовлених констант](class.regexiterator.md#regexiterator.constants)

**Режими роботи [RegexIterator](class.regexiterator.md)**

| значение | константа |
| --- | --- |
|  | [RegexIterator::MATCH](class.regexiterator.md#regexiterator.constants.match) |
|  | [RegexIterator::GETMATCH](class.regexiterator.md#regexiterator.constants.get-match) |
|  | [RegexIterator::ALLMATCHES](class.regexiterator.md#regexiterator.constants.all-matches) |
|  | [RegexIterator::SPLIT](class.regexiterator.md#regexiterator.constants.split) |
|  | [RegexIterator::REPLACE](class.regexiterator.md#regexiterator.constants.replace) |

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::setMode()****

```php
<?php
$test = array ('str1' => 'test 1', 'test str2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
// Отбор всех элементов, которые начинаются со слова 'test ', за которым идут числа
$regexIterator = new RegexIterator($arrayIterator, '/^test (\d+)/');
// Режим работы: Замена совпавших строк
$regexIterator->setMode(RegexIterator::GET_MATCH);

foreach ($regexIterator as $key => $value) {
    // вывод совпавших чисел
    echo $key . ' => ' . $value[1] . PHP_EOL;
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
str1 => 1
str3 => 123
```

### Дивіться також

-   [RegexIterator::getMode()](regexiterator.getmode.md) - Повертає режим роботи
