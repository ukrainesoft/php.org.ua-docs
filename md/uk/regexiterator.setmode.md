---
navigation:
  - regexiterator.setflags.md: '« RegexIterator::setFlags'
  - regexiterator.setpregflags.md: 'RegexIterator::setPregFlags »'
  - index.md: PHP Manual
  - class.regexiterator.md: RegexIterator
title: 'RegexIterator::setMode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RegexIterator::setMode

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

RegexIterator::setMode — Встановлення режиму роботи

### Опис

```methodsynopsis
public RegexIterator::setMode(int $mode): void
```

Встановлює режим роботи.

### Список параметрів

`mode`

Режим роботи.

Нижче наведено можливі режими. Сенс та значення режимів описані в розділі [зумовлених констант](class.regexiterator.md#regexiterator.constants)

**Режими роботи [RegexIterator](class.regexiterator.md)**

| значение | константа |
| --- | --- |
|  | [RegexIterator::MATCH](class.regexiterator.md#regexiterator.constants.match) |
|  | [RegexIterator::GET\_MATCH](class.regexiterator.md#regexiterator.constants.get-match) |
|  | [RegexIterator::ALL\_MATCHES](class.regexiterator.md#regexiterator.constants.all-matches) |
| 3 | [RegexIterator::SPLIT](class.regexiterator.md#regexiterator.constants.split) |
| 4 | [RegexIterator::REPLACE](class.regexiterator.md#regexiterator.constants.replace) |

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** RegexIterator::setMode()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
str1 => 1
str3 => 123
```

### Дивіться також

-   [RegexIterator::getMode()](regexiterator.getmode.md) \- Повертає режим роботи
