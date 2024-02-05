---
navigation:
  - regexiterator.getregex.md: '« RegexIterator::getRegex'
  - regexiterator.setmode.md: 'RegexIterator::setMode »'
  - index.md: PHP Manual
  - class.regexiterator.md: RegexIterator
title: 'RegexIterator::setFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RegexIterator::setFlags

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

RegexIterator::setFlags — Установка прапорів

### Опис

```methodsynopsis
public RegexIterator::setFlags(int $flags): void
```

Задає прапори налаштування.

### Список параметрів

`flags`

Прапори, бітова маска класу констант.

Нижче наведено доступні прапори. Сенс та значення прапорів описані в розділі [зумовлених констант](class.regexiterator.md#regexiterator.constants)

**Флаги[RegexIterator](class.regexiterator.md)**

| значение | константа |
| --- | --- |
|  | [RegexIterator::USE\_KEY](class.regexiterator.md#regexiterator.constants.use-key) |

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**RegexIterator::setFlags()\*\*\*\*

Створює новий об'єкт-ітератор, який вибирає елементи, ключі яких починаються зі слова '`test`'.

```php
<?php
$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');

$arrayIterator = new ArrayIterator($test);
$regexIterator = new RegexIterator($arrayIterator, '/^test/');
$regexIterator->setFlags(RegexIterator::USE_KEY);

foreach ($regexIterator as $key => $value) {
    echo $key . ' => ' . $value . "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
teststr2 => another test
```

### Дивіться також

-   [RegexIterator::getFlags()](regexiterator.getflags.md) \- Отримання прапорів налаштування
